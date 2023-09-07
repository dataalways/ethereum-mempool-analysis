# Ethereum Mempool Analytics

This repository leverages Flashbots [public mempool datasets](https://mempool-dumpster.flashbots.net/index.html), combining the data wit block data from [Dune Analytics](https://dune.com/) to cluster transactions between private mempool, public mempool, and not-included transactions.

- The Flashbots data comes in parquet files.
- This notebook uses CSVs from Dune Analytics because the dataset would cost thousands of credits to download through the API.
  - https://dune.com/queries/3000017
- This notebook also uses a CSV from Dune Analytics for tracking sandwich trades, although this might make sense to do via the API.
  - https://dune.com/queries/3000675

**\
The attached script assumes that all the data files have been renamed in the convention of: YYYY-MM-DD-dune-transactions.csv, YYYY-MM-DD-sandwich-tx.csv, YYYY-MM-DD.parquet\
**

---

- Author: [Data Always](dataalways.substack.com)
- Last Modified: September 7, 2023

TODO: fix the sandwich data Dune query to output frontrun and backrun hashes in the same column.
- Currently the csv download requires post-processing to turn the two columns into one and rename the column 'hash'

---

An example of looking at transaction inclusion times:

![inclusion_times]

An example of looking at relative gas usage vs priority fees paid.

![pie_chart]



[inclusion_times]: ./tmp-figures/tx-profile.png
[pie_chart]: ./tmp-figures/pie-example.png