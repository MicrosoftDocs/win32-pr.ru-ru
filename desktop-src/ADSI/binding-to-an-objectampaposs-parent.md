---
title: Привязка к родительскому объекту
description: В ADSI каждый объект каталога представлен COM-объектом ADSI, предоставляющим интерфейс IADs.
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, использование, привязка к родителю объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d72f3b3db3af9f13892494d3855dc5dcb2a74d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887584"
---
# <a name="binding-to-an-objects-parent"></a><span data-ttu-id="ae418-104">Привязка к родительскому объекту</span><span class="sxs-lookup"><span data-stu-id="ae418-104">Binding to an Object's Parent</span></span>

<span data-ttu-id="ae418-105">В ADSI каждый объект каталога представлен COM-объектом ADSI, предоставляющим интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="ae418-105">In ADSI, every directory object is represented by an ADSI COM object that exposes the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="ae418-106">Чтобы получить родительский контейнер объекта, используйте метод [**iAds:: Get \_ Parent**](iads-property-methods.md) , чтобы получить путь к родительскому объекту, а затем выполните привязку к ADsPath родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="ae418-106">To obtain the parent container of an object, use the [**IADs::get\_Parent**](iads-property-methods.md) method to obtain the ADsPath of the parent object, then bind to the ADsPath of the parent.</span></span>

<span data-ttu-id="ae418-107">В следующем примере кода C++ показано, как получить родительский объект для объекта.</span><span class="sxs-lookup"><span data-stu-id="ae418-107">The following C++ code example shows how to obtain the parent of an object .</span></span>


```C++
HRESULT GetParentObject(IADs *pObject,   // Pointer to the object whose parent to bind to.
                        IADs **ppParent) // Return a pointer to the parent object.
{
    if(NULL == ppParent)
    {
        return E_INVALIDARG;
    }
 
    *ppParent = NULL;

    if(NULL == pObject)
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    BSTR bstr;

    // Get the ADsPath of the parent.
    hr = pObject->get_Parent(&bstr);
    if(SUCCEEDED(hr))
    {
        // Bind to the parent.
        hr = ADsOpenObject(bstr,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)ppParent);

        SysFreeString(bstr);
    }

    return hr;
}
```



 

 




