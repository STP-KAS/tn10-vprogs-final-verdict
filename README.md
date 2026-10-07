> **Experimental. We are just trying this.**
>
> Good intentions, shaky hands. STP does not know what he is doing. We test, we write down what we think we saw, and that is the whole product. A number here is not the truth. A chart is not the truth. Any other sentence that sounds sure of itself is not the truth either. Do not count any of it as a claim.
>
> [Disclaimer](DISCLAIMER.md)

> **Experimental only. Not a product.**
>
> Do not use wallet integrations on this GitHub. STP remains a clown. [DISCLAIMER.md](DISCLAIMER.md)

# Final verdict (up for debate)

**26 Sep 2026. Testnet-10 only. Not Kaspa core. Not an audit. Not advice.**

This verdict reads one document: [STP-KAS/tn10-vprogs-build-opinion](https://github.com/STP-KAS/tn10-vprogs-build-opinion), including [CHECKS.md](https://github.com/STP-KAS/tn10-vprogs-build-opinion/blob/main/CHECKS.md). That opinion is the evidence. This page is the decision. The decision is up for debate. A later measurement listed below replaces it.

The opinion already named [biryukovmaxim](https://github.com/biryukovmaxim) on [issue 1](https://github.com/STP-KAS/tn10-vprogs-build-opinion/issues/1). This page does not add a second request. If the mention was noise, kick this desk out.

## Verdict

Testnet-10 kept making blocks and taking transactions through this one-operator flood. The headline numbers in the public stress notes do not describe that chain.

What the evidence supports:

- **Packing, not the 12,175 peak.** A signed minimum payment packs at about 3,079 per second. A payment that creates a 0.5 tKAS output packs at about 250 per second, storage mass about 20,000, about 25 per block. Their unsigned mass-571 scripts pack at about 8,760 per second only if each transaction is counted once. The published 12,175 is a 10-second peak of transactions inside processed block bodies. The same transaction can sit in more than one block. That peak is above the 8,760 ceiling. It is the wrong number for selected-chain throughput.
- **The vprogs client lost the flood. The guest rule held, in exec mode.** Upstream tic-tac-toe finished 5 games under the full storm, then 8. The failures were a relay-floor fee, a coin still in the mempool, and an assert when the first coin was too small for the deposit. The small guest executed 0 of 3,518 impossible debits, then 0 of 4,291. Proofs were off. Rounds 5 and 6, including 63,614 and 600,055 finished games, are ordinary L1 payload chains. They are not vprogs.
- **The node lost to a lowered cap, then to disk.** kaspad 2.1.0 exited once on `100001 > 100000`. That cap is `--ram-scale=0.1`. The default cap is 1,000,000. Later peaks near 100,000 evicted transactions and did not panic. A restart drops the mempool. The long run stopped because free disk ran out. The 26 Sep pruning move grew consensus data from about 75 GB to about 89 GB with the storm already off.
- **The public health document was stale and said it was synced.** At about 15:31 CEST on 26 Sep, `/info/health` still reported blue score 568,825,293, `isSynced: true`, and a transaction time of 21:45:05 CEST on 25 Sep. The live blue score was 569,462,361. The cause is not in the evidence. The overload is only a neighbor in time.
- **Pull 165 is identified, not confirmed.** It is open, draft, and unmerged, head `081af9b9de0689b61e1a456cf296a4ad9e562b73`. The file list matches the opinion. Nobody in that note retested it. The hosted demo's settlement had moved, to settled DAA 580,940,363, and was still about 39,844 DAA behind the virtual score. vprogs master was still `f9b84a8`. The runs themselves were on `3a61c0b`.

Gross fees in the notes are a counter, not a cost. Their miners were finding a large share of TN10 blocks, so much of that fee came back as coinbase. No reconciled net is in the public set.

## Up for debate

The verdict changes if a public measurement does any of these:

1. A selected-chain count, not the processing log, holds a rate above the packing ceilings above.
2. The same mempool assert fires at the default cap of 1,000,000, or a fair run shows it does not.
3. A retest on pull 165, with `--utxoindex`, shows games finishing through a flood, or shows the carrier assert and the in-mempool coin reuse still there. Record the fee per game and how often one carrier spends almost the whole coin.
4. The indexer stall gets a cause. Timing next to this flood is not a cause.
5. One fee window matched against miner coinbase produces a net that is not "about 57% came back."
6. The round-5 storage-mass figure of about 69,000 grams, which the opinion did not recompute from a raw transaction, comes out different.

Until one of those is public, the decision stays: the testnet held, the headlines do not, the vprogs client lost to its fee and its coins, the node lost to an assert at a cap the operator lowered and then to disk, and the public health document was stale while saying it was synced.

This is not a mainnet result. This is not a product testnet. This is not a passed review of pull 165. Whether the verdict is useful is up for debate.

## Scope

The opinion left [sixpack.wtf](https://github.com/STP-KAS/sixpack.wtf), [kaspa-master-file](https://github.com/STP-KAS/kaspa-master-file), [kns-spec](https://github.com/STP-KAS/kns-spec), and [kns-tn10-testing](https://github.com/STP-KAS/kns-tn10-testing) outside the stress reading. This verdict leaves them there. Private repos were not used. No wallet address, seed, or key is in this repository.

---

> **Standard disclaimer.** This GitHub, not the topic above.
>
> Intentions are good; thought process is questionable. STP remains delusional. Si vis pacem, para bellum.
>
> Intern at https://sixpack.wtf/  
> X: https://x.com/StppStp · GitHub: https://github.com/STP-KAS
