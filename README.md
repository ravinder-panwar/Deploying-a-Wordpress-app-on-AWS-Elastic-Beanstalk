# Deploying a WordPress app on AWS Elastic Beanstalk
**Step 1: Go to WordPress.org and download it.**
Make a zip file of it.

![1](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/e72de3b7-276e-4ac2-8c57-d84e9024fe3b)

**Step 2: Creating an IAM Policy.**
1. Go to IAM.
2. Policy.
3. Create Policy ( I created the policy name by **CodeDeployDemo-EC2-Permissions** )
4. Choose JSON.
5. Remove the script and paste the new script.
6. Save.

![2](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/1388be32-7b43-4bd2-9379-d3b848d7cf72)

![3](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/71cfa194-bbd8-44ea-b696-67484e1a89cc)

![4](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/ac98b456-fe13-4368-a072-9d3acda226e4)

![5](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/6b4d081a-c002-4895-9e2b-3a1f9db9af9c)

**Step 3: Creating an IAM Role.**
1. In AWS Console go to Services and choose IAM.
2. Click Roles from the left menu and press the Create Role button ( I created the IAM Role name by **ElasticBeanStalkInstanceRoleWeb** )

![6](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/b262993a-42a7-4219-b3ad-e75b09ea1eda)

3. Select AWS Service under a trusted entity type.
4. Select EC2 under the use case.
5. Click Next.

![7](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/b8c4a18d-257b-4fd1-91e0-31b061f713d0)

6. Under Permission policies, search for the policy named **AWSElasticBeanstalkWebTier**, **CodeDeployDemo-EC2-Permissions**, and **AmazonSSMManagedInstanceCore** and check the box.
7. Click Next.

![8](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/1ba76327-1b05-4e51-b878-53a2df5a6cf9)

![9](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/4a4fe887-3cc4-4b95-a77d-b3c8aefb91bb)

**Step 4: Create Elastic Beanstalk Environment**
1. Go to the AWS Console, from Services choose Elastic Beanstalk, and click Create Application.
2. Create Environment.

![10](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/98f51c0c-4308-41c3-801f-5bcb74e635f6)

3. Configure as I have done.
   
![11](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/ca267e0d-2c9b-4897-b6ea-ba93c9f6b785)

![12](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/c46ecd80-a6b4-4359-94e9-3266134d883f)

![13](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/f2b28d54-af28-4898-9773-843912e29b04)

![14](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/e02a5c7c-f21d-4ce6-bbc1-db9ff94fa65e)

![15](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/7f8600a2-7f95-43f1-93c5-6fa5d50d92e6)

![16](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/998bd907-bf64-4df3-b43a-4c18f90d342a)

![17](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/78cf20cc-b88b-4f05-a7d3-beff449b26f0)

4. Review everything carefully and **sumbit.**

![18](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/c8bb6b03-d091-49b1-9fa1-7180b6f805c6)

5. Wait 5-10 minutes till web application has been launched completed. Once it is launched successfully you will get a Domain URL.

![19](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/6409fd02-f18e-40e4-9c1f-c220ae888e5a)

6. Copy this URL and open it.

![Capture](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/cb7736c1-0837-4222-ac74-0129b7852c45)

7. CONGRATS! We have successfully deployed the wordpress web app on AWS Elastic Beanstalk.

![20](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/ca51129c-42c1-4dde-9c8c-de086f229759)

**Step 5: Setting up WordPress.**

1. Go to RDS and copy the Endpoint from the Connectivity & Security section.
2. Also Copy the Database name from the Configuration section ( Database name is **ebdb** ).

![21](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/673b9a57-2b28-466d-aa8a-6744580bd0c9)

3. Fill the details and write the username and password correctly.

![22](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/e0721b62-ea34-4625-9a08-31699d8195e0)

![23](https://github.com/ravinder-panwar/Deploying-a-Wordpress-app-on-AWS-Elastic-Beanstalk/assets/133412857/1bb4aa97-5582-4651-bd77-ab6e6712b58d)

**<h1> Completed** 







































