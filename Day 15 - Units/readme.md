<div align="center">
  <h1> 30 Days Of Solidity: Units</h1>
  <a class="header-badge" target="_blank" href="https://twitter.com/abc0xmattyic333">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/abc0xmattyic333?style=social">
  </a>

<sub>Author:
<a href="https://github.com/abc0xmattyic333" target="_blank">abc0xmattyic333</a><br>
<small> May 29th, 2023</small>
</sub>

</div>

[<< Day 14](../Day%2014%20-%20Mappings/readme.md) | [Day 16 >>](../Day%2016%20-%20Require%20Statement/readme.md)

![Day 15](./cover.png)

---

# 📔 Day 15

In solidity we can use wei, gwei or ether as a suffix to a literal to be used to convert various ether based denominations. Lowest unit is wei and 1e12 represents 1 x 10^12.

Similar to currency, Solidity has time units where lowest unit is second and we can use seconds, minutes, hours, days and weeks as suffix to denote time.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract MyUnits {
    // 1 wei == 1
    // 1 gwei == 1e9
    // 1 ether == 1e18
    uint256 costOfNFT = 12.5 ether;
    uint256 gasLimit = 3000 wei;

    //1 == 1 seconds
    //1 minutes == 60 seconds
    //1 hours == 60 minutes
    //1 days == 24 hours
    //1 weeks == 7 days

    uint256 durationOfMint = 7 days;
}
```

---

[<< Day 14](../Day%2014%20-%20Mappings/readme.md) | [Day 16 >>](../Day%2016%20-%20Require%20Statement/readme.md)
