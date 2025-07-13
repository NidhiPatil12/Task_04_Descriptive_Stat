# Task_04_Descriptive_Stat
This project performs descriptive statistical analysis on three political datasets using Pure Python, Pandas, and Polars. It explores count, mean, standard deviation, and value frequency, along with grouped insights. The goal is to compare performance, flexibility, and usability across these tools.

Datasets:
1.	Facebook Ads: 2024_fb_ads_president_scored_anon.csv
2.	Facebook Posts: 2024_fb_posts_president_scored_anon.csv
3.	Twitter Posts: 2024_tw_posts_president_scored_anon.csv

Input File (Pure Python)
1.	Pure_python_stats_fb_ads_president.ipynb
2.	Pure_python_stats_fb_ads_president.ipynb
3.	Pure_python_stats_fb_ads_president.ipynb

Input File (Pandas)
1.	Pandas_stats_fb_ads_president.ipynb
2.	Pandas_stats_fb_posts_president.ipynb
3.	Pandas_stats_tw_posts_president.ipynb

Input File (Polars)
1.	Polars_2024_fb_ads_president_scored.ipynb
2.	Polars_2024_fb_ads_president_scored.ipynb
3.	Polars_2024_fb_ads_president_scored.ipynb

Output Files (Pure Python)
Output_Python_fb_ads_stats.txt
Output_Python_fb_posts_stats.txt
Output_Python_tw_posts_entire_dataset.txt
Output_Pandas_fb_ads_stats.txt
Output_Pandas_fb_posts.txt
Output_Pandas_tw_posts.txt
Output_Polar_tw_posts.txt
Output_Polars_fb_ads_stats.txt
Output_Python_fb_posts_stats.txt



Summary of Approaches

In this project, we explored three distinct methods for performing descriptive statistics on structured datasets: Pure Python, Pandas, and Polars.

Pure Python Approach:
The Pure Python method relied solely on the standard library modules such as csv, math, and collections. This approach involved manually loading the CSV data, identifying numeric columns, calculating descriptive statistics like mean, min, max, standard deviation, and determining frequency counts for categorical fields. It provided maximum control and transparency over the process, which is beneficial for learning or when fine-tuned logic is required. However, this method was the most labor-intensive and verbose. It required writing custom code for even basic operations and was less efficient when handling large datasets. This approach also lacked built-in data type inference and concise syntax, making it more error-prone and harder to scale or maintain.

Pandas Approach:
The Pandas approach was significantly more user-friendly and efficient. Using pandas.read_csv(), we were able to load the dataset in a single line, and descriptive statistics were quickly derived using built-in functions like describe(), value_counts(), and nunique(). Grouped operations by columns like page_id or Facebook_Id were also simple to implement using groupby(). Pandas abstracts away many low-level operations and offers a vast array of utilities that are optimized for typical data analysis workflows. It strikes a good balance between readability, functionality, and performance, making it a popular choice among data analysts and data scientists. For most medium-scale datasets and day-to-day analysis, Pandas is the ideal tool.

Polars Approach:
Polars is a newer DataFrame library designed for speed and efficiency, leveraging Rust under the hood. In our analysis, it handled large datasets very smoothly and performed computations faster than Pandas in several scenarios. The syntax is slightly different but logically similar, and operations like grouping, filtering, and aggregation are available through a functional API. It required explicit casting of numeric fields, which made the processing more predictable. For grouped statistics, Polars performed just as well as Pandas, if not better, especially in terms of execution time. While the learning curve is slightly steeper for those new to it, Polars is an excellent option for large-scale or performance-sensitive data analysis tasks.




What I Learned:
Working with all three methods—Pure Python, Pandas, and Polars—taught me how each tool approaches data analysis differently. While they all provided the essential descriptive statistics like count, mean, min, max, and unique values, the ease of use and output readability varied. Pure Python made me think critically about each step in the analysis, which was great for building foundational understanding. Pandas offered the most intuitive and readable syntax for grouping and summarizing data. Polars, on the other hand, provided lightning-fast performance and handled larger files efficiently, but required careful handling of data types and slightly different syntax.

One interesting issue I encountered was with standard deviation. Pure Python calculates population standard deviation by default, while both Pandas and Polars compute the sample standard deviation. This led to mismatched values until I adjusted the calculation method in my Python script to align with the sample-based results from the libraries. It was a good reminder that even basic statistics can differ slightly depending on the tool used.

Polars surprised me with both its performance and strict typing. Initially, some columns that were supposed to be numeric were read as strings, which caused null outputs for certain statistics. I had to explicitly cast these columns to numeric types to fix the problem. Also, getting value counts (like top 3 most frequent values) in Polars required a different syntax than Pandas. Overall, I found Polars ideal for fast, large-scale data tasks, Pandas best for exploratory data analysis and everyday use, and Pure Python most helpful for reinforcing logic and understanding what libraries automate for us.

