# theorem-marketplace-contract
This repo stores the code for the Theorem Marketplace smart contract which allows you to deposit and claim bounties on theorem proofs. It's used by my https://theorem-marketplace.com/ website.
If you're going to deploy it, you're going to need your own Chainlink oracle for verifying theorem proofs (when deploying, you'll need the operator contract id and the job id.)

Use the `declareBounty` and `requestBounty` functions for the main functionality; the `theoremBounties` mapping to check the size of existing bounties,
and the `closedBounties` mapping to see which bounties have been closed already. If you're trying to deposit a bounty on a theorem but it's already been proven, 
you can at least retrieve the transaction hash that proved the theorem, and hopefully retrieve the proof from that transaction.