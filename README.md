# Challenge 18 - Blockchain - Using an existing blockchain to add user friendly features
The purpose of this Challenge 18 was to modify the code set that was generated throughout the Module by the student.  Specifically, to a functioning blockchain, several attributes were to be added.  The scenario is an example situation.  

## Background
You’re a fintech engineer who’s working at one of the five largest banks in the world. You were recently promoted to act as the lead developer on their decentralized finance team. Your task is to build a blockchain-based ledger system, *complete with a user-friendly web interface*. This ledger should allow partner banks to conduct financial transactions (that is, to transfer money between senders and receivers) and to verify the integrity of the data in the ledger.

The list of added attributes is found below:

1.  Create a new data class named Record. This class will serve as the blueprint for the financial transaction records that the blocks of the ledger will store.

2.  Change the existing Block data class by replacing the generic data attribute with a record attribute that’s of type Record.

3.  Create additional user input areas in the Streamlit application. These input areas should collect the relevant information for each financial record that you’ll store in the PyChain ledger.

4.  Test your complete PyChain ledger


The main elements of a successful (highly subjective) blockchain were developed during the Module 18 and included, among others:

1. Building the Ledger environment

2. Hashing elements through the Hash function to encode the unique element ID

3. Chaining the Blocks in the blockchain

4. Using Consensus to validate transactions on the blockchain

5. Tying it all together so that the creator can modify the level of difficulty (through the nonce function) in order to maintain a level flow of data passing into the blockchain. 

6. Using Streamlit in order to deliver the blockchain environment to a user via web browser.  

There are several primary steps that must be achieved to accomplish taking the mostly defined blockchain and added more functionality to make it more user friendly.  

These are:

## Step 1: Create a Record Data Class
1. Define a new Python data class named Record. Give this new class a formalized data structure that consists of the sender, receiver, and amount attributes. To do so, complete the following steps:

2. Define a new class named Record.

3. Add the @dataclass decorator immediately before the Record class definition.

4. Add an attribute named sender of type str.

5. Add an attribute named receiver of type str.

6. Add an attribute named amount of type float.

7. Note that you’ll use this new Record class as the data type of your record attribute in the next section.

## Step 2: Modify the Existing Block Data Class to Store Record Data

1. Rename the data attribute in your Block class to record, and then set it to use an instance of the new Record class that you created in the previous section. To do so, complete the following steps:

2. In the Block class, rename the data attribute to record.

3. Set the data type of the record attribute to Record.

## Step 3: Add Relevant User Inputs to the Streamlit Interface
1. Code additional input areas for the user interface of your Streamlit application. Create these input areas to capture the sender, receiver, and amount for each transaction that you’ll store in the Block record. To do so, complete the following steps:

2. Delete the input_data variable from the Streamlit interface.

3. Add an input area where you can get a value for sender from the user.

4. Add an input area where you can get a value for receiver from the user.

5. Add an input area where you can get a value for amount from the user.

6. As part of the Add Block button functionality, update new_block so that Block consists of an attribute named record, which is set equal to a Record that contains the sender, receiver, and amount values. The updated Blockshould also include the attributes for creator_id and prev_hash.

## Step 4: Test the PyChain Ledger by Storing Records
1. Test your complete PyChain ledger and user interface by running your Streamlit application and storing some mined blocks in your PyChain ledger. Then test the blockchain validation process by using your PyChain ledger. To do so, complete the following steps:

2. In the terminal, navigate to the project folder where you've coded the Challenge.

3. In the terminal, run the Streamlit application by using streamlit run pychain.py.

4. Enter values for the sender, receiver, and amount, and then click the Add Block button. Do this several times to store several blocks in the ledger.

5. Verify the block contents and hashes in the Streamlit drop-down menu. Take a screenshot of the Streamlit application page, which should detail a blockchain that consists of multiple blocks. Include the screenshot in the README.md file for your Challenge repository.

6. Test the blockchain validation process by using the web interface. Take a screenshot of the Streamlit application page, which should indicate the validity of the blockchain. Include the screenshot in the README.md file for your Challenge repository.

---




## Analyze the Performance
As mentioned above, the code (once the user is satisfied with it) can be immediately modified to increase or decrease the level of difficulty.  

This is done by change the "Nonce" value.  The nonce value is the number of zeroes in the leading (left hand side) portion of the resulting hash ID.  By increasing the number of zeroes, the difficulty to solve for a more specific input set can be altered to be more or less difficult given the needs of the program performance.  

Solving the hash ID with the appropriate leading number of zeroes solves the mathematical "puzzle" that the miner seeks to solve.  By solving the puzzle, the miner is rewarded by money, tokens, coins or the like, given the particular blockchain.  The particular rewards are beyond the scope of this Challenge.  

By using the Slider, the blockchain can either manually or automatically increase or decrease the number of zeroes and the corresponding difficulty of the puzzle.  

        Note: The slider was modified to provide the user (of the program) with the ability to select a level of difficulty from 1 to 10.  



# Technologies

This project was completed almost entirely in VS Code and also in Steamlit.  The README.md was written in VS Code.  

There were numerous libraries used in this project:

import streamlit as st

from dataclasses import dataclass

from typing import Any, List

import datetime as datetime

import pandas as pd

import hashlib

More information can be found regarding each of these libraries at the following links:

Streamlit.io - https://docs.streamlit.io/

dataclasses/dataclass - https://docs.python.org/3/library/dataclasses.html

typing - Any, List - https://docs.python.org/3/library/typing.html

datetime - https://docs.python.org/3/library/datetime.html

pandas - https://pandas.pydata.org/

hashlib - https://docs.python.org/3/library/hashlib.html

This program was written and will run on Windows 10.  

---

# Installation Guide

## Import the Data, Modify it and Perfect it
Use the pychain.py file to complete the following steps:

*Note: This is a Python file rather than a Jupyter Notebook file (.ipynb) and for utility, I've used Streamlit.  Streamlit is a web based tool to assist the developer and user to code and test the functionality. I have used VS Code to code this program while running the Python program in the terminal.*

1. Navigate the terminal in VS Code to the folder where pychain.py is found.  

2. In the File Explorer window in VS Code, a user can find or create a new file.  In this case, we open the pychain.py program and edit in the main window.  

3. Make sure and import the needed libraries and dependencies for the program/blockchain.  

4. When completed, enter the text in the terminal (make sure to navigate to the directory that holds the pychain.py program), "Streamlit run pychain.py."

5. Depending upon how your code is written, a browser instantiates and shows the results of the code set or any errors.  
    A. If typical "print" functions are used, the code runs in the terminal, which is fine - is that's where you want it. 

    B. If you want it to execute in the browser a similar function "st.write" is used.  By using Streamlit, the user can include numerous functionality quite easily like downloading a file, creating a button to execute a command or build a slider to change the parameters in short order.  In this case, we used a slider to modify the "difficulty" of the solution, to be explained later. 

After the code was written, tested and functioned as designed, two screenshots were taken.  

1. The first from the terminal in VS Code to show the command line input and the resulting output:

![Terminal](https://github.com/Cryptopher2022/Challenge_18_blockchain/blob/main/images/Terminal.png)

2. The second image is from the Streamlit browser that was spawned as a result of the streamlit code being written into the Python program (as briefly explained above).

![Streamlit](https://github.com/Cryptopher2022/Challenge_18_blockchain/blob/main/images/Streamlit_result.png)

---

## Contributors

This was done solely by Christopher Todd Garner

---

## License

Feel free to use this program with proper reference to this program in any work that's published (or turned in as part of an assignment).  
