Potential nft royalty issue solution:
- In a future where all human owned wallets have a sort zk badge that proves that they are humans.
- Nft contracts have two separate transfer functions: 
	- One for transferring between their own wallets,
	- One for selling.
- The transfer function checks if the address calling it is human (by checking for the zk badge). If the sender is human, it's likely gonna be a user transferring to a cold wallet or something like that. (no royalty fees then)
- If the function calling the transfer is initiated via a marketplace, then the nft should require a multi-sig to the money as an argument to the transfer.