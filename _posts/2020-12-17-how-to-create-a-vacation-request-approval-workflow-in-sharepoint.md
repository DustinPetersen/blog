---
layout: post
title: How to create a Vacation Request Approval workflow in SharePoint
date: 2020-12-17 13:32 -0700
categories:
    - Microsoft
    - Lists
tags:
    - Microsoft
    - Lists
    - Data Management
---

Vacation Request or PTO (Paid Time Off) is a common type of request in every organization. Hey, we all need vacations from time to time. 🙂  While some firms have special software in place to request vacations, for the most part, many rely on the back and forth email. With this post, I would like to explain how you can build a simple Vacation Request Approval workflow in SharePoint. And the best part – it can be done using an out of the box functionality, without a single line of code! To better illustrate the example, I will rely on a recent request from one of my clients, for whom I built the exact functionality I outline below. These were their requirements:

Ability for submitter to view own requests only
Ability for manager field to be dynamic (different approving managers for different employees)
Email notification for both the approving manager and submitter of the requests
Ability to view all vacation requests in a calendar mode
Ability for the manager to type in rejection comments
Let me now explain how I arrived at the proposed solution and how I achieved and satisfied (almost) all of their requirements. The solution is based on SharePoint out of the box features and does not rely on any other tools, like SharePoint Designer or Microsoft Flow. If you have SharePoint Online/Office 365, I strongly suggest that you consider and use Flow for building the above process. As a matter of fact, it would be quite an easy undertaking using such a tool. I will document this in one of the later posts. But for now, let’s build it using SharePoint out of the box.

## STEP 1: CHOOSING THE CORRECT WEB PART
Theoretically, we could use any SharePoint list to start off with the request form. We could start from Custom List, Issues Web part, Calendar or Task List. However, the requirement to be able to view vacation requests in a Calendar mode leaves us with just two possible choices: Calendar web part itself and Tasks (Tasks web part has many built-in views, including the Calendar view). Moreover, since we need an ability for an approving manager field to be dynamic, we are left with just the Tasks web part (since it has the Assigned To column and automatic email notification for “Assigned To” column). So the chosen web part is Tasks!

## STEP 2: CONFIGURE LIST SETTINGS
Let’s go ahead and configure some back-end settings. Here is what we need to do:

In Versioning settings – enable versioning (this will help review request history if needed)Vacation Request Approval workflow in SharePoint
In Versioning settings – enable Content Approval on a list. This will add the necessary “approval” mechanism along with the approval/rejection columns + comments field. I documented Content Approval feature in great detail in this post – please check it out.Vacation Request Approval workflow in SharePoint
In Advanced settings – enable Content types – this will be necessary in next step so we can hide unnecessary columns and/or change order of the columns
In Advanced settings – enable Item Level Permissions. This will allow for vacation requests to only be seen by submitters and approvers and no one else. I explain how Item Level Permissions works in this post
In Advanced settings – enable Email notification. This will send an email notification to the users whose name appears in the Assigned To column
In Advanced settings – disable attachments. There is no reason for users to submit any files as attachments when they request vacations
In Advanced settings – disable the Quick Edit view – we don’t want users to mess with any requests in bulk – so this will help avoid this
## STEP 3: CONFIGURE COLUMNS
Tasks web part has lots of columns that are meant for project scheduling, etc. We don’t need most of them. So go ahead and hide them (via Content Type). The only ones we need are Title, Start and End Dates, Description. Also, change the default column name as necessary, so they are a bit more descriptive. For example, change Due Date to End Date and Assigned To to Manager Name. Also, change format of dates for Start and End Dates to standard from friendly (so it shows actual calendar dates, instead of “due in 3 days”)

Vacation Request Approval workflow in SharePoint

## STEP 4: CLEAN UP VIEWS
Just like with columns above, we need to cleanup the views. We don’t need most of them. For example, Gantt Chart or Completed views can be removed (deleted). Go ahead and delete them. On the remaining ones, hide/show columns as required. Hide the Timeline from the view as well – we don’t need it here (it is handy for project management only). Change names of views as necessary (i.e. change All Tasks to All Requests and My Submissions to My Requests).

Vacation Request Approval workflow in SharePoint

## STEP 5: SET UP ALERTS
Since the manager will be notified about the submission when their name appears in the Assigned To column, there is nothing else we need to do on that front. So the only alert that needs to be set up is for the submitter. However, here is a problem – when we enable Item Level Permissions – alert feature won’t work. So alert for submitter is not a requirement we will be able to satisfy here with the existing setup.



If, however, Item Level Permissions is not required (requests can be viewed by anyone) – then I recommend below settings for the alert – this way, the user will only be notified about their requests only (approvals/rejections).



That’s all – you see, it did not take long at all – and we now ended up with the fully-functional Vacation Request Approval workflow in SharePoint! And we satisfied almost all of our original requirements too! The only inconvenience here – you have to specify manager name, and there is no automatic manager field lookup. In my opinion – this is a very small price to pay, especially if you want to go on vacation! 🙂  Enjoy your vacation!

Vacation Request Approval workflow in SharePoint