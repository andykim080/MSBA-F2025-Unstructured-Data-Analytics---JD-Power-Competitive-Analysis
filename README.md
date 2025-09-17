# Entry-Level Luxury Car Forum Analysis

Analyzing consumer sentiment and brand mentions from scraped forum posts

# Summary

This project involves collecting and analyzing unstructured text data from the Edmunds online forum on entry-level luxury sedans. The workflow begins with web scraping using Selenium and BeautifulSoup to extract thousands of discussion posts, including usernames, dates, and raw text content. The scraped data is stored in a CSV file for further analysis.

The dataset undergoes data preprocessing, including handling duplicates, removing HTML artifacts, and cleaning text through lowercasing, punctuation removal, and stopword filtering. Frequently occurring car model names are standardized to their corresponding brands (e.g., “3-series” → “BMW”) to allow consistent brand-level analysis.

Exploratory analysis is conducted with word frequency counts to identify the most frequently mentioned brands. Natural Language Processing (NLP) techniques such as tokenization and stopword removal are applied to refine results. To capture brand associations, lift ratio analysis is used to measure how often pairs of brands co-occur relative to their independent frequencies, highlighting competitive or complementary positioning.

Network analysis is also introduced: brands are represented as nodes, with edges weighted by lift ratios. Centrality measures (in-degree, PageRank) identify the most influential brands in discussions, offering insights into consumer aspirations and attention distribution.

# How to Use

Install required libraries:

selenium, webdriver_manager, pandas, numpy, matplotlib, networkx, nltk.

Configure the scraper by setting the target forum URL and number of posts to collect.

Run the notebook to:

Scrape forum posts and save them to edmunds_entry_level_luxury_posts.csv.

Clean and preprocess the raw text data.

Replace model references with brand names using the provided mapping.

Generate frequency counts and lift ratios.

Visualize brand associations with network graphs.

Analyze the outputs:

Word frequency tables for brand mentions.

Lift ratio tables for co-occurring brands.

Network plots showing central brands in consumer discussions.

# Evaluation

The project successfully demonstrates how unstructured forum data can be transformed into structured insights on brand positioning. Frequency analysis highlights BMW, Lexus, and Mercedes-Benz as consistently mentioned brands. Lift ratio results reveal which brands are disproportionately associated with aspirational language.

Network analysis identifies central brands through PageRank and in-degree, indicating which brands drive the bulk of consumer attention. For example, BMW emerges as a highly aspirational and influential brand, appearing in posts at a higher-than-expected rate compared to baseline mentions.

Overall, the project showcases a complete pipeline from data acquisition (web scraping) to NLP preprocessing, frequency/lift analysis, and network modeling, providing actionable insights into competitive dynamics in the luxury automotive market.
