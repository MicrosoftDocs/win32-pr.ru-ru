---
description: В этом разделе показано, как можно задать выходную матрицу исходного голоса Mono, которая выводит на стерео-находящийся звуковой поток, чтобы выполнить панорамирование между левым и верным динамиками.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: Как сдвигать звук
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e91ff27dfe7c951f95c37fed194a83dac09de8ccec7e37ebc5ad35ca548199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696273"
---
# <a name="how-to-pan-a-sound"></a>Как сдвигать звук

В этом разделе показано, как можно задать выходную матрицу исходного голоса Mono, которая выводит на стерео-находящийся звуковой поток, чтобы выполнить панорамирование между левым и верным динамиками.

## <a name="to-setup-panning"></a>Настройка панорамирования

1.  Извлеките конфигурацию динамика с помощью [**IXAudio2MasteringVoice:: жетчаннелмаск**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  Создайте массив для хранения выходной матрицы. Минимальный размер выходной матрицы — число каналов в исходном речевом формате, которое превышает количество каналов в выходном голосовом потоке. В этом случае восемь массивов элементов будут обработаны в любом выходном формате до 7,1ного звучания.

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  Вычислите уровни отправки на основе требуемого панорамирования между левым и верным колонками. В этом примере значения панорамы будут находиться в диапазоне от-1 до 1 с параметром-1, что означает, что весь звук отображается на левом динамике, а 1 — на правом докладчике.

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  Задайте индексы выходной матрицы, соответствующие левым и правым колонкам, со значениями, вычисленными на предыдущем шаге. Левый и правый динамики определяются по маске канала, возвращенной [**IXAudio2MasteringVoice:: жетчаннелмаск**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask). Так как каналы всегда должны быть закодированы в порядке, указанном на странице ссылки [**вавеформатекстенсибле**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , можно определить индекс массива, соответствующий отдельному докладчику.

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  Примените выходную матрицу к исходному голосовому счету с помощью [**IXAudio2Voice:: сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix). Исходным голосовым назначением является либо исходный или субмикс, либо отправка голоса на субмикс или на основной Voice. Сведения об исходном и целевом голоса, например их количестве каналов, можно получить с помощью [**IXAudio2Voice:: жетвоицедетаилс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Элемент управления громкостью и шагом XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
