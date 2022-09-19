# AWS CLI with CDK and Dotnet

The container produced from the Dockerile in this repository was built to be able to deploy AWS CDK apps built with Dotnet using BitBucket pipelines. 

As alwasy, there might be a better way / more gracious way to do this, but this is here for others trying to solve the same issue I had.

It uses the aws-cli Docker image as its base, just to have the AWS CLI stuff in place. This way it should be possible to use this image to synth and deploy the Dotnet CDK app, as well as peform other AWS actions.

## Usage

The prebuilt images for the platform linux/amd64 can be found here: https://hub.docker.com/r/haxzorer/aws-cdk-dotnet

To use it with a CDK app that is using Dotnet 3.1: docker run --rm -it haxzorer/aws-cdk-dotnet:cdk-2.42.0-dotnet-3.1

To use it with a CDK app that is using Dotnet 6.0: docker run --rm -it haxzorer/aws-cdk-dotnet:cdk-2.42.0-dotnet-6.0
