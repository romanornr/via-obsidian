
---

The original Viacoin is a cryptocurrency that supported embedded consensus. Embedded consensus is a design pattern or method for building layer-2 logic on top of Bitcoin without changing Bitcoin itself. 

In 2014 when Viacoin was launched with support for embedded consensus to create a system similar to what Mastercoin and its Counterparty were doing. Counterparty came out, and we thought that idea definitely had legs, but we believed it should be built on an altcoin.

There are many ways to embed data within the blockchain. Several methods, such as multisig encoding and OP_RETURN, embed data within the blockchain. While different ways are possible, the ability to censor embedded content within the Bitcoin blockchain raises questions and is open to discussion.

So you may wonder what OP_RETURN is and why it is important for embedding data. A bitcoin transaction is basically a script. So if I have some coins and want to transfer value to you, I write a transaction script where I sign over my coins or unspent outputs to you, which are encumbered to your address. 

So normally, the script is saying only the person who can now unlock it is the person who owns the private key for this Bitcoin address. That’s the most common Bitcoin transaction. So, for you to spend that, you have to supply your private key and then write a transaction message that unlocks that and sends it to someone else. So, within the Bitcoin scripting language, there are many different ‘commands’ within the scripting language, and OP_RETURN says the following is a bit of metadata. 

When Mastercoin came out, there was quite a reaction from bitcoin developers who viewed it more as blockchain spam. Their idea of a blockchain is just transactions, sending value from Alice to Bob instead of sending a “fake” transaction with the only goal of embedding some metadata and the same for Counterparty. Even right now in 2025 we still see the arguing and push back since Bitcoin Core developers and a part of its community view this as "bloating" the blockchain.  

Counterparty released its whitepaper and found a new way of encoding its metadata using OP_RETURN with 80 bytes of data. Within about a month of that paper's release, Bitcoin Core released a new version that sliced OP_RETURN from 80 bytes to 40. It was and still is unfortunate that many Bitcoin Developers believe sending metadata isn’t a valid use. 

Lots of people have a different view on what is a valid use of the (Bitcoin) blockchain. We don’t want to negatively judge Bitcoin Developers for the view they held or still hold because, in some sense, it’s valid and, in some ways, also understandable. In 2014, if you wanted to build an embedded consensus system, then Bitcoin was not the best due to the ongoing censorship at the time, which is why Viacoin was created. Viacoin accepted embedded consensus systems like Counterparty.

------

While the Counterparty developers were pushing hard to raise the limit due to issues with speed and transaction costs. However, Bitcoin Core refused. This led to frustration among the XCP team and highlighted just how dependent XCP was on Bitcoin. Being a second-layer token creation platform also meant being at the mercy of the Bitcoin Core Developers. 

Out of this frustration, a reaction was made. Okay, so what if we launch our own Blockchain since the Bitcoin Core developers don’t want bloat. Viacoin was launched to leave those underlying problems behind. 

If you’re going to create something like Counterparty or Mastercoin, you’re relying on an upstream project. If that upstream project is changing the rules underneath your feet, that’s a problem, especially when it comes to designing a system that could be used in finance and potentially scaled up.

Core developer Peter Todd was brought in as Chief Scientist, during which time Peter Todd helped implement BIP65 [CLTV (CheckLockTimeVerify) on the Viacoin blockchain](https://cointelegraph.com/news/peter-todd-and-the-expansion-of-bitcoin) before any other altcoin or Bitcoin. CheckLockTimeVerify was an innovation that would later become an essential feature in Bitcoin itself. The lightning network is possible due to CheckLockTimeVerify which Viacoin implemented before Bitcoin did. 

Because of this experimental and forward-thinking approach, Viacoin earned a reputation as a "testbed" blockchain. A place to try out potential improvements to Bitcoin without needing consensus from Bitcoin Core. We also implemented Segwit before Bitcoin did. 

Viacoin also ClearingHouse, which was like Counterparty, allowing various smart contracts and actions to be created and deployed. It was more of an integrated, stripped-down version of the Ethereum Virtual Machine to support basic smart contracts.

While Counterparty used Bitcoin as its settlement layer, Clearinghouse used Viacoin. Bitcoin Core had limited the OP_RETURN field to 40 bytes to censor the Counterparty. For Viacoin we extended OP_RETURN to 120 bytes for Viacoin's ClearingHouse project. 

It's worth nothing Bitcoin Core developers shot themselves a bit in the foot and raised the limit later back to 80 bytes. So, for example, with the proposal of stealth addresses back then, there may be a need to communicate some data to the recipient so that the data is then stored in the op return. Cutting down from 80 bytes to 40 bytes impaired the stealth address proposal as well, so it wasn’t just Counterparty that got into trouble.

Censoring transactions is difficult on the Bitcoin blockchain. People will constantly find a way to put metadata into the Bitcoin blockchain. It's like trying to cut the head off a hydra. Whilst one could reduce OP_RETURN 80 and cut that head off, then another bare multisig encoding raises its head and if you cut that heads off, then there’s surely another way to encode metadata. 

After that, Viacoin hired Peter Todd as Chief Scientist to research Treechains. One of the hurdles with blockchain is scalability. As more people use it, the network can get bogged out, leading to slower confirmation times, higher fees, etc. Treechains allows for blockchain scalability and side-chain coordination. Furthermore, Treechains would promote a greater degree of mining decentralization. Imagine a network of interconnected blockchains, like a tree with multiple branches, and each branch can process transactions independently, making the system much more scalable. It’s like taking the pressure off a single highway by creating a highway of interconnected roads. Remember, this was all in 2014.

---

Treechains did not gain traction (It was ambitious, maybe too ambitious) and as better concepts like rollups, state channels, and modular blockchains (Celestia, Optimism, etc.) tackled similar scalability challenges with clearer paths to implementation. Rollups bundle transactions off-chain and settle them on the main blockchain, while modular designs separate data storage from execution.

Rollups bundle transactions off-chain and settle them on the main blockchain, while modular designs separate data storage from execution. 

Viacoin had strengths, flexibility, and innovations, but running a separate blockchain came with challenges. Bitcoin has a massive hash power and global adoption, while it is true that Viacoin relied on auxiliary proof-of-work to thrive for years, while other proof-of-work coins could not. Viacoin was still based on Bitcoin and relied on large centralized exchanges, keeping it listed to have any value and keep miners incentivized to keep mining. 

A lot has changed over the past decade as Bitcoin has opened up potential layer 2 solutions that could extend its capabilities without bloating the chain.

Take Taproot, which became active in 2021. It brought better scripting and multi-signature efficiency, making more complex applications possible. The Lightning Network is made possible by CheckLockTimeVerify, which shows that Layer 2 can handle fast, cheap transactions. Even inscriptions such as Ordinals proved you could embed metadata on Bitcoin. Meanwhile, rollups and modular architecture were proving their worth on other chains, offering scalability and functionality while leaning on a secure settlement layer.

Rollups, which process transactions off-chain and settle them on Bitcoin instead of Ethereum could keep things fast, cheap without sacrificing security or bloating the chain for everyone. 

Then we started to wonder. Why keep pushing when we could build on Bitcoin itself? Running an altcoin based on Bitcoin, while Bitcoin’s ecosystem started to expand slowly. Viacoin gave us a head start, letting us test ideas like CLTV and ClearingHouse, but Bitcoin’s security, hash power, and user base were there and unprecedented. 

So, eventually, we made the call to build Via as our own Bitcoin Layer 2 solution. Using zk-rollups, we can process transactions off-chain extremely fast and cheap while settling them on Bitcoin instead of any other chain.

Bitcoin itself, being the most decentralized, superior sound asset backed by proof-of-work, real-world energy expenditure ensuring integrity, is also grounded in physics instead of committee votes. After all, why would we want to build on the “second best” if we can build on the best? The second-best chain is up for debate, but the best, without a doubt, is Bitcoin. 

Want smart contracts? We can have them, echoing the spirit of both Counterparty and ClearingHouse. We'll use Taproot for multi-signatures and inscriptions for metadata. 

It’s not about ditching Viacoin’s legacy, which cannot be explained in text. You just had to be there at the time. However, it’s about adapting and evolving. We’re taking the flexibility and practicality with us. Take Ethereum, for example. A large part of its market cap and TVL is dominated by Ethereum Layer 2, and the upside for Bitcoin L2s is huge. 

A layer 2 would let us scale up as we are not just building a new layer on top of Bitcoin but also an entire DeFi ecosystem.

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

