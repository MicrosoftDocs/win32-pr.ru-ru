---
description: 'В этом разделе описываются две связанные понятия: пропорции рисунка и пропорции пикселей.'
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Пропорции рисунка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263499"
---
# <a name="picture-aspect-ratio"></a>Пропорции рисунка

В этом разделе описываются две связанные понятия: пропорции рисунка и пропорции пикселей. Затем он описывает, как эти понятия выражаются в Microsoft Media Foundation с помощью типов мультимедиа.

-   [Пропорции рисунка](#picture-aspect-ratio)
    -   [Пустых](#letterboxing)
    -   [Панорамирование и сканирование](#pan-and-scan)
-   [Пропорция в пикселях](#pixel-aspect-ratio)
-   [Работа с пропорциями](#working-with-aspect-ratios)
-   [Примеры кода](#code-examples)
    -   [Поиск отображаемой области](#finding-the-display-area)
    -   [Преобразование между пропорциями в пикселях](#converting-between-pixel-aspect-ratios)
    -   [Вычисление области Леттербокс](#calculating-the-letterbox-area)
-   [См. также](#related-topics)

## <a name="picture-aspect-ratio"></a>Пропорции рисунка

Пропорции *рисунка* определяет форму отображаемого видеоизображения. Пропорции рисунка — это КС:И, где КС:И — отношение ширины изображения к высоте изображения. Большинство стандартов видео используют пропорции изображения 4:3 или 16:9. Пропорции 16:9 обычно называются *широкоформатными*. На пленке в кинотеатрах часто используется пропорции 1:85:1 или 1:66:1. Пропорции изображения также называются *отображаемыми* пропорциями (Dar).

![Схема, показывающая пропорции 4:3 и 16:9](images/aspect-ratio01.png)

Иногда видеоизображение не имеет такой же формы, как и отображаемая область. Например, видео 4:3 может отображаться на широкоформатном телевизоре (16 × 9). Видео на компьютере может отображаться в окне с произвольным размером. В этом случае можно создать три способа размещения изображения в области экрана:

-   Растяните изображение вдоль одной оси в соответствии с отображаемой областью.
-   Масштабирование изображения в соответствии с областью экрана с сохранением пропорций исходного изображения.
-   Обрезка изображения.

Растяжение изображения по размеру отображаемой области почти всегда неверно, поскольку не сохраняет правильные пропорции изображения.

### <a name="letterboxing"></a>Пустых

Процесс масштабирования широкоэкранных изображений в соответствии с отображаемым 4:3 называется *пустых*, как показано на следующей схеме. Итоговые ректанглулар области в верхней и нижней части изображения обычно заполняются черным цветом, хотя можно использовать и другие цвета.

![Схема, показывающая правильный способ леттербокс](images/aspect-ratio02.png)

Обратная ситуация, масштабирование изображения 4:3 в соответствии с широкоэкранным дисплеем, иногда называется *пилларбоксинг*. Однако термин *леттербокс* также используется в общем смысле, что означает Масштабирование видеоизображения в соответствии с заданной областью экрана.

![Диаграмма, показывающая пилларбоксинг](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Панорамирование и сканирование

Сдвиг и сканирование — это способ, с помощью которого изображение с широкоэкранным экраном обрезается до 4 × 3 прямоугольной области, отображаемой на устройстве с дисплеем 4:3. Полученное изображение заполняет весь экран, не требуя черной леттербокс областей, но фрагменты исходного изображения обрезаются из изображения. Обрезанная область может перемещаться из рамки в рамку в качестве области сдвигов интересов. Термин «PAN» в « *сдвиге» и «сканирование* » обозначает эффекты панорамирования, вызванные перемещением области «сдвиг и сканирование».

![Схема, показывающая панораму и сканирование](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Пропорция в пикселях

*Попиксельное соотношение сторон* (номинал) измеряет форму пикселя.

При захвате цифрового изображения изображение выводится как по вертикали, так и по горизонтали, что приводит к выделению прямоугольного массива примеров квантования, называемых *пикселями* или *пикселей*. Форма сетки выборки определяет форму пикселей в разрядном изображении.

Ниже приведен пример, в котором для упрощения математических вычислений используются небольшие числа. Предположим, что исходное изображение является квадратным (то есть пропорция изображения — 1:1); Предположим, что сетка выборки содержит 12 элементов, расположенных в сетке 4 × 3. Форма каждого полученного пикселя будет больше по сравнению с шириной в ширину. В частности, форма каждого пикселя будет иметь значение 3 × 4. Пиксели, которые не являются квадратными, называются *неквадратными пикселями*.

![Схема, показывающая неквадратную сетку выборки](images/aspect-ratio05.png)

Пропорции пикселя также применяются к устройству вывода. Физическая форма устройства вывода и разрешение физического пикселя (по горизонтали и вертикали) определяют номинал отображаемого устройства. Мониторы компьютеров обычно используют квадратные пикселы. Если изображение имеет номинал и отображаемое значение не совпадает, изображение должно масштабироваться в одном или вертикальном или горизонтальном порядке для правильного вывода. Следующая формула относится к НОМИНАЛу, отображению пропорций (DAR) и размеру изображения в пикселях:

*Dar* = (*Ширина изображения в пикселях*  /  *Высота изображения в пикселях*) × *номинал*

Обратите внимание, что ширина и высота изображения в этой формуле относятся к изображению в памяти, а не к отображаемому изображению.

Пример практического практического примера: аналоговый видеоролик NTSC-M содержит строки сканирования 480 в активной области изображения. ITU-R Rec. BT. 601 задает горизонтальную частоту выборки 704 видимых пикселей в строке, что приводит к получению цифрового изображения с 704 x 480 пикселей. Предполагаемый пропорции изображения — 4:3, что дает НОМИНАЛу 10:11.

-   DAR: 4:3
-   Ширина в пикселях: 704
-   Высота в пикселях: 480
-   НОМИНАЛ: 10/11

4/3 = (704/420) x (10/11)

Чтобы правильно отобразить это изображение на устройстве вывода с квадратными пикселами, необходимо масштабировать ширину на 10/11 или высоту на 11/10.

## <a name="working-with-aspect-ratios"></a>Работа с пропорциями

Правильная форма видеокадра определяется *попиксельным пропорциями* (номинал) и *областью просмотра*.

-   Номинал определяет форму пикселей в изображении. Квадратные пиксели имеют пропорции 1:1. Любые другие пропорции описывают неквадратные Пиксели. Например, NTSC-Телевизор использует 10:11 НОМИНАЛа. Если вы проводите показ видео на мониторе компьютера, экран будет иметь квадратные пиксели (1:1 номинал). Значение НОМИНАЛа для исходного содержимого указывается в атрибуте пропорции [**MF \_ MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md) в типе носителя.
-   Область отображения — это регион видеоизображения, которое должно отображаться. Существует две соответствующие области, которые можно указать в типе носителя:
    -   Апертура и сканирование. Апертура "сдвиг и сканирование" — это 4 × 3 региона видео, который должен отображаться в режиме панорамирования и сканирования. Он используется для отображения содержимого на широком экране на 4 × 3 дисплее без пустых. Апертура «сдвиг и сканирование» задается в атрибуте [**\_ \_ \_ \_ апертуры панорамного поиска в MF**](mf-mt-pan-scan-aperture-attribute.md) , и его следует использовать только в том случае, если атрибуту « [**\_ \_ \_ \_ Включить сканирование MF в Pan**](mf-mt-pan-scan-enabled-attribute.md) » задано **значение true**.
    -   Отображение апертуры. Это Апертура определено в некоторых стандартах видео. Все, что находится за пределами отображаемого Апертура, является областью пересканирования и не должна отображаться. Например, NTSC-телевизор — 720 × 480 пикселей с отображаемым апертуром в 704 × 480. Отображаемый Апертура задается в атрибуте « [**\_ \_ Минимальный \_ отображаемый \_ Апертура MF MT**](mf-mt-minimum-display-aperture-attribute.md) ». Если он есть, его следует использовать, если режим панорамирования и сканирования имеет **значение false**.

Если режим "сдвиг и с" имеет **значение false** и не задано окно апертуры, отображается весь видеокадр. На самом деле, это так для большинства видеоматериалов, отличных от телевизионных и DVD-видео. Пропорции всего изображения рассчитывается как (*Отображаемая ширина*  /  *отображаемой области высота*) × *номинал*.

## <a name="code-examples"></a>Примеры кода

### <a name="finding-the-display-area"></a>Поиск отображаемой области

В следующем коде показано, как получить область отображения из типа мультимедиа.


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a>Преобразование между пропорциями в пикселях

В следующем коде показано, как преобразовать прямоугольник из одной пиксельной пропорции (НОМИНАЛа) в другую, сохраняя пропорции изображения.


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a>Вычисление области Леттербокс

Следующий код вычисляет область леттербокс с учетом исходного и целевого прямоугольников. Предполагается, что оба прямоугольника имеют одинаковое значение НОМИНАЛа.


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы носителей](media-types.md)
</dt> <dt>

[Типы видеоклипов](video-media-types.md)
</dt> <dt>

[**\_ \_ Минимальный \_ \_ Апертура экрана MF MT**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_ \_ \_ Апертура для поиска MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**\_ \_ включена проверка панорамы MF MT \_ \_**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**пропорции MF \_ MT \_ пикселей \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



