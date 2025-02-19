---
title: How long does Azure AD store reporting data? | Microsoft Docs
description: Learn how long Azure stores the various types of reporting data. 
services: active-directory
documentationcenter: ''
author: MarkusVi
manager: karenhoran
editor: ''

ms.assetid: 183e53b0-0647-42e7-8abe-3e9ff424de12
ms.service: active-directory
ms.devlang: 
ms.topic: reference
ms.tgt_pltfrm: 
ms.workload: identity
ms.subservice: report-monitor
ms.date: 11/05/2020
ms.author: markvi
ms.reviewer: dhanyahk

ms.collection: M365-identity-device-management
---
# How long does Azure AD store reporting data?


In this article, you learn about the data retention policies for the different activity reports in Azure Active Directory. 

### When does Azure AD start collecting data?

| Azure AD Edition | Collection Start |
| :--              | :--   |
| Azure AD Premium P1 <br /> Azure AD Premium P2 | When you sign up for a subscription |
| Azure AD Free| The first time you open the [Azure Active Directory blade](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview) or use the [reporting APIs](./overview-reports.md)  |

---

### When is the activity data available in the Azure portal?

- **Immediately** - If you have already been working with reports in the Azure portal.
- **Within 2 hours** - If you haven’t turned on reporting in the Azure portal.

---

### How soon can I see activities data after getting a premium license?

If you already have activities data with your free license, then you can see it immediately on upgrade. If you don’t have any data, then it will take up to three days for the data to show up in the reports after you upgrade to a premium license.

---

### When does Azure AD start collecting security signal data?  

For security signals, the collection process starts when you opt-in to use the **Identity Protection Center**. 

---

### How long does Azure AD store the data?

**Activity reports**	

| Report                 | Azure AD Free | Azure AD Premium P1 | Azure AD Premium P2 |
| :--                    | :--           | :--                 | :--                 |
| Audit logs             | Seven days        | 30 days             | 30 days             |
| Sign-ins               | Seven days        | 30 days             | 30 days             |
| Azure AD MFA usage        | 30 days       | 30 days             | 30 days             |

You can retain the audit and sign-in activity data for longer than the default retention period outlined above by routing it to an Azure storage account using Azure Monitor. For more information, see [Archive Azure AD logs to an Azure storage account](quickstart-azure-monitor-route-logs-to-storage-account.md).

**Security signals**

| Report         | Azure AD Free | Azure AD Premium P1 | Azure AD Premium P2 |
| :--            | :--           | :--                 | :--                 |
| Risky users    | No limit      | No limit            | No limit            |
| Risky sign-ins | 7 days        | 30 days             | 90 days             |

> [!NOTE]
> Risky users are not deleted until the risk has been remediated.

---

### Can I see last month's data after getting an Azure AD premium license?

**No**, you can't. Azure stores up to seven days of activity data for a free version. This means, when you switch from a free to a to a premium version, you can only see up to 7 days of data.

---
