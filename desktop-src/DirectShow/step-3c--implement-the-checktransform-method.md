---
description: Шаг 3C.
ms.assetid: e780df46-bf47-4334-b788-05ad8179f051
title: Шаг 3C. Реализация метода Чекктрансформ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430ad933acfa7fc41a8b075183080e0b710a5d4780b55fa89cd4bf80984c1edc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075594"
---
# <a name="step-3c-implement-the-checktransform-method"></a>Шаг 3C. Реализация метода Чекктрансформ

Это шаг 3C из руководства по созданию [фильтров преобразования](writing-transform-filters.md).

> [!Note]  
> Этот шаг не является обязательным для фильтров, производных от **ктрансинплацефилтер**.

 

Метод [**ктрансформфилтер:: чекктрансформ**](ctransformfilter-checktransform.md) проверяет, совместим ли предложенный тип выходных данных с текущим типом входных данных. Метод также вызывается, если входной ПИН-код переключается после подключения выходного контакта.

В следующем примере проверяется, является ли формат RLE8 видео. размеры изображения соответствуют входному формату. и записи в палитре одинаковы. Он также отклоняет исходный и целевой прямоугольники, которые не соответствуют размеру изображения.


```C++
HRESULT CRleFilter::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    // Check the major type.
    if (mtOut->majortype != MEDIATYPE_Video)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the subtype and format type.
    FOURCCMap fccMap = FCC('MRLE'); 
    if (mtOut->subtype != static_cast<GUID>(fccMap))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if ((mtOut->formattype != FORMAT_VideoInfo) || 
        (mtOut->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare the bitmap information against the input type.
    ASSERT(mtIn->formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pBmiOut = HEADER(mtOut->pbFormat);
    BITMAPINFOHEADER *pBmiIn = HEADER(mtIn->pbFormat);
    if ((pBmiOut->biPlanes != 1) ||
        (pBmiOut->biBitCount != 8) ||
        (pBmiOut->biCompression != BI_RLE8) ||
        (pBmiOut->biWidth != pBmiIn->biWidth) ||
        (pBmiOut->biHeight != pBmiIn->biHeight))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Compare source and target rectangles.
    RECT rcImg;
    SetRect(&rcImg, 0, 0, pBmiIn->biWidth, pBmiIn->biHeight);
    RECT *prcSrc = &((VIDEOINFOHEADER*)(mtIn->pbFormat))->rcSource;
    RECT *prcTarget = &((VIDEOINFOHEADER*)(mtOut->pbFormat))->rcTarget;
    if (!IsRectEmpty(prcSrc) && !EqualRect(prcSrc, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
    if (!IsRectEmpty(prcTarget) && !EqualRect(prcTarget, &rcImg))
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the palette table.
    if (pBmiOut->biClrUsed != pBmiIn->biClrUsed)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pBmiOut->biClrUsed * sizeof(RGBQUAD);
    if (mtOut->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    if (0 != memcmp(pBmiOut + 1, pBmiIn + 1, cbPalette))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



**Переподключение ПИН-кода**

Приложения могут отключаться и повторно подключать ПИН-коды. Предположим, что приложение соединяет оба контакта, отсоединяет входной ПИН-код, а затем повторно подключает входной ПИН-код с помощью нового размера изображения. В этом случае **чекктрансформ** завершается сбоем, так как измерения изображения больше не совпадают. Такое поведение имеет смысл, хотя фильтр может попытаться повторно подключить выходной ПИН-код к новому типу носителя.

Далее. [Шаг 4. Задайте свойства распределителя](step-4--set-allocator-properties.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Повторное подключение ПИН-кодов](reconnecting-pins.md)
</dt> <dt>

[Исходные и целевые прямоугольники в модулях подготовки видео](source-and-target-rectangles-in-video-renderers.md)
</dt> <dt>

[написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



