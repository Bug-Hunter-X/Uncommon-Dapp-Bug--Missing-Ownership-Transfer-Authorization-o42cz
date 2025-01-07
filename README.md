# Uncommon Dapp Bug: Missing Ownership Transfer Authorization

This repository demonstrates a common vulnerability in Dapps where ownership transfer lacks authorization checks.  The bug allows anyone to transfer ownership of the contract.  The solution adds the necessary check to ensure only the current owner can perform the transfer.

## Vulnerability

The original contract allows any address to call `transferOwnership`, bypassing any authentication mechanism.  This is a critical security flaw.

## Solution

The fix involves adding a check within the `transferOwnership` function to ensure that only the current owner (`_owner`) can execute the transfer. This prevents unauthorized changes to the contract's ownership.

## How to use

1. Clone this repository.
2. Compile and deploy both the buggy and fixed versions of the contract.
3. Experiment to see how the vulnerability manifests in the buggy contract and is mitigated in the fixed contract.