# Lab 10 — Blockchain
## Objectives:
- Study the GitHub repository [Lesson 10](https://github.com/kevinwlu/iot/tree/master/lesson10)
- Run hash_value.py twice and compare results
- Run snakecoin.py
- Run snakecoin-server-full-code.py on Terminal 1 and mine a new block on Terminal 2
- Clone Python blockchain app and uncomment the last line of node_server.py
- Run node_server.py on Terminal 1 and run_app.py on Terminal 2

## Run `hash_value.py` twice and compare results
```
$ python3 hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: -513330691104508829
The hash for a tuple of vowels is: -1261226560690955229
The hash for an object of person is: -7700208450287719401

$ python3 hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: -1638959576483072430
The hash for a tuple of vowels is: 1917975463167930686
The hash for an object of person is: -3466059058047159078
```
### Hashes for 1, 1.0, and 3.14 stayed the same.
### Hashes for Python, Tuple, and Object changed:
|     Hash For         |     First Run        |      Second Run      |
| -------------------- | -------------------- | -------------------- |
|       Python         | -513330691104508829  | -1638959576483072430 |
|   tuple of vowels    | -1261226560690955229 |  1917975463167930686 |
|   object of person   | -7700208450287719401 | -3466059058047159078 |

## Run `snakecoin.py`
```
$ python3 snakecoin.py
Block #1 has been added to the blockchain!
Hash: c4c5de087dcb396d9c73c90015f4d16ab464ea00e3565e3041d2b3c15cc0d588

Block #2 has been added to the blockchain!
Hash: 460895f065e0b8a9fbeb6b0721e0b8a61f900001df4e54de32f2520bbbc736d3

Block #3 has been added to the blockchain!
Hash: e5cdbe44fa99f7c6ffc3c4170d3ae8a1c20314f6761af102849333847d72423d

Block #4 has been added to the blockchain!
Hash: e8567f2347cb55204282a47d5fef596393377b39326741c6820d8f179a3dcf26

Block #5 has been added to the blockchain!
Hash: 58177c5dc0d4240b30a14b8016d749891bdbf6618444d17f46bb1e06e4ae2da5

Block #6 has been added to the blockchain!
Hash: 89a486d28bd3f618e24d6c4c0baa4b3bb23290f36fae97bff2eddf64ed18accf

Block #7 has been added to the blockchain!
Hash: 8eb9af710ec31dbda95d9aa769ba3e4952362c6c96f1bd42d6731b8c9a8a95c2

Block #8 has been added to the blockchain!
Hash: 80519cf34db01a20d770bc1aa7c882524900bef72bc674208f66cb613cdb6e4d

Block #9 has been added to the blockchain!
Hash: 7ff6deeea4cc4cd26a27cb1f3df60ef7950e1e29ba6f001a02cfcf82c891195f

Block #10 has been added to the blockchain!
Hash: 3c8aa6aa90044cd0e9074ed0e27a65b4cb672e1a146e31b56675eee9811a9567

Block #11 has been added to the blockchain!
Hash: 5ae64124a6d577faeac9a39b6c3abf46b2cba4a408fc0d74863a1b07d4ad3e27

Block #12 has been added to the blockchain!
Hash: e8b5c74e25f3125e769bb397e29be2d88d52db5586f547927661ca132a0b7142

Block #13 has been added to the blockchain!
Hash: dfa4c5cc20bc6bb4c9d164422161218d9448d9ff49a4f2feed25a7c88dba345b

Block #14 has been added to the blockchain!
Hash: 47030878f4c6a1268fa8dcc1c4c6b3932a62c12a1c5a9f483943c601885a676f

Block #15 has been added to the blockchain!
Hash: e7a786e11948c678ce90d5bac3e2c09217c857bb2381017a1b04547e263aa5bf

Block #16 has been added to the blockchain!
Hash: bd11efd346f997dacaecbc9874d4cd80e7bba31e5ccfb51a9436852249e7ba74

Block #17 has been added to the blockchain!
Hash: daa679a852360aba72f14673889dd25e6a3932761db147b7ecb2405994949ee7

Block #18 has been added to the blockchain!
Hash: a3be02075554a642f38ff563fe323fa05d26a102e0d2bf1332dcb9c029104b53

Block #19 has been added to the blockchain!
Hash: a8c0a908da4b1849636d7a05cf49b35ff6101860c8b632ae80d9d80e31f9a4eb

Block #20 has been added to the blockchain!
Hash: abdca1e76d18b9b5c4c051732e21308fc6f93d3dc6d035cc4c1c9a3803ae6481
```

## Run `snakecoin-server-full-code.py` on Terminal 1 and mine a new block on Terminal 2
### Terminal 1 (`snakecoin-server-full-code.py`)
```
$ python3 snakecoin-server-full-code.py
 * Serving Flask app 'snakecoin-server-full-code'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:5000
Press CTRL+C to quit
127.0.0.1 - - [06/May/2023 16:04:33] "GET / HTTP/1.1" 200 -
127.0.0.1 - - [06/May/2023 16:04:33] "GET /favicon.ico HTTP/1.1" 200 -
127.0.0.1 - - [06/May/2023 16:04:59] "GET /mine HTTP/1.1" 200 -
```
### "SnakeCoin Server" now running on [http://127.0.0.1:5000/](http://127.0.0.1:5000)
![image](https://github.com/mbanks01/CPE-322-A/blob/main/lab10/1.2.PNG)
### Terminal 2 - Create a transaction and mine a new block at [http://127.0.0.1:5000/mine](http://127.0.0.1:5000/mine)
![image](https://github.com/mbanks01/CPE-322-A/blob/main/lab10/1.1.PNG)
```
$ curl "localhost:5000/txion" \
     -H "Content-Type: application/json" \
     -d '{"from": "akjflw", "to":"fjlakdj", "amount": 3}'
$ curl localhost:5000/mine
```

## Clone Python blockchain app and uncomment the last line of node_server.py
### Terminal 1: Uncomment the last line of node_server.py
```
$ python3 node_server.py
 * Serving Flask app 'node_server'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:8000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 294-414-302
```

### Terminal 2: Run run_app.py

```
$ python3 run_app.py
 * Serving Flask app 'app'
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:5000
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 294-414-302
127.0.0.1 - - [06/May/2023 16:25:44] "GET / HTTP/1.1" 200 -
127.0.0.1 - - [06/May/2023 16:25:45] "GET / HTTP/1.1" 200 -
```

## Run node_server.py on Terminal 1 and run_app.py on Terminal 2
![image](https://github.com/mbanks01/CPE-322-A/blob/main/lab10/1.3.PNG)
![image](https://github.com/mbanks01/CPE-322-A/blob/main/lab10/1.4.PNG)
![image](https://github.com/mbanks01/CPE-322-A/blob/main/lab10/1.6.PNG)
![image](https://github.com/mbanks01/CPE-322-A/blob/main/lab10/1.5.PNG)
![image](https://github.com/mbanks01/CPE-322-A/blob/main/lab10/1.7.PNG)
