# Healthcare Readmission Data Analysis  

### By Group 1: Taliah, Aysha, and Joe  

---

## **Example Python Code**  
Here is an example of how to load the dataset and perform basic analysis:  

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
data = pd.read_csv('hospital_readmission_data.csv')

# Preview the data
print(data.head())

# Group data by region and calculate average readmission rates
region_avg = data.groupby('Region')['Predicted Readmission Rate'].mean()

# Plot the average readmission rates by region
region_avg.plot(kind='bar', title='Average Readmission Rates by Region')
plt.ylabel('Readmission Rate')
plt.xlabel('Region')
plt.show()
