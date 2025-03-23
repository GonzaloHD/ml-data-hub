
# 🐼 Pandas Basics – Quick Notes

## 🔹 Importing Pandas
```
import pandas as pd
```

## 🔹 Creating DataFrames
```
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35]
}
df = pd.DataFrame(data)
```

## 🔹 Reading & Writing Data
```
pd.read_csv('file.csv')                  # Read CSV
pd.read_excel('file.xlsx')               # Read Excel
df.to_csv('output.csv', index=False)     # Write CSV
df.to_excel('output.xlsx', index=False)  # Write Excel
```

## 🔹 DataFrame Basics
```
df.head()                                # First 5 rows
df.tail()                                # Last 5 rows
df.shape                                 # (rows, columns)
df.columns                               # Column names
df.info()                                # Summary
df.describe()                            # Stats summary
```

## 🔹 Selecting Data
```
df['Age']                                # Single column
df[['Name', 'Age']]                      # Multiple columns
df.loc[0]                                # Row by label
df.iloc[0]                               # Row by index
df.loc[0, 'Name']                        # Specific cell
```

## 🔹 Filtering Rows
```
df[df['Age'] > 30]                       # Age > 30
df[(df['Age'] > 25) & (df['Age'] < 35)] # Multiple conditions
```

## 🔹 Modifying Data
```
df['Age'] = df['Age'] + 1                # Update column
df['NewCol'] = df['Age'] * 2             # New column
df.rename(columns={'Age': 'Years'})      # Rename column
df.drop(columns=['NewCol'], inplace=True)# Drop column
```

## 🔹 Handling Missing Data
```
df.isnull()                              # Check missing
df.dropna()                              # Drop rows with NA
df.fillna(0)                             # Replace NA with 0
```

## 🔹 Grouping & Aggregating
```
df.groupby('Name').mean()                # Group by name, get mean
df.groupby('Name')['Age'].sum()          # Group + single col
```

## 🔹 Sorting & Ranking
```
df.sort_values(by='Age')                 # Sort by Age
df.sort_values(by='Age', ascending=False)
```

## 🔹 Merging & Joining
```
pd.concat([df1, df2])                    # Stack vertically
pd.merge(df1, df2, on='key')             # SQL-style join
```

## 🔹 Exporting Data
```
df.to_csv('filename.csv', index=False)
df.to_excel('filename.xlsx', index=False)
```
