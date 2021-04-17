---
description: Настройка типа носителя группы
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Настройка типа носителя группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674541"
---
# <a name="setting-the-group-media-type"></a>Настройка типа носителя группы

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

Все группы должны определять несжатый тип носителя: аудио или видео. Тип носителя без сжатия — это формат, который зрители видят или прослушивают во время воспроизведения. Как правило, окончательный результат будет иметь сжатый формат. Дополнительные сведения см. [в разделе Подготовка проекта к просмотру](rendering-a-project.md).

Чтобы задать несжатый формат, создайте структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) и заполните ее соответствующим старшим типом, подтипом и заголовком формата. Для видео выделите структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) для блока Format и задайте ширину, высоту и глубину цвета. Для звука необходимо выделить структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) для блока Format и задать частоту выборки, глубину и число каналов. Если задать только основной тип, DES предоставляет значения по умолчанию для других значений. На практике необходимо явно задать значения для управления выходными данными.

После инициализации структуры типа мультимедиа вызовите метод [**иамтимелинеграуп:: сетмедиатипе**](iamtimelinegroup-setmediatype.md) , чтобы задать тип носителя для группы.

В следующем примере задается 16-разрядное видео RGB, 320 пикселей в ширину на 240 пикселей в высоком формате:


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



В следующем примере указана звуковая группа с указанием для типа носителя группы 16-разрядный стерео, 44100 выборок в секунду:


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



Для управления типами мультимедиа можно также использовать класс [**кмедиатипе**](cmediatype.md) в [базовых классах DirectShow](directshow-base-classes.md) . Он содержит некоторые полезные вспомогательные методы и автоматически освобождает блок формата.

## <a name="related-topics"></a>См. также

<dl> <dt>

[О типах носителей](about-media-types.md)
</dt> <dt>

[Создание временной шкалы](constructing-a-timeline.md)
</dt> </dl>

 

 
