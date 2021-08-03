# Plutus-Pioneer-Program
I was part of the second cohort which had  early access to a set of courses that taught the core principles of Haskell and Plutus.

This is week by week of what I learned and the assignments I completed all annotated.

- [Lecture #1](https://youtu.be/_zr3W8cgzIQ)

  - Welcome.
  - The (E)UTxO-model.
  - Building the example code.
  - An auction contract in the EUTxO-model.
  - A brief look at the auction code.
  - Running an example auction contract on a local Playground.
  - Homework.

- [Lecture #2](https://youtu.be/sN3BIa3GAOc)

  - Triggering change.
  - Low-level, untyped on-chain validation scripts.
  - High-level, typed on-chain validation scripts.

- [Lecture #3](https://youtu.be/6_rfCCY9_gY)

  - Script contexts.
  - Time handling.
  - Parameterized contracts.

- [Lecture #4](https://youtu.be/g4lvA14I-Jg)

  - Monads.
  - The `EmulatorTrace`-monad.
  - The `Contract`-monad.

- [Lecture #5](https://youtu.be/SsaVjSsPPcg)

  - Values.
  - Native Tokens.
  - NFT's.

- [Lecture #6](https://youtu.be/24SHPHEc3zo)

  - Oracles.
  - Using the PAB.

## Code Examples

- Lecture #1:  [English Auction](code/week01)
- Lecture #2:  [Simple validation](code/week02)
- Lecture #3:  [Script Context & Parameterized Contracts](code/week03)
- Lecture #4:  [Monad, Traces & Contracts](code/week04)
- Lecture #5:  [Native Tokens](code/week05)
- Lecture #6:  [Oracles](code/week06)

## Exercises

- Week #1

  - Clone the [The Plutus repository](https://github.com/input-output-hk/plutus), check out the correct commit
    as specified in [cabal.project](code/week01/cabal.project).
  - Install NixOS cross-referencing the following resources.
     - https://nixos.org/download.html
     - https://docs.plutus-community.com
     - A few resources to understand the what and why regarding NixOS
       - https://nixos.org/manual/nix/stable
       - https://serokell.io/blog/what-is-nix
  - Set-up IOHK binary caches [How to set up the IOHK binary caches](https://github.com/input-output-hk/plutus#iohk-binary-cache). "If you do not do this, you will end up building GHC, which takes several hours. If you find yourself building GHC, STOP and fix the cache."
  - Enter a `nix-shell`.
  - Build the [English Auction](code/week01) contract with `cabal build` (you may need to run `cabal update` first).
  - Go to the `plutus-playground-client` folder.
  - Start the Playground server with `plutus-playground-server`.
  - Start the Playground client (in another `nix-shell`) with `npm run start`.
  - Copy-paste the auction contract into the Playground editor.
  - Compile.
  - Simulate various auction scenarios.

- Week #2

  - Fix and complete the code in the [Homework1](code/week02/src/Week02/Homework1.hs) module.
  - Fix and complete the code in the [Homework2](code/week02/src/Week02/Homework2.hs) module.

- Week #3

  - Fix and complete the code in the [Homework1](code/week03/src/Week03/Homework1.hs) module.
  - Fix and complete the code in the [Homework2](code/week03/src/Week03/Homework2.hs) module.

- Week #4

  - Implement function `payTrace` in the [Homework](code/week04/src/Week04/Homework.hs) module.
  - Handle exceptions thrown by `submitTx` in function `payContract` in the same module.

- Week #5

  - Add a deadline to the minting policy in the [Homework1](code/week05/src/Week05/Homework1.hs) module.
  - Fix the token name to the empty ByteString in the NFT contract in the [Homework2](code/week05/src/Week05/Homework2.hs) module.

- Week #6

  - Get the Oracle demo running and extend it in some way.

