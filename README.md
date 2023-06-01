# Topic: Using Subgraphs for Flipside Defi and Dex Labels

Subgraphs are a product of [The Graph](https://thegraph.com/), which provide an industry standard on how to access blockchain data via open APIs. Many defi & dex protocols leverage subgraphs to track activity within their liquidity pools. Since these subgraphs are open, we can also tap into the data and label these pools!

In order to be able to tap into these open APIs we are going to leverage Flipside Crypto's LiveQuery capabilities, which allows us to call an API within our SQL statements. 
For more information revolving around the LiveQuery capabilities, check out our previous [Beehive article](https://flipsidecrypto.beehiiv.com/p/real-time-crypto), which summarizes and provides examples!

# Reproduce Analysis

All analysis is reproducible using the R programming language. You'll need (1) an API key to copy our SQL queries and extract data from the [FlipsideCrypto data app](https://next.flipsidecrypto.xyz/); and (2) renv to get the exact package versions we used.

## shroomDK

shroomDK is an R package that accesses the FlipsideCrypto REST API; it is also available for Python. You pass SQL code as a string to our API and get up to 1M rows of data back!

Check out the [documentation](https://docs.flipsidecrypto.com/flipside-api/getting-started) and get your free API Key today.

## renv

renv is a package manager for the R programming language. It ensures analysis is fully reproducible by tracking the exact package versions used in the analysis.

`install.packages('renv')`

## Instructions

To replicate this analysis please do the following:

1.  Clone this repo.
2.  Save your API key into a .txt file as 'api_key.txt' (this exact naming allows the provided .gitignore to ignore your key and keep it off github).
3.  Open the `Subgraphs-for-Labels` R Project file in your R IDE (we recommend, RStudio).
4.  Confirm you have renv installed.
5.  Restore the R environment using `renv::restore()` while in the `Subgraphs-for-Labels` R Project.
6.  You can now run `Subgraph_labels.Rmd`

If any errors arise, double check you have saved your API key in the expected file name and format.
