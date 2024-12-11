# Cosmocloud - Backend Intern Task 2 Submission

This repository contains aggregation pipelines for queries on the **`sample_mflix`** dataset from MongoDB Atlas. Each question’s solution adheres to the required schema and is saved in JSON files (`1.json` to `5.json`).

---

## Dataset Ambiguities and Justifications

While implementing the pipelines, I encountered the following issues in the dataset:

1. **Duplicate Titles with Different `_id`**  
   Some movies share the same title but have distinct `_id` values, leading to potential ambiguity in grouping by title (e.g., Questions 2 and 3).  
   **Justification**: I followed the requirement to group by `title` while acknowledging the impact of this duplication.

2. **Mismatch Between `released` and `year` Fields**  
   The `released` (date) and `year` (integer) fields occasionally conflict.  
   **Justification**: I used the `released` field for date-based filtering (e.g., Question 5) due to its precision.

These decisions prioritize schema compliance for automated testing, but the dataset's inconsistencies might affect result accuracy.

