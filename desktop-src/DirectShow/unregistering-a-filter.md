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
# <a name="unregistering-a-filter"></a><span data-ttu-id="e94bc-103">Отмена регистрации фильтра</span><span class="sxs-lookup"><span data-stu-id="e94bc-103">Unregistering a Filter</span></span>

<span data-ttu-id="e94bc-104">Чтобы отменить регистрацию фильтра, реализуйте функцию **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="e94bc-104">To unregister a filter, implement the **DllUnregisterServer** function.</span></span> <span data-ttu-id="e94bc-105">В этой функции вызовите функцию DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) со значением **false**.</span><span class="sxs-lookup"><span data-stu-id="e94bc-105">Within this function, call the DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function with a value of **FALSE**.</span></span> <span data-ttu-id="e94bc-106">Если вы вызвали **IFilterMapper2:: регистерфилтер** при регистрации фильтра, вызовите метод [**IFilterMapper2:: унрегистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) здесь.</span><span class="sxs-lookup"><span data-stu-id="e94bc-106">If you called **IFilterMapper2::RegisterFilter** when you registered the filter, call the [**IFilterMapper2::UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) method here.</span></span>

<span data-ttu-id="e94bc-107">В следующем примере показано, как отменить регистрацию фильтра.</span><span class="sxs-lookup"><span data-stu-id="e94bc-107">The following example shows how to unregister a filter:</span></span>


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



 

 



