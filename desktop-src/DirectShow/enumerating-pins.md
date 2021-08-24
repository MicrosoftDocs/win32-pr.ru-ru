---
description: Перечисление ПИН-кодов
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Перечисление ПИН-кодов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d772903321c71ab2c6d66f7cc46b7ca61b11f96a4bc17b13b8b2f8931d8eac5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748714"
---
# <a name="enumerating-pins"></a>Перечисление ПИН-кодов

Фильтры поддерживают метод [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , который перечисляет ПИН-коды, доступные в фильтре. Он возвращает указатель на интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . Метод [**иенумпинс:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) получает указатели интерфейса [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

В следующем примере показана функция, которая находит ПИН-код с заданным направлением (вход или выход) для данного фильтра. Он использует перечисление [**\_ направления PIN-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) для указания направления ПИН-кода и метод [**Ипин:: куеридиректион**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) для поиска направления каждого перечислимого ПИН-кода. Если эта функция находит совпадающий ПИН-код, она возвращает указатель интерфейса **Ипин** с необработанным числом ссылок. Вызывающий объект отвечает за освобождение интерфейса.


```C++
HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins  *pEnum = NULL;
    IPin       *pPin = NULL;
    HRESULT    hr;

    if (ppPin == NULL)
    {
        return E_POINTER;
    }

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        hr = pPin->QueryDirection(&PinDirThis);
        if (FAILED(hr))
        {
            pPin->Release();
            pEnum->Release();
            return hr;
        }
        if (PinDir == PinDirThis)
        {
            // Found a match. Return the IPin pointer to the caller.
            *ppPin = pPin;
            pEnum->Release();
            return S_OK;
        }
        // Release the pin for the next time through the loop.
        pPin->Release();
    }
    // No more pins. We did not find a match.
    pEnum->Release();
    return E_FAIL;  
}
```



Эту функцию можно легко изменить, чтобы вернуть n-контактный заданному направлению или *n*-й несоединенный ПИН. (Чтобы узнать, подключен ли ПИН-код к другому ПИН-коду, вызовите метод [**Ипин:: коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Перечисление объектов в фильтре Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Поиск неподключенного ПИН-кода в фильтре](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[Общие методы Graph-Building](general-graph-building-techniques.md)
</dt> <dt>

[Закрепить набор свойств](pin-property-set.md)
</dt> </dl>

 

 



