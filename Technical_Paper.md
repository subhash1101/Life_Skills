

# Full Text Search Investigation Report

## Project Background

I recently joined a new project that is facing performance and scaling problems. The current search system is slow and puts heavy load on the database. As more users and data are added, the system response time is getting worse.
After reviewing the situation, the team lead asked me to investigate whether using a dedicated Full Text Search database can improve performance and scalability.

---

## What is Full Text Search

Full Text Search is a technology used to search large amounts of text data quickly.
It allows:

* Keyword searching
* Phrase searching
* Filtering results
* Ranking results based on relevance

Unlike traditional SQL queries, Full Text Search engines are specially designed for handling complex text searches efficiently.

---

## Current System Problems

The existing system uses SQL `LIKE` queries and basic indexing. This causes several issues:

* Slow response time when searching large datasets
* Poor ranking of search results
* Increased database load
* Difficulty scaling with growing data
* Limited search features such as fuzzy search or advanced filtering

Because of these limitations, a new solution is required.

---

## Investigation Approach

To improve search performance, I researched three popular Full Text Search technologies:

* Elasticsearch
* Apache Solr
* Apache Lucene

The comparison was done based on:

* Performance
* Scalability
* Ease of integration
* Flexibility
* Maintenance effort

---

## Technologies Evaluated

### 1. Elasticsearch

* Distributed search and analytics engine
* Supports horizontal scaling across servers
* Near real time indexing and search results
* Easy integration using REST APIs
* Built in aggregation and analytics features
* Strong community support

**Best suited for:** Large applications requiring fast and scalable search.

---

### 2. Apache Solr

* Enterprise level search platform built on Lucene
* Advanced caching for faster responses
* Supports faceted search and filtering
* Highly configurable schema
* Good for complex enterprise requirements

**Best suited for:** Large enterprise systems with complex search customization needs.

---

### 3. Apache Lucene

* High performance Java search library
* Provides low level control over indexing and searching
* Lightweight and embeddable
* Requires more development effort to build a complete system

**Best suited for:** Custom applications where developers need full control over search functionality.

---


## Benefits of Using Full Text Search Engine

* Faster search results
* Reduced load on main database
* Better search relevance ranking
* Improved scalability for future growth
* Advanced features like fuzzy search and autocomplete

---

## Final Recommendation

Based on the investigation:

* **Elasticsearch** is the best option for the current project because it is easy to integrate, scalable, and performs well with large real time datasets.
* **Solr** is suitable for highly customized enterprise search systems.
* **Lucene** is best when building a completely custom search solution from scratch.

Implementing Elasticsearch will improve performance, reduce database load, and provide better search experience for users.

---

## References

* [https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
* [https://solr.apache.org/guide/solr/latest/](https://solr.apache.org/guide/solr/latest/)
* [https://lucene.apache.org/core/](https://lucene.apache.org/core/)
* [https://opensearch.org/docs/latest/search-plugins/](https://opensearch.org/docs/latest/search-plugins/)
* [https://www.geeksforgeeks.org/full-text-search/](https://www.geeksforgeeks.org/full-text-search/)

---