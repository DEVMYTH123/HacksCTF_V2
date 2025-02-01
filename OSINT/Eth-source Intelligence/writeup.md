https://sepolia.etherscan.io/tx/0x9bd77b2bd621e1bc6f1a9e6eb9798aac910194a76a1f8f565b59c182c6dec565

This transaction was given as the final transaction executed by a person on on test chain. 

Solution:

Opening the transaction meta data, you see some encoded text, converting to UTF-8, you will see text starting from 0x (0x27257324f9832Bb9AC0676234cCb3E909ed44c03) stating it is another address of another contract. Read that contract's function you will see a callMe method that is present. Again going to its metadata and decoding it we find yet another address 0xbec8c262f41b4574fc3b2672eac46b8f81038347c78294c9ea629afff664288a. Decoding the input data of this transaction you see the flag: 

hacks{ethersc4n_o5Int). Mind us for the mistake in the closing parenthesis. 
