---
title: 8 CHALLENGES OF BYOD IN SHAREPOINT: AN INSIDER’S TIPS
author: Dustin Petersen
date: 2019-08-08 14:10:00 +0800
categories: [SharePoint, BYOD,]
tags: [BYOD]
---

8 CHALLENGES OF BYOD IN SHAREPOINT: AN INSIDER’S TIPS

When you look at the numbers, the challenges of BYOD in SharePoint reach far and wide. 17,000 organizations now run SharePoint as their enterprise CMS and 125 million SharePoint licenses have been sold to date, according to file-sharing company Accellion. Gartner reports 70% of organizations allow users’ personal devices to access network systems and enterprise applications, and an astounding 78% of white-collar employees in the US use their own laptops, smartphones and tablets for work purposes (Cisco Systems).

You do the math. Thousands of IT departments are dealing with the daily challenges of actively monitoring and managing a myriad of mobile devices, yet delivering SharePoint content in a way that is easy and useful so that employees don’t look to less secure alternative solutions.

So what’s the problem? Two words – data breaches. In March 2011, 40 million employee records were stolen from RSA Security; the year before that Gawker Media experienced compromised email addresses and passwords of about 1.3 million commenters on popular blogs Lifehacker, Gizmodo and Jezebel, plus the theft of the source code for Gawker’s custom-built content management system. Although not on the same scale, corporate data breaches are common. According to research firm, Ponemon, about 85% of all US companies have experienced one or more data breaches.

## SharePoint Needs Careful Management
SharePoint is capable of handling more than 200 file types out of the box. Imagine the data it can unleash. Without appropriate and consistent policies around access controls and security measures, such as restricted remote access, critical information can be left to twist in the wind.

Administrative mishaps, incorrectly configured services, and broad access rights all create security vulnerabilities. In the wrong hands, consumer-grade devices open an easy way through these vulnerable holes to enterprise data stored on the device and sometimes into the entire enterprise network.

As experts in SharePoint collaboration, we’ve learned first-hand where our customers face the biggest BYOD challenges in SharePoint, and they broadly divide into two categories: security and ease of use. The two go hand-in-hand to satisfy the needs of the organization as a whole and the individual users. Let’s start with security.

## 1. I’ve Lost my Phone
The number 1 security concern with BYOD connecting to enterprise networks is loss or theft of those devices. Foreground Security, a consulting firm, reports that 47% of employees have no passcode for their mobile phones. Malicious individuals will have access to any enterprise data stored on the device and possibly even to data stored on enterprise servers.

IT departments need to put in place, and enforce, strong password policies for every mobile device. Further, you should also consider creating password access to apps or browser access points into SharePoint, auto-wiping content after a series of unsuccessful tries, and setting up the ability to remotely wipe content from the device.

## 2. Authentication
On the topic of remotely wiping content, controlling access to SharePoint content on mobile devices is key. To protect sensitive corporate information, enterprises need to implement more fine grained security mechanisms and access control policies within the centralized or cloud-based SharePoint systems. IT departments need to pay attention to authorization policies that know who is accessing information and what type of data they are accessing, as well as what time of day, from what location and over what type of connection.

To achieve this, there needs to be proper site governance of both the content and structure of the SharePoint site. Note that this goes both ways, so that content that is created and changed on mobile devices need to follow the same set of authorization policies as those on the SharePoint site.

The good news is that SharePoint, Microsoft Outlook and Windows file server provide integration with identity providers like Active Directory Federation Services to enforce fine grained policies on what types of information users are permitted to view and access, even to the point of the specific device the user is connecting with.

Also note, for compliance with some of the more rigorous standards like HIPAA and SOX, enterprises need to go beyond access controls and encryption. To comply with these rigorous standards they need to implement logging and auditing to provide a trail of where the content is and has been.

## 3. Containerization
At the recent Gartner Security and Risk Management Summit, analyst Eric Maiwald commented: “BYOD means my phone, my tablet, my pictures, my music – it’s all about the user.” We could add to that: my confidential documents, my customer lists, my company financials, my bids and my patent information, and we have the full picture.

Separating corporate and personal data can be a thorny problem. One solution is containerization and this topic deserves an article all on its own. For the purpose of this article, we’re just making a note of its advantage. There are many choices for technologies for separating out and managing corporate email, applications and data. Just beware in making your choice, though, you’ll often need to use the vendor’s API and SDK to link customized apps to the container.

## 4. Jailbroken Devices
It’s no joke when a jail-broken iOS device appears on your corporate network. These devices pose a serious security risk. Worst case scenario is that malware can be introduced to your network through the use of unauthorized apps, and many jailbroken iOS devices also install a secure shell server that remote attackers can exploit.

Many MDM solutions are able to detect jail-broken devices, but don’t rely on your container solution to do this on its own. According to Gartner analyst Eric Maiwald: “If you have a rooted device, a container will not protect you.” You’ll need a multi-layered approach to jail-breaking, starting with educating employees about the risks and implications of jail-breaking their devices.

## 5. Malicious Apps or Hackers
What if a malicious app or person tries to access corporate documents? It has to be about the security settings you ensure all employees set on their device. For iOS devices, for example, encrypting vital information and user’s SharePoint credentials with hardware encryption and then storing them in the device’s Keychain will protect sensitive data. You’ll also want to pay attention to rogue apps that use the iPad’s screen capture capabilities, detect any modifications made to the .plist files on the iPad and if content is backed up on iTunes.

## 6. Preventing Information from Being Shared Externally
Employees often need to share documents with customers and partners, and this does create security issues for IT departments. The biggest issue is when employees send a document as an attachment to an email. Once that happens you lose the thread of who is sharing the document with whom, and there is no knowing who the customer then may share it with.

One solution is to offer the option to email documents as links in SharePoint. This adds extra security as the recipient must have the required SharePoint credentials to access the link and you can set authorization policies around the retrieval of said document.

## 7. User Interface
On the flip side of enterprise-wide security, we have ease of use for the individual. It goes without saying that if users cannot access SharePoint on their mobile devices or if they cannot access SharePoint content the way they would like to with an easy to use interface, they will look to alternate solutions for collaborating with colleagues and customers.

Out of the box, SharePoint 2013 has paid attention to the mobile experience with four browser-based experiences and the HTML-5-based contemporary view option, as well as the ability to design your own view based on your organization’s usability requirements. Your ability to choose the experiences, though, depends on a number of factors, including the devices you have and the type of site you are trying to enable.

There are also a number of third party solutions that cater to a wide range of devices to ensure employees adopt SharePoint for their mobile experience. Just note, that the user experience is tantamount to the success of your deployment and it starts with the user interface.

## 8. Working with Documents Offline
Field workers, sales professionals, external auditors are just some examples of employees who spend a large portion of their working days away from the office. To work efficiently, they will need offline access to email content stored in SharePoint. You’ll need a solution that allows users to selectively cache their SharePoint content to give them instant access to remain productive on the road or in the field.

There you have it. My hit list of measures you need to consider for successfully deploying a BYOD strategy in SharePoint.