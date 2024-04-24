# Data Preprocessing Pipeline for Amazon Product Metadata

## Objective:
The objective of this data preprocessing pipeline is to clean and transform Amazon product metadata stored in JSON format, making it suitable for further analysis or machine learning tasks.

## Pipeline Overview:
1. **Sampling JSON Data:**
   - The script begins by sampling a portion of the original JSON data based on a specified filter key and target size in gigabytes.
   - Sampling is implemented to handle large datasets efficiently and reduce memory usage.

2. **Reading Sampled JSON Data:**
   - After sampling, the script reads the sampled JSON data in chunks to avoid memory issues.
   - Each chunk is processed and loaded into memory gradually, ensuring scalability for large datasets.
   - The data is stored in a Python list for further processing.

3. **Data Cleaning:**
   - The data cleaning process involves several steps to prepare the text data for analysis:
     - Removal of HTML tags using regular expressions.
     - Elimination of punctuation and numbers.
     - Conversion of text to lowercase for consistency.
   - Cleaning is performed on text fields such as 'category', 'title', and 'feature'.

4. **DataFrame Transformation:**
   - Once the data is cleaned, it is transformed into a pandas DataFrame for structured analysis.
   - Unnecessary columns are removed to reduce dimensionality and improve processing efficiency.
   - New columns are created to store cleaned versions of 'category', 'title', and 'feature'.

5. **Saving the Processed Data:**
   - The final step involves saving the processed DataFrame to a JSON file.
   - The saved file contains the cleaned and transformed data in a structured format, ready for downstream tasks such as analysis or modeling.

## Results:
- The preprocessing pipeline successfully cleans and transforms the Amazon product metadata.
- The processed data is saved to a JSON file named 'f_processed_data.json' for further use.

## Conclusion:
- The data preprocessing pipeline provides a scalable and efficient solution for handling large volumes of JSON data.
- By sampling, reading in chunks, and cleaning the data systematically, the pipeline ensures data integrity and prepares it for subsequent analysis or modeling tasks.

