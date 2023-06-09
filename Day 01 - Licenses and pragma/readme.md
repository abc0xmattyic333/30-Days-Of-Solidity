<div align="center">
  <h1> 30 Days Of Solidity: Licenses and Pragma</h1>
  <a class="header-badge" target="_blank" href="https://twitter.com/abc0xmattyic333">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/abc0xmattyic333?style=social">
  </a>

<sub>Author:
<a href="https://github.com/abc0xmattyic333" target="_blank">abc0xmattyic333</a><br>
<small> May 29th, 2023</small>
</sub>

</div>

[Day 2 >>](../Day%2002%20-%20Comments/readme.md)

![Day X](./cover.png)

---

# 📔 Day 1

## Licenses

```solidity
// SPDX-License-Identifier: License Name
```

SPDX license identifiers should be added to the top of contract files.
The license should be from one of the following: [https://spdx.org/licenses/](https://spdx.org/licenses/).

⚠️ If the license identifier isn’t included in the contract file the compiler will now show a warning.

❗ If there are multiple license identifiers in the contract file the compiler will now show an error.

eg -

```solidity
// SPDX-License-Identifier: MIT
```

---

## Pragma

In Solidity the pragma keyword is used to configure compiler features and checks. The pragma directive is always local to the current file and is not global. Hence to make it applicable in your entire project of Solidity you have to include pragma directive in every file to work.

The first line is a pragma directive which tells that the source code is written for which Solidity version.

```solidity
pragma solidity ^0.8.20;
// Anything above 0.8.20

pragma solidity >=0.8.0 <0.9.0;
// Anything between 0.8.0 to 0.9.0 where 0.9.0 is not included.

pragma solidity 0.8.20;
// Only Version 0.8.20
```

---

[Day 2 >>](../Day%2002%20-%20Comments/readme.md)
