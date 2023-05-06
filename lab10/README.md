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


## Run `snakecoin-server-full-code.py` on Terminal 1 and mine a new block on Terminal 2


## Clone Python blockchain app and uncomment the last line of node_server.py


## Run node_server.py on Terminal 1 and run_app.py on Terminal 2

