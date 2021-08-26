---
description: Отмена регистрации фильтра
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Отмена регистрации фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e26f2d524ff501fcff1db645c9ccdf1a1c9c80c4056af1af206b996f801207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049684"
---
# <a name="unregistering-a-filter"></a>Отмена регистрации фильтра

Чтобы отменить регистрацию фильтра, реализуйте функцию **DllUnregisterServer** . в этой функции вызовите функцию DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) с значением **FALSE**. Если вы вызвали **IFilterMapper2:: регистерфилтер** при регистрации фильтра, вызовите метод [**IFilterMapper2:: унрегистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) здесь.

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



 

 



