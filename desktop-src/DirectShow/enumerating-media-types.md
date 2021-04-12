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
# <a name="enumerating-media-types"></a>Перечисление типов мультимедиа

ПИН-коды поддерживают метод [**Ипин:: енуммедиатипес**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) , который перечисляет предпочтительные типы файлов мультимедиа. Он возвращает указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) . Метод [**иенуммедиатипес:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) получает указатели на [**структуры \_ \_ типов мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) , описывающие типы мультимедиа.

Перечислитель типа мультимедиа в основном существует, чтобы помочь диспетчеру графов фильтров выполнять интеллектуальные подключения, и приложения, скорее всего, не будут его использовать. ПИН-код не обязательно возвращает никаких предпочтительных типов мультимедиа. Более того, возвращаемые типы носителей могут зависеть от состояния соединения фильтра. Например, закрепление вывода фильтра может возвращать другой набор типов мультимедиа в зависимости от того, какой тип носителя был задан для входного ПИН-кода фильтра.

В следующем примере выполняется поиск предпочтительного типа мультимедиа, соответствующего указанному основному типу, подтипу или типу формата.


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
> В этом примере функция [саферелеасе](/windows/desktop/medfound/saferelease) используется для высвобождения указателей интерфейса.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Перечисление объектов в графе фильтра](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 
