---
description: Вы можете выполнять потоковую передачу звуковых данных в XAudio2, создавая отдельный поток и выполняя операции чтения звуковых данных в потоке потоковой передачи, а затем используя обратные вызовы для управления этим потоком.
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: 'Руководство: организация звукового потока с диска'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c5598e8913514d6b0bf81b55bab5b481dbc43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815273"
---
# <a name="how-to-stream-a-sound-from-disk"></a>Руководство: организация звукового потока с диска

> [!Note]  
> Это содержимое применимо только к классическим приложениям, и для работы в приложении Магазина Windows потребуется редакция. Обратитесь к документации по **CreateFile2**, [креативентекс](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [сетфилепоинтерекс](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)и **жетоверлаппедресултекс**. См. пример Стреамеффект Windows 8 из [коллекции примеров Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).

 

Вы можете выполнять потоковую передачу звуковых данных в XAudio2, создавая отдельный поток и выполняя операции чтения звуковых данных в потоке потоковой передачи, а затем используя обратные вызовы для управления этим потоком.

-   [Выполнение операций чтения буфера в потоке потоковой передачи](#performing-buffer-reads-in-the-streaming-thread)
-   [Создание класса обратного вызова](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a>Выполнение операций чтения буфера в потоке потоковой передачи

Чтобы выполнить операции чтения буфера в потоке потоковой передачи, выполните следующие действия:

1.  Создайте массив буферов чтения.

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  Инициализация структуры с перекрытием.

    Структура используется для проверки завершения асинхронного чтения с диска.

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  Вызовите функцию [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) для [**исходного голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) , который будет воспроизводить потоковую передачу звука.

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  Цикл, пока текущая точка чтения не прошла конец звукового файла.

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    В цикле выполните следующие действия.

    1.  Считывает фрагмент данных с диска в текущий буфер чтения.

        ```
        DWORD dwRead;
        if( SUCCEEDED(hr) && 0 == ReadFile( hFile, pData, dwDataSize, &dwRead, pOverlapped ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
            DWORD cbValid = min( STREAMING_BUFFER_SIZE, cbWaveSize - CurrentPosition );
            DWORD dwRead;
            if( 0 == ReadFile( hFile, buffers[CurrentDiskReadBuffer], STREAMING_BUFFER_SIZE, &dwRead, &Overlapped ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );
            Overlapped.Offset += cbValid;

            //update the file position to where it will be once the read finishes
            CurrentPosition += cbValid;
        ```

        

    2.  Используйте функцию **GetOverlappedResult** для ожидания события, которое сигнализирует о завершении чтения.

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  Подождите, пока количество буферов, помещенных в очередь [**исходного голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) , будет меньше числа буферов чтения.

        Состояние [**исходного голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) проверяется с помощью функции- [**State**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  Отправьте текущий буфер чтения в [**Исходный голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) с помощью функции [**субмитсаурцебуффер**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .

        ```
        XAUDIO2_BUFFER buf = {0};
        buf.AudioBytes = cbValid;
        buf.pAudioData = buffers[CurrentDiskReadBuffer];
        if( CurrentPosition >= cbWaveSize )
        {
            buf.Flags = XAUDIO2_END_OF_STREAM;
        }
        pSourceVoice->SubmitSourceBuffer( &buf );
        ```

        

    5.  Установите текущий индекс буфера чтения в следующий буфер.

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  После завершения цикла дождитесь завершения воспроизведения оставшихся буферов в очереди.

    Когда оставшиеся буферы завершают воспроизведение, звук останавливается, и поток может выйти из программы или повторно использовать для потоковой передачи другого звука.

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a>Создание класса обратного вызова

Чтобы создать класс обратного вызова, создайте класс, наследующий от интерфейса [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .

Класс должен задавать событие в методе [**онбуфференд**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) . Это позволяет потоку потоковой передачи переключаться в спящий режим до тех пор, пока событие не выдает ему сигнал о том, что XAudio2 закончил чтение из буфера аудио. Дополнительные сведения об использовании обратных вызовов с XAudio2 см. [в статье Использование исходных обратных вызовов](how-to--use-source-voice-callbacks.md).


```
struct StreamingVoiceContext : public IXAudio2VoiceCallback
{
    HANDLE hBufferEndEvent;
    StreamingVoiceContext(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
    ~StreamingVoiceContext(){ CloseHandle( hBufferEndEvent ); }
    void OnBufferEnd( void* ){ SetEvent( hBufferEndEvent ); }
    ...
};
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Потоковая передача звуковых данных](streaming-audio-data.md)
</dt> <dt>

[Обратные вызовы в XAudio2](callbacks.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Руководство: использование обратных вызовов речевых источников](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
