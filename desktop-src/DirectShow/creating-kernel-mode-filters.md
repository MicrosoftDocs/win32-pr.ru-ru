---
description: Создание фильтров Kernel-Mode
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Создание фильтров Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473565046c462e8992350c3662360e4c22b3b5b75e10f0e79e1399885355056e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953943"
---
# <a name="creating-kernel-mode-filters"></a>Создание фильтров Kernel-Mode

Некоторые фильтры режима ядра нельзя создать с помощью **CoCreateInstance**, поэтому они не имеют идентификаторов CLSID. Эти фильтры включают в себя [преобразователь tee/Sink-to-Sink](tee-sink-to-sink-converter.md), фильтр [декодера CC](cc-decoder-filter.md) и фильтр [кодека WST](wst-codec-filter.md) . Чтобы создать один из этих фильтров, используйте объект [перечислителя системных устройств](system-device-enumerator.md) и выполните поиск по имени фильтра.

1.  Создайте перечислитель системных устройств.
2.  Вызовите метод [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) с идентификатором CLSID категории фильтра для этого фильтра. Этот метод создает перечислитель для категории фильтра. ( *Перечислитель* — это просто объект, который возвращает список других объектов с использованием определенного COM-интерфейса.) Перечислитель возвращает **IMoniker** указатели, которые представляют фильтры в этой категории.
3.  Для каждого моникера вызовите **IMoniker:: биндтостораже** , чтобы получить интерфейс **ипропертибаг** .
4.  Вызовите метод **ипропертибаг:: Read** , чтобы получить имя фильтра.
5.  Если имя совпадает, вызовите **IMoniker:: биндтубжект** , чтобы создать фильтр.

В следующем коде показана функция, которая выполняет следующие действия:


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



В следующем примере кода эта функция используется для создания фильтра декодера CC и его добавления в граф фильтра:


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разделы, посвященные расширенному записи](advanced-capture-topics.md)
</dt> <dt>

[Использование перечислителя системных устройств](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



