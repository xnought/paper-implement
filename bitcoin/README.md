# Bitcoin

## Papers

- https://bitcoin.org/bitcoin.pdf
- https://www.youtube.com/watch?v=bBC-nXj3Ng4
- ...

## Notes

- Peer to peer transactions without financial institutions (and no peers cheating)
- Main innovation is a chain verified by proof of work that cannot be easily reproduced by someone trying to claim different transactions
- Lets suppose I have 5 coins and I want to pay you 1. In general, we would have to check that I have enough to pay you, which I do, then we add that transaction to a history so we can track that I do indeed have 1 less and you now have 1 more. First of all, what if I go in and modify the ledger later so you pay me more. Also if there are tons of different people one the network, which ledger is the correct one for transactions?
- In order to solve these problems we need a way for everyone to agree on when and what transactions were made. All transactions must also be public.
- Satoshi suggests a timestamp server can solve the timing problems. We take transactions made at a time and hash them to be showed publicly. The previous time stamp is stored to form a chain. Hence block chain.
- Proof of work is just a computational effort to add a new block to the chain. We have to get a certain number of bits as 0 of a hashed value. Which takes a long time. So let's say an attacker wanted to put their own history of transactions. They would have to figure out the number to hash to get those number of 0s for the new change for a ton of different blocks which would involve outmining the entire network.
- 