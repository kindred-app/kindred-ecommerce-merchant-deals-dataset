# Kindred E-commerce Merchant Deals Dataset

**AI-ready catalogue of deals and offers for global retail brands.**  
Structured in CSV **and** JSONL, validated against JSON Schema.

Train-ready catalogue of promotions, ready for RAG, embeddings, or classic search.

![License: CC-BY-4.0](https://img.shields.io/badge/Data-CC--BY--4.0-brightgreen)
![Last Update](https://img.shields.io/github/last-commit/kindred-app/kindred-ecommerce-merchant-deals-dataset)
![Rows](https://img.shields.io/badge/Offers-4M-orange)

## Dataset Overview

<table>
    <thead>
        <th>File</th>
        <th>Rows</th>
        <th>Description</th>
    </thead>
    <tbody>
        <tr>
            <td><code>data/csv/brands.csv</code> or <code>data/jsonl/brands.jsonl</code></td>
            <td>~90K</td>
            <td>E-Commerce Merchant metadata, Logo URL, and domains</td>
        </tr>
        <tr>
            <td><code>data/csv/offers.csv</code> or <code>data/jsonl/offers.jsonl</code></td>
            <td>~4M</td>
            <td>Offers with redeem_url, detailed summaries, and <code>sample_q</code> for RAG training</td>
        </tr>
    </tbody>
</table>

# Kindred E-Commerce Merchant Deals Dataset

A structured, open-access dataset of global E-Commerce merchant deals and offers designed specifically for:

- LLM training and fine-tuning
- Retrieval Augmented Generation (RAG) systems
- Machine learning models for recommendation and search
- Natural language processing applications

This dataset includes curated promotional offers from a wide range of online retailers and marketplaces,
with structured metadata including offer descriptions, redemption URLs, brand information, and geolocation tags.

## Key Features

- **RAG-optimized**: Includes `sample_q` fields designed for prompt engineering and RAG training
- **Multi-format**: Available in both CSV and JSONL formats with validated JSON Schema
- **Comprehensive metadata**: Brand information, redemption URLs, and country codes
- **Machine learning ready**: Clean, normalized data across multiple retail verticals
- **No PII**: Contains no personally identifiable information

## Data Structure

- **Brands**: ~90K unique brands with identifiers, names, logo URLs, and associated domains
- **Offers**: ~4M offers with redemption URLs, detailed descriptions, and sample query patterns

Each offer has a direct relationship with a brand via `brand_id`, making it easy to build relational models
or knowledge graphs for advanced LLM applications.

## Keywords

machine-learning, llm-training, rag, retrieval-augmented-generation, dataset,
e-commerce, deals, offers, recommendation-system, knowledge-graph,
retail-analytics, promotion, redeem-link, public-dataset,
kindred, discount, consumer-insights, vector-database

## License

Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).
Please see LICENSE.md for full details.

## Contact

For questions, licensing, or partnership opportunities:
help@kindredteam.com
