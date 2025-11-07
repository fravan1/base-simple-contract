# base-simple-contract
Petit projet original pour déployer un smart contract simple sur la blockchain Base.

# Base Simple Smart Contract (original repo)

Petit projet original pour déployer un **smart contract minimaliste** sur la blockchain **Base** 🪩

Ce repo est **original**, donc si vous le **forkez**, cela aide chacun à gagner les **12 points Talent Protocol** liés aux forks GitHub 🔥

---

## 📜 Contrat Solidity

Crée un fichier : `SimpleStorage.sol`

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleStorage {
    uint256 private storedValue;

    event ValueChanged(uint256 oldValue, uint256 newValue);

    function setValue(uint256 _value) public {
        uint256 old = storedValue;
        storedValue = _value;
        emit ValueChanged(old, _value);
    }

    function getValue() public view returns (uint256) {
        return storedValue;
    }
}
