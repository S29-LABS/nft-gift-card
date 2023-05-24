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
