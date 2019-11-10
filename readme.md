# AWS-AIML-examples


***


## Prerequisites

You need an AWS account for these labs, and depending on the lab you also need a role with administrator access on the account to configure the necessary IAM roles. These labs should performed in non-Production accounts, ideally in sandbox environments.


***


## Step 1 - apply lab credits if you have any


***


1.1. Navigate to the account link at the top right of your window.

Select **Account**. 

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/navigate-account.png]]


***


1.2. Then navigate down to **Credits** and enter in the coupon.

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/apply-credits.png]]

***

## Step 2 - Set up your Sagemaker Jupyter Notebook instance


***


2.1. In the AWS console, navigate to Sagemaker. 


***

2.2. Make sure that your region in the top-right corner is "US East (N. Virginia)"


***


2.3. Then select, **Notebook** | **Notebook Instances**. 

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/notebook-instances-select.png]]

***

2.4. Click the **Create Notebook instance** button.

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/create-notebook-istance1.png]]


***

2.5. Fill in details around the notebook instance. Use defaults unless stated otherwise.

* **Notebook instance name:** aimlbootcamp
* **Notebook instance type:** any xlarge instance type

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/create-notebook-instance-2.png]]

***

2.6. **Select the creation of a new IAM role**. Give it access to all S3 buckets.

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/create-new-iam-role-when-creating-nb-instance.png]]

***

2.7. When you get to the Git section, choose the following.

Git repositories:
* Choose "Clone a public Git repository to this notebook only"
* Git repository URL: https://github.com/dupled3031/AWS-AIML-examples.git

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/create-notebook-instance-git-repo-config.png]]

***

2.8. Click **Create Notebook Instance**
  
The instance will take about five minutes to start up. In the mean time, proceed to the next step.

***

## Step 3 - Give the Sagemaker instance IAM permissions to invoke with other AWS services

***

3.1. For the notebook instance you just created in the previous step, click on the hyperlink with the name of the instance to open up the instance detail panel. Even if the notebook instance is still launching, you can continue with this section as it involves setting IAM roles for upcoming labs.

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/navigate-created-notebook-instance.png]]

***

3.2. Now scroll down until you see the section **"Permissions and encryption"**. 

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/click-sagemaker-role.png]]

***

3.3. Where you see "IAM role ARN", click on the hyperlink, which will open up IAM.  

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/iam-viewing-sagemaker-role.png]]

***

3.4. Select the option to **"Add inline policy"**.

***

3.5. Where it shows the tabs "Visual Editor" and "JSON", click on **"JSON"**. 

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/iam-create-policy.png]]

***

3.6. Then copy the Json that is in the location (it is easier to open in a separate window).

[iam-policy.json](https://github.com/dupled3031/AWS-AIML-examples/blob/master/setup/iam-policy.json)

***

3.7. No copy the copied json in the IAM policy section.


[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/json-edit.png]]

This is what it looks like after pasting.

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/policy%20after%20copy-paste.png]]

***

3.8. Click continue/review policy.

***

3.9. Give it a name like aimlbootcamppolicyforsagemaker

***

3.10. Step through all the steps. You should have something that looks like this.

[[https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/iam-policy-done.png]]

Your setup is now done.  You can now access the Jupyter (if your in stance is up and running).

***

## Step 4 - Access your Jupyter environment.

4.1. Log into Jupyter.

Locate your notebook instance. Wait until it is in service. Once it is in service, click the link "**Open Jupyter**".

![Locate your Notebook instance](https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/locate-created-nb-instance-open-jupyter.png)

***

4.2. You will now see a folder structure that align with the Github sample structure. In here you will have Jupyter notebooks that you can use for labs and sample code.

![Jupyter environment](https://github.com/dupled3031/AWS-AIML-examples/blob/master/images/accessing-jupyter-notebook.png)

***

4.3 (Optional): Navigate to a sample notebook. 

You can use this one as a sample: AWS-AIML-examples/aiservices/rekognition/amazon-rekognition-labels-faces-text-detection.ipynb

Choose "Cell", "Run All" from the menu and validate that it runs.

Make sure that all the steps run without error.


