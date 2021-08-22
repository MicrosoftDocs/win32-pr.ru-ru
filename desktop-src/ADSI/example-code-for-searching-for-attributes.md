---
title: Пример кода для поиска атрибутов
description: В следующем примере кода показано, как использовать \_ \_ параметр поиска ADS сеарчпреф аттрибтипес \_ только для получения имен атрибутов, которым были назначены значения.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, пример кода C/C++, поиск атрибутов
- Пример кода для поиска атрибутов
- ADSI, поиск, IDirectorySearch, другие параметры поиска, возврат только имен атрибутов, пример кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207fcfd2bd688f5bb6ddcd19dcb9b1a87a2e40ddb0a7db1e63e9457e671f9947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428467"
---
# <a name="example-code-for-searching-for-attributes"></a>Пример кода для поиска атрибутов

В следующем примере кода показано, как использовать параметр поиска **ADS \_ сеарчпреф \_ аттрибтипес \_ только** для получения имен атрибутов, которым были назначены значения. В примере инициализируется информационная структура [**ADS \_ сеарчпреф \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) и задается предпочтение поиска путем вызова метода [**сетсеарчпреференце**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) интерфейса [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Затем в примере вызывается метод [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) для выполнения поиска.


```C++
// Setting the search preference.
// m_pSearch is a valid pointer to an IDirectorySearch interface.
ADS_SEARCHPREF_INFO prefInfo[1];
LPWSTR pszColumn = NULL;

// Set the search preference to indicate attribute names only.
prefInfo[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
prefInfo[0].vValue.dwType = ADSTYPE_BOOLEAN;
prefInfo[0].vValue.Integer = TRUE;
hr = m_pSearch->SetSearchPreference(prefInfo, 1);

// Execute the search.
hr = m_pSearch->ExecuteSearch(
                L"(|(objectCategory=domainDNS)(objectCategory=organizationalUnit))", 
                NULL, -1, &hSearch );

if(FAILED(hr))
{
   return;
}

// Retrieve the column name.
hr = m_pSearch->GetNextRow(hSearch);

if(FAILED(hr))
{
   return;
}
    
while( m_pSearch->GetNextColumnName( hSearch, &pszColumn ) != S_ADS_NOMORE_COLUMNS )
{
   wprintf(L"%S ", pszColumn );
   FreeADsMem( pszColumn );
}
```



 

 




