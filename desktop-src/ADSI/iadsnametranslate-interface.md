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
# <a name="iadsnametranslate-interface"></a><span data-ttu-id="ee42d-107">Интерфейс Иадснаметранслате</span><span class="sxs-lookup"><span data-stu-id="ee42d-107">IADsNameTranslate Interface</span></span>

<span data-ttu-id="ee42d-108">Интерфейс [**иадснаметранслате**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) используется для преобразования различающихся имен между различными форматами.</span><span class="sxs-lookup"><span data-stu-id="ee42d-108">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface is used to translate distinguished names between various formats.</span></span> <span data-ttu-id="ee42d-109">Преобразования имен выполняются на сервере каталогов, и этот интерфейс в настоящее время доступен только для объектов в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ee42d-109">Name translations are performed on the directory server, and this interface is currently available only to objects in Active Directory.</span></span>

<span data-ttu-id="ee42d-110">В следующем примере кода имя учетной записи преобразуется из формата Windows в формат LDAP.</span><span class="sxs-lookup"><span data-stu-id="ee42d-110">The following code example converts an account name from Windows format into LDAP format.</span></span>


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



 

 




