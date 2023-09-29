---
description: A bitmap parcel represents a the landscape data of a bitcoin transaction.
---

# 🏡 parcel theory

Parcel theory poses that each Bitcoin transaction within a Block is a Parcel in a Bitmap District.

Applying bitmap theory, we transmute the data into its natural spatial analogues, which becomes the landscape of the parcel.

Each district is made up of at least 1 parcel, just as each block is made up of at least 1 transaction.

In the example of `404.bitmap`, there is only one parcel, which is referred to as `0.404.bitmap`

The Parcel is an intrinsic part of the District meaning that when a District is inscribed, it comes with all the parcels within it.

Furthermore, Parcels can be inscribed by the District owners which effectively detaches the Parcel from the District, allowing the fractionalization of the District and distribution of Parcels.

This process, known as Parcelling, is achieved by inscribing the parcel-number (in transaction order upon block, starting from 0) followed by the _blockheight_ number, followed by `.bitmap`. To prevent the potential of front-running, users MUST confirm the parcel by _tapping_ the district. Tapping simply means to send the district to yourself to confirm.

Parcel inscriptions must follow the [parcel-ruleset.md](../ruleset/parcel-ruleset.md "mention") to recognized within parcel theory.
