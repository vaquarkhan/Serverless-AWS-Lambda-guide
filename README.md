

![Alt Text](https://cdn-images-1.medium.com/max/1600/1*CAS2UKlhVhNT8O_TzD-YpA@2x.png)

# AWS Lambda Recipes :

AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume - there is no charge when your code is not running.With Lambda, you can run code for virtually any type of application or backend service - all with zero administration. Just upload your code and Lambda takes care of everything required to run and scale your code with high availability. You can set up your code to automatically trigger from other AWS services or call it directly from any web or mobile app

#### Building Blocks of a Lambda Application
* Function – A script or program that runs in AWS Lambda. Lambda passes invocation events to your function. The function processes an event and returns a response. For more information, see Working with Lambda Functions.

* Runtimes – Lambda runtimes allow functions in different languages to run in the same base execution environment. You configure your function to use a runtime that matches your programming language. The runtime sits in-between the Lambda service and your function code, relaying invocation events, context information, and responses between the two. You can use runtimes provided by Lambda, or build your own. For more infromation, see AWS Lambda Runtimes.

* Layers – Lambda layers are a distribution mechanism for libraries, custom runtimes, and other function dependencies. Layers let you manage your in-development function code independently from the unchanging code and resources that it uses. You can configure your function to use layers that you create, layers provided by AWS, or layers from other AWS customers. For more infromation, see AWS Lambda Layers

* Event source – An AWS service, such as Amazon SNS, or a custom service, that triggers your function and executes its logic. For more information, see AWS Lambda Event Source Mapping.

* Downstream resources – An AWS service, such as DynamoDB tables or Amazon S3 buckets, that your Lambda function calls once it is triggered.

* Log streams – While Lambda automatically monitors your function invocations and reports metrics to CloudWatch, you can annotate your function code with custom logging statements that allow you to analyze the execution flow and performance of your Lambda function to ensure it's working properly.

* AWS SAM – A model to define serverless applications. AWS SAM is natively supported by AWS CloudFormation and defines simplified syntax for expressing serverless resources. For more information, see What Is AWS SAM? in the AWS Serverless Application Model Developer Guide.



* Handler :

* Context :

* Logging :

* Errors :

* Tracing

------------------------------------------------------------------------------------------------

####  Events that can trigger a Lambda function
 You can configure these events to trigger Lambda functions:

* Table updates in Amazon DynamoDB.
* Modifications to objects in S3 buckets.
* Notifications sent from Amazon SNS.
* Messages arriving in an Amazon Kinesis stream.
* AWS API call logs created by AWS CloudTrail.
* Client data synchronization events in Amazon Cognito.

------------------------------------------------------------------------------------------------

####  AWS Lambda has the following limitations.
Runtime Environment limitations:

The disk space is limited to 512 MB.
* The default deployment package size is 50 MB.
* Memory range is from 128 to 1536 MB.
* Maximum execution timeout for a function is 15 minutes*.
Requests limitations by lambda:

Request and response body payload size are maximized to 6 MB.
* Event request body can be up to 128 KB.

- https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html

------------------------------------------------------------------------


#### Link 
- https://github.com/dwyl/learn-aws-lambda
- https://aws.amazon.com/lambda/resources/
- https://github.com/vaquarkhan/serverless-architecture-with-aws
- https://github.com/anaibol/awesome-serverless
- https://github.com/danteata/awesome-aws-lambda
- https://www.tutorialspoint.com/aws_lambda/aws_lambda_tutorial.pdf
- http://riptutorial.com/Download/aws-lambda.pdf
- https://github.com/danilop/AWS_Lambda_in_Action
- https://github.com/awslabs/aws-serverless-auth-reference-app
- https://github.com/PacktPublishing/Mastering-AWS-Lambda
- https://www.puresec.io/blog/aws-security-best-practices-config-rules-lambda-security
- https://github.com/danilop/LambdAuth
- https://github.com/PacktPublishing/Hands-On-Serverless-Applications-with-Go
- https://ivanjov.com/aws-serverless-stack-api-gateway-lambda-and-dynamodb/
- https://aws.amazon.com/blogs/compute/error-handling-patterns-in-amazon-api-gateway-and-aws-lambda/
- https://github.com/vaquarkhan/awesome-serverless
-------------------------------------------------------------------
#### Video
- https://www.youtube.com/watch?v=WrPOz2dx8XY
- https://www.youtube.com/watch?v=oQFORsso2go
- https://www.youtube.com/watch?v=ew_MnhRyAfE
- https://www.youtube.com/watch?v=BLcElBUhfrQ
- https://id-vision.net/detail/real-time-data-processing-using-aws-lambda-V10n9Uahk_M.html
- https://www.infoq.com/presentations/serverless-computing
- https://www.youtube.com/watch?v=yBWVN_iaHvQ
- https://www.youtube.com/watch?v=_mB1JVlhScs
- https://www.youtube.com/watch?v=QRSc1dL-I4U
- https://www.youtube.com/watch?v=Gr2TH277EdA
- https://www.youtube.com/watch?v=AV24RTvbgWA
- https://www.youtube.com/watch?v=9ElpSPXk-g8
- https://www.youtube.com/watch?v=4nrRt0dOcFk
- https://www.youtube.com/watch?v=V10n9Uahk_M
- https://www.youtube.com/watch?v=WbHw14hF7lU
- https://www.youtube.com/watch?v=08AjVGGQaKQ
- https://www.youtube.com/watch?v=nTIgpOLaLS8

#### AWS Orchestration (AWS Step Functions)

AWS Step Functions lets you coordinate multiple AWS services into serverless workflows so you can build and update apps quickly. Using Step Functions, you can design and run workflows that stitch together services such as AWS Lambda and Amazon ECS into feature-rich applications. Workflows are made up of a series of steps, with the output of one step acting as input into the next. Application development is simpler and more intuitive using Step Functions, because it translates your workflow into a state machine diagram that is easy to understand, easy to explain to others, and easy to change. You can monitor each step of execution as it happens, which means you can identify and fix problems quickly. Step Functions automatically triggers and tracks each step, and retries when there are errors, so your application executes in order and as expected.

- https://aws.amazon.com/step-functions/resources/
- https://medium.com/@tturnbull/passing-data-between-lambdas-with-aws-step-functions-6f8d45f717c3
- https://cloudacademy.com/blog/aws-step-functions-a-serverless-orchestrator/
- https://docs.aws.amazon.com/step-functions/latest/dg/tutorial-creating-activity-state-machine.html
- https://github.com/rlondner/aws-stepfunctions-samples
- https://github.com/OsamaJBR/teach-me-aws-stepfunctions
- https://github.com/serverless/blog/blob/master/posts/2017-09-18-how-to-manage-your-aws-step-functions-with-serverless.md
- https://github.com/awsdocs/aws-step-functions-developer-guide/blob/master/doc_source/tutorial-create-iterate-pattern-section.md
- https://github.com/awsdocs/aws-step-functions-developer-guide/blob/master/doc_source/tutorial-creating-activity-state-machine.md
- https://github.com/mugglmenzel/step-functions-example-workflow

#### Video
- https://www.youtube.com/watch?v=Dh7h3lkpeP4
- https://www.youtube.com/watch?v=rL6EqaMbC5U
- https://www.youtube.com/watch?v=8rmgF-SbcIk
- https://www.youtube.com/watch?v=VXa2eVatW54
- https://www.youtube.com/watch?v=75MRve4nv8s
- https://www.youtube.com/watch?v=sMaqd5J69Ns
- https://www.youtube.com/watch?v=aJ6WaoQDE_M
- https://www.youtube.com/watch?v=qE_ZD98K43I
- https://www.youtube.com/watch?v=zwD157KKEWg&list=PLrOyJq2oDA6Hq9N-YQOWxtttW6i7eE863
-------------------------------------------------------------------
## AWS Lambda Layers

You can configure your Lambda function to pull in additional code and content in the form of layers. A layer is a ZIP archive that contains libraries, a custom runtime, or other dependencies. With layers, you can use libraries in your function without needing to include them in your deployment package.

Layers let you keep your deployment package small, which makes development easier. You can avoid errors that can occur when you install and package dependencies with your function code. For Node.js, Python, and Ruby functions, you can develop your function code in the Lambda console as long as you keep your deployment package under 3 MB.

- https://github.com/mthenw/awesome-layers
------------------------------------------------------------------------------------------------

## Hands-on Guide For Building Serverless Applications

This is a hands-on guide for building Serverless applications. This guide is divided into various sections. The first section is about building serverless applications with the [Serverless](https://github.com/serverless/serverless) framework and [AWS Lambda](https://aws.amazon.com/lambda/). This guide is a work in progress so I will keep adding content as I continue to learn and understand the Serverless ecosystem.

I plan to cover different Serverless providers and tools in the Serverless ecosystem. Follow this repository to learn and master the Serverless ecosystem.

## Sections

1. [Hands-on guide for building serverless applications with AWS Lambda and Serverless Framework](./01-aws-lambda-serverless-framework): This section covers how to build Serverless applications with AWS Lambda and Serverless framework. Throughout this section, we will build an online coding round evaluator that organizations can use to automate their coding interview.

------------------------------------------------------------------------
## Serverless-failure-stories

- https://github.com/cristim/serverless-failure-stories

------------------------------------------------------------------------
<object data="https://www.jfokus.se/jfokus18/preso/Serverless-Architecture-Patterns-and-Best-Practices.pdf" type="application/pdf" width="700px" height="700px">
    <embed src="https://www.jfokus.se/jfokus18/preso/Serverless-Architecture-Patterns-and-Best-Practices.pdf">
        <p>This browser does not support PDFs. Please download the PDF to view it: <a href="https://www.jfokus.se/jfokus18/preso/Serverless-Architecture-Patterns-and-Best-Practices.pdf">Download PDF</a>.</p>
    </embed>
</object>
