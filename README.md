# AWS-Glue-and-Athena- Serverless Data processing and querying

Data Source Acquisition: Checkout for any free available dataset and download in a CSV or Json format. (I have used COVID-19 cases and deaths data from WHO).

IAM Role Creation: Establish an IAM Role granting necessary permissions for AWS Glue access, configured with Poweruseraccess permissions.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/ac0b682d-4e88-4371-b49c-d9f1e4d42648)

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/0db4a18f-2a17-48a5-a997-5ee7fdf6b651)


S3 Bucket Setup: Create distinct S3 buckets for input data, output data, and scripts.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/c1524f87-d31b-4fbf-bb06-775f8c76fe9a)


Data Upload: Upload the dataset into the designated input data S3 bucket.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/db1efb3d-ef59-4bf1-a563-937d9e19f15b)


Database Creation in Glue: Establish a database within AWS Glue to manage the structured data.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/89246306-5d4b-4a38-9954-a766fe2754a3)


Crawler Configuration: Set up a crawler within AWS Glue, assigning the input S3 bucket as the source, along with specifying the IAM role and database for metadata cataloging.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/bbd7b81d-4d77-4d77-8795-9d654ff1d2f5)

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/a4eedb08-fd03-4c0f-b24b-e555b2f88ca8)


Crawler Execution: Initiate the crawler to traverse the data source, utilize classifiers to infer schema, and it should create metadata tables in the data catalog.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/cc3d73ce-bdfe-43b1-81aa-ad04001a8ae5)

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/0d001197-815c-43ec-8e43-1d319e59bb0b)


ETL Job Configuration: Develop an Extract, Transform, Load (ETL) job within AWS Glue, utilizing the Glue Data Catalog as the source and selecting the designated database.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/24ab945e-00c3-42ca-9194-66d80186ae7d)


Schema Transformation: Specify actions for schema modification and transformation, such as dropping unnecessary columns.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/a850dd1d-ba5f-415c-a2a0-93d23b67a122)


Output Configuration: Define the target S3 bucket for transformed data storage, specify required formats (e.g., CSV) and compression types (e.g., Zip).

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/3ac550ff-16c7-4e80-bbe2-62572051d562)



Job Details Specification: Name the ETL job, specify required format (e.g., Python), and provide the script path pointing to the stored script in the designated S3 bucket. Save the configured job.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/c5136363-434c-4c81-af16-5a1082076818)


Script Generation: AWS Glue automatically generates scripts tailored to the specified output requirements.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/afe000ca-fc77-438f-a4b5-b6dc7f993601)


Job Monitoring: Monitor the execution of the ETL job within the job monitoring interface provided by AWS Glue.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/5e662669-93d9-4410-b6aa-ee093e0bb6ab)


Output Validation: Verify the successful transformation and storage of the output file within the designated output S3 bucket. Download, extract, and inspect the resulting file.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/069f8894-1c87-4284-be21-26bdf902890c)


Data Querying with Athena: Utilize AWS Athena to query the transformed data stored in the Glue output data catalog.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/f9a2df25-0e2d-4e0b-8db6-8b8083f4522b)


Athena Setup: Create a separate S3 bucket dedicated to storing Athena query results.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/5f4cfb23-a397-4fe8-badd-ffda73984f26)


SQL Query Execution: Compose and execute SQL queries within Athena to analyze and retrieve desired insights from the transformed data.

![image](https://github.com/maheshkoheda/AWS-Glue-and-Athena/assets/25144175/dbfe1508-b306-4a4b-9f1d-6f230c7c00fc)


