---
description: В этом разделе описывается, как найти неподключенный ПИН-код для фильтра. Поиск неподключенного ПИН-кода полезен при подключении фильтров.
ms.assetid: d0a906a8-bae4-43b3-8b02-ee5b97c9323d
title: Поиск неподключенного ПИН-кода в фильтре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee47b811c027161b70769cb04063d0e8214934a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072133"
---
# <a name="find-an-unconnected-pin-on-a-filter"></a>Поиск неподключенного ПИН-кода в фильтре

В этом разделе описывается, как найти неподключенный ПИН-код для фильтра. Поиск неподключенного ПИН-кода полезен при подключении фильтров.

В типичном сценарии построения графа DirectShow требуется неподключенный ПИН-код, соответствующий определенному направлению ПИН-кода (входные или выходные данные). Например, при подключении двух фильтров вы подключаете выходной ПИН-код из одного фильтра к входному ПИН-коду из другого фильтра. Перед подключением оба ПИН-кода должны быть отключены.

Сначала нам нужна функция, которая проверяет, подключен ли ПИН-код к другому ПИН-коду. Эта функция вызывает метод [**Ипин:: коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) , чтобы проверить, подключен ли ПИН-код к другому ПИН-коду.


```C++
// Query whether a pin is connected to another pin.
//
// Note: This function does not return a pointer to the connected pin.

HRESULT IsPinConnected(IPin *pPin, BOOL *pResult)
{
    IPin *pTmp = NULL;
    HRESULT hr = pPin->ConnectedTo(&pTmp);
    if (SUCCEEDED(hr))
    {
        *pResult = TRUE;
    }
    else if (hr == VFW_E_NOT_CONNECTED)
    {
        // The pin is not connected. This is not an error for our purposes.
        *pResult = FALSE;
        hr = S_OK;
    }

    SafeRelease(&pTmp);
    return hr;
}
```



> [!Note]  
> В этом примере функция [саферелеасе](/windows/desktop/medfound/saferelease) используется для высвобождения указателей интерфейса.

 

Далее нам нужна функция, которая проверяет, соответствует ли ПИН-код указанному направлению ПИН-кода. Эта функция вызывает метод [**Ипин:: куеридиректион**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) для получения направления ПИН-кода.


```C++
// Query whether a pin has a specified direction (input / output)
HRESULT IsPinDirection(IPin *pPin, PIN_DIRECTION dir, BOOL *pResult)
{
    PIN_DIRECTION pinDir;
    HRESULT hr = pPin->QueryDirection(&pinDir);
    if (SUCCEEDED(hr))
    {
        *pResult = (pinDir == dir);
    }
    return hr;
}
```



Следующая функция сопоставляет ПИН-код по обоим критериям (направление ПИН-кода и состояние соединения).


```C++
// Match a pin by pin direction and connection state.
HRESULT MatchPin(IPin *pPin, PIN_DIRECTION direction, BOOL bShouldBeConnected, BOOL *pResult)
{
    assert(pResult != NULL);

    BOOL bMatch = FALSE;
    BOOL bIsConnected = FALSE;

    HRESULT hr = IsPinConnected(pPin, &bIsConnected);
    if (SUCCEEDED(hr))
    {
        if (bIsConnected == bShouldBeConnected)
        {
            hr = IsPinDirection(pPin, direction, &bMatch);
        }
    }

    if (SUCCEEDED(hr))
    {
        *pResult = bMatch;
    }
    return hr;
}
```



Наконец, следующая функция использует интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) для прохода по контактам в фильтре. Вызывающий объект указывает требуемое направление ПИН-кода. Для каждого ПИН-кода функция вызывает, `MatchPin` чтобы проверить, является ли ПИН-код совпадением. Если направление соответствия и ПИН-код не соединены, функция возвращает указатель на соответствующий ПИН-код в параметре *пппин* .


```C++
// Return the first unconnected input pin or output pin.
HRESULT FindUnconnectedPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin **ppPin)
{
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    BOOL bFound = FALSE;

    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = MatchPin(pPin, PinDir, FALSE, &bFound);
        if (FAILED(hr))
        {
            goto done;
        }
        if (bFound)
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();
            break;
        }
        SafeRelease(&pPin);
    }

    if (!bFound)
    {
        hr = VFW_E_NOT_FOUND;
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    return hr;
}
```



Пример того, как можно использовать эту функцию, см. в разделе [Connect Two Filters](connect-two-filters.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Перечисление ПИН-кодов](enumerating-pins.md)
</dt> <dt>

[Общие методы Graph-Building](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: Финдпин**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
