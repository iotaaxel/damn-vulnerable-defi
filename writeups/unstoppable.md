# Unstoppable Challenge Writeup

## Initial thinking
- At first, I considered using a ReEntrancy Attack. After all, they have been quite useful for hackers to score huge payouts. Upon reviewing the `UnstoppableLender.sol` code, I show that OpenZepplin's `ReentrancyGuard` is used. Specifically, `nonReentrant` mutex is used to guard against single-function reentrancy attacks.

## Approach
- I decided to try using a cross-function reentrancy attack. For this, I focused on the `transfer` function. I am able to transfer before the state is updated.

## Resources
- [Protect your Solidity Smart Contracts from Reentrancy attacks](https://medium.com/coinmonks/protect-your-solidity-smart-contracts-from-reentrancy-attacks-9972c3af7c21)
- [Solidity by Example: Re-entrancy](https://solidity-by-example.org/hacks/re-entrancy/)
-[Learn Web3: Reentrancy](https://learnweb3.io/courses/c446d19f-a25d-42c6-b3e4-4311c5040587/lessons/9e9b8ea7-156e-45ba-8540-5f86a9b8ccc2)