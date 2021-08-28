---
description: Использование средства сопоставления фильтров
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Использование средства сопоставления фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48758c40b97477200b4fab1215eaccac53823771add86d6a8b915370776495a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049617"
---
# <a name="using-the-filter-mapper"></a>Использование средства сопоставления фильтров

средство [сопоставления фильтров](filter-mapper.md) — это COM-объект, перечисляющий DirectShow фильтры на основе различных критериев поиска. Средство сопоставления фильтров может быть менее эффективным, чем перечислитель системных устройств, поэтому если вам нужны фильтры из определенной категории, следует использовать перечислитель системных устройств. Но если необходимо выбрать фильтр, который поддерживает определенное сочетание типов мультимедиа, но не входит в категорию четких вырезания, может потребоваться использовать средство сопоставления фильтров. (Пример может быть фильтром визуализации или фильтром декодера.)

Средство сопоставления фильтров предоставляет интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) . Чтобы найти фильтр, вызовите метод [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Этот метод принимает несколько параметров, определяющих условия поиска, и возвращает перечислитель для соответствующих фильтров. Перечислитель поддерживает интерфейс [**иенуммоникер**](/windows/win32/api/objidl/nn-objidl-ienummoniker) и предоставляет уникальный моникер для каждого фильтра сопоставления.

В следующем примере перечисляются фильтры, которые принимают входные цифровые видео (DV) и имеют по крайней мере один выходной ПИН-код любого типа носителя. (Фильтр [видеодекодера DV](dv-video-decoder-filter.md) соответствует этим критериям.)


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



Метод [**енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) имеет достаточно большое количество параметров, которые добавляются в комментарий в примере. К этим примерам относятся следующие:

-   Минимальное количество недоступных: для фильтра должно быть задано значение неуспешное \_ \_ \_ использование.
-   Типы входных данных. вызывающий объект передает массив, содержащий пары основных типов и подтипов. Будут соответствовать только те фильтры, которые поддерживают хотя бы одну из этих пар.
-   Точное совпадение. фильтр может регистрировать значения **null** для основного типа, подтипа, категории закрепления или средних. Если не указано точное соответствие, значение **null** выступает в качестве подстановочного знака, совпадающего с любым указанным значением. С точным соответствием фильтр должен точно соответствовать вашим критериям. Однако если в критериях поиска вы придаете параметр **null** , он всегда действует как подстановочный знак или значение "не важно", соответствующее любому фильтру.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Перечисление устройств и фильтров](enumerating-devices-and-filters.md)
</dt> <dt>

[интеллектуальные Подключение](intelligent-connect.md)
</dt> </dl>

 

 
