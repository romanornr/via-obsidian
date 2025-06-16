
---

**
The original Viacoin is a cryptocurrency that supported embedded consensus. Embedded consensus is a design pattern or method for building layer-2 logic on top of Bitcoin without changing Bitcoin itself. 

In 2014 when Viacoin was launched with support for embedded consensus to create a system similar to what Mastercoin and its Counterparty were doing. Counterparty came out, and we thought that idea definitely had legs, but we believed it should be built on an altcoin.

When Mastercoin came out, there was quite a reaction from bitcoin developers who viewed it more as blockchain spam. Their idea of a blockchain is just transactions, sending value from Alice to Bob instead of sending a “fake” transaction with the only goal of embedding some metadata and the same for Counterparty. Even right now in 2025 we still see the arguing and push back since Bitcoin Core developers and a part of its community view this as "bloating" the blockchain.  

Counterparty released its whitepaper and found a new way of encoding its metadata using OP_RETURN with 80 bytes of data. Within about a month of that paper's release, Bitcoin Core released a new version that sliced OP_RETURN from 80 bytes to 40. It was and still is unfortunate that many Bitcoin Developers believe sending metadata isn’t a valid use. 

If you’re going to create something like Counterparty or Mastercoin, you’re relying on an upstream project. If that upstream project is changing the rules underneath your feet, that’s a problem, especially when it comes to designing a system that could be used in finance and potentially scaled up.
**


**
While the Counterparty developers were pushing hard to raise the limit due to issues with speed and transaction costs. However, Bitcoin Core refused. This led to frustration among the XCP team and highlighted just how dependent XCP was on Bitcoin. Being a second-layer token creation platform also meant being at the mercy of the Bitcoin Core Developers. 

Out of this frustration, a reaction was made. Okay, so what if we launch our own Blockchain since the Bitcoin Core developers don’t want bloat. Viacoin was launched to leave those underlying problems behind. 

Core developer Peter Todd was brought in as Chief Scientist, during which time Peter Todd helped implement CLTV (CheckLockTimeVerify) on the VIA blockchain before any other altcoin or Bitcoin. CheckLockTimeVerify was an innovation that would later become an essential feature in Bitcoin itself. For example, it’s now being used for the lightning network. 

Because of this experimental and forward-thinking approach, VIA earned a reputation as a "testbed" blockchain. A place to try out potential improvements to Bitcoin without needing consensus from Bitcoin Core. We also implemented Segwit before Bitcoin did. 

Viacoin also released ClearingHouse, which was like Counterparty, allowing various smart contracts and actions to be created and deployed. It was more of an integrated, stripped-down version of the Ethereum Virtual Machine to support basic smart contracts.

While Counterparty used Bitcoin as its settlement layer, Clearinghouse used Viacoin. Bitcoin Core had limited the OP_RETURN field to 40 bytes to censor the Counterparty. It's worth nothing Bitcoin Core developers shot themselves a bit in the foot and raised the limit later back to 80 bytes. 

After that, Viacoin hired Peter Todd as Chief Scientist to research Treechains. One of the hurdles with blockchain is scalability. As more people use it, the network can get bogged out, leading to slower confirmation times, higher fees, etc. Treechains allows for blockchain scalability and side-chain coordination. Furthermore, Treechains would promote a greater degree of mining decentralization. Imagine a network of interconnected blockchains, like a tree with multiple branches, and each branch can process transactions independently, making the system much more scalable. It’s like taking the pressure off a single highway by creating a highway of interconnected roads. Remember, this was all in 2014.

However Treechains failed to gain traction as better concepts like rollups, state channels, and modular blockchains (Celestia, Optimism, etc.) tackled similar scalability challenges with clearer paths to implementation.

**
## Background: Mastercoin, Counterparty, and “Blockchain Spam”

- **Mastercoin (Early Layer-2 Attempt)**
  - Introduced the concept of embedding metadata in Bitcoin transactions.
  - Sparked controversy among Bitcoin developers who saw it as “blockchain spam.”
  - Bitcoin devs viewed the Bitcoin blockchain **exclusively** for monetary transactions (Alice → Bob), not for arbitrary data embedding.

- **Counterparty (XCP)**
  - Similar goals: **Layer-2** functionality on Bitcoin (e.g., token issuance, smart contracts).
  - Relied on `OP_RETURN` to store metadata:
    - Initially **80 bytes** of data.
    - Bitcoin Core devs soon **reduced** this to **40 bytes**, effectively limiting XCP’s scalability.

- **Problem: Upstream Dependency**
  - Projects like Mastercoin and Counterparty **depended** on Bitcoin Core.
  - If the **upstream rules change** (e.g., reducing `OP_RETURN` size), the layer-2 project is at risk.
  - This highlighted the **risks** of relying on Bitcoin as a settlement layer for advanced features.

---

## Birth of Viacoin:

- **Catalyst:**
  - Frustration with Bitcoin Core’s strict limitation on `OP_RETURN`.
  - Desire to support **embedded consensus** without being at the mercy of upstream changes.
- **Goal:** Create a cryptocurrency and blockchain where second-layer features (like Counterparty) could live **natively**, with a larger `OP_RETURN` field (120 bytes).

---

## Experimental “Testbed” Blockchain

- **Peter Todd’s Role (Chief Scientist)**
  - Hired early in VIA’s development.
  - Implemented **CheckLockTimeVerify (CLTV)** on Viacoin **before** Bitcoin or other altcoins.
  - **SegWit** was also implemented on VIA **prior** to Bitcoin.
- **Reputation:**
  - Viacoin became a **“testbed”** chain—innovating with features destined for Bitcoin but without requiring Bitcoin Core’s consensus.

---

##  ClearingHouse vs. Counterparty

- **ClearingHouse on Viacoin:**
  - Inspired by Counterparty’s model.
  - Uses Viacoin (instead of Bitcoin) as the settlement layer.
  - Allows creation and deployment of **smart contracts** or other second-layer logic.
- **Why It Matters:**
  - Larger `OP_RETURN` size (120 bytes) for storing metadata (e.g., “mint 100 tokens”).
  - Faster/cheaper than embedding the same data in Bitcoin.

---

## Embedded Consensus and Scalable Layer-2

- **Definition of Embedded Consensus:**
  - Protocol rules enforced **off-chain**, with crucial data anchored “on-chain” (via `OP_RETURN` or similar).
  - No changes needed in the base protocol’s consensus rules.
- **Importance for Viacoin:**
  - Frees developers from Bitcoin’s restrictive `OP_RETURN`.
  - Allows more complex token logic, smart contracts, or notary services to exist **natively**.

---

## Blockchain Notary and Custody Chains

- **Blockchain Notary:**
  - Timestamp digital assets (art, documents, intellectual property).
  - Provides a tamper-proof record of creation/ownership.
- **Custody Chains:**
  - Track **ownership** changes over time (e.g., supply chain, evidence handling).
  - All transfers recorded and verified on the blockchain.
- **Proof of Existence (PoE):**
  - Hash critical documents (like **Supreme Court rulings**) on-chain.
  - Any tampering = mismatch with on-chain hash.

---

## Scalability: Treechains Research

- **Peter Todd’s Focus:**
  - Research on **Treechains**, a concept for **horizontal/branched** scalability.
  - Distributes load across multiple sub-chains for parallel processing.
- **Advantages:**
  - Greater **mining decentralization** and faster transaction throughput.
  - A blueprint for **side-chain** coordination without bogging down a single main chain.

---

## Bitmessage Integration Possibilities

- **Bitmessage:**
  - Decentralized, encrypted messaging protocol.
  - Potential synergy with Viacoin for **censorship-resistant** communication.
- **Security Implications:**
  - Strong encryption disliked by certain agencies (e.g., NSA).
  - Embedding or integrating Bitmessage-like protocols could broaden VIA’s use cases.

---

## Post-Launch Developments

- **Overstock Rumors (2015):**
  - Speculation that Overstock might integrate Viacoin.
  - Ultimately did not materialize.
- **BtcDrak’s Next Project (XCH):**
  - Similar in spirit to Counterparty (XCP).
  - Generated hype about potential integration with **ETM** (Electronic Transaction Machine) systems.

---

##  Notes

1. **Origins in Friction:** Viacoin was born because Bitcoin Core’s policies limited `OP_RETURN`, hindering projects like Counterparty and Mastercoin.
2. **Independence & Innovation:** VIA served as a self-contained ecosystem (larger `OP_RETURN`, faster transactions) for **embedded consensus** and advanced features.
3. **Testbed Success:** Early adoption of **CLTV**, **SegWit**, and research into **Treechains** all happened on VIA before Bitcoin.
4. **Real-World Applications:**  
   - **Blockchain Notary**, **Custody Chains**, and **Proof of Existence** were envisioned and implemented in some form as early as **2014**.
   - Potential integration with decentralized messaging (Bitmessage).
5. **Future Directions:**  
   - Shows how altcoins can experiment with new features Bitcoin may adopt later.
   - Highlights the tension between “pure monetary transactions” vs. “meta-transactions” in the blockchain space.

---

## References & Further Reading

- **Counterparty (XCP) vs. Mastercoin**  
  - [[Counterparty Docs]](https://counterparty.io/docs/)  
  - Historical references on Mastercoin (later Omni).
- **Viacoin & ClearingHouse**  
  - [[Viacoin Site]](https://viacoin.org/)  

---

