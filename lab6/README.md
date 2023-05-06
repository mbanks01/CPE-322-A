# Lab 1 — Node.js and Pystache
## Objectives:
- Study the GitHub repository [Lesson 6](https://github.com/kevinwlu/iot/tree/master/lesson6)
- Install Node.js and run hello-world.js, hello.js, and http.js
  - Refresh the webpage to see server activities
- Install Pystache and run say_hello.py that uses the template in say_hello.mustache

## hello-world.js

![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab6/1.1.PNG)
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab6/1.2.PNG)

## hello.js
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab6/2.1.PNG)

## http.js
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab6/3.1.PNG)
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab6/3.2.PNG)
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab6/3.3.PNG)

## Install Pystache
```
$ pip install pystache
Collecting pystache
  Downloading pystache-0.6.0.tar.gz (78 kB)
     ---------------------------------------- 78.2/78.2 kB ? eta 0:00:00
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'done'
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'done'
Building wheels for collected packages: pystache
  Building wheel for pystache (pyproject.toml): started
  Building wheel for pystache (pyproject.toml): finished with status 'done'
  Created wheel for pystache: filename=pystache-0.6.0-py3-none-any.whl size=83719 sha256=21072b4ec52b499b741da5e079e49394e9f81cad5a802641a5a3d8e054b35a69
  Stored in directory: c:\users\micha\appdata\local\pip\cache\wheels\85\d6\50\39ee0fc0f15b32c9a98467fefff466a68b5cb3a04a76401aca
Successfully built pystache
Installing collected packages: pystache
Successfully installed pystache-0.6.0

```

## say_hello.py
```
$ python3 say_hello.py
Hi Alexa!
Hello, World!

['Hey ', _SectionNode(key='who', index_begin=12, index_end=18, parsed=[_EscapeNode(key='.'), '!'])]
Hey Google!
Hey Siri!

```
