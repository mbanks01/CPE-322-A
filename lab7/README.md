# Lab 7 — ThingSpeak and Google Sheets
## Objectives:
- Sign up and log in MathWorks ThingSpeak
- Run thingspeak_cpu_loop.py or thinkspeak_feed.py in a demo folder
- Install gspread and oauth2client
- Log in the Google Cloud Platform Identity and Access Management, create a - project cpudata, enable both Drive API and Sheets API, create and download service account JSON key file
- Start a new Google sheet cpudata, share it with the client email in the JSON file, delete Rows 2 to 1000, and edit the header cells
- Run cpu_spreadsheet.py with the JSON key file in a demo folder

## MathWorks ThingSpeak Channel Settings
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab7/1.1.PNG)

## thingspeak_cpu_loop.py
```
$ cat thingspeak_cpu_loop.py
import http.client, urllib.request, urllib.parse, urllib.error
from time import localtime, strftime
import psutil
import time
def doit():
        cpu_pc = psutil.cpu_percent()
        mem = psutil.virtual_memory()
        mem_avail_mb = mem.available/(1024*1024)
        params = urllib.parse.urlencode({'field1': cpu_pc, 'field2':
             mem_avail_mb,'key':'YOURKEYHERE'})
        headers = {"Content-type":
               "application/x-www-form-urlencoded","Accept": "text/plain"}
        conn = http.client.HTTPConnection("api.thingspeak.com:80")
        try:
                conn.request("POST", "/update", params, headers)
                response = conn.getresponse()
                print(cpu_pc)
                print(mem_avail_mb)
                print(strftime("%a, %d %b %Y %H:%M:%S", localtime()))
                print(response.status, response.reason)
                data = response.read()
                conn.close()
        except:
                print("connection failed")
#sleep for 60 seconds (message update interval limit of 15 seconds)
if __name__ == "__main__":
        while True:
                doit()
                time.sleep(60)
```
## thingspeak_feed.py
```
$ cat thingspeak_feed.py
import http.client, urllib.request, urllib.parse, urllib.error
from time import localtime, strftime
import psutil
import time
"""
2020-11-26: Pridhvi Myneni added lines 13-18, 25, and 43-54
1. gitignore (https://git-scm.com/docs/gitignore) now prevents students from pushing up credentials.
2. This program now attempts to cache the API key, but always prompts the user for their preference prior to saving credentials locally.
3. Pickle data type used to store credentials. Pickle is a binary storage version of JSON. Please note not-human-readable does not mean secure.
4. Removed key storage in source, which is generally a bad practice, as it leads to version control systems having your key.
5. Key for storage in a dictionary. This could be expanded in the future if other information needs to be similarly stored.
"""
from pickle import dump as pickle_dump
from pickle import load as pickle_load
from os.path import exists as file_exists
from os.path import isfile as is_file
PICKLE_FILE_NAME = "API_KEY.pickle"
API_KEY_INDEX = "API_KEY"
def doit():
        cpu_pc = psutil.cpu_percent()
        mem = psutil.virtual_memory()
        mem_avail_mb = mem.available/(1024*1024)
        params = urllib.parse.urlencode({'field1': cpu_pc, 'field2':
#             mem_avail_mb,'key':'YOURKEYHERE'})
             mem_avail_mb,'key':KEY})
        headers = {"Content-type":
               "application/x-www-form-urlencoded","Accept": "text/plain"}
        conn = http.client.HTTPConnection("api.thingspeak.com:80")
        try:
                conn.request("POST", "/update", params, headers)
                response = conn.getresponse()
                print(cpu_pc)
                print(mem_avail_mb)
                print(strftime("%a, %d %b %Y %H:%M:%S", localtime()))
                print(response.status, response.reason)
                data = response.read()
                conn.close()
        except:
                print("connection failed")
#sleep for 60 seconds (message update interval limit of 15 seconds)
if __name__ == "__main__":
#caching the Write Key for the ThingSpeak API
        if file_exists(PICKLE_FILE_NAME) and is_file(PICKLE_FILE_NAME):
                save_file = None
                with open(PICKLE_FILE_NAME, 'rb') as f:
                        save_file = pickle_load(f)
                KEY = save_file[API_KEY_INDEX]
        else:
                key = input("An API key savefile was not found. Enter Write API Key >>> ")
                should_save = input("Should we save this key for future use? [y/N] >>> ")
                KEY = key.strip()
                if len(should_save)>0 and should_save.lower().startswith("y"):
                        with open(PICKLE_FILE_NAME, 'wb') as f:
                                pickle_dump({API_KEY_INDEX: KEY}, f)
        while True:
                doit()
                time.sleep(60)
```



## Install gspread and oauth2client
```
$ pip install -U gspread oauth2client
Collecting gspread
  Downloading gspread-5.8.0-py3-none-any.whl (40 kB)
     ---------------------------------------- 40.5/40.5 kB 1.9 MB/s eta 0:00:00
Collecting oauth2client
  Downloading oauth2client-4.1.3-py2.py3-none-any.whl (98 kB)
     ---------------------------------------- 98.2/98.2 kB ? eta 0:00:00
Collecting google-auth>=1.12.0 (from gspread)
  Downloading google_auth-2.17.3-py2.py3-none-any.whl (178 kB)
     ------------------------------------- 178.2/178.2 kB 11.2 MB/s eta 0:00:00
Collecting google-auth-oauthlib>=0.4.1 (from gspread)
  Downloading google_auth_oauthlib-1.0.0-py2.py3-none-any.whl (18 kB)
Collecting httplib2>=0.9.1 (from oauth2client)
  Downloading httplib2-0.22.0-py3-none-any.whl (96 kB)
     ---------------------------------------- 96.9/96.9 kB 5.4 MB/s eta 0:00:00
Collecting pyasn1>=0.1.7 (from oauth2client)
  Downloading pyasn1-0.5.0-py2.py3-none-any.whl (83 kB)
     ---------------------------------------- 83.9/83.9 kB 4.6 MB/s eta 0:00:00
Collecting pyasn1-modules>=0.0.5 (from oauth2client)
  Downloading pyasn1_modules-0.3.0-py2.py3-none-any.whl (181 kB)
     ------------------------------------- 181.3/181.3 kB 11.4 MB/s eta 0:00:00
Collecting rsa>=3.1.4 (from oauth2client)
  Using cached rsa-4.9-py3-none-any.whl (34 kB)
Requirement already satisfied: six>=1.6.1 in c:\users\micha\appdata\local\programs\python\python311\lib\site-packages (from oauth2client) (1.16.0)
Collecting cachetools<6.0,>=2.0.0 (from google-auth>=1.12.0->gspread)
  Downloading cachetools-5.3.0-py3-none-any.whl (9.3 kB)
Collecting requests-oauthlib>=0.7.0 (from google-auth-oauthlib>=0.4.1->gspread)
  Downloading requests_oauthlib-1.3.1-py2.py3-none-any.whl (23 kB)
Requirement already satisfied: pyparsing!=3.0.0,!=3.0.1,!=3.0.2,!=3.0.3,<4,>=2.4.2 in c:\users\micha\appdata\local\programs\python\python311\lib\site-packages (from httplib2>=0.9.1->oauth2client) (3.0.9)
Collecting oauthlib>=3.0.0 (from requests-oauthlib>=0.7.0->google-auth-oauthlib>=0.4.1->gspread)
  Downloading oauthlib-3.2.2-py3-none-any.whl (151 kB)
     ---------------------------------------- 151.7/151.7 kB ? eta 0:00:00
Collecting requests>=2.0.0 (from requests-oauthlib>=0.7.0->google-auth-oauthlib>=0.4.1->gspread)
  Downloading requests-2.30.0-py3-none-any.whl (62 kB)
     ---------------------------------------- 62.5/62.5 kB ? eta 0:00:00
Collecting charset-normalizer<4,>=2 (from requests>=2.0.0->requests-oauthlib>=0.7.0->google-auth-oauthlib>=0.4.1->gspread)
  Downloading charset_normalizer-3.1.0-cp311-cp311-win_amd64.whl (96 kB)
     ---------------------------------------- 96.7/96.7 kB ? eta 0:00:00
Collecting idna<4,>=2.5 (from requests>=2.0.0->requests-oauthlib>=0.7.0->google-auth-oauthlib>=0.4.1->gspread)
  Using cached idna-3.4-py3-none-any.whl (61 kB)
Collecting urllib3<3,>=1.21.1 (from requests>=2.0.0->requests-oauthlib>=0.7.0->google-auth-oauthlib>=0.4.1->gspread)
  Downloading urllib3-2.0.2-py3-none-any.whl (123 kB)
     ---------------------------------------- 123.2/123.2 kB ? eta 0:00:00
Collecting certifi>=2017.4.17 (from requests>=2.0.0->requests-oauthlib>=0.7.0->google-auth-oauthlib>=0.4.1->gspread)
  Using cached certifi-2022.12.7-py3-none-any.whl (155 kB)
Installing collected packages: urllib3, pyasn1, oauthlib, idna, httplib2, charset-normalizer, certifi, cachetools, rsa, requests, pyasn1-modules, requests-oauthlib, oauth2client, google-auth, google-auth-oauthlib, gspread
Successfully installed cachetools-5.3.0 certifi-2022.12.7 charset-normalizer-3.1.0 google-auth-2.17.3 google-auth-oauthlib-1.0.0 gspread-5.8.0 httplib2-0.22.0 idna-3.4 oauth2client-4.1.3 oauthlib-3.2.2 pyasn1-0.5.0 pyasn1-modules-0.3.0 requests-2.30.0 requests-oauthlib-1.3.1 rsa-4.9 urllib3-2.0.2
```
## Running `$ python3 thingspeak_feed.py` with Write API Key
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab7/1.2.PNG)

## ![Google Spreadsheet](https://docs.google.com/spreadsheets/d/1bHjOKGg1OsUZyHVR-MQYjF1T3VqPI-Mr_ilejmav138/edit?usp=sharing)
