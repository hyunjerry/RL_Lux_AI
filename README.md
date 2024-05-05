## Run.ipynb File can be used to train the models and create submission file. 
### Train a models for Ensemble method
```
# Model parameters could be changed from line 334
# update ./UNet_attention_jason_0-3_ensemble/train.py
# For each epoch, model is saved if current epoch shows higher accuracy than previous epoch.
# Early stopping is applied so if model does not see improvement for 3 epochs, the training will stop.

!python UNet_attention_jason_0-3_ensemble/train.py
```

### Create Ensemble submission file
```
# Submission file will be created at ./UNet_attention_jason_0-3

%cd f'./UNet_attention_jason_0-3''
!tar -czf submission.tar.gz *
```

### Modify Ensemble Model
- If you have new model files (.pth) that you would like to include, modify ./UNet_attention_jason_0-3_ensemble/agent.py
- Note that Kaggle submission file has to be less than 100Mb


### Train/Modify Transformer method
```
# Open the file transformer/Transformer_LuxAI.ipynb
# Follow the instructions inside. You can tune your hyperparameter inside this notebook.
# This notebook will save model.pth from each epoch. Simply observe the accuracy after each epoch from choosing the model you want. 
```

Files greater than 100mb has been removed in accordance to github policy. 
Removed files:
- ./UNet_attention_jason_0-3_ensemble/submission.tar
- ./transformer/checkpoint.pth
