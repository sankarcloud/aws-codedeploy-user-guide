--------

 The procedures in this guide support the new console design\. If you choose to use the older version of the console, you will find many of the concepts and basic procedures in this guide still apply\. To access help in the new console, choose the information icon\. 

--------

# Create an Amazon ECS Compute Platform Deployment \(Console\)<a name="deployments-create-console-ecs"></a>

1. Sign in to the AWS Management Console and open the AWS CodeDeploy console at [https://console\.aws\.amazon\.com/codedeploy](https://console.aws.amazon.com/codedeploy)\.
**Note**  
Sign in with the same account or IAM user information that you used in [Getting Started with AWS CodeDeploy](getting-started-codedeploy.md)\.

1. Do one of the following:
   +  If you want to deploy an application, in the navigation pane, expand **Deploy**, and then choose **Applications**\. Choose the name of the application you want to deploy\. Make sure the **Compute platform** column for your application is **Amazon ECS\.**
   +  If you want to redeploy a deployment, in the navigation pane, expand **Deploy**, and then choose **Deployments**\. Choose the deployment you want to redeploy, and in the **Application** column, choose the name of its application\. Make sure the **Compute platform** column for your deployment is **Amazon ECS**\.

1. On the **Deployments** tab, choose **Create deployment**\.
**Note**  
Your application must have a deployment group before it can be deployed\. If your application does not have a deployment group, on the **Deployment groups** tab, choose **Create deployment group**\. For more information, see [Create a Deployment Group with AWS CodeDeploy](deployment-groups-create.md)\. 

1. In **Deployment group**, choose a deployment group to use for this deployment\.

1. Next to **Revision location**, choose where your revision is located:
   + **My application is stored in Amazon S3** — For information, see [Specify Information About a Revision Stored in an Amazon S3 Bucket](deployments-create-console-s3.md), and then return to step 6\. 
   + **Use AppSpec editor** — Select either JSON or YAML, then type your AppSpec file into the provided editor\. You may save the AppSpec file you type in by selecting **Save as text file**\. When you click **Deploy** at the end of these steps you will receive an error if your JSON or YAML is not valid\. For more information about creating an AppSpec file, see [Add an Application Specification File to a Revision for AWS CodeDeploy](application-revisions-appspec-file.md)\. 

1. \(Optional\) In **Deployment description**, enter a description for this deployment\.

1. \(Optional\) In **Rollback configuration overrides**, you can specify different automatic rollback options for this deployment than were specified for the deployment group, if any\.
**Note**  
For information about rollbacks in AWS CodeDeploy, see [Redeployments and Deployment Rollbacks](deployment-steps.md#deployment-rollback-lambda) and [Redeploy and Roll Back a Deployment with AWS CodeDeploy](deployments-rollback-and-redeploy.md)\.

   Choose from the following:
   + **Roll back when a deployment fails** — AWS CodeDeploy will redeploy the last known good revision as a new deployment\.
   + **Roll back when alarm thresholds are met** — If alarms were added to the deployment group, AWS CodeDeploy will redeploy the last known good revision when one or more of the specified alarms is activated\.
   + **Disable rollbacks** — Do not perform rollbacks for this deployment\.

1. Choose **Create deployment**\. 

   To track the status of your deployment, see [View AWS CodeDeployDeployment Details ](deployments-view-details.md)\.