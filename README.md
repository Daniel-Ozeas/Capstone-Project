# About the Project

Everything about the dataset and every step is explained inside Jupyter Notebook.

# How run into EMR cluster

#### Create EC2 key pair
* Go to EC2 instance
* In NETWORK & SECURITY choose key pairs
* Create key pair and save the .pem archieve in ~/.ssh/

## Create a EMR cluster

#### Software Configurations
* Release: emr-5.29
* Applications: Spark: Spark 2.4.4 on Hadoop 2.8.5 YARN with Ganglia 3.7.2 and Zeppelin 0.8.2

#### Hardware Configurations
* Instance type: m5.xlarge
* Number of instances: 3 (1 master and 2 core nodes)

#### Security and Access
* EC2 key pair: Choose the one created above
* Permissions: Default
* EMR role: EMR_DefaultRole
* EC2 instance profile: EMR_EC2_DefaultRole 

## Create a Notebook
* Enter in AWS EMR and Go to Notebooks option
  * Note: region South America (São Paulo) doesn't have notebooks
* Choose the notebook name and description 
* Chosse an existing cluster and select the one created above
* Security groups: Use default security groups
* AWS service role: EMR_Notebooks_DeafultRole
* Notebook location: Use default S3 location
* Open the Notebook and upload the CapstoneProject.ipynb
* Change the kernel to Pyspark

Note: See if the security group configurations to Notebook is the same of the [AWS instructions](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-managed-notebooks-security-groups.html)

