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
# <a name="find-an-unconnected-pin-on-a-filter"></a><span data-ttu-id="d5399-104">Поиск неподключенного ПИН-кода в фильтре</span><span class="sxs-lookup"><span data-stu-id="d5399-104">Find an Unconnected Pin on a Filter</span></span>

<span data-ttu-id="d5399-105">В этом разделе описывается, как найти неподключенный ПИН-код для фильтра.</span><span class="sxs-lookup"><span data-stu-id="d5399-105">This topic describes how to find an unconnected pin on a filter.</span></span> <span data-ttu-id="d5399-106">Поиск неподключенного ПИН-кода полезен при подключении фильтров.</span><span class="sxs-lookup"><span data-stu-id="d5399-106">Finding an unconnected pin is useful when you are connecting filters.</span></span>

<span data-ttu-id="d5399-107">В типичном сценарии построения графа DirectShow требуется неподключенный ПИН-код, соответствующий определенному направлению ПИН-кода (входные или выходные данные).</span><span class="sxs-lookup"><span data-stu-id="d5399-107">In a typical DirectShow graph-building scenario, you need an unconnected pin that matches a particular pin direction (input or output).</span></span> <span data-ttu-id="d5399-108">Например, при подключении двух фильтров вы подключаете выходной ПИН-код из одного фильтра к входному ПИН-коду из другого фильтра.</span><span class="sxs-lookup"><span data-stu-id="d5399-108">For example, when you connect two filters, you connect an output pin from one filter to an input pin from the other filter.</span></span> <span data-ttu-id="d5399-109">Перед подключением оба ПИН-кода должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="d5399-109">Both pins must be unconnected before you connect them.</span></span>

<span data-ttu-id="d5399-110">Сначала нам нужна функция, которая проверяет, подключен ли ПИН-код к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="d5399-110">First, we need a function that tests whether a pin is connected to another pin.</span></span> <span data-ttu-id="d5399-111">Эта функция вызывает метод [**Ипин:: коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) , чтобы проверить, подключен ли ПИН-код к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="d5399-111">This function calls the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method to test whether the pin is connected to another pin.</span></span>


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
> <span data-ttu-id="d5399-112">В этом примере функция [саферелеасе](/windows/desktop/medfound/saferelease) используется для высвобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d5399-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

<span data-ttu-id="d5399-113">Далее нам нужна функция, которая проверяет, соответствует ли ПИН-код указанному направлению ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d5399-113">Next, we need a function that tests whether a pin matches a specified pin direction.</span></span> <span data-ttu-id="d5399-114">Эта функция вызывает метод [**Ипин:: куеридиректион**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) для получения направления ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d5399-114">This function calls the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to get the pin direction.</span></span>


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



<span data-ttu-id="d5399-115">Следующая функция сопоставляет ПИН-код по обоим критериям (направление ПИН-кода и состояние соединения).</span><span class="sxs-lookup"><span data-stu-id="d5399-115">The next function matches a pin by both criteria (pin direction and connection status).</span></span>


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



<span data-ttu-id="d5399-116">Наконец, следующая функция использует интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) для прохода по контактам в фильтре.</span><span class="sxs-lookup"><span data-stu-id="d5399-116">Finally, the following function uses the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on the filter.</span></span> <span data-ttu-id="d5399-117">Вызывающий объект указывает требуемое направление ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d5399-117">The caller specifies the desired pin direction.</span></span> <span data-ttu-id="d5399-118">Для каждого ПИН-кода функция вызывает, `MatchPin` чтобы проверить, является ли ПИН-код совпадением.</span><span class="sxs-lookup"><span data-stu-id="d5399-118">For each pin, the function calls `MatchPin` to test whether the pin is a match.</span></span> <span data-ttu-id="d5399-119">Если направление соответствия и ПИН-код не соединены, функция возвращает указатель на соответствующий ПИН-код в параметре *пппин* .</span><span class="sxs-lookup"><span data-stu-id="d5399-119">If the direction matches and the pin is unconnected, the function returns a pointer to the matching pin in the *ppPin* parameter.</span></span>


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



<span data-ttu-id="d5399-120">Пример того, как можно использовать эту функцию, см. в разделе [Connect Two Filters](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d5399-120">For an example of how this function can be used, see [Connect Two Filters](connect-two-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5399-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d5399-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5399-122">Перечисление ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="d5399-122">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="d5399-123">Общие методы Graph-Building</span><span class="sxs-lookup"><span data-stu-id="d5399-123">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="d5399-124">**ICaptureGraphBuilder2:: Финдпин**</span><span class="sxs-lookup"><span data-stu-id="d5399-124">**ICaptureGraphBuilder2::FindPin**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin)
</dt> </dl>

 

 
