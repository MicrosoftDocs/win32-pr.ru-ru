---
description: В этом разделе показано, как можно изменить громкость голоса на общем уровне, на каждом выходном канале или между каждым каналом голоса и другим голосовым сендлист.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: Как изменить громкость голоса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab433cc0e5c0e3ddc4bea3c58f49afae36cf8833fa8f003c99f1c45b237c70a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696261"
---
# <a name="how-to-change-voice-volume"></a>Как изменить громкость голоса

В этом разделе показано, как можно изменить громкость голоса на общем уровне, на каждом выходном канале или между каждым каналом голоса и другим голосовым [**сендлист**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a>Установка общего уровня громкости для входных данных голоса

-   Используйте функцию [**сетволуме**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a>Задание объема выходных каналов голоса

1.  Создайте массив чисел с плавающей запятой, содержащих нужные тома всех выходных каналов в голоса.

    Массив будет иметь одну запись для каждого канала в голоса.

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  Используйте функцию [**сетчаннелволумес**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) , чтобы задать объем выходных каналов.

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a>Задание объема подключений

Установите в [**сендлист**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)том соединения между голосовым и голосовым.

1.  Создайте массив чисел с плавающей запятой, определяющий выходную матрицу, если голоса отправляется другому голосовому.

    > [!Note]  
    > Массив должен иметь несколько записей, равных исходным голосовым каналам х назначения. В этом примере Сопоставление осуществляется из голоса с одним каналом на голоса с двумя каналами.

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  Чтобы задать выходную матрицу, используйте функцию [**сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) .

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Элемент управления громкостью и шагом XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
