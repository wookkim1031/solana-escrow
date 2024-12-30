In Solana, smart contracts are called programs

What is escrow? 

Escrow highlights well what a blockchain makes possible. 
For example, Person A and B has an asset and wants to trade their assets.
Neither wants to send the asset first. 

Traditional way of solving this problem: Bank. However, using the blockchain technology 
the trusted third party C is placed with the code on blockchain and specifically 
a smart contract that verifiably acts the same way a trusted third party would. 

Solana programs are stateless. Thats why we need accounts to store states. Accounts can only be owned by programs.

Accounts are owned by programs. Only the account owner may debit an account and adjust its data 

All accounts to be written to or read must be passed into the entrypoint

Program flow:
1. Someone calls the entrypoint
2. The entrypoint forwards the arguments to the processor
3. The processor asks **instruction.rs** to decode the **instruction_data** argument from the entrypoint function.
4. Using the decoded data, the processor will now decide which processing function to use to process the request
5. The processor may use **state.rs** to encode state into or decode the state of an account which has been passed into the entrypoint

Theroy
- the devleopers should use the data field to save data inside accounts
- the token program owns token accounts which - inside their data field - hold relevant information 
- the token program also owns token mint accounts with relevant data
- each token accounts holds a reference to their token mint account, thereby stating which token mint they belong to 
- the token program allows the authority of a token account to transfer its ownership to another address
- All internal Solana internal account infromatio nare saved into fields on the account

Generating a new keypair

For added security, enter a BIP39 passphrase

NOTE! This passphrase improves security of the recovery seed phrase NOT the
keypair file itself, which is stored as insecure plain text

BIP39 Passphrase (empty for none): 

Wrote new keypair to /Users/joki/.config/solana/id.json
============================================================================
pubkey: 4jYTnr73dsbMxRUQaVtKf9VYRnPpWyzhMDgCV93DNGQU
============================================================================
Save this seed phrase and your BIP39 passphrase to recover your new keypair:
video shallow pitch tourist early make side ketchup gospel permit bleak desk
============================================================================