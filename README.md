# EVA_S6
Assignment-6 which includes Batch-Norm and Regularization implementation.

This Assignment covers using of L1 and L2 Regularization with BatchNorm and GhostBatchNorm.
We will train the MNIST dataset with different techniques such as L1,L2,BN,GBN and will observe the effect on Training,Validation accuracy.
```
Steps-
```
```
*) Prepare the dataloader for the model and make a basic skeleton of your model with less than 10k parameters.
*) Define the GBN class and use it to generate another model skeleton with GBN not with BN.
*) Define the training/testing function with different cases of using L1,L2,BN,GBN.
*) training and ploting of Val_accuracy and Val_loss curves.
*) Find 25 misclassified images for 2 models(Without L1,L2 with BN and Without L1,L2 with GBN) and plot them.
```

```
                                                             Results-
```

```
                                                      Validation Accuracy Curve.
```

![Screenshot from 2022-06-09 11-32-04](https://user-images.githubusercontent.com/28132746/172825547-9a5d7ba2-8ab4-4eec-8dac-4c488afcd18a.png)

```
                                                      Validation Loss Curve.
```

![Screenshot from 2022-06-09 11-31-54](https://user-images.githubusercontent.com/28132746/172825786-a540c0fb-305e-4ce8-a094-68b1758bcccb.png)


```
Misclassified images for Model Without L1 and L2 and with BN.
Each Image has-
upper-left number -> prediction from model.
Lower-left number -> traget.
```

![Screenshot from 2022-06-09 11-31-17](https://user-images.githubusercontent.com/28132746/172825908-f95b69ca-610f-411f-91c1-9f3089352264.png)


```
Misclassified images for Model Without L1 and L2 and with GBN.
Each Image has-
upper-left number -> prediction from model.
Lower-left number -> traget.
```

![Screenshot from 2022-06-09 11-31-41](https://user-images.githubusercontent.com/28132746/172825953-51c6367c-d9f4-4cf6-8d2e-d24df5127227.png)

```
                                                      Observations-
```
```
Model Arch                        Val Accuracy(best %)                        Train Accuracy(best %)              Val Loss(best %)
Without L1 L2 with BN                   99.43                                       98.82                               0.0164
Without L1 L2 with GBN                  99.52                                       98.74                               0.0150    
with L1 with BN                         99.51                                       98.83                               0.0158
with L1 with GBN                        99.41                                       98.83                               0.0200
with L2 with BN                         99.45                                       98.82                               0.0189
with L2 with GBN                        99.43                                       98.76                               0.0184
with L1 and L2 with BN                  99.50                                       98.84                               0.0160
with L1 and L2 with GBN                 99.52                                       98.77                               0.0153
```
```
*) Without L1, L2 with GBN, gave good results and there seems consistency in the good accuracy as well.
*) Adding GBN with Larger Batch Size helps for model accuracy (But not always as larger batch size is not useful all the time)
*) Adding only L1, very slight chance of overfitting as well increase in accuracy.
*) Adding only L2, less chance of overfitting an daccuracy also slightly decrease.
*) Adding both L1 and L2 are used to get good accuracy and which is also consistent. As no hard rule to find correct L1, so it may tend to less accuracy
*) Model With L1, L2 with BN gave better results than Without L1,L2 with BN. That means adding correct L1 increased the accuracy but increase slight chance of model overfitting as compared to others but L2 helps to reduce the chance of model overfitting. But it is not straight forward as i did lots of iterations to find these values. Before that adding L1,L2 (specially L1) was giving less accuracy for the model.
*) L2 Regularization is default with Pytorch and can be implement with "weight_decay " parameter only.
```

```
Note-
```
It can be said that all it depends on type of datasets and model architecture which we are training on. My model architecture for MNIST with above combination gave these results.


