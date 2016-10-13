# Testing the demo app

## Preamble

The HiPay Fullservice SDK for iOS is shipped with a demo application which allows you to quickly test the built-in payment screen integration.

This demo application presents a screen that allows you to generate a payment screen based on many parameters such as: amount, payment product categories, etc.

This particular screen in not part of the SDK and your users will not see it. It's part of the demo application and has been created for testing purposes only.

## Installation guide

### Clone the repository

First, you need to check out the repository. Go in your projects folder and type the following command:

	$ git clone https://github.com/hipay/hipay-fullservice-sdk-ios.git

Then, go in the project directory:

	$ cd hipay-fullservice-sdk-ios

### CocoaPods

This project is built using [CocoaPods][cocoapods], the most popular package manager for Cocoa projects. If you've already installed CocoaPods on your workstation, skip this section.

If you did not install CocoaPods yet, install it by typing the following command:

	$ sudo gem install cocoapods

### Set up the project

First, go in the demo app directory:

	$ cd Example

To generate the project workspace, run the following command:

	$ pod install

### Open the project

Open the `HiPayFullservice.xcworkspace` workspace by typing the following command:

	$ open HiPayFullservice.xcworkspace

### Add your credentials

To try the demo application with your HiPay Fullservice API test credentials, open the `parameters.plist` file and set your API username and password, as below:

![Setting API credentials for the demo app](images/demo/credentials.png)

To find your credentials, refer to the [Prerequisites and recommentations](#prerequisites-and-recommentations) section.

### Set the proper pass phrase

The demo app uses a HiPay's test web service which generates the signature based on a specific pass phrase. Thus, in order to test the demo app, you must set the same specific pass phrase on your HiPay Fullservice test account.

To set the pass phrase, sign in to your HiPay Fullservice merchant back office. Then, go to the "Integration" section and click on "Security settings". Finally, set the following string in the "secret pass phrase" input field: 

	32JUWB3veDWWmHySNJvtvPyBnqrDFEHbaP3jr

**Warning: do NOT set this passphrase on your live/production account. This specific pass phrase must only be used for testing purposes.**

You should get that on your screen:

![](images/demo/passphrase.png)

Don't forget to apply your changes.  

### Run the demo app

Finally, build and run the `HiPayFullservice-Example` target.

[repo]: https://github.com/hipay/hipay-fullservice-sdk-ios
[cocoapods]: https://cocoapods.org/