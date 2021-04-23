---
description: Перечисление типов мультимедиа
ms.assetid: 7878885f-c285-4744-8eab-445678dcfd49
title: Перечисление типов мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3909c25e9ae5f90a3084eebb531431cc93ef46cd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351392"
---
# <a name="enumerating-media-types"></a><span data-ttu-id="c05b7-103">Перечисление типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c05b7-103">Enumerating Media Types</span></span>

<span data-ttu-id="c05b7-104">ПИН-коды поддерживают метод [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) , который перечисляет предпочтительные типы файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c05b7-104">Pins support the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method, which enumerates a pin's preferred media types.</span></span> <span data-ttu-id="c05b7-105">Он возвращает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="c05b7-105">It returns a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="c05b7-106">Метод [**иенуммедиатипес:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) получает указатели на [**структуры \_ \_ типов мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) , описывающие типы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c05b7-106">The [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method retrieves pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures describing media types.</span></span>

<span data-ttu-id="c05b7-107">Перечислитель типа мультимедиа в основном существует, чтобы помочь диспетчеру графов фильтров выполнять интеллектуальные подключения, и приложения, скорее всего, не будут его использовать.</span><span class="sxs-lookup"><span data-stu-id="c05b7-107">The media type enumerator exists primarily to help the Filter Graph Manager make intelligent connections, and your applications will probably not use it.</span></span> <span data-ttu-id="c05b7-108">ПИН-код не обязательно возвращает никаких предпочтительных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c05b7-108">A pin does not necessarily return any preferred media types.</span></span> <span data-ttu-id="c05b7-109">Более того, возвращаемые типы носителей могут зависеть от состояния соединения фильтра.</span><span class="sxs-lookup"><span data-stu-id="c05b7-109">Moreover, the media types it returns might depend on the filter's connection status.</span></span> <span data-ttu-id="c05b7-110">Например, закрепление вывода фильтра может возвращать другой набор типов мультимедиа в зависимости от того, какой тип носителя был задан для входного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="c05b7-110">For example, a filter's output pin might return a different set of media types depending on which media type was set for the filter's input pin.</span></span>

<span data-ttu-id="c05b7-111">В следующем примере выполняется поиск предпочтительного типа мультимедиа, соответствующего указанному основному типу, подтипу или типу формата.</span><span class="sxs-lookup"><span data-stu-id="c05b7-111">The following example finds a preferred media type that matches a specified major type, subtype, or format type.</span></span>


```C++
// Given a pin, find a preferred media type 
//
// pPin         Pointer to the pin.
// majorType    Preferred major type (GUID_NULL = don't care).
// subType      Preferred subtype (GUID_NULL = don't care).
// formatType   Preferred format type (GUID_NULL = don't care).
// ppmt         Receives a pointer to the media type. Can be NULL.
//
// Note: If you want to check whether a pin supports a desired media type,
//       but do not need the format details, set ppmt to NULL.
//
//       If ppmt is not NULL and the method succeeds, the caller must
//       delete the media type, including the format block. 

HRESULT GetPinMediaType(
    IPin *pPin,             // pointer to the pin
    REFGUID majorType,      // desired major type, or GUID_NULL = don't care
    REFGUID subType,        // desired subtype, or GUID_NULL = don't care
    REFGUID formatType,     // desired format type, of GUID_NULL = don't care
    AM_MEDIA_TYPE **ppmt    // Receives a pointer to the media type. (Can be NULL)
    )
{
    *ppmt = NULL;

    IEnumMediaTypes *pEnum = NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    BOOL bFound = FALSE;
    
    HRESULT hr = pPin->EnumMediaTypes(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    while (hr = pEnum->Next(1, &pmt, NULL), hr == S_OK)
    {
        if ((majorType == GUID_NULL) || (majorType == pmt->majortype))
        {
            if ((subType == GUID_NULL) || (subType == pmt->subtype))
            {
                if ((formatType == GUID_NULL) || 
                    (formatType == pmt->formattype))
                {
                    // Found a match. 
                    if (ppmt)
                    {
                        *ppmt = pmt;  // Return it to the caller
                    }
                    else
                    {
                        _DeleteMediaType(pmt);
                    }
                    bFound = TRUE;
                    break;
                }
            }
        }
        _DeleteMediaType(pmt);
    }

    SafeRelease(&pEnum);
    if (SUCCEEDED(hr))
    {
        if (!bFound)
        {
            hr = VFW_E_NOT_FOUND;
        }
    }
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="c05b7-112">В этом примере функция [саферелеасе](/windows/desktop/medfound/saferelease) используется для высвобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c05b7-112">This example uses the [SafeRelease](/windows/desktop/medfound/saferelease) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c05b7-113">См. также</span><span class="sxs-lookup"><span data-stu-id="c05b7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c05b7-114">Перечисление объектов в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="c05b7-114">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="c05b7-115">**иенуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="c05b7-115">**IEnumMediaTypes**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 
