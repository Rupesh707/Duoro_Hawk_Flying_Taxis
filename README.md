# Duoro_Hawk_Flying_Taxis

[![image](https://www.linkpicture.com/q/BMW-1.jpg)](https://www.linkpicture.com/view.phpimg=LPic63bf680209b2c372151899)


#### 1. CODE STRUCTURE Code
The code is structured into distinct files & folders:

#### Submission - [Click](https://github.com/Rupesh707/Duoro_Hawk_Flying_Taxis/tree/Master/submission_data%2Bparameters)

#### Duoro_Hawk_Pipeline - [Click](https://github.com/Rupesh707/Duoro_Hawk_Flying_Taxis)
- Images - Output of images from the pipeline
- Esn_class.py - Has general purpose methods which do not rely on a given task
- Esn_loaddata.py - Dataloader
- Esn_mackleyglass.py - Mackey-Glass (τ=17) time series for benchmarking
- EsnModelSelection.py - Optimizer for model building neural nets
- esnTrainAndTestUtils.py - Helper for train & test
- utils.py - Helper functions


### 2. FINAL RESULTS

- The best parameters found by the grid search are:
Nr = 250 sigma =0.4 lambda =0.01 Leak rate = 1 Connectivity = 30%

The top model gives a
- validation error of km 1.016 (MHD), and a
- train error of km 0.801 (MHD).

It is trained with the first 2,500 trips and tested over the 5,000 following ones.We can also see how the network predicts the destination as the taxi ride goes on, the green points are the predicted destination as we go through the real trajectory (red points). The X stands for the predicted final destination of which we evaluate the MHD.