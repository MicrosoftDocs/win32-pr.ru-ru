---
description: Настройка типов мультимедиа для DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Настройка типов мультимедиа для DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684781"
---
# <a name="setting-media-types-on-a-dmo"></a>Настройка типов мультимедиа для DMO

Прежде чем DMO сможет обработать какие-либо данные, клиент должен задать тип носителя для каждого потока. (Для этого правила существует одно небольшое исключение; см. [дополнительные потоки](optional-streams.md).) Чтобы узнать число потоков, вызовите метод [**имедиаобжект:: жетстреамкаунт**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Этот метод возвращает два значения, число входов и число выходов. Эти значения фиксируются в течение времени существования DMO.

**Предпочтительные типы**

Для каждого потока DMO назначает список возможных типов носителей в порядке предпочтения. Например, в этом порядке предпочтительными типами могут быть 32-RGB, 24-разрядный RGB и 16-разрядный RGB. Когда клиент задает типы носителей, он может использовать эти списки в качестве подсказки. Чтобы получить предпочтительный тип для потока, вызовите метод [**имедиаобжект:: жетинпуттипе**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) или [**Имедиаобжект:: жетаутпуттипе**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) . Укажите номер потока и значение индекса для типа (начиная с нуля). Например, следующий код извлекает первый предпочтительный тип из первого входного потока:


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



Чтобы перечислить все предпочтительные типы мультимедиа в заданном потоке, используйте цикл, увеличивающий индекс типа до тех пор, пока метод \_ не вернет DMO \_ \_ \_ , а не больше элементов, как показано в следующем примере:


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



Обратите внимание на следующие моменты о предпочтительных типах:

-   DMO может возвращать тип, не имеющий блока Format. Например, DMO может указать тип видео, например 24-разрядный RGB, без указания ширины и высоты изображения. Однако при задании типа необходимо указать полный блок формата. (Некоторые типы носителей, например MIDI, никогда не нуждаются в блоке формата, в этом случае это замечание не применяется.)
-   DMO не требуется поддерживать каждое сочетание предпочтительных типов, которые он возвращает. Например, если у DMO есть два потока, и каждый поток имеет четыре основных типа, существует 16 возможных сочетаний, но не все они гарантированно являются допустимыми.
-   Когда клиент задает тип носителя для одного потока, DMO может обновить предпочтительные типы для других потоков, чтобы отразить новое состояние. Однако это не обязательно.
-   Для некоторых потоков DMO может не предлагать никаких предпочтительных типов. Как правило, DMO должен предлагать по крайней мере некоторые предпочтительные типы в некоторых потоках.
-   DMO не требуется для предоставления полного списка типов мультимедиа, которые он может принять. Могут существовать "необъявленные" типы, которые поддерживаются DMO, но не предлагаются в качестве предпочитаемых типов.

Вкратце, клиент должен рассматривать предпочтительные типы как только рекомендации. Единственный способ убедиться в том, какие типы поддерживаются, — это проверить их, как описано в следующем разделе.

**Установка типа мультимедиа в потоке**

Используйте методы [**имедиаобжект:: сетинпуттипе**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) и [**Имедиаобжект:: сетаутпуттипе**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) , чтобы задать тип для каждого потока. Необходимо предоставить структуру **\_ \_ типа мультимедиа DMO** , содержащую полное описание типа мультимедиа. В следующем примере задается тип мультимедиа в потоке входных данных 0 с использованием 16-разрядного стереозвука стерео 44,1-кГц:


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



Чтобы проверить тип мультимедиа, не настроив его, вызовите **сетинпуттипе** или **сетаутпуттипе** с \_ \_ флагом DMO Set типеф \_ только тестовый \_ . Метод возвращает значение S \_ , если тип приемлем, или \_ false в противном случае:


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Поскольку параметры одного потока могут повлиять на другой поток, может потребоваться очистить тип носителя потока. Для этого вызовите **сетинпуттипе** или **СЕТАУТПУТТИПЕ** с помощью DMO \_ Set \_ типеф \_ clear флаг.

Для декодера DMO клиент, как правило, должен сначала задать входной тип, а затем выбрать тип выходных данных. Для кодировщика DMO клиент должен сначала задать тип вывода, а затем тип входных данных.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Непосредственное размещение DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



