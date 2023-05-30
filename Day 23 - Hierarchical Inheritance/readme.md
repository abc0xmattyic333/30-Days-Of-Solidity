<div align="center">
  <h1> 30 Days Of Solidity: Hierarchical Inheritance</h1>
  <a class="header-badge" target="_blank" href="https://twitter.com/abc0xmattyic333">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/abc0xmattyic333?style=social">
  </a>

<sub>Author:
<a href="https://github.com/abc0xmattyic333" target="_blank">abc0xmattyic333</a><br>
<small> May 29th, 2023</small>
</sub>

</div>

[<< Day 22](../Day%2022%20-%20Multi-level%20Inheritance/readme.md) | [Day 24 >>](../Day%2024%20-%20Multiple%20Inheritance/readme.md)

![Cover](./cover.png)

---

# 📔 Day 23

## Hierarchical Inheritance

In Hierarchical inheritance, a parent contract has more than one child contracts. It is mostly used when a common functionality is to be used in different places.

**Example**: In the below example, contract A is inherited by contract B, contract A is inherited by contract C, thus demonstrating Hierarchical Inheritance.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

// Defining parent contract A
contract A {
    string internal x;

    function getA() external {
        x = "Hierarchical Inheritance";
    }

    uint256 internal sum;

    function setA() external {
        uint256 a = 10;
        uint256 b = 20;
        sum = a + b;
    }
}

// Defining child contract B inheriting parent contract A
contract B is A {
    // Defining external function to return state variable x
    function getAstr() external view returns (string memory) {
        return x;
    }
}

// Defining child contract C inheriting parent contract A
contract C is A {
    // Defining external function to return state variable sum
    function getAValue() external view returns (uint256) {
        return sum;
    }
}

// Defining calling contract
contract caller {
    // Creating object of contract B
    B contractB = new B();

    // Creating object of contract C
    C contractC = new C();

    // Defining public function to
    // return values of state variables
    // x and sum
    function testInheritance() public view returns (string memory, uint256) {
        return (contractB.getAstr(), contractC.getAValue());
    }
}
```

Output:

when we call the testInheritance function, the output is ("Hierarchical Inheritance", 30).

---

[<< Day 22](../Day%2022%20-%20Multi-level%20Inheritance/readme.md) | [Day 24 >>](../Day%2024%20-%20Multiple%20Inheritance/readme.md)
