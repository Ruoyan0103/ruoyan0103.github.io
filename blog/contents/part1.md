---
layout: default
title: "Notes for Part I: Find the Correct ML Approach"
date: 2025-11-17
---

# Notes for Part I: Find the Correct ML Approach

## Start with the Product Goal

1. **Frame your product goal in an ML paradigm**  
   When building a product, start by considering the service you want to deliver to users.

2. **Evaluate the feasibility of the ML task**  
   Determine whether the problem is suitable for a machine learning approach.

3. **Narrow down ML approaches into categories**  
   - **Classification and Regression**  
   - **Knowledge Extraction**  
   - **Catalog Organization**  
   - **Generative Models**

---

## How to Evaluate a Successful Product

- **Business Performance**  
  Clear feature goals; e.g., for a recommendation system, measure how many people click it and whether the recommendations are actually useful.

- **Model Performance**  
  Evaluate using standard metrics in code; e.g., cross-entropy, accuracy.  
  Ensure the product goal is realistic so that the current method can achieve it.

> Note: Model metrics and product metrics should be incorporated together.

---

## Action Steps

1. **Start with simple rules as a baseline**  
   ML is not always necessary.
   - **From experts**: How do people currently solve this problem?  
   - **From exploratory data analysis**: How would you solve this task manually based on the dataset?

2. **Utilize open data**  
   - Use datasets with similar input and output types (domain does not have to match).  
   - If a model performs well on a similar dataset, it is likely to perform well on the target dataset.

3. **Utilize open code**  
   - Abstract the problem by its input and output types to find similar codebases.  
   - Reproduce results from these codebases to learn and iterate.  

**Conclusion:**  
- Find open code → reproduce results  
- Find similar datasets → apply models  
- Iterate based on model metrics
