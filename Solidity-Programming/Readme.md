
# Task 1 : Basic Calculator

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.26;

contract calculator{

    uint256 result = 0;

    function add(uint256 num) external {
        result += num;
    }

    function sub(uint256 num) public {
        result -= num;
    }

    function mult(uint256 num) public {
        result *= num;
    }

     function div(uint256 num) public {
        result /= num;
    }

    function get() public view returns (uint256){

        return result;
    }
}

```

![image](https://github.com/user-attachments/assets/156d9903-23d4-40a8-8a20-32688763ec46)

# Task 2 Mapping
```solidity
// SPDX-License-Identifier: MIT

pragma solidity ^0.8.26;
contract Twitter{

    mapping (address => string)public tweets;

    function createTweet(string memory _tweet) public {
        tweets[msg.sender] = _tweet;
    }

    function getTweet(address _owner) public view returns(string memory){
        return tweets[_owner];
    }

}

```
