---
title: Overview
description: Use Amplify CLI to create and manage cloud-connected file & data storage for your app.
---

Amplify CLI's `storage` category enables you to create and manage cloud-connected file & data storage. Use the `storage` category when you need to store:

1. app content (images, audio, video etc.) in an public, protected or private storage bucket or
2. app data in a NoSQL database and access it with a REST API + Lambda

## Setup a new storage resource

You can setup a new storage resource by running the following command:

```bash
amplify add storage
```

Amplify allows you to either setup a app content storage (images, audio, video etc.) backed by Amazon S3 or a NoSQL database backed by Amazon DynamoDB.

### Adding S3 storage

```console
? Please select from one of the below mentioned services:
> Content (Images, audio, video, etc.)
  NoSQL Database
? Please provide a friendly name for your resource that will be used to label this category in the project:
> mystorage
? Please provide bucket name:
> mybucket
```

Follow the prompts to provide your content storage's resource name.
Next, configure the access permissions for your Amazon S3 bucket. If you haven't set up the `auth` category already, the Amplify CLI will guide you through a workflow to enable the auth category.

If you want to restrict this storage bucket to only authenticated users, then select "Auth users only". If you want unauthenticated users to access this storage bucket as well, then select "Auth and guest users".

```console
? Who should have access:
Auth users only
Auth and guest users
```

Next, you'll be prompted to set the access scopes for your authenticated and (if selected prior) unauthenticated users.

```console
? What kind of access do you want for Authenticated users? (Press <space> to select, <a> to toggle all, <i> to invert selection)
 ◯ create/update
❯◯ read
 ◯ delete
? What kind of access do you want for Guest users?
❯◯ create/update
 ◯ read
 ◯ delete
```

```console
? Do you want to add a Lambda Trigger for your S3 Bucket? (y/N)
```

If you want to configure a Lambda trigger for your S3 bucket, you'll have the option. Learn more about this workflow [here](~/cli/usage/lambda-triggers.md#s3-lambda-triggers).

That's it! Your content storage is set up! Head to the [library's storage docs](~/lib/storage/getting-started.md) to integrate this newly created S3 bucket into your app.

### Adding a NoSQL database

```console
? Please select from one of the below mentioned services:
> Content (Images, audio, video, etc.)
  NoSQL Database
? Please provide a friendly name for your resource that will be used to label this category in the project:
> dynamo2e1dc4eb
? Please provide table name:
> dynamo2e1dc4eb
```

Follow the prompts to provide your NoSQL Database's resource name. Next, you'll go through a table-creation wizard. First, you'll create the columns of your table:

```console
You can now add columns to the table.

? What would you like to name this column: id
? Please choose the data type: string
? Would you like to add another column? Yes
```

Then, you'll need to specify your indexes. The concept behind "indexes", "partition key", "sort key" and "global secondary indexes" are explained in-depth [here](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.CoreComponents.html#HowItWorks.CoreComponents.PrimaryKey).

```console
? Please choose partition key for the table: id
? Do you want to add a sort key to your table? (y/N)
```

```console
? Do you want to add a Lambda Trigger for your Table? (y/N)
```

If you want to configure a Lambda trigger for your Table, you'll have the option. Learn more about this workflow [here](~/cli/usage/lambda-triggers.md#dynamodb-lambda-triggers).

That's it! Your NoSQL Database is set up!
