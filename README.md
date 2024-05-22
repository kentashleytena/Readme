// SPDX-License-Identifier: MIT
pragma solidity >=0.6.12 <0.9.0;

contract HelloWorld {
 
 string public tokenName = "ITELECTIVE";
 string public tokenAbbrv = "SOLIDITY";
 uint public totalSupply = 0;

    mapping(address => uint) public balances;

  function mint (address _address, uint value) public  {
    totalSupply += value;
    balances[_address] += value;
  }
  function burn (address _address, uint value) public  {
    if (balances[_address] >= value) {
      totalSupply -= value;
      balances[_address] -= value;
    }
  }
  }
