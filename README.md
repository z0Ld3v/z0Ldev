# Hello, I'm Zo 👋🏾
## About Me 🚀
I am a passionate Web3 Developer specializing in smart contract security research, dedicated to enhancing the security and reliability of decentralized applications. With a solid foundation in smart contract auditing, I am actively expanding my expertise to include comprehensive, high-level security analysis and mitigation strategies.

## Skills 💼
- **Languages**: Solidity
- **Frameworks/Tools**: Foundry, Remix
- **Testing & Security Tools**: Slither, Echidna, Aderyn

## Professional Development 🌱
- Security patterns in smart contract design
- Common vulnerabilities and exploits in smart contracts
- Advanced testing techniques for decentralized applications

## Projects 🛠️
Here’s a brief overview of some projects I've developed:
- **ERC20 Token**: A fully functional token adhering to the ERC20 standard.
- **Fund-Me Fundraiser Contract**: A decentralized platform for fundraising, leveraging smart contracts for transparent and secure transactions.
- **Smart Contract Lottery**: A decentralized lottery system implemented using Ethereum smart contracts.
- **Mood NFT**: A unique NFT project where users can mint NFTs reflecting their mood.
- **DeFi Stablecoin**: A stablecoin system designed to maintain a stable value through algorithmic mechanisms.
- **Simple DAO**: A basic decentralized autonomous organization allowing token holders to vote on community proposals.

## Smart Contract Audits 🔍
Additional audits are being conducted as I further advance the field of smart contract security through rigorous analysis and strategic enhancements.


   ## Audit #1: PasswordStore
   - **Summary:** This audit highlighted significant vulnerabilities in the PasswordStore contract, including:
     - **[H-1]** Storing the password on-chain without encryption makes it visible to anyone.
     - **[H-2]** Lack of access control on the `setPassword` function allows any user to change the stored password.
     - **[I-1]** Incorrect natspec comment in the `getPassword` function signature.

   - **Impact & Mitigations:** 
     - **Severity:** High (for H-1 and H-2)
     - **Mitigations:** Implement encryption, add access controls, and correct documentation.

   ## Audit #2: PuppyRaffle Audit Report
   - **Summary:** This audit identified multiple vulnerabilities in the PuppyRaffle contract, including:
     
      - **High Severity**
         - **[H-1]** Reentrancy attack in `PuppyRaffle::refund` allows entrant to drain raffle balance.
         - **[H-2]** Weak randomness in `PuppyRaffle::selectWinner` allows users to influence or predict winners.
         - **[H-3]** Integer overflow of `PuppyRaffle::totalFees` loses fees.
     
     - **Medium Severity**
         - **[M-1]** Potential denial of service (DoS) attack due to looping through players array to check for duplicates in PuppyRaffle::enterRaffle.
         - **[M-2]** Unsafe cast of `PuppyRaffle::fee` loses fees.
         - **[M-3]** Smart contract wallets raffle winners without a receive or a fallback function will block the start of a new contest.

     - **Low Severity**
         - **[L-1]** `PuppyRaffle:getActivePlayerIndex` returns 0 for non-existent players and for players at index 0, causing a player at index 0 to incorrectly think they have not entered the raffle.

     - **Gas Optimizations**
         - **[G-1]** Unchanged state variables should be declared constant or immutable.
         - **[G-2]** Storage variables in a loop should be cached.

     - **Informational / Non-Critical**
         - **[I-1]** Solidity pragma should be specific, not wide.
         - **[I-2]** Using an outdated version of Solidity is not recommended.
         - **[I-3]** Missing checks for `address(0)` when assigning values to address state variables.
         - **[I-4]** `PuppyRaffle::selectWinner` does not follow CEI, which is not a good practice.
         - **[I-5]** Use of "magic" numbers is not recommended.
         - **[I-6]** State changes are missing events.
         - **[I-7]** `PuppyRaffle::_isActivePlayer` is never used and should be removed.
     
     - **Impact & Mitigations:**
       
         - **Mitigations:** Follow CEI (Checks, Effects, Interactions) pattern, use a cryptographically secure random number generator, update Solidity version and use SafeMath.

More audits will be added as I further establish my expertise in smart contract security and contribute leading-edge practices to the industry.


## Let's Connect! 🌐
Feel free to reach out to me through the following platforms:
- **X**: [@z0Ldev](https://x.com/z0Ldev)
- **Email**: [z0Ldev@proton.me](mailto:z0Ldev@proton.me)

---

Thank you for visiting my GitHub profile! I'm always interested in collaborating on projects and ideas that push the boundaries of what's possible with blockchain technology and smart contract security.
