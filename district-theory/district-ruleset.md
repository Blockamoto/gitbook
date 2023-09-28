---
description: A schema for claiming districts upon the meta-terrain of a Bitcoin Block.
---

# 📃 district ruleset

{% hint style="info" %}
Click to expand for an explanation of each rule.
{% endhint %}

<details>

<summary><code>district = bitmap based upon blockheight</code></summary>

Bitcoins on-chain activity creates a natural meta-terrain made up of Blocks across spacetime, backed up and served immutably by each and every Bitcoin Node and Miner. By invoking the law of equivalence, a valid District takes on the traits of the block referenced by the blockheight number.

</details>

<details>

<summary><code>district claim command = blockheight.bitmap</code></summary>

To make a claim on a block, a text inscription must be made using Ordinals Theory. The inscription must contain the blockheight (based on sequential order of blocks on the chain, starting from 0), followed by .bitmap, as above. This is considered a District Claim. However, it is only verified as a valid .bitmap if it satisfies the full ruleset.

</details>

<details>

<summary><code>404.bitmap = example command to claim district at blockheight:404</code></summary>

This example demonstrates how you would claim district 404, based upon blockheight 404.

</details>

<details>

<summary><code>regex validation = ^(?:0|[1-9][0-9]*)\.bitmap$</code></summary>

This regular expression denotes the accepted characters usable according to the standard for claiming bitmap districts. It simply means use sequential numbers only, followed by .bitmap. The only valid bitmap number beginning with 0 is 0.

</details>

<details>

<summary><code>district claim ≤ inscription blockheight</code></summary>

The district being claimed must be equal to, or lower than the blockheight of the inscsription itself. This simply means, the block must exist at the time of the claim to be considered.

</details>

<details>

<summary><code>first is first = first valid inscription transaction on block</code></summary>

If there are multiple bitmap district claims within the same block, the winner is first valid inscription transaction.

</details>
