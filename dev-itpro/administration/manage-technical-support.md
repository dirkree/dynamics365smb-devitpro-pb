---
title: Managing technical support
description: Learn about how to support your Business Central customers, online and on-premises.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 11/25/2019
ms.author: edupont

---

# Managing Technical Support

If users report that they are having a problem with [!INCLUDE [prodshort](../developer/includes/prodshort.md)], superusers and the internal administrator can often find a solution. The internal administrator can find technical information in the **Help and Support** page as described in the following sections, and they can then escalate relevant issues to the reselling partner.  

The reselling partner can log in to their customer's [!INCLUDE [prodshort](../developer/includes/prodshort.md)] as the delegated admin for troubleshooting. Both internal administrators and the reselling partner can use the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)] to manage environments and upgrades.  

## Finding technical information

The **Help and Support** page is a powerful tool for internal administrators to find technical information about your customers' [!INCLUDE [prodshort](../developer/includes/prodshort.md)], both online and on-premises. The **Troubleshooting** section gives easy access to the most recent error message, and it has a link to inspect pages for further troubleshooting.  

> [!div class="mx-imgBorder"]
> ![Links for troubleshooting and support from the Help and Support page](../developer/media/admin/helpsupport_managed.png)

Also in the **Help and Support** page, users can see support contact information, provided that this has been set up. For more information, see [To supply your support contact information in the administration center](../technical-support.md#to-supply-your-support-contact-information-in-the-administration-center). The **Help and Support** page also shows which version of [!INCLUDE [prodshort](../developer/includes/prodshort.md)], the tenant is on.  

As an administrator, you also have access to this information in the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)]. You can use the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)] to easily navigate to your customers' tenants, and you can create sandbox environments that can help troubleshoot any issues reported by your customers. For more information, see [The Business Central Administration Center](tenant-admin-center.md).  

### Azure Active Directory tenant

If you have configured the support email address, and your customer uses that to contact you, then the **Help and Support** page encourages them to include information about their Azure Active Directory tenant ID in the email. This information is shown at the bottom of the **Help and Support** page. You can use that to identify the tenant in the administration center, and you can use it to log into their tenant for troubleshooting, for example.  

You also have access to this information in the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)].  

### Version

You can use the information about which version the tenant is on to help you troubleshoot the issue that the customer has reported, for example. This information is also listed in the **Troubleshooting** section of the **Help and Support** page. For more information, see [Version numbers in Business Central](version-numbers.md).  

### Last known error

The link behind the sentence *View the last known error* will find and show the most recent error message that was was generated by the application code. This includes errors from field validation, posting routines, and other code behind business functionality.  

The information that you can get from this link includes the following:

- Text

    This is the error message that the user sees, either in a dialog window or next to a user interface element that cannot render, for example.
- Code

    This is the code snippet that threw the error.
- Callstack

    This shows how the error was triggered.
- Object

    This shows information about the runtime objects.

The link cannot open errors that were generated by the platform. So if you suspect that the issue is caused by the platform, you can try to reproduce the error in a sandbox environment before you contact Microsoft for support. For more information, see [Create a sandbox environment](tenant-admin-center-environments.md#create-a-sandbox-environment).

## Escalating your customer's support issues

Sometimes the tenant has run into a problem that you cannot resolve. In those cases, the reselling partner can use the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)] to easily submit a support request to Microsoft.  

You can submit support requests from the Partner Center or from the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)].

### Submitting support requests on behalf of your customer

If you are logged into the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)], you can use the **New Support Request** link in the Help menu to submit a support request on behalf of your customer. This opens a new browser tab so that you can submit the support request in the Power Platform Admin Center.  

> [!IMPORTANT]
> Your company must be registered as a partner in order to submit a support request, and you must have the ASfP (Advanced Support for Partners) support plan. The support person can be a member of the Helpdesk Agent group in the customer's Azure AD tenant or a global administrator. For more information, see [Delegated admin privileges in Azure AD](/partner-center/customers_revoke_admin_privileges#delegated-admin-privileges-in-azure-ad). Your service account manager can get you more information about getting the ASfP, and if you already have a support plan, they can get the contract information and access ID that you must specify when you submit a new support request on behalf of your customer.  

In the Power Platform Admin Center, you are automatically logged in with information about the customer tenant that you are working on behalf of. Create a new support request and fill in the fields as appropriate. You can find most of the necessary information in the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)], including the tenant ID and the [!INCLUDE [prodshort](../developer/includes/prodshort.md)] version numbers.  

For more information, see [Power Platform Admin Center](/power-platform/admin/admin-documentation).

<!-- TODO: How to manage your customers' support issues -->

## Report customer outages

When a customer has a situation where no users can log in to [!INCLUDE [prodshort](../developer/includes/prodshort.md)], you must take immediate action. You can report this outage to Microsoft by using the **Report Production Outage** action for the relevant production environment in the [!INCLUDE [prodadmincenter](../developer/includes/prodadmincenter.md)]. This action creates a support ticket for Microsoft with all the information that is needed to begin steps to resolve the issue.  

> [!NOTE]
> This option is not available in sandbox environments.  

> [!IMPORTANT]
> You must be registered as a partner in order to report an outage.

To report an outage:

1. On the **Environments** tab of the [!INCLUDE[prodadmincenter](../developer/includes/prodadmincenter.md)], choose the relevant environment to open the environment details.
2. In the action ribbon, choose **Report Production Outage**.
3. In the **Report Production Outage** pane, choose the outage type:

    - Unable to log on (all users)
    - Cannot access API/Web Service

4. Enter your name, email address, and phone number. This information will be included in the support ticket.  
5. Choose **Next**.
6. In the next pane, provide details about the outage, including which browsers users have tried to log in with, any companies that you can log into, and errors and correlation IDs. This information will be included in the support ticket.  
7. Finally, add the date and time when the outage began. This information will also flow to the support ticket.  
8. Choose the consent checkbox, and then choose **Report**.

A support request ticket is then created, and you will see a dialog box with the ticket ID. You can then monitor progress in the **Reported Outages** section. From there, you can access the tickets in the Partner Center. For more information, see the [Microsoft Partner Center](/partner-center/) documentation.  

## See Also

[Inspecting and Troubleshooting Pages](../developer/devenv-inspecting-pages.md)  
[The Business Central Administration Center](tenant-admin-center.md)  
[Technical Support for Business Central](../technical-support.md)  
[Provide technical support (Microsoft Partner Center)](/partner-center/provide-technical-support)  
[Deployment Overview](../deployment/Deployment.md)  
[Administration of Business Central Online](tenant-administration.md)  
[Administration of Business Central On-Premises](Administration.md)  
