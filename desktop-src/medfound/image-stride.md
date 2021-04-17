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
# <a name="image-stride"></a><span data-ttu-id="7ac60-103">Шаг изображения</span><span class="sxs-lookup"><span data-stu-id="7ac60-103">Image Stride</span></span>

<span data-ttu-id="7ac60-104">Когда видеоизображение хранится в памяти, буфер памяти может содержать дополнительные байты заполнения после каждой строки пикселей.</span><span class="sxs-lookup"><span data-stu-id="7ac60-104">When a video image is stored in memory, the memory buffer might contain extra padding bytes after each row of pixels.</span></span> <span data-ttu-id="7ac60-105">Заполнение байтов влияет на то, как изображение хранится в памяти, но не влияет на способ отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="7ac60-105">The padding bytes affect how the image is stored in memory, but do not affect how the image is displayed.</span></span>

<span data-ttu-id="7ac60-106">*Шаг* — это число байтов от одной строки пикселей в памяти до следующей строки пикселей в памяти.</span><span class="sxs-lookup"><span data-stu-id="7ac60-106">The *stride* is the number of bytes from one row of pixels in memory to the next row of pixels in memory.</span></span> <span data-ttu-id="7ac60-107">Шаг также называется *шаг*.</span><span class="sxs-lookup"><span data-stu-id="7ac60-107">Stride is also called *pitch*.</span></span> <span data-ttu-id="7ac60-108">Если заданы байты заполнения, шаг шире, чем ширина изображения, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="7ac60-108">If padding bytes are present, the stride is wider than the width of the image, as shown in the following illustration.</span></span>

![Диаграмма, показывающая изображение и заполнение.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

<span data-ttu-id="7ac60-110">Два буфера, содержащие видеокадры с одинаковыми измерениями, могут иметь два разных шага.</span><span class="sxs-lookup"><span data-stu-id="7ac60-110">Two buffers that contain video frames with equal dimensions can have two different strides.</span></span> <span data-ttu-id="7ac60-111">При обработке видеоизображения необходимо выполнить шаг с учетом.</span><span class="sxs-lookup"><span data-stu-id="7ac60-111">If you process a video image, you must take the stride into account.</span></span>

<span data-ttu-id="7ac60-112">Кроме того, можно разместить изображение в памяти двумя способами.</span><span class="sxs-lookup"><span data-stu-id="7ac60-112">In addition, there are two ways that an image can be arranged in memory.</span></span> <span data-ttu-id="7ac60-113">В изображении *сверху вниз* верхняя строка в изображении появляется в первую очередь в памяти.</span><span class="sxs-lookup"><span data-stu-id="7ac60-113">In a *top-down* image, the top row of pixels in the image appears first in memory.</span></span> <span data-ttu-id="7ac60-114">В изображении *снизу вверх* последняя строка пикселей появляется в первую очередь в памяти.</span><span class="sxs-lookup"><span data-stu-id="7ac60-114">In a *bottom-up* image, the last row of pixels appears first in memory.</span></span> <span data-ttu-id="7ac60-115">На следующем рисунке показано различие между изображением сверху вниз и изображением снизу вверх.</span><span class="sxs-lookup"><span data-stu-id="7ac60-115">The following illustration shows the difference between a top-down image and a bottom-up image.</span></span>

![Схема, демонстрирующая изображения сверху вниз и снизу вверх.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

<span data-ttu-id="7ac60-117">Изображение в нижней части имеет отрицательный шаг, поскольку шаг определяется как число байтов, которое необходимо переместить в меньшую часть пикселей относительно отображаемого изображения.</span><span class="sxs-lookup"><span data-stu-id="7ac60-117">A bottom-up image has a negative stride, because stride is defined as the number of bytes need to move down a row of pixels, relative to the displayed image.</span></span> <span data-ttu-id="7ac60-118">Изображения YUV всегда должны быть сверху вниз, а все изображения, содержащиеся в области Direct3D, должны быть сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="7ac60-118">YUV images should always be top-down, and any image that is contained in a Direct3D surface must be top-down.</span></span> <span data-ttu-id="7ac60-119">Изображения RGB в системной памяти обычно находятся снизу вверх.</span><span class="sxs-lookup"><span data-stu-id="7ac60-119">RGB images in system memory are usually bottom-up.</span></span>

<span data-ttu-id="7ac60-120">В частности, преобразования видео обрабатывали буферы с несовпадающими шагами, так как входной буфер может не соответствовать выходному буферу.</span><span class="sxs-lookup"><span data-stu-id="7ac60-120">Video transforms in particular need to handle buffers with mismatched strides, because the input buffer might not match the output buffer.</span></span> <span data-ttu-id="7ac60-121">Например, предположим, что необходимо преобразовать исходное изображение и записать результат в образ назначения.</span><span class="sxs-lookup"><span data-stu-id="7ac60-121">For example, suppose that you want to convert a source image and write the result to a destination image.</span></span> <span data-ttu-id="7ac60-122">Предположим, что оба изображения имеют одинаковую ширину и высоту, но могут иметь разные форматы пикселей или один и тот же шаг изображения.</span><span class="sxs-lookup"><span data-stu-id="7ac60-122">Assume that both images have the same width and height, but might not have the same pixel format or the same image stride.</span></span>

<span data-ttu-id="7ac60-123">В следующем примере кода показан обобщенный подход к написанию такого рода функций.</span><span class="sxs-lookup"><span data-stu-id="7ac60-123">The following example code shows a generalized approach for writing this kind of function.</span></span> <span data-ttu-id="7ac60-124">Это не полный рабочий пример, так как он абстрагирует многие конкретные подробности.</span><span class="sxs-lookup"><span data-stu-id="7ac60-124">This is not a complete working example, because it abstracts many of the specific details.</span></span>


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



<span data-ttu-id="7ac60-125">Эта функция принимает шесть параметров:</span><span class="sxs-lookup"><span data-stu-id="7ac60-125">This function takes six parameters:</span></span>

-   <span data-ttu-id="7ac60-126">Указатель на начало сканирования строки 0 в целевом изображении.</span><span class="sxs-lookup"><span data-stu-id="7ac60-126">A pointer to the start of scan line 0 in the destination image.</span></span>
-   <span data-ttu-id="7ac60-127">Шаг конечного изображения.</span><span class="sxs-lookup"><span data-stu-id="7ac60-127">The stride of the destination image.</span></span>
-   <span data-ttu-id="7ac60-128">Указатель на начало сканирования строки 0 в исходном изображении.</span><span class="sxs-lookup"><span data-stu-id="7ac60-128">A pointer to the start of scan line 0 in the source image.</span></span>
-   <span data-ttu-id="7ac60-129">Шаг исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="7ac60-129">The stride of the source image.</span></span>
-   <span data-ttu-id="7ac60-130">Ширина изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7ac60-130">The width of the image in pixels.</span></span>
-   <span data-ttu-id="7ac60-131">Высота изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7ac60-131">The height of the image in pixels.</span></span>

<span data-ttu-id="7ac60-132">Основная идея состоит в том, чтобы обрабатывать по одной строке за раз, просматривая каждый пиксель в строке.</span><span class="sxs-lookup"><span data-stu-id="7ac60-132">The general idea is to process one row at a time, iterating over each pixel in the row.</span></span> <span data-ttu-id="7ac60-133">Предположим, что исходный тип и тип пиксельного пиксела \_ \_ \_ \_ являются структурами, представляющими макет пикселей для исходных и целевых изображений соответственно.</span><span class="sxs-lookup"><span data-stu-id="7ac60-133">Assume that SOURCE\_PIXEL\_TYPE and DEST\_PIXEL\_TYPE are structures representing the pixel layout for the source and destination images, respectively.</span></span> <span data-ttu-id="7ac60-134">(Например, в 32-разрядном RGB используется структура [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) .</span><span class="sxs-lookup"><span data-stu-id="7ac60-134">(For example, 32-bit RGB uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure.</span></span> <span data-ttu-id="7ac60-135">Не каждый формат пикселей имеет стандартную структуру.) Приведение указателя массива к типу структуры позволяет получить доступ к компонентам RGB или YUV каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="7ac60-135">Not every pixel format has a predefined structure.) Casting the array pointer to the structure type enables you to access the RGB or YUV components of each pixel.</span></span> <span data-ttu-id="7ac60-136">В начале каждой строки функция сохраняет указатель на строку.</span><span class="sxs-lookup"><span data-stu-id="7ac60-136">At the start of each row, the function stores a pointer to the row.</span></span> <span data-ttu-id="7ac60-137">В конце строки указатель увеличивается на ширину шага изображения, что перемещает указатель на следующую строку.</span><span class="sxs-lookup"><span data-stu-id="7ac60-137">At the end of the row, it increments the pointer by the width of the image stride, which advances the pointer to the next row.</span></span>

<span data-ttu-id="7ac60-138">В этом примере вызывается гипотетическая функция с именем Трансформпикселвалуе для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="7ac60-138">This example calls a hypothetical function named TransformPixelValue for each pixel.</span></span> <span data-ttu-id="7ac60-139">Это может быть любая функция, которая вычисляет целевой пиксель из исходного пикселя.</span><span class="sxs-lookup"><span data-stu-id="7ac60-139">This could be any function that calculates a target pixel from a source pixel.</span></span> <span data-ttu-id="7ac60-140">Конечно, точные сведения будут зависеть от конкретной задачи.</span><span class="sxs-lookup"><span data-stu-id="7ac60-140">Of course, the exact details will depend on the particular task.</span></span> <span data-ttu-id="7ac60-141">Например, при наличии плоского формата YUV необходимо получить доступ к плоскостям чрома независимо от плоскости яркости. При использовании чередования видео может потребоваться обработка полей по отдельности. и т. д.</span><span class="sxs-lookup"><span data-stu-id="7ac60-141">For example, if you have a planar YUV format, you must access the chroma planes independently from the luma plane; with interlaced video, you might need to process the fields separately; and so forth.</span></span>

<span data-ttu-id="7ac60-142">Чтобы придать более конкретный пример, следующий код преобразует 32-битное изображение RGB в образ АЙУВ.</span><span class="sxs-lookup"><span data-stu-id="7ac60-142">To give a more concrete example, the following code converts a 32-bit RGB image into an AYUV image.</span></span> <span data-ttu-id="7ac60-143">Доступ к пикселям RGB осуществляется с помощью структуры [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , а доступ к айув пикселей осуществляется с помощью структуры структуры [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .</span><span class="sxs-lookup"><span data-stu-id="7ac60-143">The RGB pixels are accessed using an [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure, and the AYUV pixels are accessed using a [**DXVA2\_AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) structure structure.</span></span>


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



<span data-ttu-id="7ac60-144">В следующем примере показано преобразование 32-битного изображения RGB в образ YV12.</span><span class="sxs-lookup"><span data-stu-id="7ac60-144">The next example converts a 32-bit RGB image to a YV12 image.</span></span> <span data-ttu-id="7ac60-145">В этом примере показано, как управлять плоским форматом YUV.</span><span class="sxs-lookup"><span data-stu-id="7ac60-145">This example shows how to handle a planar YUV format.</span></span> <span data-ttu-id="7ac60-146">(YV12 имеет формат плоской 4:2:0.) В этом примере функция поддерживает три отдельных указателя для трех плоскостей в целевом изображении.</span><span class="sxs-lookup"><span data-stu-id="7ac60-146">(YV12 is a planar 4:2:0 format.) In this example, the function maintains three separate pointers for the three planes in the target image.</span></span> <span data-ttu-id="7ac60-147">Однако базовый подход тот же, что и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="7ac60-147">However, the basic approach is the same as the previous example.</span></span>


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



<span data-ttu-id="7ac60-148">Во всех этих примерах предполагается, что приложение уже определило шаг изображения.</span><span class="sxs-lookup"><span data-stu-id="7ac60-148">In all of these examples, it is assumed that the application has already determined the image stride.</span></span> <span data-ttu-id="7ac60-149">Иногда эти сведения можно получить из буфера мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7ac60-149">You can sometimes get this information from the media buffer.</span></span> <span data-ttu-id="7ac60-150">В противном случае необходимо вычислить его на основе формата видео.</span><span class="sxs-lookup"><span data-stu-id="7ac60-150">Otherwise, you must calculate it based on the video format.</span></span> <span data-ttu-id="7ac60-151">Дополнительные сведения о вычислении шага образа и работе с буферами мультимедиа для видео см. в разделе [несжатые Видеобуферы](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="7ac60-151">For more information about calculating image stride and working with media buffers for video, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ac60-152">См. также</span><span class="sxs-lookup"><span data-stu-id="7ac60-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ac60-153">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="7ac60-153">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="7ac60-154">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="7ac60-154">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
