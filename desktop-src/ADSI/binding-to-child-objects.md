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
# <a name="binding-to-child-objects"></a>Привязка к дочерним объектам

В ADSI объект контейнера предоставляет интерфейс [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . Метод [**иадсконтаинер:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) используется для непосредственной привязки к дочернему объекту. Объект, возвращаемый функцией **иадсконтаинер:: GetObject** , имеет тот же контекст безопасности, что и объект, для которого был вызван метод. Это означает, что если используются альтернативные учетные данные, альтернативные учетные данные не обязательно передаются в функцию привязки или метод для сохранения одних и тех же учетных данных.

Метод [**иадсконтаинер:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) принимает относительное различающееся имя (RDN) относительно текущего объекта. Этот метод также принимает необязательное имя класса и возвращает указатель интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , представляющий дочерний объект. Чтобы получить необходимый интерфейс ADSI, например [**iAds**](/windows/desktop/api/Iads/nn-iads-iads), вызовите метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) этого указателя интерфейса **IDispatch** .

В следующем примере кода C++ показана функция, извлекающая указанный дочерний объект.


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



 

 