---
description: Шаг 3A.
ms.assetid: 774fcb12-8928-4667-8ef6-dce86717cc29
title: Шаг 3A. Реализация метода Чеккинпуттипе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eb6ff440838d7a4b65b586e5dba963ff254eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674177"
---
# <a name="step-3a-implement-the-checkinputtype-method"></a>Шаг 3A. Реализация метода Чеккинпуттипе

Это шаг 3A из руководства по созданию [фильтров преобразования](writing-transform-filters.md).

Метод [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) вызывается, когда вышестоящий фильтр предлагает тип мультимедиа для фильтра преобразования. Этот метод принимает указатель на объект [**кмедиатипе**](cmediatype.md) , который является тонкой оболочкой для структуры [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) . В этом методе необходимо проверить каждое соответствующее поле структуры **\_ \_ типа мультимедиа AM** , включая поля в блоке форматирования. Можно использовать методы доступа, определенные в **кмедиатипе**, или ссылаться на члены структуры напрямую. Если какое-либо поле недопустимо, возвращается \_ тип VFW E \_ \_ не \_ принят. Если весь тип мультимедиа является допустимым, возвращается значение S \_ OK.

Например, в фильтре кодировщика RLE тип входных данных должен быть 8-разрядным или 4-битовым несжатым видео RGB. Нет причин поддерживать другие форматы ввода, например 16-или 24-разрядный RGB, так как фильтр должен преобразовать их в более низкую глубину, а в DirectShow уже есть фильтр [преобразователя цветового пространства](color-space-converter-filter.md) для этой цели. В следующем примере предполагается, что кодировщик поддерживает 8-разрядное видео, но не 4-разрядное видео:


```C++
HRESULT CRleFilter::CheckInputType(const CMediaType *mtIn)
{
    if ((mtIn->majortype != MEDIATYPE_Video) ||
        (mtIn->subtype != MEDIASUBTYPE_RGB8) ||
        (mtIn->formattype != FORMAT_VideoInfo) || 
        (mtIn->cbFormat < sizeof(VIDEOINFOHEADER)))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    VIDEOINFOHEADER *pVih = 
        reinterpret_cast<VIDEOINFOHEADER*>(mtIn->pbFormat);
    if ((pVih->bmiHeader.biBitCount != 8) ||
        (pVih->bmiHeader.biCompression != BI_RGB))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Check the palette table.
    if (pVih->bmiHeader.biClrUsed > PALETTE_ENTRIES(pVih))
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
    DWORD cbPalette = pVih->bmiHeader.biClrUsed * sizeof(RGBQUAD);
    if (mtIn->cbFormat < sizeof(VIDEOINFOHEADER) + cbPalette)
    {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }

    // Everything is good.
    return S_OK;
}
```



В этом примере метод сначала проверяет основной тип и подтип. Затем проверяется тип формата, чтобы блок формата был [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) структурой. Фильтр также может поддерживать [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2), но в этом случае нет никаких реальных преимуществ. Структура **VIDEOINFOHEADER2** добавляет поддержку чередования и неквадратных пикселей, которые, скорее всего, не будут важны в 8-разрядном видео.

Если тип формата правильный, пример проверяет элементы **бибиткаунт** и **бикомпрессион** структуры **видеоинфохеадер** , чтобы убедиться в том, что формат имеет 8-битный несжатый RGB. Как показано в этом примере, необходимо привести


```C++
pbFormat
```



Указатель на правильную структуру в зависимости от типа формата. Перед приведением указателя всегда проверяйте тип GUID (**форматтипе**) и размер блока форматирования (**кбформат**).

В этом примере также проверяется, что число записей палитры совместимо с битовой глубиной, а блок формата достаточно велик для хранения записей палитры. Если все эти сведения верны, метод возвращает значение S \_ ОК.

Далее. [Шаг 3b. Реализация метода жетмедиатипе](step-3b--implement-the-getmediatype-method.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



