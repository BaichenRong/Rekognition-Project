# Rekognition-Project on detecting common traits in Expensive Houses
This project utilized Rekognition and various Python visualization and statistic methods to observe and measure common traits among the Expensive Houses. It uses built-in python [Amazon Rekognition Labels Detection](https://docs.aws.amazon.com/rekognition/latest/dg/labels.html) to identify which labels are frequently exists in these expensive houses and how the confidence level of these label can in fact tell the observer any information related to the housing price.

## Architecture and explanation
![Architecture](./Diagram.png)

We collected 9 expensive Houses ranged from 1 million to 2 million dollars in the website [LianJia](https://bj.lianjia.com/), the largest second-hand trade platform in China. There are also websites that can be accessed to collect similar sources such as [Zillow](https://www.zillow.com/) and [Trulia](https://www.trulia.com/). All of the websites provided basic information of the real estate property, such as pictures of the houses, housing price, location, neiborhood, transportation around and etc. After collecting pictures, upload all these pictures to S3 buckets. By using Rekogntion to detect labels and confidence level, use the Seaborn or Matplotlib to generate analysis and visualization.

## Example of detection
![example](./example/example.png)

We wrote three lines of code to generate these capture.
First is to call the AWS Rekogntion Service from the Boto3 packages
Second is to indicated the Path in the S3 Bucket for Rekogntion to detect
Third is to display the detected labels
We can see the built in Rekogntion Service succesfully capture and detect elements in the picture
