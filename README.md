# AWS-AIML-examples

## Prerequisites

You need an AWS account for these labs, and depending on the lab you also need a role with administrator access on the account to configure the neccessary IAM roles.

## Step 1 - apply lab credits if you have any

Navigate to the account link at the top right of your window.

Select **Account**. Then navigate down to **Credits** and enter in the coupon.

## Step 2 - Set up your Sagemaker Jupyter Notebook instance

In the AWS console, navigate to Sagemaker. Then select, **Notebook** | **Notebook Instances**. Click the **Create Notebook instance** button.


Notebook instance name: aimlbootcamp
Notebook instance type: any xlarge instance type
Git repositories:
> Choose "Clone a public Git repository to this notebook only"

> Git repository URL: https://github.com/dupled3031/AWS-AIML-examples.git

Click **Create Notebook Instance**
Choose a name for the notebook, for example "aimlbootcamp" as the instance name. 
You can bump the instance size up to extra large.  

The instance will take about five minutes to start up. In the mean time, proceed to the next step.


## Step 3 - Give the Sagemaker instance IAM permissions to invoke with other AWS services

For the notebook instance you just created in the previous step, click on the hyperlink with the name of the instance to open up the instance detail panel.

Now scroll down until you see the section **"Permissions and encryption"**. 

Where you see "IAM role ARN", click on the hyperlink, which will open up IAM.  

Select the option to **"Add inline policy"**.

Where it shows the tabs "Visual Editor" and "JSON", click on **"JSON"**. 

Then paste in the following JSON in the window.  




