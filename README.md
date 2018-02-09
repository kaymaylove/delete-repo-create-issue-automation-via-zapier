
# Delete Repository, Create Issue Automation through using Zapier Webhook

Webhooks by Zapier listen for selected changes that occur on another app. This webhook will listen for when a repository is deleted on github and create an issue in a repository in the same organization as the deleted repository. It also has ability notify users and assign the issue to an individual in that organization.

### Prerequisites
* Create a [Zapier Account](https://zapier.com/sign-up/) - a service that connects different applications and allows you to automate actions between different apps, once the first action is triggered. The benefits of using Zapier is that they have over 1000+ integrations and it does not require developers, an admin could easily learn how to utilize Zapier to make much more efficient workflows in an office setting. Also, the time saved from manual actions, could easily increase profits and offset the monthly fee to use Zapier. There is a free trial period where an admin can test if this method is right for the company.

### Getting Started
* Once, an account is created and a user logs in, it will navigate to Zapier's [integrations page](https://zapier.com/apps/integrations)
* Search for Webhooks by Zapier and select it to add it to the filter
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/1.png)
* Search for Github and select it to add it to the filter
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/2.png)
* On the the upper right corner of the screen, select `make a zap`
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/3.png)
* Click on `Webhooks`
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/4.png)
* At the boottom of the page, Click `create this zap` and then a user wil begin to set up the catch hook which will listen to events that happen (i.e. deleting a repo)
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/5.png)
* Then, click `Save and Continue` and then pick off the child key of "action": "deleted" (this will specifically look for repos that have been deleted)
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/6.png)
* Copy the custom webhook url
* Navigate to github in another tab to create a [webhook](https://github.com/organizations/yourorg/settings/hooks/new)
	* In payload url, enter the custom webhook url created from Zapier
	* Select Application/JSON
	* Select `Let me select individual events`, then mark off `Repository` events and click `create webhook`
* Navigate to the other tab where Zapier was and click `Ok, I did this`
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/7.png)
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/8.png)
* To test the webhook, create a repo and then delete a repo and it will come back as successful
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/9.png)
* Click continue and begin set up the action step (the action that will occur when a repo is deleted)
* Click on Github or search if it does not appear
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/10.png)
* Click `create issue`
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/11.png)
* To create issues remotely or through webhooks, it has to be authenticated/authorized through github
* Login to the github account or select a github account if it was authenticated before
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/12.png)
* Click `save + continue`
* Enter the desired fields for the Github issue that will be committed each time a repo is deleted
    * A user can select custom fields to create dynamic issues that reference the repos name that was deleted
    * Add the name of the repo where you want to add the issues to
    * Create the title name (e.g. Deleted Repo: [Repository Full Name] )
    * Enter content into the body of the issue and mention users/collaborators if desired
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/13.png)
* Lastly, test to make sure this webhook is working
    * Delete a repo, not the one you set notifications to
    * Check the repo where notifications are sent to and a user should see an issue with the deleted repo name and a body message with mentions other users and possibly it is assigned to someone
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/14.png)
* Lastly, Create a name for this zap and turn it on/off whenever needed
![](https://github.com/Todaiji/Todaiji-delete-repo-create-issue-automation-via-zapier/blob/master/step-by-step-images/15.png)

## Authors

* **Karen Port** - [kaymaylove](https://github.com/kaymaylove)

## Acknowledgments

* [Zapier](https://zapier.com/)
* [Github](https://developer.github.com/v3/)


***

keep calm and automate on
