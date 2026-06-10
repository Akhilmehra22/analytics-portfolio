# Cheat Sheet 01 -- Setup, Git, pandas Basics

---

## Daily Session Commands
cd "C:\Users\admin\Documents\Projects\analytics-portfolio\fifa"
.venv\Scripts\activate
jupyter lab

Shortcut: goto-fifa (activates environment and navigates in one command)

---

## Tools
- uv: installs Python and manages packages
- venv: isolated box per project -- each project has its own packages
- (fifa) in prompt: environment is active. If missing, imports will fail.

---

## Git -- Daily Workflow
git add .                          # stage all changes
git commit -m "message"            # save snapshot with description
git push                           # send to GitHub

First time pushing a new branch only:
git push --set-upstream origin main

---

## DataFrame vs Series
- DataFrame: a full table with rows and columns -- like a SQL table in memory
- Series: a single column pulled from a DataFrame, keeps the same row index

---

## Key pandas Patterns

# Select specific columns
df[['col1', 'col2']]

# Filter rows (boolean mask)
df[df['col'] > value]

# Filter rows AND select columns
df[df['col'] > value][['col1', 'col2']]

# Add new column
df['new_col'] = df['col1'] + df['col2']

# Single aggregation
df.groupby('col')['value'].sum()

# Multiple aggregations
df.groupby('col').agg(
    name1=('col1', 'sum'),
    name2=('col2', 'count')
).sort_values('name1', ascending=False)

# iloc vs loc
df.iloc[0]           # row at position 0 -- changes after sort
df.loc[0]            # row with label 0 -- never changes after sort
df.iloc[0:5, 0:6]    # rows 0-4, columns 0-5 by position

# Missing data
df.isnull().sum()    # check how many NaN per column
df.fillna(0)         # replace NaN with 0
df.dropna()          # remove rows with any NaN

---

## Chart Template
plt.figure(figsize=(10, 6))
plt.bar(x, y, color='steelblue')       # bar chart
plt.scatter(x, y, alpha=0.6, s=100)   # scatter plot
plt.plot(x, y, color='orange')        # line chart
plt.title('Title')
plt.xlabel('X Label')
plt.ylabel('Y Label')
plt.tight_layout()
plt.show()


all_events = [] then append inside loop
pd.concat(list, ignore_index=True)
df.reset_index()
