---
title: Обработка видео
description: Обработка видео
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP видео
- подключаемые модули, DSP видео
- подключаемые модули обработки цифровых сигналов, обработка видео
- Подключаемые модули DSP, обработка видео
- подключаемые модули DSP видео, обработка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8d21aaa3999d05ea3628ff341c74379b07a6dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070186"
---
# <a name="processing-the-video"></a><span data-ttu-id="38a0a-108">Обработка видео</span><span class="sxs-lookup"><span data-stu-id="38a0a-108">Processing the Video</span></span>

<span data-ttu-id="38a0a-109">Сведения об обработке видео зависят от формата. Это не относится к этой документации, чтобы предоставить эти сведения.</span><span class="sxs-lookup"><span data-stu-id="38a0a-109">The details of processing video vary for each format; it is beyond the scope of this documentation to provide these details.</span></span> <span data-ttu-id="38a0a-110">В общем смысле, цель подключаемого модуля заключается в изменении цветовых данных во входном буфере и последующем копировании данных в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="38a0a-110">In a general sense, the goal of the plug-in is to change the color data in the input buffer and then copy the data to the output buffer.</span></span>

<span data-ttu-id="38a0a-111">Пример подключаемого модуля обрабатывает два типа видео форматов: YUV и RGB.</span><span class="sxs-lookup"><span data-stu-id="38a0a-111">The sample plug-in processes two types of video formats: YUV and RGB.</span></span>

<span data-ttu-id="38a0a-112">Для видеороликов YUV сведения о цветах красного и синего цвета кодируются в значениях параметров «вы» и «V», а уровень освещенности представляется значением Y. значение зеленого цвета кодируется и может быть восстановлено с помощью алгоритма.</span><span class="sxs-lookup"><span data-stu-id="38a0a-112">For YUV video, the red and blue color information is encoded in the U and V values and the luminance level is represented by the Y value; the green value is encoded and can be recovered by using an algorithm.</span></span> <span data-ttu-id="38a0a-113">Пример подключаемого модуля просто изменяет значения параметров "вы" и "V", чтобы они влияли на уровень цвета.</span><span class="sxs-lookup"><span data-stu-id="38a0a-113">The sample plug-in simply changes the U and V values to affect the color level.</span></span> <span data-ttu-id="38a0a-114">Каждый байт U или V имеет значение от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="38a0a-114">Each U or V byte has a value between zero and 255.</span></span> <span data-ttu-id="38a0a-115">Подключаемый модуль сначала корректирует каждое значение, чтобы оно было представлено диапазоном от-128 до 127, а затем масштабирует значение по предоставленному коэффициенту масштабирования.</span><span class="sxs-lookup"><span data-stu-id="38a0a-115">The plug-in first adjusts each value to be represented by a range from -128 to 127, and then scales the value by the supplied scale factor.</span></span> <span data-ttu-id="38a0a-116">Наконец, код настраивает значение еще раз для исходного диапазона от нуля до 255 и копирует данные в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="38a0a-116">Finally, the code adjusts the value again for the original zero-to-255 range and copies the data to the output buffer.</span></span> <span data-ttu-id="38a0a-117">В следующем примере кода обрабатывается видео UYVY.</span><span class="sxs-lookup"><span data-stu-id="38a0a-117">The following example code processes UYVY video.</span></span> <span data-ttu-id="38a0a-118">В этом формате каждый второй байт имеет значение U или Y.</span><span class="sxs-lookup"><span data-stu-id="38a0a-118">In this format, every other byte is a U or Y value.</span></span>


```C++
while( dwHeight-- )
{
    DWORD x = dwWidth; 

        while( x-- )
        {
        // Scale the U and V bytes to 128.
        // Just copy the Y bytes.
        if( x%2 )
        {
            pbTarget[x] = pbSource[x];
        }
        else
        {
            long temp = (long)((pbSource[x] - 128) * m_fScaleFactor);

            // Truncate if exceeded full scale.
            if (temp > 127)
            temp = 127;
            if (temp < -128)
            temp = -128;

            pbTarget[x] = temp + 128;
        }
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="38a0a-119">Для видео в формате RGB сведения о цвете и освещенности кодируются как отдельные значения красного, зеленого и синего.</span><span class="sxs-lookup"><span data-stu-id="38a0a-119">For RGB video, the color and luminance information is encoded as separate red, green, and blue values.</span></span> <span data-ttu-id="38a0a-120">Пример подключаемого модуля вычисляет среднее из трех значений, чтобы определить значение серого, а затем корректирует каждое значение цвета с помощью предоставленного коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="38a0a-120">The sample plug-in computes the average of the three values to determine the value for gray, and then adjusts each color value by using the supplied scale factor.</span></span> <span data-ttu-id="38a0a-121">Опять же, перед масштабированием значения должны быть нормализованы для диапазона от-128 до 127.</span><span class="sxs-lookup"><span data-stu-id="38a0a-121">Once again, the values must be normalized for the -128 to 127 range before scaling.</span></span> <span data-ttu-id="38a0a-122">В следующем коде из Process32Bit показан процесс для RGB32:</span><span class="sxs-lookup"><span data-stu-id="38a0a-122">The following code from Process32Bit shows the process for RGB32:</span></span>


```C++
while( dwHeight-- )
{
    RGBQUAD* pPixelIn = (RGBQUAD*)pbSource;
    RGBQUAD* pPixelOut = (RGBQUAD*)pbTarget;

    for( DWORD x = 0; x < dwWidth; x++ )
    {
    // Get the color bytes.
    long lBlue = (long) pPixelIn[x].rgbBlue;
    long lGreen = (long) pPixelIn[x].rgbGreen;
    long lRed = (long) pPixelIn[x].rgbRed;

    // Compute the average for gray.
    long lAverage = ( lBlue + lGreen + lRed ) / 3;

    // Scale the colors to the average.
    pPixelOut[x].rgbBlue = (BYTE)( ( lBlue - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbGreen = (BYTE)( ( lGreen - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbRed = (BYTE)( ( lRed - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbReserved = pPixelIn[x].rgbReserved;
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="38a0a-123">Дополнительные сведения о форматах видео см. на [веб-сайте FourCC](../directshow/fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="38a0a-123">For more information about video formats, see the [FourCC website](../directshow/fourcc-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="38a0a-124">См. также</span><span class="sxs-lookup"><span data-stu-id="38a0a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38a0a-125">**Реализация подключаемого модуля DSP видео**</span><span class="sxs-lookup"><span data-stu-id="38a0a-125">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 