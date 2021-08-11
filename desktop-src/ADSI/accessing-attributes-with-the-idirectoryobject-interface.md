---
title: Доступ к атрибутам с помощью интерфейса Идиректорйобжект
description: Интерфейс Идиректорйобжект предоставляет клиентское приложение, написанное на C и C++ с прямым доступом к объектам службы каталогов.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Доступ к атрибутам с помощью интерфейса Идиректорйобжект ADSI
- Идиректорйобжект ADSI, доступ к атрибутам с помощью
- ADSI ADSI, использование, использование интерфейса Идиректорйобжект для доступа к атрибутам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fb7f2b8302c2e92a7e604bdc85389fb78acb24a59e467ca42b8bbd3c6c004e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181543"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a>Доступ к атрибутам с помощью интерфейса Идиректорйобжект

Интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) предоставляет клиентское приложение, написанное на C и C++ с прямым доступом к объектам службы каталогов. Интерфейс обеспечивает доступ посредством прямого сетевого протокола, а не через кэш атрибутов ADSI. Вместо свойств, поддерживаемых интерфейсом [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) , **идиректорйобжект** предоставляет методы, которые поддерживают критическое подмножество методов обслуживания объекта и предоставляют доступ к его атрибутам. С помощью **идиректорйобжект** клиент может получить или задать любое количество атрибутов объекта с помощью одного вызова метода. В отличие от соответствующих методов автоматизации, которые являются пакетными, эти **идиректорйобжект** выполняются при вызове метода. Поскольку методы этого интерфейса не нуждаются в создании экземпляра объекта каталога службы автоматизации, затраты на производительность невелики.

Клиенты, написанные на языках C и C++, должны использовать методы интерфейса [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) для оптимизации производительности и использования преимуществ собственных интерфейсов службы каталогов. Клиенты автоматизации не могут использовать **идиректорйобжект**. Вместо этого они должны использовать интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .

Метод [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) извлекает атрибуты с одним и несколькими значениями. Этот метод принимает список запрошенных атрибутов и возвращает структуру [**\_ \_ сведений о attr в ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) . ADSI выделяет эту структуру; вызывающая сторона должна освободить эту память, если она больше не нужна с помощью функции [**фриадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

Порядок возвращаемых значений атрибутов не обязательно совпадает с порядком, в котором были запрошены атрибуты. Поэтому необходимо сравнить имена атрибутов, возвращенные из ADSI.

> [!Note]  
> Структура [**\_ \_ сведений attr для ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) не возвращает все запрошенные атрибуты. Только те атрибуты, которые содержат значения, являются частью возвращенной структуры.

 

Число возвращаемых атрибутов определяется параметром *двнумбераттрибутес* , передаваемым методу [**Идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .

В следующем примере кода выполняется привязка к объекту и используется метод [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) для получения атрибутов объекта.


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




