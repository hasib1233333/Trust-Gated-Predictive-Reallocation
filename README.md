Title

Trust Gated Predictive Reallocation for Multi Robot Task Allocation Under Lossy Networks

Abstract

Decentralized task allocation in multi-robot systems typically relies on market-based auctions that assume every announce-bid-award-acknowledge message arrives reliably. Real deployments rarely meet that assumption: robots differ in transmit reliability due to hardware wear, antenna quality, or power budget. Existing communication-robust methods either reduce message frequency or reassign failed tasks after the fact; none treats reliability as a continuously estimated quantity shaping the allocation decision. This paper introduces Trust-Gated Predictive Reallocation (TGPR), a decentralized auction built around a per-robot Bayesian estimate of round-trip reliability, an idea standard in sensor-network security but not previously applied to auctions. TGPR discounts bids toward robots that are both capable and reachable, sizes the acknowledgment timeout adaptively per robot instead of one fixed value, and lets idle robots that overheard a stalled award claim it before the coordinator finishes its own recovery. We compare TGPR against fixed-timeout, backoff, periodic-reconciliation, and consensus-based baselines across five channel-quality regimes, two team sizes, and a hardware-heterogeneity ablation. TGPR cuts duplicate-execution waste by 24 percent and messaging overhead by 14 percent versus the simplest baseline, exceeding the consensus-based baseline similarly, with both gains widening as channel quality worsens. It does not improve, and in poor channel conditions significantly reduces, completion rate; the cost grows rather than shrinks with hardware heterogeneity, opposite to expectation. A factorial ablation traces this cost to the adaptive timeout component rather than trust-discounted ranking or bystander claiming, and identifies a tested alternative that keeps most of the efficiency gain while avoiding most of the cost.

Keywords

multi-robot task allocation, decentralized auctions, lossy communication, Bayesian trust, task reallocation, wireless reliability
