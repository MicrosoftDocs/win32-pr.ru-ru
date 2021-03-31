---
title: Рекомендации по выбору учетной записи входа в службу
description: Служба на основе Win32 может выполняться в контексте безопасности локальной учетной записи пользователя, учетной записи пользователя домена или учетной записи LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Рекомендации по выбору учетной записи входа в службу AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067370"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a><span data-ttu-id="2b99d-104">Рекомендации по выбору учетной записи входа в службу</span><span class="sxs-lookup"><span data-stu-id="2b99d-104">Guidelines for Selecting a Service Logon Account</span></span>

<span data-ttu-id="2b99d-105">Служба на основе Win32 может выполняться в контексте безопасности локальной учетной записи пользователя, учетной записи пользователя домена или учетной записи LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="2b99d-105">A Win32-based service can run in the security context of a local user account, a domain user account, or the LocalSystem account.</span></span> <span data-ttu-id="2b99d-106">Чтобы решить, какую учетную запись следует использовать, администратор должен установить службу с минимальным набором разрешений, необходимых для выполнения операций службы.</span><span class="sxs-lookup"><span data-stu-id="2b99d-106">To decide which account to use, an administrator should install the service with the minimum set of permissions required to perform the service operations.</span></span> <span data-ttu-id="2b99d-107">В стандартной службе с поддержкой каталогов это означает, что установщик службы должен создать учетную запись пользователя домена для службы и предоставить этой учетной записи определенные права доступа и привилегии, необходимые службе во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2b99d-107">In a typical directory-enabled service, this means the service installer should create a domain user account for the service and grant that account the specific access rights and privileges required by the service at run time.</span></span> <span data-ttu-id="2b99d-108">Служба должна выполняться только под учетной записью LocalSystem, если службе требуются права администратора или она должна работать как часть операционной системы на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2b99d-108">A service should only run under the LocalSystem account if the service requires administrative privileges or must act as part of the operating system on the local computer.</span></span>

<span data-ttu-id="2b99d-109">Имейте в виду, что установщик службы по умолчанию должен настроить службу для запуска от имени учетной записи пользователя домена.</span><span class="sxs-lookup"><span data-stu-id="2b99d-109">Be aware that the service installer should, by default, set up the service to run under a domain user account.</span></span> <span data-ttu-id="2b99d-110">Чтобы запустить службу под учетной записью LocalSystem, установщик службы должен запросить у администратора разрешение на это.</span><span class="sxs-lookup"><span data-stu-id="2b99d-110">To run the service under the LocalSystem account, the service installer should query the administrator for permission to do so.</span></span>

<span data-ttu-id="2b99d-111">Дополнительные сведения о описаниях, преимуществах и недостатках каждого типа учетной записи см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2b99d-111">For more information about descriptions, advantages, and disadvantages of each account type, see:</span></span>

-   <span data-ttu-id="2b99d-112">[Локальные учетные записи пользователей](local-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="2b99d-112">[Local User Accounts](local-user-accounts.md).</span></span>
-   <span data-ttu-id="2b99d-113">[Учетные записи пользователей домена](domain-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="2b99d-113">[Domain User Accounts](domain-user-accounts.md).</span></span>
-   <span data-ttu-id="2b99d-114">[Учетная запись LocalSystem](the-localsystem-account.md).</span><span class="sxs-lookup"><span data-stu-id="2b99d-114">[The LocalSystem Account](the-localsystem-account.md).</span></span>

 

 




