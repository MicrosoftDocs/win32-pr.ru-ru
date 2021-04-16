---
description: Шаг 3B.
ms.assetid: 0ec57083-b192-404a-938f-bc6bb1cf0ddb
title: Шаг 3B. Реализация метода Жетмедиатипе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab3ee41c6740fc2914f943784c0d51116f90428
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547359"
---
# <a name="step-3b-implement-the-getmediatype-method"></a>Шаг 3B. Реализация метода Жетмедиатипе

Это шаг 3B из руководства [Создание фильтров преобразования](writing-transform-filters.md).

> [!Note]  
> Этот шаг не является обязательным для фильтров, производных от **ктрансинплацефилтер**.

 

Метод [**ктрансформфилтер:: жетмедиатипе**](ctransformfilter-getmediatype.md) возвращает один из предпочтительных выходных типов фильтра, на который ссылается номер индекса. Этот метод никогда не вызывается, если входной ПИН-код фильтра уже не подключен. Таким образом, можно использовать тип мультимедиа из вышестоящего соединения, чтобы определить предпочтительные типы выходных данных.

Кодировщик обычно предлагает один предпочтительный тип, представляющий целевой формат. Декодеры обычно поддерживают ряд выходных форматов и предлагают их в порядке убывания качества или эффективности. Например, в этом порядке список может быть UYVY, Y211, RGB-24, RGB-565, RGB-555 и RGB-8. Фильтры эффектов могут потребовать точного соответствия между выходным форматом и форматом входных данных.

В следующем примере возвращается один выходной тип, который создается путем изменения типа входных данных для указания сжатия RLE8:


```C++
HRESULT CRleFilter::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    ASSERT(m_pInput->IsConnected());
    if (iPosition < 0)
    {
        return E_INVALIDARG;
    }
    if (iPosition == 0)
    {
        HRESULT hr = m_pInput->ConnectionMediaType(pMediaType);
        if (FAILED(hr))
        {
            return hr;
        }
        FOURCCMap fccMap = FCC('MRLE'); 
        pMediaType->subtype = static_cast<GUID>(fccMap);
        pMediaType->SetVariableSize();
        pMediaType->SetTemporalCompression(FALSE);

        ASSERT(pMediaType->formattype == FORMAT_VideoInfo);
        VIDEOINFOHEADER *pVih =
            reinterpret_cast<VIDEOINFOHEADER*>(pMediaType->pbFormat);
        pVih->bmiHeader.biCompression = BI_RLE8;
        pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader); 
        return S_OK;
    }
    // else
    return VFW_S_NO_MORE_ITEMS;
}
```



В этом примере метод вызывает [**Ипин:: коннектионмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) , чтобы получить входной тип из входного ПИН-кода. Затем он изменяет некоторые поля, чтобы указать формат сжатия следующим образом:

-   Он назначает новый идентификатор GUID подтипа, созданный из кода FOURCC "МРЛЕ", с помощью класса [**фаурккмап**](fourccmap.md) .
-   Он вызывает метод [**кмедиатипе:: сетвариаблесизе**](cmediatype-setvariablesize.md) , который устанавливает для флага **бфикседсизесамплес** **значение false** , а элемент **лсамплесизе** — равным нулю, указывая выборки размера переменной.
-   Он вызывает метод [**кмедиатипе:: сеттемпоралкомпрессион**](cmediatype-settemporalcompression.md) со значением **false**, указывающим, что каждый кадр является ключевым кадром. (Это поле доступно только для информационных целей, поэтому его можно спокойно проигнорировать.)
-   Он устанавливает для поля **бикомпрессион** значение BI \_ RLE8.
-   Он задает для поля **бисизеимаже** размер изображения.

Далее. [шаг 3c. Реализация метода чекктрансформ](step-3c--implement-the-checktransform-method.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



