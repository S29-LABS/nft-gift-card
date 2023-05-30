# nft-gift-card
 A protocol to seed or create and redeem an nft in form of a gift card via L1 - L2

 A good reference website is apple, https://www.apple.com/shop/buy-giftcard/giftcard.
 A user interacts with our similar frontend as apple to purchase a gift card. The gift card is an NFT, in more detail its a jpeg backed nft.
 The user selects the price of the Gift card, ideally this is the price of ETH or OP Token decided to be gifted.
 The user specifies the address of the recipient, and a message for this recipient.
 who ever is the recipient of the Gift card owns the NFT and can do what ever he wants to do with it. 
 On the other hand the NFT owns the eth or op token.
 
 N.B the recipient of the giftcard is dynamic, meaning when an nft is transfered between users, they immediately hold ownership.
 N.B the token standard is ERC721 and maybe ERC1155
 
 1) How do we implement an NFT to own something, in this case eth or op ?
 We would both create a simple contract that illustrates 1)
 
 2) After solving 1) we then try and understand the flow between L1 - L2 ?


we would create a factory contract, the factory would clone an implementation of a smart contract that represents 
a user account or pool in our project and would be able to mint and redeem nfts accross mainnet L1 && mainnet L2

how does bridging work, 
if i mint an nft gift card on L1, i would deposit a transaction on optimisms portal contract, this deposit would buy L2 gas, send the gas to 
our projects contract on L2, and register in a mapping the nft that would be used to redeem it.

ideally sending eth from L2 to L1 is not the best of users experience since rollups process withdrawals for 1 week.

the value proposition would be gifting l2 asset to anyone from L1.

1. we need to create a factory contract on L1, that creates other contracts from a cloned representaion
2. this contract is an erc721 contract
3. when a user mints a new contract, we need to send a transaction specifying a recipient for their nft or gift card
   to our projects smart contract on L2
   
   we would also store the recipients info on L1
   
4. we need it simple and gas optimized
6. the tokens or eth that back this contract all exist on the L2 side of things.
7. Its ok if this is shitty, but we woul get it perfect.
