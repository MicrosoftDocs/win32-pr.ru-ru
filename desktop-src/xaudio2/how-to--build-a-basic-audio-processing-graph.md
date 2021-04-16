---
description: Минимальным требованием для включения XAudio2 для воспроизведения звуковых данных является график обработки звука, который формируется на основе одного голоса для главной системы и одного исходного голоса.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Руководство: создание базовой схемы обработки звука'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712285"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>Руководство: создание базовой схемы обработки звука

Минимальным требованием для включения XAudio2 для воспроизведения звуковых данных является график обработки звука, который формируется на основе одного голоса для главной системы и одного исходного голоса.

## <a name="to-build-a-basic-audio-processing-graph"></a>Создание базового графика обработки звука

1.  Инициализируйте подсистему XAudio2, выполнив действия, описанные в разделе [инструкции. Инициализация XAudio2](how-to--initialize-xaudio2.md).
2.  Заполните структуру [**\_ буфера**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **вавеформатекс** и XAUDIO2, выполнив действия, описанные в разделе [как загружать файлы аудиоданных в XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).
3.  Создайте исходный голоса с помощью функции [**креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .

    Если для аргумента Псендлист параметра [**креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)указано значение null, выходные данные исходного голоса будут переводиться на основной язык, созданный на шаге 1.

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    После завершения этого шага появляется простой графический график, состоящий из исходного голоса, голоса для главной системы и звукового устройства. Оставшиеся действия, описанные в этом разделе, показывают, как начать передачу звуковых данных через граф.

    Простая звуковая диаграмма

    ![простая звуковая диаграмма.](images/xaudio2-audio-graph.png)

4.  Используйте функцию [**субмитсаурцебуффер**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) для отправки [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) в исходный голоса.

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  Используйте функцию [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) для запуска исходного голоса.

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Графики воспроизведения](audio-graphs.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> </dl>

 

 
