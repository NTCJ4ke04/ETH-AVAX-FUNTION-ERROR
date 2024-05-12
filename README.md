# ETH-AVAX-FUNTION-ERROR
ITELECT 2 Module: Functions and Errors - ETH + AVAX Project
// SPDX-License-Identifier: MIT
pragma solidity >=0.6.8 <0.9.0;

contract MoralesContract {
    uint256 public value;
	address public owner;
	
	constructor() {
	owner = msg.sender;
	}
	
	function setValue(uint256 _newValue) public {

		require(msg.sender == owner, "Owner can only set the value");

		assert(_newValue != 0);

		if (_newValue < value){
		        revert("The value must be greater than or equal to current value");
            } else {

                value = _newValue;
