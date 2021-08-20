---
title: Проверка работы на контроллере домена
description: в следующем коде функция верифиверсионинфо используется для определения того, выполняется ли вызывающий процесс на контроллере домена Windows 2000.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb49577994716598bb730fcc7e86a9cce76a2835e8cfa1558b7d608b9cbc5ea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024592"
---
# <a name="testing-whether-running-on-a-domain-controller"></a>Проверка работы на контроллере домена

в следующем коде функция [**верифиверсионинфо**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) используется для определения того, выполняется ли вызывающий процесс на контроллере домена Windows 2000. Программа установки службы может использовать этот тест перед установкой службы под учетной записью LocalSystem. Если тест указывает на то, что вы работаете на контроллере домена, необходимо либо установить службу для запуска от имени учетной записи пользователя, либо попытаться отобразить диалоговое окно с предупреждением о рисках, которые выполняются в качестве LocalSystem на контроллере домена (то есть служба будет иметь неограниченный доступ к службам домен Active Directory, крайне мощный контекст безопасности, который может повредить всю сеть).


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



 

 