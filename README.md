# Solana ETL Table Definitions

This repo contains table definitions for Solana.

If you want to parse logs and instructions on Solana and make them cheaper to query on BigQuery, feel free to submit a PR with your new table definitions.

The tables will be available in the `blockchain-etl.solana_{dataset}` dataset, e.g.:

```
SELECT *
FROM blockchain-etl.solana_mango.MangoMarketsV3_event_WithdrawLog 
WHERE date(block_timestamp) = '2022-04-24'
```

## How To Submit New Table Definitions

1. Fork this repository
2. Create a new branch and upload your new files to this branch
3. Create a PR to merge to this main repository
4. Wait for it to be reviewed and merged, your BigQuery tables should show up shortly under the \_\_ project.
5. Now you can query your newly parsed tables more efficiently and for a smaller cost.

## My Dataset doesn't show up?

Certain datasets are currently private while others are public.
If your blockchain is considered private, please sign up for a Nansen Query Plan with your google cloud account.
You will then be able to access theses private datasets.

## EVM Chains

For EVM chains refer to this repository https://github.com/nansen-ai/evmchain-etl-table-definitions
