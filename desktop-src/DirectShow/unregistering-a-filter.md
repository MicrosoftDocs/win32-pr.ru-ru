---
description: Отмена регистрации фильтра
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Отмена регистрации фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d161b7d1f169b84ba43ac734bf01708a37eb700a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911083"
---
# <a name="unregistering-a-filter"></a>Отмена регистрации фильтра

Чтобы отменить регистрацию фильтра, реализуйте функцию **DllUnregisterServer** . В этой функции вызовите функцию DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) со значением **false**. Если вы вызвали **IFilterMapper2:: регистерфилтер** при регистрации фильтра, вызовите метод [**IFilterMapper2:: унрегистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) здесь.

В следующем примере показано, как отменить регистрацию фильтра.


```C++
STDAPI DllUnregisterServer()
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
        return hr;
 
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_SomeFilter);

    pFM2->Release();
    return hr;
}
```



 

 



