# Automotive Data Analysis with Pandas

## Technical Implementation

### Data Pipeline Architecture

graph TD
    A[Raw Data] --> B[Data Cleaning]
    B --> C[Feature Engineering]
    C --> D[Analysis]
    D --> E[Visualization]

## Core Operations

| Component           | Techniques Applied                  | Tools Used          |
|---------------------|-------------------------------------|---------------------|
| **Data Cleaning**   | Missing value imputation, Deduplication | Pandas, NumPy      |
| **Feature Engineering** | Temporal extraction, Text splitting | Regex, Datetime    |
| **Optimization**    | Vectorization, Dtype downcasting    | Pandas, Categorical|

### Performance Gains
# Before optimization
df.iterrows() - 2.93 ms ± 30.9 μs 

# After optimization
df.apply() - 31.1 μs ± 131 ns	


## How to Use
1. Clone repository
2. Install requirements: pip install -r requirements.txt
3. Run Jupyter notebooks in order (ex00-ex04)