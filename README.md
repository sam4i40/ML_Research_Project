# Base research paper : 
Are You an Introvert or Extrovert? Accurate Classification With Only Ten Predicors. - Chaechan So.

# Method : 
1. Get the full dataset
2. Take only the selected 10/91 questions.
3. Take total extroversion score ES of all records.
4. If ES >= X -> label 1(Extrovert), else if ES < X -> label 0(Introvert)
5. Rerun the models

# Data preprocessing : 
## Data on 91 questions :

### Their data :
1. Take only A (Q1A, Q2A...)
2. Take out all the rows such that IE = 3
3. Save as original_91.csv
  
### Our data :
1. If sum >= 273 IE = 2
    else IE = 1
2. Save as our_91.csv
  
## Data on 10 questions :

### Their data :
1. Create the list of 10 questions.
2. Keep only those 10 columns
3. save as original_10.csv

### Our data : 
1. if sum >= 30 IE = 2
    else IE = 1
2. save as our_10.csv
