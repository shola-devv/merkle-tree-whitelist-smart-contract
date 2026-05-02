# 🌿 Merkle Tree Whitelist — Foundry

A gas-efficient whitelist using Merkle Trees. Only the root is stored on-chain; users prove inclusion with off-chain proofs.

---

## How It Works

- Off-chain: build a Merkle Tree from `(address, maxMintAllowance)` pairs
- On-chain: store only the `bytes32` root
- At mint time: user submits a proof → contract verifies it

**Leaf encoding:**
```solidity
keccak256(abi.encodePacked(msg.sender, maxAllowanceToMint))
```

---

## Contracts

### `Whitelist.sol`
```solidity
constructor(bytes32 _merkleRoot)

function checkInWhitelist(bytes32[] calldata proof, uint64 maxAllowanceToMint) public view returns (bool)
```
Verifies a Merkle proof against the stored root using the [Murky](https://github.com/dmfxyz/murky) library.

---

## Project Structure
```
merkle-trees/
├── src/
│   └── Whitelist.sol
├── test/
│   └── MerkleRoot.t.sol
└── lib/
    └── murky/
```

---

## Getting Started

**Prerequisites:** [Foundry](https://book.getfoundry.sh/getting-started/installation)

```bash
git clone <your-repo-url>
cd merkle-trees
forge install dmfxyz/murky
forge build
forge test
```

---

## Use Cases
- NFT mint whitelists
- Token distribution allowlists
- On-chain access control
