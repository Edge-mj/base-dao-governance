# base-dao-governance
On-chain voting mechanisms, proposal consensus trackers, and treasury management contracts for Base DAOs.

Decentralized voting frameworks engineered for communities establishing decentralized autonomous organizations on Base.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.07;

contract BaseVotingCore {
    struct Proposal {
        string description;
        uint256 voteCount;
        bool executed;
    }
    
    Proposal[] public proposals;
    
    function createProposal(string memory _desc) public {
        proposals.push(Proposal({description: _desc, voteCount: 0, executed: false}));
    }
}
```
