📁 1. Importing Libraries
Essential Python libraries are imported:
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
warnings.filterwarnings("ignore")
pandas and numpy for data manipulation
matplotlib and seaborn for visualization
warnings to suppress warning messages

📂 2. Loading the Dataset
    ds = pd.read_csv("product_data.csv")
    The dataset is loaded using pandas.read_csv() and stored in a DataFrame named ds.

🧾 3. Viewing the Dataset
    print(ds.to_string())
    ds.info()
    to_string() shows the entire dataset.
    info() provides a summary: column names, data types, and null values.

📊 4. Data Cleaning Steps

🔁 a. Check for Duplicates
   ds.duplicated().sum()
   Identifies and counts duplicate rows.

❌ b. Remove Duplicates
    ds = ds.drop_duplicates()
    
🧼 c. Handle Missing Values
    ds.isnull().sum()
    Shows number of missing values per column.
    
    ds = ds.dropna()
    Drops rows with any missing values.

📌 d. Check for Duplicates Again
   ds.duplicated().sum()
   Rechecks to confirm duplicates are removed.

📈 e. Statistical Summary
   ds.describe()
   Returns descriptive statistics like mean, median, std deviation, etc.

