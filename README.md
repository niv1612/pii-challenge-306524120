# Personally Identifiable Information (PII) Detector

The *Data Direct* service enables the sharing of Comma Separated Value (CSV) files. The objective of this assignment is to enhance the service by implementing a sanitization pipeline that removes PII.

## Objective

Implement a sanitization pipeline that removes [Email addresses].

## Prerequisites

- Docker runtime environment (E.g. [Rancher Desktop], [Docker Desktop], etc.)
- [Docker Compose] version 2

## Instructions

You are provided with two S3 buckets: `input` and `output`. The `input` bucket stores uploaded files, while the `output` bucket is for sanitized files (objects).
The sanitization pipeline should scan each object in the `input` bucket. If an Email address is detected, the object should be moved to the `blocked` prefix within the `input` bucket. Otherwise, if no PII is detected, the object should be moved to the `output` bucket.

## Clarification

1. Email address has its own dedicated value/column in the CSV
2. Each uploaded file is not larger than 64MB
3. Store your implementation in `my-solution` Git branch
4. Use `src` directory for the implementation
5. All [status checks] must pass before submitting the assignment
6. You may add your own [workflows] but do not modify existing steps
7. Do not modify the `tests` directory
8. We leverage Localstack, see [Localstack AWS services supportability] for more information

<!-- References -->
[Email addresses]: https://en.wikipedia.org/wiki/Email_address#Syntax
[Rancher Desktop]: https://github.com/rancher-sandbox/rancher-desktop
[Docker Desktop]: https://www.docker.com/products/docker-desktop
[Docker Compose]: https://docs.docker.com/compose/install/#installation-scenarios
[status checks]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/collaborating-on-repositories-with-code-quality-features/about-status-checks
[workflows]: https://docs.github.com/en/actions/using-workflows/about-workflows
[Localstack AWS services supportability]: https://docs.localstack.cloud/user-guide/aws/feature-coverage/
