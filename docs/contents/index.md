# AWS Controllers for Kubernetes

**AWS Controllers for Kubernetes (ACK)** lets you define and use AWS service resources directly from Kubernetes. With ACK, you can take advantage of AWS managed services for your Kubernetes applications without needing to define resources outside of the cluster or run services that provide supporting capabilities like databases or message queues within the cluster.

This is a new open source project built with ❤️ by AWS and available as a **Developer Preview**. We encourage you to try it out, provide feedback and contribute to development.

*Important: Because this project is a preview, there may be significant and breaking changes introduced in the future. We encourage you to try and experiment with this project. Please do not adopt it for production use.*

## Background
Kubernetes applications often require a number of supporting resources like databases, message queues, and object stores to operate. AWS provides a set of managed services that you can use to provide these resources for your applications, but provisioning and integrating them with Kubernetes was complex and time consuming. ACK lets you define and consume many AWS services and resources directly within a Kubernetes cluster. ACK gives you a unified, operationally seamless way to manage your application and its dependencies.

## How it works
ACK is a collection of [Kubernetes Custom Resource Definitions](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/) (CRDs) and controllers which work together to extend the Kubernetes API and create AWS resources on your cluster’s behalf.
[ACK](https://github.com/aws/aws-controllers-k8s/) comprises a set of Kubernetes custom [controllers](https://kubernetes.io/docs/reference/glossary/?fundamental=true#term-controller).

Each controller manages [custom resources](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/) representing API resources of a single AWS service API. For example, the service controller for AWS Simple Storage Service (S3) manages custom resources
that represent AWS S3 buckets, keys, etc.

Instead of logging into the AWS console or using the `aws` CLI tool to interact with the AWS service API, Kubernetes users can install a controller for an AWS service and then create, update, read and delete AWS resources using the Kubernetes API.

This means they can use the Kubernetes API to fully describe both their
containerized applications, using Kubernetes resources like `Deployment` and `Service`, as well as any AWS managed services upon which those applications depend.

## Getting Started
To get started, [choose and install](https://aws.github.io/aws-controllers-k8s/user-docs/install/) the controllers for the AWS services you want to manage. Then, [configure permissions](https://aws.github.io/aws-controllers-k8s/user-docs/permissions/) and [define your first AWS resource](https://aws.github.io/aws-controllers-k8s/user-docs/usage/).

## Getting Help
If you have feedback, questions, or suggestions please don't hesitate to submit an [issue](https://github.com/aws/aws-controllers-k8s/issues), a pull request or comment on an existing issue.

You can also search our [mailing list](https://groups.google.com/forum/#!forum/aws-service-operator-user/) or talk with us on the #provider-aws channel on the Kubernetes Slack (https://kubernetes.slack.com/) community.
