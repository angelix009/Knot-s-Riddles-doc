# Community Participation

## Getting Involved

### 1. Contribution Areas
- Riddle creation
- Development
- Community moderation
- Content creation

### 2. Reward System
```solidity
contract CommunityRewards {
    struct Contribution {
        ContributionType contributionType;
        uint256 value;
        uint256 timestamp;
    }
    
    enum ContributionType {
        RIDDLE_CREATION,
        CODE_CONTRIBUTION,
        COMMUNITY_SUPPORT,
        CONTENT_CREATION
    }
    
    mapping(address => Contribution[]) public userContributions;
    
    function reward(
        address contributor,
        ContributionType cType,
        uint256 value
    ) public {
        // Reward distribution logic
    }
}
```

## Engagement Programs

### 1. Ambassador Program
- Role description
- Responsibilities
- Benefits
- Application process

### 2. Community Events
- Weekly challenges
- Monthly tournaments
- Special events
- Community calls
