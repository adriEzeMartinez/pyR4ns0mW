## Program Structure:
In order for the program, the server uses PyNgrok to tunnel it and make the server reacheable from evrywhere.

The project is composed of two main **parts/programs**: **the server and the ransomware**

the **server** is organised in **two parts**:
- **SQL database:** create a SQL database with a CLIENT table where user datas such as key, digits, time are stored in there
- **HTTP server:** basic http server to handle POST requests made from the ransomware.

the **ransomware** is organised  in **four parts**:
 - **Find Files:** find files by extensions and store the path into **path.txt**
 - **Encrypt Files:** encrypt files in **path.txt**, generate **digits id**, **send key and id**
 - **Decrypt:** ask for money, wait for the key, and decrypt file if key is correct
-  **Send data:** send data to our http server

## How to run
You need to have python3 installed and configured

 - Download the repository via git or zip
 - Install requirements: `pip install -r requirements.txt`

1.Run the server: `python3 server.py`
Before running the ransomware, you'll need to modify a few things in ransom.py:

 1. Put the url you've got when you started the server

 

 2. I recommend running it in a testing directory, otherwise all of your files will be encrypted

2. Run it: `python3 ransom0.py`

## To do:
 - [x] Add logs
 - [x] Add filter to exclude system files
 - [x] Message in a GUI windows (Tkinter)
 - [x] !! Add a databases or server instead of mail (SQL) 
 - [ ] !! Add a Web Interface ( Frontend: VueJs ? Backend: Django?) 
 - [ ] !! Bypass permission / Privileges Escalation (WinPwnage)
 - [ ] Hide logs
 - [ ] Automatically  show the message on startup
 - [ ] Generate executable for all OS (pyinstaller)


## Testing
This Program have been test on VW with:

 - **Windows 10 & 11**
 - **Mac OS Catalina 10.15.6 (19G73)**
 - **Mac OS Big Sur 11.2.1 (20D74)**
 - **Ubuntu server 18.04 LTS**

## DISCLAIMER 
**THIS PROJECT IS FOR EDUCATION PURPOSE ONLY**
**I AM NOT RESPONSIBLE FOR ANY DAMAGED CAUSED BY THE ILLEGAL USAGE OF THIS PROGRAM**
