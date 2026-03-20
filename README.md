# Counter
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Counter {
    uint256 public count;

    function increment() external {
        count += 1;
    }

    function decrement() external {
        require(count > 0, "Cannot decrement below 0");
        count -= 1;
    }

    function getCount() external view returns (uint256) {
        return count;
    }
}
