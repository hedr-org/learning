# Shamir's Secret Sharing
## Introduction
[Secret Sharing](https://en.wikipedia.org/wiki/Secret_sharing) in cryptography refers to methods that split a given secret amongst `t` parties such that it requires at least `n` parties to figure out the whole secret, where `1 <= n <= t`.

Shamir and Blakley independently invented secret sharing in 1979, this document covers Shamir's Secret Sharing.
## Quick overview
1. Information-theoretically Secure - no group of parties with less than `n` shares of the secret can figure out the whole secret.
2. Perfect Secrecy - no information can be gained about the secret from any number of shares less than `n`.
3. Minimal - the size of each share does not exceed the size of the original secret.
4. Extensible - shares can be dynamically added or deleted without affecting existing shares
5. Dynamic - security can be enhanced by periodically constructing new shares for each participant
6. Flexible - each party can be allocated different number of shares
## Math
### Basis
[Lagrange interpolation theorem](https://en.wikipedia.org/wiki/Lagrange_polynomial) - `k` points are enough to reconstruct a polynomial of `k - 1` degree.
### Steps
1. Encode your secret as an integer `s`.
2. Figure out the minimum number of shares required to figure out the secret, `k`.
3. Construct a polynomial of degree `k - 1` such that the constant term is `s`.
4. Solve the polynomial `n` times to generate `n` shares.
## Code
### Security considerations
WIP
