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