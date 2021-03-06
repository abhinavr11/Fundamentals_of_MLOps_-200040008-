
 ## Link
>https://github.com/abhinavr11/MLOps_Assignment
>> the src folder contains the exp.py file for both branches while the metrics and all other csv files are in s3 bucket


## Steps and Commans involved in PART !
* First we create the bucket and github repo as given in the assignment
* ->
`$ mkdir mlops_dvc`
 
`$ cd mlops_dvc`

`$ git init`

`$ git remote add origin <github-repo-link>`

`$ git branch -M main`

`$ dvc init `

`$ dvc add data/creditcard.csv`

`$ git add data/data.csv.dvc data/.gitignore `

`$ git commit -m "Add raw data" ` 

`$ dvc remote add -d storage s3://mlopsdvc200040008/datastore`

`$ git add .dvc/config`

`$ git commit -m "Configure remote storage"`

`$ dvc push`

`$ git push origin main`


## Accuracy
### exp1_dt
>"Accuracy": 0.9992802219023208, "f1 Score": 0.9992663256896973

### expt2_rf
>"Accuracy": 0.9996664442961974, "f1 Score": 0.9996520057812976


### Two Folders one for each experiment
-> datastore for experiment one 
-> dvcstore for experiment two

![](images/both.png)
<br>

### Decesion Tree (exp1_dt)
-> Contains [ creditcard.csv , model.pkl , test.csv , train.csv , acc_f1.json ]
![](images/exp1_dt.png)
<br>
<br>
### Random Forest (expt2_rf)
-> Contains [ creditcard.csv , model.pkl , test.csv , train.csv , acc_f1.json ]
![](images/expt2_rf.png)
