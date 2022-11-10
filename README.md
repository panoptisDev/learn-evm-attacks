# <h1 align="center"> Reproduced Exploits Library </h1>
A library with previously exploited vulnerabilities, categorized by type (common denominator of each exploit). 

Also, utils that perform flashloans and swaps are provided in `test/utils` to ease the job of reproducing future attacks.
 
Each exploit can be found under the test folder.

## Index
### [How to Install, Compile and Run](https://github.com/coinspect/prev-exploit-library#-hardhat-x-foundry-template-)

### Bad Input Validation
- [Olympus DAO Bond, Oct 2022 - ($300,000) - Arbitrary Tokens/Unchecked transfers](/test/Bad_Data_Validation/Bond_OlympusDAO.attack.sol)
- [Multichain a.k.a AnySwap, Jan 2022 - ($960,000) - Arbitrary Tokens/Unchecked Permit](/test/Bad_Data_Validation/Multichain_Permit.attack.sol)
- [Bad Guys NFT, Sept 2022 - (400 NFTs) - Unchecked mint amount](/test/Bad_Data_Validation/Bad_Guys_NFT.attack.sol)


### Business Logic
- [Fantasm Finance, Mar 2022 - ($2.4MM) - Unchecked payments while minting](/test/Business_Logic/Fantasm_Finance.attack.sol)
- [BVaults, Oct 2022 - ($35,000) - DEX pair manipulation](/test/Business_Logic/Bvaults.attack.sol)
- [Nomad Bridge, Aug 2022 - (~$190MM) - Invalid Root Hash Commitment / Poor root validation](/test/Business_Logic/NomadBridge.attack.sol)


# <h2 align="center"> How to Install, Compile and Run </h2>

**Template repository for getting started quickly with Hardhat and Foundry in one project**

### Getting Started

 * Use Foundry: 
```bash
forge install
forge test
```

 * Use Hardhat:
```bash
npm install
npx hardhat test
```

### Features

 * Write / run tests with either Hardhat or Foundry:
```bash
forge test
# or
npx hardhat test
```

 * Use Hardhat's task framework
```bash
npx hardhat example
```

 * Install libraries with Foundry which work with Hardhat.
```bash
forge install rari-capital/solmate # Already in this repo, just an example
```

### Notes

Whenever you install new libraries using Foundry, make sure to update your `remappings.txt` file by running `forge remappings > remappings.txt`. This is required because we use `hardhat-preprocessor` and the `remappings.txt` file to allow Hardhat to resolve libraries you install with Foundry.
