Commands I will use every session 
cd "C:\Users\admin\Documents\Projects\analytics-portfolio\fifa"
.venv\Scripts\activate
jupyter lab

what each line does 
- uv:installs python and manages packages
- venv: isolated box per project
- pip install via uv: puts packages in the active box/enviorment
- import pandas as pd: load pandas, nicknames it pd
- import matplotlib.pyplot as plt: laods the charting interface of pandas
why (fifa) in the prompt matters:
it basically tewll you that this venv is for which project If (fifa) is NOT showing, any package I install goes to the wrong place and my imports will fail.

Git -- git add, git commit, git push
git add stages all the changes we have made
gitcommit those changes that measns saves the changes 
git push pushes these changes to the remote version of the same folder in git hub
we need to type u- if something doesn't exists in the remote folder so you have to tell using u that craeate this branch and link it to same branch in the local 

Data frame V/s Series
Data frame is a data stored in the table form like in sql tables but this called in memory of the session and is in a form of coulms and rowns

data series it's just one column pulled out of a DataFrame, has the same row index as the original table.

Boolean filtering : is basiaclly inititally taking the brackets and creating a yes or no in the internal series for a columne then using those positions of those places outer bracket gives the entire dataframe where that series is yes 

can select specific columns by passing a list of column names inside double brackets on a DataFrame
can filter rows using a boolean mask -- pandas evaluates a condition on a column and returns True/False for each row, then the outer brackets return only the rows where the condition is True. I can chain column selection after filtering using double brackets at the end
can add a new column to a DataFrame by assigning a calculation to a new column name -- e.g. df['new_col'] = df['col1'] - df['col2']
can group by any column and perform aggregations -- single aggregation returns a Series, multiple aggregations using .agg() returns a DataFrame with named columns. Chain .sort_values() at the end to order the result