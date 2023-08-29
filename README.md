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
1. Take only A(Q1A, Q2A...) and IE
2. If IE == 3 delete the row
3. Save as original_91.csv
  
### Our data :
1. If IE == 3 delete the row
2. for each record take the sum, if the index is present in ignore, ignore, else if it is in reverse, reverse, else take sum.
3. If sum >= 237 IE = 1
    else IE = 2
4. take only A (Q1A, Q2A..)
5. Save as our_91.csv
  
## Data on 10 questions :

### Their data :
1. Create the list of 10 questions.
2. Keep only those 10 columns
3. save as original_10.csv

### Our data : 
1. if sum >= 30 IE = 2
    else IE = 1
2. save as our_10.csv

# Evaluation:
maximum sum = 295
minimum sum = 187

original (91) : 
intro = 4404
extro = 2784
Precision:  0.9514134275618374
Recall:  0.9693969396939695
F1-score:  0.9603209986625055

our_91 (237) : 
values changed : 2539
intro = 3861
extro = 3327
Precision:  0.5623409669211196
Recall:  0.6779141104294478
F1-score:  0.6147426981919332

our_91 (210) : 
values changed : 1053
intro = 7037
extro = 151
Precision:  0.9782850779510023
Recall:  0.9994311717861206
F1-score:  0.9887450759707372

our_91 (200) : 
