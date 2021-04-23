---
description: Перечисление ПИН-кодов
ms.assetid: 231f10c1-46b4-4b66-b0ce-06a191237dfb
title: Перечисление ПИН-кодов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322f1764c46c146d1b899c869d1708eac1f0427d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894606"
---
# <a name="enumerating-pins"></a><span data-ttu-id="11621-103">Перечисление ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="11621-103">Enumerating Pins</span></span>

<span data-ttu-id="11621-104">Фильтры поддерживают метод [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) , который перечисляет ПИН-коды, доступные в фильтре.</span><span class="sxs-lookup"><span data-stu-id="11621-104">Filters support the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method, which enumerates the pins available on the filter.</span></span> <span data-ttu-id="11621-105">Он возвращает указатель на интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="11621-105">It returns a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="11621-106">Метод [**иенумпинс:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) получает указатели интерфейса [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="11621-106">The [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method retrieves [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointers.</span></span>

<span data-ttu-id="11621-107">В следующем примере показана функция, которая находит ПИН-код с заданным направлением (вход или выход) для данного фильтра.</span><span class="sxs-lookup"><span data-stu-id="11621-107">The following example shows a function that locates a pin with a given direction (input or output) on a given filter.</span></span> <span data-ttu-id="11621-108">Он использует перечисление [**\_ направления PIN-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) для указания направления ПИН-кода и метод [**Ипин:: куеридиректион**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) для поиска направления каждого перечислимого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="11621-108">It uses the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration to specify the pin direction, and the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method to find the direction of each enumerated pin.</span></span> <span data-ttu-id="11621-109">Если эта функция находит совпадающий ПИН-код, она возвращает указатель интерфейса **Ипин** с необработанным числом ссылок.</span><span class="sxs-lookup"><span data-stu-id="11621-109">If this function finds a matching pin, it returns an **IPin** interface pointer with an outstanding reference count.</span></span> <span data-ttu-id="11621-110">Вызывающий объект отвечает за освобождение интерфейса.</span><span class="sxs-lookup"><span data-stu-id="11621-110">The caller is responsible for releasing the interface.</span></span>


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



<span data-ttu-id="11621-111">Эту функцию можно легко изменить, чтобы вернуть n-контактный заданному направлению или *n*-й несоединенный ПИН.</span><span class="sxs-lookup"><span data-stu-id="11621-111">This function could easily be modified to return the nth pin with the specified direction, or the *n* th unconnected pin.</span></span> <span data-ttu-id="11621-112">(Чтобы узнать, подключен ли ПИН-код к другому ПИН-коду, вызовите метод [**Ипин:: коннектедто**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .)</span><span class="sxs-lookup"><span data-stu-id="11621-112">(To find out if a pin is connected to another pin, call the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="11621-113">См. также</span><span class="sxs-lookup"><span data-stu-id="11621-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11621-114">Перечисление объектов в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="11621-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="11621-115">Поиск неподключенного ПИН-кода в фильтре</span><span class="sxs-lookup"><span data-stu-id="11621-115">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
</dt> <dt>

[<span data-ttu-id="11621-116">Общие методы Graph-Building</span><span class="sxs-lookup"><span data-stu-id="11621-116">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="11621-117">Закрепить набор свойств</span><span class="sxs-lookup"><span data-stu-id="11621-117">Pin Property Set</span></span>](pin-property-set.md)
</dt> </dl>

 

 



