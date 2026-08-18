# AWS-Lambda-Project

AWS Lambda is a serverless computer service that can run code without provisioning or managing servers.

This is a personal write-up for the following AWS lambda project

https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html

# Creating a Lambda function within the console

For this workshop, the example function multiples two integers and returns the product as a JSON string

Open functions page in Lambda console and create a new function.

export const handler = async (event, context) => {

```
  
  const length = event.length;
  const width = event.width;
  let area = calculateArea(length, width);
  console.log(`The area is ${area}`);
        
  console.log('CloudWatch log group: ', context.logGroupName);
  
  let data = {
    "area": area,
  };
    return JSON.stringify(data);
    
  function calculateArea(length, width) {
    return length * width;
  }
};

```


