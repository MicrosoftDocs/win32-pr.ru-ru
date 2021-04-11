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
# <a name="testing-whether-running-on-a-domain-controller"></a>Проверка работы на контроллере домена

В следующем коде функция [**верифиверсионинфо**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) используется для определения того, выполняется ли вызывающий процесс на контроллере домена сервера Windows 2000. Программа установки службы может использовать этот тест перед установкой службы под учетной записью LocalSystem. Если тест указывает на то, что вы работаете на контроллере домена, необходимо либо установить службу для запуска от имени учетной записи пользователя, либо попытаться отобразить диалоговое окно с предупреждением о рисках, которые выполняются в качестве LocalSystem на контроллере домена (то есть служба будет иметь неограниченный доступ к службам домен Active Directory, крайне мощный контекст безопасности, который может повредить всю сеть).


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



 

 