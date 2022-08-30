# Morpholabs

I used Web3.py,Infura,Chainlink,Coumpound and Etherscan.

First of all, I would like to congratulate the French on their fantastic fundraising. 
I heard about this protocol some time ago but it is only recently that I went into it technically. 
Morpholabs is a protocol that created a layer on top of the Compound protocol to connect borrowers and providers in a direct way. 
In this way rewards are maximised as the interests paid by a borrower aren't divided between all suppliers. 

So I made this code to answer at this question 'What are the top 10 users in dollars matched P2P (borrow and supply) at a given block?'. 
I took it like a challenge, I made investigations on the docs of morpholabs and Compound. I tested several functions on etherscan of the smart contracts of Morpholabs' proxy and Compound's ctokens. 


I wrote getRedeemRateCtoken(addressCtoken) function but it is useless cause I was thinking getCurrentBorrowBalanceInOf().call() and getCurrentSupplyBalanceInOf().call() returned ctoken balance.

## Method

I collected all the addresses that had interacted with the morphlab protocol. Then I examined what their P2P balance was for all the markets they had entered (tokens supply or borrow). I totaled the P2P balances multiplied by the price of supply/borrow tokens. I added a block number into all call() functions. This is how I found the top 10 suppliers and borrowers P2P in dollars at a given block. 
