---
description: При создании исходного голоса можно передать ему структуру, которая определяет обратные вызовы для определенных событий аудио. Эти обратные вызовы можно использовать для выполнения действий или для сигнализации другого кода.
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: 'Руководство: использование обратных вызовов речевых источников'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c10005ed838a22ea0dfce59312d6f293c213c39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810468"
---
# <a name="how-to-use-source-voice-callbacks"></a>Руководство: использование обратных вызовов речевых источников

При создании исходного голоса можно передать ему структуру, которая определяет обратные вызовы для определенных событий аудио. Эти обратные вызовы можно использовать для выполнения действий или для сигнализации другого кода.

1.  Создайте класс, наследующий от интерфейса [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) . Все функции элементов **IXAudio2VoiceCallback** являются исключительно виртуальными и должны быть определены. Единственная интересная функция в этом примере — [**онстреаменд**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend). Поэтому остальные функции являются заглушками. Функция **онстреаменд** запускает событие, показывающее, что воспроизведение звука завершено.

    ```
    class VoiceCallback : public IXAudio2VoiceCallback
    {
    public:
        HANDLE hBufferEndEvent;
        VoiceCallback(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
        ~VoiceCallback(){ CloseHandle( hBufferEndEvent ); }

        //Called when the voice has just finished playing a contiguous audio stream.
        void OnStreamEnd() { SetEvent( hBufferEndEvent ); }

        //Unused methods are stubs
        void OnVoiceProcessingPassEnd() { }
        void OnVoiceProcessingPassStart(UINT32 SamplesRequired) {    }
        void OnBufferEnd(void * pBufferContext)    { }
        void OnBufferStart(void * pBufferContext) {    }
        void OnLoopEnd(void * pBufferContext) {    }
        void OnVoiceError(void * pBufferContext, HRESULT Error) { }
    };
    ```

    

2.  Создайте [**Исходный голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) с помощью [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) , используя экземпляр класса обратного вызова, созданный ранее в качестве параметра пкаллбакк.

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  После запуска голоса используйте метод [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) , чтобы дождаться срабатывания события.

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обратные вызовы](callbacks.md)
</dt> <dt>

[Обратные вызовы в XAudio2](xaudio2-callbacks.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Руководство: организация звукового потока с диска](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
