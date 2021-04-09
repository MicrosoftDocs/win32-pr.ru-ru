---
title: Интерфейс Иадснаметранслате
description: Интерфейс Иадснаметранслате используется для преобразования различающихся имен между различными форматами. Преобразования имен выполняются на сервере каталогов, и этот интерфейс в настоящее время доступен только для объектов в Active Directory.
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI интерфейса Иадснаметранслате
- Иадстранслате ADSI, использование
- ADSI ADSI, пример кода C/C++, использование Иадстранслате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ff5b44288289f118c41463a22e619aa815ecb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887532"
---
# <a name="iadsnametranslate-interface"></a>Интерфейс Иадснаметранслате

Интерфейс [**иадснаметранслате**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) используется для преобразования различающихся имен между различными форматами. Преобразования имен выполняются на сервере каталогов, и этот интерфейс в настоящее время доступен только для объектов в Active Directory.

В следующем примере кода имя учетной записи преобразуется из формата Windows в формат LDAP.


```C++
HRESULT TranslateNTNameToLDAPName( BSTR * pNTName, BSTR * pLDAPName )
{
    IADsNameTranslate *pTrans;
    HRESULT hr = S_OK;
 
    hr = CoCreateInstance(CLSID_NameTranslate, 
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsNameTranslate,
                          (void**) &pTrans );
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Init(ADS_NAME_INITTYPE_DOMAIN, 
                      CComBSTR("Fabrikam.com"));
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Set(ADS_NAME_TYPE_NT4, *pNTName);
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Get(ADS_NAME_TYPE_1779, pLDAPName);
    pTrans->Release();
    return hr;
}
```



 

 




