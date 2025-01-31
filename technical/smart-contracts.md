# Smart Contracts

## Core Contracts

### 1. Main Contract
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/IERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";
import "@openzeppelin/contracts/security/ReentrancyGuard.sol";

contract KnotRiddles is Ownable, ReentrancyGuard {
    IERC20 public rewardToken;
    
    struct Riddle {
        bytes32 riddleHash;
        uint256 difficulty;
        uint256 reward;
        bool solved;
        address solver;
    }
    
    mapping(uint256 => Riddle) public riddles;
    mapping(address => UserStats) public userStats;
    
    event RiddleSolved(uint256 riddleId, address solver, uint256 reward);
    event NewRiddle(uint256 riddleId, uint256 difficulty, uint256 reward);
    
    constructor(address _rewardToken) {
        rewardToken = IERC20(_rewardToken);
    }
    
    // Core functions...
}
```

### 2. Reward System
```solidity
contract RewardSystem {
    function calculateReward(
        uint256 difficulty,
        uint256 timeSpent,
        uint256 userLevel
    ) public pure returns (uint256) {
        // Reward calculation logic
    }
    
    function distributeRewards(
        address user,
        uint256 amount
    ) public nonReentrant {
        // Reward distribution logic
    }
}
```

## Security Features

### 1. Access Control
- Role-based permissions
- Multi-signature requirements
- Time-lock mechanisms

### 2. Anti-Exploit Measures
- Rate limiting
- Gas optimization
- Reentrancy protection
