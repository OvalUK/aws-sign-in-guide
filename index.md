# AWS user sign in guide

This guide is a step by step guide on how to sign in as a new user to AWS, setup your MFA device and create CLI access keys.

---

## Account access

Copy the url from your LastPass user credentials item

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step01.png)

Complete the user form and sign in.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step02.png)

If this is your first sign in the you will have to create a new password, this requires *lowercase*, *uppercase*, *numbers* and *special characters*.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step03.png)

In the AWS search bar, type **iam** (it is case insensitive), then click the Service title in the list.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step04.png)

On the IAM dashboard click either of the **User** links.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step05.png)

Search for your user name, the list will display all the users (often searching is the quickest way). When it appears in the list click the name.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step06.png)

In the Summary page, click the **Security credentials** tab.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step07.png)

In the Sign-in credentials section find the **Assign MFA device** and click the **Manage** link.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step08.png)

Select the type of MFA device you wish to use and follow the wizard to complete the setup.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step09.png)

## *Optional* additional steps for CLI access

In a new tab or window open [this link](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-windows.html) and follow the steps to install the AWS CLI V2. Then return the IAM page an follow below.

In the user Summary page, under **Access keys** click the **Create access key** button.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step10.png)

Your new credentials will be displayed in a modal.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step11.png)

You can copy them from here into the credentials file that will have been created on your system. If the file does not exist then create a file so it's path would match this:

```sh
~/.aws/credentials
```

Then open it in a text editor and paste in the credentials from the AWS console. If you have a pre-existing *default* account that you wish to keep then add these details with another label.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step12.png)

This AWS user account will allow you access to certain other AWS accounts via *Assumed role access* to setup each account add a block like the ones below. Each *role_arn*  would be the role from the account you are going to access, not the current account.

![AccountAccess](https://s3.eu-west-2.amazonaws.com/oval-generic-20210414092403/public/assets/aws-sign-in-guide/step13.png)
