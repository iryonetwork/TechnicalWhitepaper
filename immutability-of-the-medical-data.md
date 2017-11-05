# **Immutability of the medical data**

The first line of defense is offered by zero-knowledge encryption itself. Data integrity is much more easily defendable when the attacker doesn't know what to change since everything is encrypted in the first place.

The second line is offered by redundant storage nodes and saved medical data checksums on the patient device. If anything gets changed, a user will know.

The final line of defense is to find out which node was changed. All storage nodes would provide cryptographic proofs to patients, by writing hashes in the EOS blockchain. Patients would be able to verify independently that the provided proof is really there \(with blockchain receipt\). That way if the checksum verification fails, compromised storage node can be easily identified and replaced.

To reduce the number of hashes, they will be aggregated into a Merkle tree. Clients get blockchain receipt[^1] they can use to independently verify the blockchain proof.

[^1]: whaaaat.

