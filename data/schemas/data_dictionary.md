# Kindred RAG Data Dictionary

This document provides detailed information about the datasets in this repository to facilitate efficient use with Retrieval Augmented Generation (RAG) systems.

## Brands Dataset

The brands dataset contains information about E-Commerce Merchant.

| Field Name | Data Type        | Description                                                | Example                                                                        |
| ---------- | ---------------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------ |
| brand_id   | string (UUID)    | Unique identifier for the brand                            | "1db1f766-18be-4a52-9354-166667df5c72"                                         |
| name       | string           | Name of the brand                                          | "Created Brilliance Diamonds"                                                  |
| logo       | string or null   | URL to the brand's logo image or NULL if no logo available | "https://cdn.sitesasset.com/affiliate-static/2022/12/02166992456534245353.png" |
| domains    | array of strings | List of domains associated with the brand                  | ["withconfetti.com", "confetti-store.com"]                                     |

**Note**: In the CSV format, each brand-domain combination is represented as a separate row with a single domain. In the JSONL format, domains are stored as an array property within each brand record.

## Offers Dataset

The offers dataset contains promotional offers linked to brands.

| Field Name   | Data Type      | Description                                       | Example                                       |
| ------------ | -------------- | ------------------------------------------------- | --------------------------------------------- |
| id           | string (UUID)  | Unique identifier for the offer                   | "a1b2c3d4-e5f6-4a3b-8c9d-1a2b3c4d5e6f"        |
| brand_id     | string (UUID)  | Foreign key reference to the brand                | "1db1f766-18be-4a52-9354-166667df5c72"        |
| brand_name   | string         | Name of the brand associated with this offer      | "Created Brilliance Diamonds"                 |
| summary      | string or null | Detailed description of the offer                 | "Get 20% off all summer items through August" |
| redeem_url   | string         | URL link to redeem or activate the deal           | "https://example.com/offer/123"               |
| sample_q     | string         | Ready-made prompt/response pairs for LLM training | "Discount codes from Walgreens in the US"     |
| country_code | string         | ISO country code where the offer is valid         | "US", "GB", "DE"                              |

## Relationships

- Each brand can have zero to many offers (`brand_id` in the Offers dataset references `brand_id` in the Brands dataset).

## File Formats

- Data is stored in JSONL format (one JSON object per line)
- Schema definitions follow JSON Schema specification (draft-07)

## Usage for RAG Systems

When using this data with RAG systems, consider:

1. Brands can be retrieved by their unique UUID or searched by name
2. Offers should be linked to their corresponding brands using the brand_id relationship
3. Logo URLs may be NULL and should be handled accordingly
