# Duoro_Hawk_Flying_Taxis

[![image](https://www.linkpicture.com/q/BMW-1.jpg)](https://github.com/Rupesh707/Duoro_Hawk_Flying_Taxis/blob/Master/Duro_Hawk.ipynb)


#### 1. REPOSITORY STRUCTURE 
The code is structured into distinct files & folders:

#### Submission - [Click](https://github.com/Rupesh707/Duoro_Hawk_Flying_Taxis/tree/Master/submission_data%2Bparameters)

#### Full_Study - [Click](https://github.com/Rupesh707/Duoro_Hawk_Flying_Taxis/blob/Master/Duro_Hawk.ipynb)

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

The top model after training :
- Validation error of km 1.016 (MHD).
- Train error of km 0.801 (MHD).

The model is trained with the first 2,500 trips and tested over 5,000 following ones.We can also see how the network predicts the destination as the taxi ride goes on, the green points are the predicted destination as we go through the real trajectory (red points). The X stands for the predicted final destination of which we evaluate the Mean Haversine Distance(MHD).

[![](https://www.linkpicture.com/q/Traj.png)](https://www.linkpicture.com/view.php?img=LPic63bf73f456cde368928031)

# Echo State Network (ESN)


[![Echo State Network](https://www.linkpicture.com/q/ESN-Model.png)](https://www.linkpicture.com/view.php?img=LPic63bf7067ea4791208584718)

## AWS Fly Connect - A predictive fleet management services


[![AWS Fly](https://www.linkpicture.com/q/BMW-2.jpg)](https://www.linkpicture.com/view.php?img=LPic63bf853809b721181603192)

The data would flow from the fleet vehicles to Amazon S3, then to Amazon Kinesis, where it would be processed by Lambda and stored in DynamoDB, also it would be indexed and visualized using Amazon Elasticsearch Service. If certain conditions are met, SNS will send notifications accordingly.

- The fleet vehicles would be equipped with GPS and sensor devices that would collect data such as location, speed, and sensor readings.
- The data would be sent to Amazon S3, where it would be stored.
- The data would then be streamed in real-time to Amazon Kinesis.
- Amazon Lambda functions would be triggered by the data stream, and they would perform tasks such as calculating vehicle speeds and distances traveled.
- The processed data would be stored in Amazon DynamoDB.
- The data would also be indexed and visualized using Amazon Elasticsearch Service, and can be queried by the system users.
- If certain conditions are met, Amazon SNS would send notifications, such as an email or SMS message, to the appropriate parties.

It's worth mentioning that this is a high-level illustration, specific details and the design of the dataflow could be adjusted based on the specific requirements of the system.



[![AWS Fly Connect](https://www.linkpicture.com/q/AWSFly-Connect.jpg)](https://www.linkpicture.com/view.php?img=LPic63bf78005901c158239597)
