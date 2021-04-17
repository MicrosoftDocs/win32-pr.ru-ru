---
description: Шаг изображения
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Шаг изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567332"
---
# <a name="image-stride"></a>Шаг изображения

Когда видеоизображение хранится в памяти, буфер памяти может содержать дополнительные байты заполнения после каждой строки пикселей. Заполнение байтов влияет на то, как изображение хранится в памяти, но не влияет на способ отображения изображения.

*Шаг* — это число байтов от одной строки пикселей в памяти до следующей строки пикселей в памяти. Шаг также называется *шаг*. Если заданы байты заполнения, шаг шире, чем ширина изображения, как показано на следующем рисунке.

![Диаграмма, показывающая изображение и заполнение.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Два буфера, содержащие видеокадры с одинаковыми измерениями, могут иметь два разных шага. При обработке видеоизображения необходимо выполнить шаг с учетом.

Кроме того, можно разместить изображение в памяти двумя способами. В изображении *сверху вниз* верхняя строка в изображении появляется в первую очередь в памяти. В изображении *снизу вверх* последняя строка пикселей появляется в первую очередь в памяти. На следующем рисунке показано различие между изображением сверху вниз и изображением снизу вверх.

![Схема, демонстрирующая изображения сверху вниз и снизу вверх.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Изображение в нижней части имеет отрицательный шаг, поскольку шаг определяется как число байтов, которое необходимо переместить в меньшую часть пикселей относительно отображаемого изображения. Изображения YUV всегда должны быть сверху вниз, а все изображения, содержащиеся в области Direct3D, должны быть сверху вниз. Изображения RGB в системной памяти обычно находятся снизу вверх.

В частности, преобразования видео обрабатывали буферы с несовпадающими шагами, так как входной буфер может не соответствовать выходному буферу. Например, предположим, что необходимо преобразовать исходное изображение и записать результат в образ назначения. Предположим, что оба изображения имеют одинаковую ширину и высоту, но могут иметь разные форматы пикселей или один и тот же шаг изображения.

В следующем примере кода показан обобщенный подход к написанию такого рода функций. Это не полный рабочий пример, так как он абстрагирует многие конкретные подробности.


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



Эта функция принимает шесть параметров:

-   Указатель на начало сканирования строки 0 в целевом изображении.
-   Шаг конечного изображения.
-   Указатель на начало сканирования строки 0 в исходном изображении.
-   Шаг исходного изображения.
-   Ширина изображения в пикселях.
-   Высота изображения в пикселях.

Основная идея состоит в том, чтобы обрабатывать по одной строке за раз, просматривая каждый пиксель в строке. Предположим, что исходный тип и тип пиксельного пиксела \_ \_ \_ \_ являются структурами, представляющими макет пикселей для исходных и целевых изображений соответственно. (Например, в 32-разрядном RGB используется структура [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) . Не каждый формат пикселей имеет стандартную структуру.) Приведение указателя массива к типу структуры позволяет получить доступ к компонентам RGB или YUV каждого пикселя. В начале каждой строки функция сохраняет указатель на строку. В конце строки указатель увеличивается на ширину шага изображения, что перемещает указатель на следующую строку.

В этом примере вызывается гипотетическая функция с именем Трансформпикселвалуе для каждого пикселя. Это может быть любая функция, которая вычисляет целевой пиксель из исходного пикселя. Конечно, точные сведения будут зависеть от конкретной задачи. Например, при наличии плоского формата YUV необходимо получить доступ к плоскостям чрома независимо от плоскости яркости. При использовании чередования видео может потребоваться обработка полей по отдельности. и т. д.

Чтобы придать более конкретный пример, следующий код преобразует 32-битное изображение RGB в образ АЙУВ. Доступ к пикселям RGB осуществляется с помощью структуры [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , а доступ к айув пикселей осуществляется с помощью структуры структуры [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



В следующем примере показано преобразование 32-битного изображения RGB в образ YV12. В этом примере показано, как управлять плоским форматом YUV. (YV12 имеет формат плоской 4:2:0.) В этом примере функция поддерживает три отдельных указателя для трех плоскостей в целевом изображении. Однако базовый подход тот же, что и в предыдущем примере.


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



Во всех этих примерах предполагается, что приложение уже определило шаг изображения. Иногда эти сведения можно получить из буфера мультимедиа. В противном случае необходимо вычислить его на основе формата видео. Дополнительные сведения о вычислении шага образа и работе с буферами мультимедиа для видео см. в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы видеоклипов](video-media-types.md)
</dt> <dt>

[Типы носителей](media-types.md)
</dt> </dl>

 

 
