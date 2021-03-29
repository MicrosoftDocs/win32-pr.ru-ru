---
title: Проверка синтаксиса фильтра запросов
description: API LDAP предоставляет простую функцию проверки синтаксиса. Имейте в виду, что он проверяет только синтаксис, а не существование свойств, указанных в фильтре.
ms.assetid: 4e564cd9-2f8b-4e70-928c-3a8bd804aeba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da2c15052309bc2acbcff9d6bdabea95337db1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067273"
---
# <a name="checking-the-query-filter-syntax"></a>Проверка синтаксиса фильтра запросов

API LDAP предоставляет простую функцию проверки синтаксиса. Имейте в виду, что он проверяет только синтаксис, а не существование свойств, указанных в фильтре.

Следующая функция проверяет синтаксис фильтра запросов и возвращает команду **s \_ ОК** , если фильтр является допустимым, или значение false в противном \_ случае.


```C++
HRESULT CheckFilterSyntax(
    LPOLESTR szServer, // NULL binds to a DC in the current domain.
    LPOLESTR szFilter) // Filter to check.
{
HRESULT hr = S_OK;
DWORD dwReturn;
LDAP *hConnect = NULL;  // Connection handle
 
if (!szFilter)
  return E_POINTER;
 
// LDAP_PORT is the default port, 389
 
hConnect  = ldap_open(szServer,  LDAP_PORT);
 
// Bind using the preferred authentication method on Windows 2000
// and the calling thread's security context.
 
dwReturn = ldap_bind_s( hConnect, NULL, NULL, LDAP_AUTH_NEGOTIATE );
if (dwReturn==LDAP_SUCCESS) {
    dwReturn = ldap_check_filter(hConnect, szFilter);
    if (dwReturn==LDAP_SUCCESS)
        hr = S_OK;
    else
        hr = S_FALSE;
}
 
// Unbind to free the connection.
 
ldap_unbind( hConnect );
 
return hr;
}
```



 

 




