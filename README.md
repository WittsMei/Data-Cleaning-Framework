# Data-Cleaning-Framework

## Data Analyics Lifecycle

One key principle to keep in mind is that for any new analytic skill you're learning, it's always important to really understand the business context in which it's being applied. 

<img width="843" alt="Screenshot 2024-10-05 at 12 51 36" src="https://github.com/user-attachments/assets/fe9aafe6-fcfa-44d6-b50a-b47bef2b461b">


## Step 1: Conceptualize the dataset

- **Identify grain, measure, and dimensions**

<img width="774" alt="Screenshot 2024-10-05 at 13 12 18" src="https://github.com/user-attachments/assets/21df1f41-91fc-422f-bff7-601fe60a6989">


- **Identify critical vs. non-critical**

<img width="778" alt="Screenshot 2024-10-05 at 13 17 46" src="https://github.com/user-attachments/assets/4afca7f0-7305-4d2f-9081-5bcecdcf68ed">


- **Understand column definitions**
<img width="768" alt="Screenshot 2024-10-05 at 13 16 57" src="https://github.com/user-attachments/assets/dda8ac32-84a7-498b-994a-44427a426489">




It is recommended that you spend 30 mins to an hour understanding the dataset. By the end of the step, you should be able to say something like:

This dataset represents sales data, where every single record represents a transaction. The most important columns are the sales columns and the data columns. And there's also supplementary information about the product, customer demographics and marketing information. The data spans from 2019 to 2024.



## Step 2: Locate solvable issues

- **Formatting**: currency, date, and number formats

- **Consistency**: spelling, spacing differences, categorization consistency

- **Duplicates**: erroneously repeated


How to find those isseus?

<img width="777" alt="Screenshot 2024-10-05 at 13 49 16" src="https://github.com/user-attachments/assets/94e85a39-755c-41c2-a2b1-510fbb15aa5b">



When it is acturally good enough?

The most important thing is not to find every signle issue and end up with a perfect dataset. You just need to prioritize the columns that you identify as critical columns at first to make them useable, and then move forward with the analysis and start diving into the insights. Make sure you always have a raw version dataset so that you can always circle back to this process and clean the data even more if you need to.



## Step 3: Evaluate unsolvable challenges

Two types of data: missing data, nonsensical data (eg: sale date after refund date, non-existent country code)

#### Calculate the magnitude (% impacted) of the issue


<img width="646" alt="Screenshot 2024-10-05 at 14 24 57" src="https://github.com/user-attachments/assets/b9bf9ac2-55b5-407b-8f44-5aec50b8b08a">


The dataset is not usable. You need to find another source.



<img width="758" alt="Screenshot 2024-10-05 at 14 25 37" src="https://github.com/user-attachments/assets/69cc8944-fdb8-4fa6-a760-fea7d87fda97">


You can leave as it is and then caveat it later in your analysis. 



<img width="741" alt="Screenshot 2024-10-05 at 14 27 32" src="https://github.com/user-attachments/assets/1650531a-bb96-4ca4-b4cc-d624fe1d8ec9">



You need to exercise a little bit of judgement in combination with your own domain knowledge and your understanding of what's feasible for this analysis. 

<img width="700" alt="Screenshot 2024-10-05 at 14 32 13" src="https://github.com/user-attachments/assets/581b278e-2cf9-49f8-897a-49bf32e883ae">




At the end of the step, you should be able to say something like:

About 10% of delivery timestamps were missing, and also 5% of the currency information was missing. However, there are not critical to this analysis, so they were left as is. For the 3% of refund dates that showed up as being before the sales day, they were actually excluded from the analysis, so as to not bias the data. 




## Step 4: Augmentation

- Create additional columns through calculations

- Add supplementary information from another source

At the end of the step, you should be able to say something like:

I augmented the dataset by adding in the time to deliver, the time to ship, and the time to refund, as well as regional informatin so that we could better segment the sales and refunds and also understand the data at another geographic dimension.




## Step 5: Note and document

- **Create a changelog**: document the issues you found, the magnitude and the severity, as well as whether or not it was resolved.  

<img width="671" alt="Screenshot 2024-10-05 at 15 04 37" src="https://github.com/user-attachments/assets/544ac8df-a023-47a7-8d1d-f35ab4e55f78">

<img width="557" alt="Screenshot 2024-10-05 at 15 07 39" src="https://github.com/user-attachments/assets/559ea8c9-aa85-40e7-a77b-078bef080493">

<img width="377" alt="Screenshot 2024-10-05 at 15 08 11" src="https://github.com/user-attachments/assets/5509483d-40ac-421a-9544-65cdb170b56d">



## Cleaning framwork


<img width="773" alt="Screenshot 2024-10-05 at 15 09 27" src="https://github.com/user-attachments/assets/3f765e8a-c428-4203-84d4-15d4d40b053b">














