# Process

Write program

anchor build

anchor test

anchor key list >> copy pubkey to declare_id!() in lib.rs

anchor build (again to include new program id in the binary)

Change provider.cluster in Anchor.toml to devnet

anchor deploy

anchor test

# Fix error:

>> Not enough token amounts:

solana airdrop 2 <pubKey> --url https://api.devnet.solana.com

>> BPF - not a directory

rm -rf ./cache/solana/<version-folder-name>

# Write Program

- Logic start program/<prj-name>/src/lib.rs file

- First create game state

- When write any instructions, we need create two things: a struct and a function

- Struct which used for initializing state need to be declared size of space for data of state account, payer and system program

- Struct which used for other function (different above) need a field for state to declare which account will be changed data