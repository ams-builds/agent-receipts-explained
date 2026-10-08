# Jargon Buster

Plain-English explanations of the technical words in this project. The README does not use these words when it can. This file gives the exact words for readers who want them.

**Action type**
A name for the kind of action, for example `filesystem.file.delete`. The Agent Receipts taxonomy gives each action type a default risk level.

**Anchor checkpoint**
A small signed note with the newest chain position. The signer sends it to a place that the signer cannot change, for example a write-only file or a log service. It lets you find receipts that somebody removed from the end of the chain.

**Audit trail**
A record of what a system did, in the sequence that it did it. A good audit trail lets another person check the record.

**Chain**
A sequence of receipts. Each receipt holds the hash of the receipt before it. If somebody changes or deletes a receipt in the middle, the hashes do not agree, and verification fails.

**Daemon**
A program that runs in the background as a separate process. In Agent Receipts, the daemon holds the signing key and signs the receipts, so the agent itself does not hold the key.

**DID (decentralized identifier)**
An identifier for a person or an agent, for example `did:agent:my-agent`. A verifier uses it to find the public key of the signer.

**Ed25519**
The signature method that Agent Receipts uses. A private key makes the signature. Anybody with the public key can check it.

**Hash**
A short fingerprint of some data, made with SHA-256. If the data changes by one character, the hash changes completely.

**Issuer**
The agent that did the action and signed the receipt.

**Principal**
The person or organization who authorized the action. The principal is not the company that built the agent.

**Receipt**
A signed record of one action of an AI agent. In Agent Receipts, a receipt is a W3C Verifiable Credential.

**Reversal receipt**
A new receipt that records that somebody undid an earlier action. Receipts never change after the signature, so an undo gets its own receipt.

**Risk level**
One of four levels: low, medium, high, and critical. A system can make the risk level of an action higher. It must not make it lower than the default.

**Tail truncation**
An attack where somebody removes the newest receipts from the end of a chain. The remaining chain still looks correct, so you need anchor checkpoints to find it.

**Tamper-evident**
Made so that you can see a change. Tamper-evident does not stop a change. It makes the change easy to find.

**Taxonomy**
The list of action types that Agent Receipts defines, in groups such as filesystem, system, communication, and financial.

**Verifiable Credential**
A W3C standard format for a signed statement that another party can check.

**Verify**
To check the signature of each receipt and the hash links between the receipts.
