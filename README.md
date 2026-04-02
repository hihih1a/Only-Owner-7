# Only-Owner-7
Only Owner.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract OnlyOwner {
    address public owner;

    constructor() {
        owner = msg.sender;
    }

    function changeOwner(address _newOwner) public {
        require(msg.sender == owner, "Not owner");
        owner = _newOwner;
    }
}
