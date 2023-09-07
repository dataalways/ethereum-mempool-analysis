# Ethereum Mempool Analytics

This repository leverages Flashbots [public mempool datasets](https://mempool-dumpster.flashbots.net/index.html), combining the data wit block data from [Dune Analytics](https://dune.com/) to cluster transactions between private mempool, public mempool, and not-included transactions.

**\
The attached script assumes that all the data files have been renamed in the convention of: YYYY-MM-DD-dune-transactions.csv, YYYY-MM-DD-sandwich-tx.csv, YYYY-MM-DD.parquet\
**

---

- Author: [Data Always](dataalways.substack.com)
- Last Modified: September 7, 2023

---

An example of looking at transaction inclusion times:

![inclusion_times]

An example of looking at relative gas usage vs priority fees paid.

![pie_chart]



[inclusion_times]: ./tmp-figures/tx-profile.png
[pie_chart]: ./tmp-figures/pie-example.png