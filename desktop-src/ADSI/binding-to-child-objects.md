---
title: Привязка к дочерним объектам
description: В ADSI объект контейнера предоставляет интерфейс Иадсконтаинер.
ms.assetid: 16b913ea-06a4-4e85-ad6c-68817883bbd8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, использование, привязка к дочерним объектам
- Привязка к дочерним объектам
- Дочерние объекты, привязка к
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a73d7682dedb405c84dfaf048b8b4b2659e7fd3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488268"
---
# <a name="binding-to-child-objects"></a><span data-ttu-id="e24bd-106">Привязка к дочерним объектам</span><span class="sxs-lookup"><span data-stu-id="e24bd-106">Binding to Child Objects</span></span>

<span data-ttu-id="e24bd-107">В ADSI объект контейнера предоставляет интерфейс [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="e24bd-107">In ADSI, a container object exposes the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span> <span data-ttu-id="e24bd-108">Метод [**иадсконтаинер:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) используется для непосредственной привязки к дочернему объекту.</span><span class="sxs-lookup"><span data-stu-id="e24bd-108">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method is used to bind directly to a child object.</span></span> <span data-ttu-id="e24bd-109">Объект, возвращаемый функцией **иадсконтаинер:: GetObject** , имеет тот же контекст безопасности, что и объект, для которого был вызван метод.</span><span class="sxs-lookup"><span data-stu-id="e24bd-109">The object returned by **IADsContainer::GetObject** has the same security context as the object on which the method was called.</span></span> <span data-ttu-id="e24bd-110">Это означает, что если используются альтернативные учетные данные, альтернативные учетные данные не обязательно передаются в функцию привязки или метод для сохранения одних и тех же учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e24bd-110">This means that if alternate credentials are used, the alternate credentials do not have to be passed to the binding function or method again to maintain the same credentials.</span></span>

<span data-ttu-id="e24bd-111">Метод [**иадсконтаинер:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) принимает относительное различающееся имя (RDN) относительно текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="e24bd-111">The [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method takes a relative distinguished name (RDN) that is relative to the current object.</span></span> <span data-ttu-id="e24bd-112">Этот метод также принимает необязательное имя класса и возвращает указатель интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , представляющий дочерний объект.</span><span class="sxs-lookup"><span data-stu-id="e24bd-112">This method also takes an optional class name and returns an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface pointer that represents the child object.</span></span> <span data-ttu-id="e24bd-113">Чтобы получить необходимый интерфейс ADSI, например [**iAds**](/windows/desktop/api/Iads/nn-iads-iads), вызовите метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) этого указателя интерфейса **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="e24bd-113">To obtain the desired ADSI interface, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of this **IDispatch** interface pointer.</span></span>

<span data-ttu-id="e24bd-114">В следующем примере кода C++ показана функция, извлекающая указанный дочерний объект.</span><span class="sxs-lookup"><span data-stu-id="e24bd-114">The following C++ code example shows a function that retrieves a specified child object.</span></span>


```C++
HRESULT GetChildObject(IADs *pObject, 
                       LPCWSTR pwszClass, 
                       LPCWSTR pwszRDN, 
                       IADs **ppChild)
{
    if(NULL == ppChild)
    {
        return E_INVALIDARG;
    }

    *ppChild = NULL;
    
    if((NULL == pObject) || (NULL == pwszRDN))
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADsContainer *pCont;

    hr = pObject->QueryInterface(IID_IADsContainer, (LPVOID*)&pCont);
    if(SUCCEEDED(hr))
    {
        BSTR bstrClass = NULL;
        if(pwszClass)
        {
            bstrClass = SysAllocString(pwszClass);
        }

        BSTR bstrRDN = SysAllocString(pwszRDN);
        if(bstrRDN)
        {
            IDispatch *pDisp;
            
            hr = pCont->GetObject(bstrClass, bstrRDN, &pDisp);
            if(SUCCEEDED(hr))
            {
                hr = pDisp->QueryInterface(IID_IADs, (LPVOID*)ppChild);
                
                pDisp->Release();
            }

        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        if(bstrRDN)
        {
            SysFreeString(bstrRDN);
        }

        if(bstrClass)
        {
            SysFreeString(bstrClass);
        }


        pCont->Release();
    }
    
    return hr;
}
```



 

 