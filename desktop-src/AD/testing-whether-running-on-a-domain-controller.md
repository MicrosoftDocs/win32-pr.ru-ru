---
title: Проверка работы на контроллере домена
description: В следующем коде функция Верифиверсионинфо используется для определения того, выполняется ли вызывающий процесс на контроллере домена сервера Windows 2000.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8aeb73af18be9f0c787c2ee30b150689d760aec
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133646"
---
# <a name="testing-whether-running-on-a-domain-controller"></a><span data-ttu-id="75e56-103">Проверка работы на контроллере домена</span><span class="sxs-lookup"><span data-stu-id="75e56-103">Testing Whether Running on a Domain Controller</span></span>

<span data-ttu-id="75e56-104">В следующем коде функция [**верифиверсионинфо**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) используется для определения того, выполняется ли вызывающий процесс на контроллере домена сервера Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="75e56-104">The following code uses the [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) function to determine whether the calling process is running on a Windows 2000 Server domain controller.</span></span> <span data-ttu-id="75e56-105">Программа установки службы может использовать этот тест перед установкой службы под учетной записью LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="75e56-105">Your service installation program could use this test before installing a service under the LocalSystem account.</span></span> <span data-ttu-id="75e56-106">Если тест указывает на то, что вы работаете на контроллере домена, необходимо либо установить службу для запуска от имени учетной записи пользователя, либо попытаться отобразить диалоговое окно с предупреждением о рисках, которые выполняются в качестве LocalSystem на контроллере домена (то есть служба будет иметь неограниченный доступ к службам домен Active Directory, крайне мощный контекст безопасности, который может повредить всю сеть).</span><span class="sxs-lookup"><span data-stu-id="75e56-106">If the test indicates that you are running on a domain controller, you either install the service to run under a user account, or display a dialog box warning of the dangers in running as LocalSystem on a domain controller (which are that the service would then have unrestricted access to Active Directory Domain Services, a supremely powerful security context that has the potential to damage the entire network).</span></span>


```C++
BOOL Is_Win2000_DomainController () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
 
   // Initialize the OSVERSIONINFOEX structure.
   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.wProductType = VER_NT_DOMAIN_CONTROLLER;
 
   // Initialize the condition mask.
   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, 
      VER_GREATER_EQUAL );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, 
      VER_EQUAL );
 
   // Perform the test.
   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_PRODUCT_TYPE,
      dwlConditionMask);
}
```



 

 