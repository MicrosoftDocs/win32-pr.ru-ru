---
title: Интерфейс Иадспаснаме
description: Анализирует и изменяет различные элементы ADsPath.
ms.assetid: 1f820488-2e75-4257-90c7-9ec67aac4fe4
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI интерфейса Иадспаснаме
- Иадспаснаме ADSI, использование
- ADSI ADSI, пример кода C/C++, использование Иадспаснаме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5cbc5901c8f9dcebebde485decc49fc5bcf312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887528"
---
# <a name="iadspathname-interface"></a><span data-ttu-id="6cc51-106">Интерфейс Иадспаснаме</span><span class="sxs-lookup"><span data-stu-id="6cc51-106">IADsPathname Interface</span></span>

<span data-ttu-id="6cc51-107">Интерфейс [**иадспаснаме**](/windows/desktop/api/Iads/nn-iads-iadspathname) анализирует и изменяет различные элементы ADsPath.</span><span class="sxs-lookup"><span data-stu-id="6cc51-107">The [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface parses and modifies various elements of an ADsPath.</span></span> <span data-ttu-id="6cc51-108">Он также преобразует Адспасс между различными форматами вывода.</span><span class="sxs-lookup"><span data-stu-id="6cc51-108">It also converts ADsPaths between various display formats.</span></span>

<span data-ttu-id="6cc51-109">В следующем примере кода извлекается и возвращается имя сервера из допустимого ADsPath для вывода пользователю в служебной программе обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6cc51-109">The following code example extracts and returns the server name from a valid ADsPath for display to the user in a maintenance utility.</span></span>


```C++
HRESULT GetServerName(BSTR adsPath, BSTR *adsServer)
{
    HRESULT hr = S_OK;
    IADsPathname *pIADsPathname = NULL;
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
 
    // Set the path.
    hr = pIADsPathname->Set(adsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
        // Extract and return the server name.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_SERVER, adsServer);
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
}
```



<span data-ttu-id="6cc51-110">Следующий пример кода помогает инициализировать вновь созданный объект ADSI, устанавливая свойство **различающегося имени** объекта из его собственного значения ADsPath.</span><span class="sxs-lookup"><span data-stu-id="6cc51-110">The following code example helps to initialize a newly created ADSI object by setting the object's **Distinguished Name** property from its own ADsPath.</span></span> <span data-ttu-id="6cc51-111">Имейте в виду, что вызывающая подпрограммы должна зафиксировать любые изменения в базовом хранилище каталога, вызвав метод **сетинфо** .</span><span class="sxs-lookup"><span data-stu-id="6cc51-111">Be aware that the calling routine must commit any changes to the underlying directory store by invoking the **SetInfo** method.</span></span>


```C++
HRESULT SetDistinguishedName(IADs *pIADs)
{
    HRESULT hr = S_OK;
    CComBSTR sbstrADsPath;
    IADsPathname *pIADsPathname = NULL;
 
    // Get the ADsPath for this object.
    hr = pIADs->get_ADsPath(&sbstrADsPath);
    if (FAILED(hr))
        return (hr);
 
    // Create the IADsPathname object.
    hr = CoCreateInstance(CLSID_Pathname,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsPathname,
                          (void**) &pIADsPathname);
    if (FAILED(hr))
    {
        if (pIADsPathname)
            pIADsPathname->Release();
        return (hr);
    }
     // Set the path.
    hr = pIADsPathname->Set(sbstrADsPath, ADS_SETTYPE_FULL);
    if (SUCCEEDED(hr))
    {
        CComBSTR sbstrDNPath;

        // Convert the path to Distinguished Name format.
        hr = pIADsPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,
                                     &sbstrDNPath);
 
        if (SUCCEEDED(hr))
        {
            // Set the distinguished name property.
            VARIANT var;
            VariantInit(&var);
            V_BSTR(&var) = sbstrDNPath;
            V_VT(&var) = VT_BSTR;
            hr = pIADs->Put(CComBSTR("distinguishedName"), var);
            VariantClear(&var);
        }
    }
 
    // Cleanup.
    pIADsPathname->Release();
    return (hr);
 
}
```



 

 




