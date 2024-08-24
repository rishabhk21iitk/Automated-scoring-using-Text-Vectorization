# Import pandas for dataframe 
import pandas as pd 

# Import train_rel_2.tsv into Python
with open('C:\\Users\\Rishabh Kumar\\Desktop\\train_rel_2.tsv', 'r') as f:
    lines = f.readlines()
    columns = lines[0].split('\t')
    response = []
    score = []
    for line in lines[1:]:
        temp = line.split('\t') 
        if temp[1] == '3':   # Select the Essay Set 3
            response.append(temp[-1])  # Select EssayText as response
            score.append(int(temp[2])) # Select score1 for human scoring only
        else: 
            None
