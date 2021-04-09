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
# <a name="processing-the-video"></a>Обработка видео

Сведения об обработке видео зависят от формата. Это не относится к этой документации, чтобы предоставить эти сведения. В общем смысле, цель подключаемого модуля заключается в изменении цветовых данных во входном буфере и последующем копировании данных в выходной буфер.

Пример подключаемого модуля обрабатывает два типа видео форматов: YUV и RGB.

Для видеороликов YUV сведения о цветах красного и синего цвета кодируются в значениях параметров «вы» и «V», а уровень освещенности представляется значением Y. значение зеленого цвета кодируется и может быть восстановлено с помощью алгоритма. Пример подключаемого модуля просто изменяет значения параметров "вы" и "V", чтобы они влияли на уровень цвета. Каждый байт U или V имеет значение от 0 до 255. Подключаемый модуль сначала корректирует каждое значение, чтобы оно было представлено диапазоном от-128 до 127, а затем масштабирует значение по предоставленному коэффициенту масштабирования. Наконец, код настраивает значение еще раз для исходного диапазона от нуля до 255 и копирует данные в выходной буфер. В следующем примере кода обрабатывается видео UYVY. В этом формате каждый второй байт имеет значение U или Y.


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



Для видео в формате RGB сведения о цвете и освещенности кодируются как отдельные значения красного, зеленого и синего. Пример подключаемого модуля вычисляет среднее из трех значений, чтобы определить значение серого, а затем корректирует каждое значение цвета с помощью предоставленного коэффициента масштабирования. Опять же, перед масштабированием значения должны быть нормализованы для диапазона от-128 до 127. В следующем коде из Process32Bit показан процесс для RGB32:


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



Дополнительные сведения о форматах видео см. на [веб-сайте FourCC](../directshow/fourcc-codes.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Реализация подключаемого модуля DSP видео**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 