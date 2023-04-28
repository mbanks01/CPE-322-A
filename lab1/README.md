# Lab 1 — GHDL and GTKWave
## Objectives:
- Go to the GitHub repository of Digital System Design (DSD)
  - Study VHDL and GHDL
- Go to the GHDL folder
  - Install GHDL and GTKWave
  - Run the Half Adder example
  - Run another example such as D Flip-Flop or 4-to-1 Multiplexer

## Install GHDL and GTKWave:
- Installed Notepad++
- Downloaded GHDL
- Downloaded GTKWave
- Added to Environment Variables Path

Entered into terminal:
```
$ git clone https://github.com/kevinwlu/dsd.git
$ mkdir vhdl
$ cd vhdl
$ cp ~/dsd/ghdl/*vhdl .
```
*Cloned the repo and copied the .vhdl files into new directory "vhdl"*
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab1/1.1.PNG)

##Hello World Example
```
$ ghdl -h
$ ghdl -v
$ ghdl -a hello.vhdl
$ ghdl -e hello_world
$ ghdl -r hello_world
```
*This was the first test using ghdl.*


![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab1/1.2.PNG)



## Run the Half Adder example:
```
$ ghdl -a ha.vhdl
$ ghdl -a ha_tb.vhdl
$ ghdl -e ha_tb
$ ghdl -r ha_tb --vcd=ha.vcd
$ gtkwave ha.vcd
```
*Running the half adder example.*
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab1/1.3.PNG)
Running this code opened the following window:
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab1/1.4.PNG)

## Run another example:
```
$ ghdl -a dff.vhdl
$ ghdl -a dff_tb.vhdl
$ ghdl -e dff_tb
$ ghdl -r dff_tb --vcd=dff.vcd
$ gtkwave dff.vcd
```
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab1/1.5.PNG)
Running this opened the following window:
![sample image](https://github.com/mbanks01/EE-322-A/blob/main/lab1/1.6.PNG)
