<div align="center">
  <h1> 30 Days Of Solidity: Function Modifiers </h1>
  <a class="header-badge" target="_blank" href="https://twitter.com/abc0xmattyic333">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/abc0xmattyic333?style=social">
  </a>

<sub>Author:
<a href="https://github.com/abc0xmattyic333" target="_blank">abc0xmattyic333</a><br>
<small> May 29th, 2023</small>
</sub>

</div>

[<< Day 18](../Day%2018%20-%20Revert%20Statement/readme.md) | [Day 20 >>](../Day%2020%20-%20Constructors/readme.md)

![Cover](./cover.png)

---

# 📔 Day 19

Modifiers assist in the execution of a function’s behavior. The behavior of a function can be changed using a function modifier, they can also be called before or after a function is executed.

Solidity function modifiers help in the following:

- To access restrictions
- Input accuracy checks
- Hacks protection

Example:

```solidity
contract Owner {
   modifier onlyOwner {
      require(msg.sender == owner);
      _;
   }
}
```

The function body is inserted where the special symbol "\_;" appears in the definition of a modifier. So if condition of modifier is satisfied while calling this function, the function is executed and otherwise, an exception is thrown.

Example:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Mint {
    constructor()  {
        owner = msg.sender;
    }
    modifier onlyOwner {
      require(msg.sender == owner);
      _;

    function _mint(address to , uint tokenId) onlyOwner {
      mint(to, tokenId);
    }
}
```

[<< Day 18](../Day%2018%20-%20Revert%20Statement/readme.md) | [Day 20 >>](../Day%2020%20-%20Constructors/readme.md)
