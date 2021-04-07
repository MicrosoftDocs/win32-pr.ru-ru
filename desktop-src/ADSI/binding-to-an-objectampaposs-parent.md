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
# <a name="binding-to-an-objects-parent"></a>Привязка к родительскому объекту

В ADSI каждый объект каталога представлен COM-объектом ADSI, предоставляющим интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) . Чтобы получить родительский контейнер объекта, используйте метод [**iAds:: Get \_ Parent**](iads-property-methods.md) , чтобы получить путь к родительскому объекту, а затем выполните привязку к ADsPath родительского объекта.

В следующем примере кода C++ показано, как получить родительский объект для объекта.


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



 

 




