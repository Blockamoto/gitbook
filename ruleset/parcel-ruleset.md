---
description: An inscription process and schema for divorcing parcels from their districts.
---

# 🗞 parcel ruleset

{% hint style="info" %}
Click to expand for an explanation of the rule.
{% endhint %}

<details>

<summary><code>parcel# = txindex (starting from 0)</code></summary>

When referring to parcel number (<mark style="color:yellow;">parcel#</mark>), we are referring to an indexed transaction (<mark style="color:yellow;">txindex</mark>) within the block, starting from 0, which is the mining reward.

</details>

<details>

<summary><code>parcel claim command = parcel#.blockheight.bitmap</code></summary>

To claim a parcel, one simple appends their chosen <mark style="color:yellow;">parcel#.</mark> before <mark style="color:yellow;">blockheight.bitmap</mark>.

</details>

<details>

<summary><code>0.404.bitmap = example command to claim parcel 0 within district 404</code></summary>

In this example, the parcel corresponding to transaction 0 (miners reward) within Bitcoin Block 404 is claimed by the inscription, according to Bitmap Theory.

</details>

<details>

<summary><code>regex = ^(?:0|[1-9][0-9]*)\.(?:0|[1-9][0-9]*)\.bitmap$</code></summary>

This regular expression denotes the accepted characters usable according to the standard for claiming bitmap parcels. It means use two sequential numbers only, followed by .bitmap. The only valid transaction number beginning with 0 is 0. An invalid example would be 01.404.bitmap.

</details>

<details>

<summary><code>parcel# >= 0 and &#x3C; total transactions in parent block</code></summary>

The parcel number must be equal to or more than 0, and less than the total number of transactions in the parent block.

</details>

<details>

<summary>district holder address = parcel inscriber address</summary>

The district holder address must be the same address as the parcel inscriber address.

</details>

<details>

<summary>tapping = send to self</summary>

Tapping is a term that simply means to send-to-self. It signals the confirmation of an action, or the initiation of a command within a ruleset.

</details>

<details>

<summary>tap district to resolve all confirmed parcel inscriptions as valid/invalid (ends staking)</summary>

Once parcel inscription transactions have confirmed, the district must further be tapped. Untapped parcels refers to when a district has not been tapped since parcels inscribed. Untapped parcels are considered fake by the standard ruleset and indexing.

</details>

<details>

<summary>if the parent district is sent to another wallet before tapping to confirm, any parcels created will not be verified</summary>

If the district is sent to another wallet after inscribing its parcels, instead of the district being sent-to-self (tapped), any untapped parcels will be considered fake by indexing.

</details>

