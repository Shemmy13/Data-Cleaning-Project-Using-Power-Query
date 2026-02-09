# Data-Cleaning-Project-Using-Power-Query
In the world of data analytics, the phrase "garbage in, garbage out" is a fundamental truth. No matter how sophisticated your visualisation tools are, they cannot compensate for poor data. I performed an end-to-end ETL (Extract, Transform, Load) process on a web-scraped dataset using Microsoft Power Query.The objective was to transform raw data into a clean, usable format for analysis. Here is a breakdown of my process, the challenges I faced, and the techniques I used to ensure data quality.
**1. Extraction: Getting the Data**
Every analysis begins with extraction. For this project, the data was obtained from a web page (Kaggle.com), which I downloaded onto my computer. Before touching a single row, I spent time studying the dataset. Before cleaning, I realized that it is essential to understand the data's context. Domain knowledge helps determine which data points are relevant, identify errors, and decide what should be added, removed, or modified.
**2. Transformation: The Cleaning Process**
Once the data was loaded into Power Query, I began the transformation phase. This was the most intensive part of the project, where I applied various techniques to standardize the dataset.
**Text Cleaning & Formatting**
-Standardization: I used the “Replace Values” function to clean up inconsistent naming conventions, such as replacing hyphens (-) between names with spaces and removing unwanted characters.
-Capitalization: To ensure professional consistency, I capitalized the first letter of text entries using the “Capitalize Each Word” feature.
-Correction: I identified values that appeared to be misspelt. I cross-referenced these with Google to ensure the correct spelling before fixing them in the dataset.
**Data Type & Structural Changes**
-Data Types: One of the most critical steps was defining the correct data types. I explicitly converted columns that needed to be converted to Whole Number, Decimal, Text, and Currency to prevent errors during analysis using the “Data Type” function.
-Splitting Columns: The dataset contained contract durations lumped into a single cell. I used “Split by Delimiter” to separate this into two distinct columns such as the Contract Start Date and Contract End Date.
-Merging Columns: Conversely, I used “Merge Columns” to combine related fields where a unified view was more useful for analysis.
-Removing Noise: After scrutiny, I deleted columns that provided no relevant information to streamline the dataset.
**Advanced Transformation**
-Conditional Logic: I used “Conditional Columns” to create new data points based on specific "If/Then" logic derived from the existing values.
-Statistical Operations: I utilized the Statistics and Standard tools in the Transform tab to perform necessary calculations directly within the query editor.
**3. Optimization & Quality Control**
Working with a large file presented performance challenges, which taught me valuable lessons in workflow management.
-Handling Performance Issues: At one point, the workspace began to freeze due to the file size. To manage this, I temporarily filtered columns to apply value replacements on smaller subsets of data, then removed the filters once the operation was completed.
-Data Safety: To prevent data loss during these freezes, I adopted a habit of frequently using Close & Load to save my progress.
-Final Validation: My final step was enabling “Column Quality”. I reviewed the validity bars to ensure every column was 100% valid (0% Error, 0% Empty) before concluding the project.
**Conclusion**
This project reinforced that data cleaning is not just about fixing typos; it is about structuring information so it can tell a story and can be made easy to carry out analysis. By mastering these Power Query functions, I have built a solid foundation for future data analysis projects.
