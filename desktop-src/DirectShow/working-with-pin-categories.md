---
description: Работа с категориями ПИН-кодов
ms.assetid: 1ee648b3-8370-4e4d-b513-d998131512ee
title: Работа с категориями ПИН-кодов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac58fff91821477cca51e0613772e3e5763d4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662667"
---
# <a name="working-with-pin-categories"></a>Работа с категориями ПИН-кодов

Для поиска в фильтре для ПИН-кода с заданной категорией закрепления можно использовать метод [**ICaptureGraphBuilder2:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) . В следующем примере выполняется поиск ПИН-кода для предварительного просмотра видео:


```C++
int i = 0;
hr = pBuild->FindPin(
    pFilter,               // Pointer to a filter to search.
    PINDIR_OUTPUT,         // Which pin direction?
    &PIN_CATEGORY_PREVIEW, // Which category? (NULL means "any category")
    &MEDIATYPE_Video,      // What media type? (NULL means "any type")
    FALSE,                 // Must be connected?
    i,                     // Get the i'th matching pin (0 = first match)
    &pPin                  // Receives a pointer to the pin.
);
```



Первый параметр — это указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра. Следующие три параметра указывают направление, категорию закрепления и тип носителя. Значение **false** в пятом параметре указывает на то, что ПИН-код может быть подключен или не подключен. (Точные определения этих параметров см. в документации по методу.) Если метод находит совпадающий ПИН-код, он возвращает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) в параметре *ппин* .

Хотя метод [**финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) удобен, при желании можно также написать собственные вспомогательные функции. Чтобы определить категорию ПИН-кода, вызовите метод [**икспропертисет:: Get**](ikspropertyset-get.md) , как описано в [наборе свойств ПИН-кода](pin-property-set.md)раздела.

В следующем коде показана вспомогательная функция, которая проверяет, соответствует ли ПИН-код указанной категории:


```C++
// Returns TRUE if a pin matches the specified pin category.

BOOL PinMatchesCategory(IPin *pPin, REFGUID Category)
{
    BOOL bFound = FALSE;

    IKsPropertySet *pKs = NULL;
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (SUCCEEDED(hr))
    {
        GUID PinCategory;
        DWORD cbReturned;
        hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
            &PinCategory, sizeof(GUID), &cbReturned);
        if (SUCCEEDED(hr) && (cbReturned == sizeof(GUID)))
        {
            bFound = (PinCategory == Category);
        }
        pKs->Release();
    }
    return bFound;
}
```



Следующий пример — функция, которая ищет ПИН-код по категории, аналогичный методу [**финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) :


```C++
// Finds the first pin that matches a specified pin category and direction.

HRESULT FindPinByCategory(
    IBaseFilter *pFilter, // Pointer to the filter to search.
    PIN_DIRECTION PinDir, // Direction of the pin.
    REFGUID Category,     // Pin category.
    IPin **ppPin)         // Receives a pointer to the pin.
{
    *ppPin = 0;

    HRESULT hr = S_OK;
    BOOL bFound = FALSE;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (hr = pEnum->Next(1, &pPin, 0), hr == S_OK)
    {
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            goto done;
        }
        if ((ThisPinDir == PinDir) && 
            PinMatchesCategory(pPin, Category))
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();   // The caller must release the interface.
            bFound = TRUE;
            break;
        }
        SafeRelease(&pPin);
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    if (SUCCEEDED(hr) && !bFound)
    {
        hr = E_FAIL;
    }
    return hr;
}
```



В следующем коде функция Previous используется для поиска ПИН-кода порта видео в фильтре:


```C++
IPin *pVP; 
hr = FindPinByCategory(pFilter, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT, &pVP);
if (SUCCEEDED(hr))
{
    // Use pVP ... 
    // Release when you are done.
    pVP->Release();
}
```



Дополнительные сведения о наборах свойств см. в документации по [комплекту драйверов Windows (WDK)](/windows-hardware/drivers/gettingstarted/) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Разделы, посвященные расширенному записи](advanced-capture-topics.md)
</dt> <dt>

[Закрепить набор свойств](pin-property-set.md)
</dt> <dt>

[Фильтры захвата видео DirectShow](directshow-video-capture-filters.md)
</dt> </dl>

 

 
