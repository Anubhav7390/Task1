# Task1
## Data Cleaning and Preprocessing in Excel and Pandas

### : Data Cleaning and Preprocessing Summary in Excel

- Imported Raw Data:

    Loaded a CSV file where values were tab-separated and initially merged into one column.

    Used Excel’s Text to Columns with a tab delimiter to separate values into structured columns.

- Cleaned & Transformed Columns:

    ID: Retained as unique identifier.

    Year_Birth: Used to calculate a new Age column.

    Income: Checked for missing/outlier values (removed them) and created income segments (Low, Mid, High, etc.).

    Education & Marital_Status: Standardized text formats and grouped similar categories.

    Kidhome + Teenhome: Combined into a new Total_Children column.

    Dt_Customer: Converted to date format and used to calculate Customer_Tenure.

    Spending Columns: Aggregated product-wise spendings into a Total_Spending column.

    Campaign Response Columns: Summed up to form a Total_Campaigns_Accepted metric.

    Removed or ignored technical columns like Z_CostContact, Z_Revenue (if constant).

- Final Output:

   A clean, well-structured dataset with new calculated fields ready for analysis.

 ### : Data Cleaning & Preprocessing Summary in Pandas

- Loaded Data:

   Imported the tab-separated CSV using pandas.

- Cleaned Columns:

   Checked the inconsisties , statistics , shape etc. using: info(), describe(), shape, isnull(), duplicated() etc.

   Removed missing Income values as there was 24 out of 2260.

- Feature Engineering:

   Created Age from Year_Birth.

   Combined Kidhome and Teenhome into Total_Children.

   Converted Dt_Customer to datetime and calculated Customer_Tenure_Days. using; pd.to_datetime (I was getting NaT values but searched it and troubleshotted this situation.)

   Calculated Total_Spending by summing product spending columns.

- Categorization:

   Binned Income into categories (Low, Mid-Low, Mid-High, High) via a custom function.

 
