# Integration Scenario

This section walks you though a generic integration scenario.
The process has been designed to be really simple and allow you to set it up quickly.  

## 1. Configure your Skillmeter account
### Personalize your company's test center page
This is the first step you need to take after you set up your account with Skillmeter (https://skillmeter.com).   Personalize your company's test center page with your logo and links to your website and social channels.

### Create tests
Then create/set-up one or more tests in the test section.  You have different options to parametrize your tests and you can add a wide variety of question types.

### Notifications template
If you want to let Skillmeter send email invites to  candidates each time they are assigned to a test, go to the Notifications section, customize the notification template and turn on the notifications sending.

## 2. Integrate with Skillmeter

Thanks to the API we expose, you can cover a wide types of integration between your tools/apps and Skillmeter.

The most frequent and simple scenario is to the following:  keep staying in your candidate management tool and assign Skillmeter tests from there.  In order to do that, you would need to hack the flow with only 2 steps:

#### Get the lists of available tests from Skillmeter
Simply fetch the list of tests from the [Test](Endpoints/Test.md) endpoint 
If you are certain the tests will not be deleted, you can store the Test IDs on your side to avoid calling Skillmeter each type.

#### Assign the test to your candidate
In order to do that you need to do a post call to the [Candidate](Endpoints/Candidate.md) endpoint and pass all required details.  The candidate will be also created on Skillmeter, the unique PIN code generated and the invite email sent (if notifications are turned on)
