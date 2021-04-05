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
# <a name="how-to-stream-a-sound-from-disk"></a><span data-ttu-id="b1f3c-103">Руководство: организация звукового потока с диска</span><span class="sxs-lookup"><span data-stu-id="b1f3c-103">How to: Stream a Sound from Disk</span></span>

> [!Note]  
> <span data-ttu-id="b1f3c-104">Это содержимое применимо только к классическим приложениям, и для работы в приложении Магазина Windows потребуется редакция.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="b1f3c-105">Обратитесь к документации по **CreateFile2**, [креативентекс](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [сетфилепоинтерекс](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)и **жетоверлаппедресултекс**.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-105">Please refer to the documentation for **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and **GetOverlappedResultEx**.</span></span> <span data-ttu-id="b1f3c-106">См. пример Стреамеффект Windows 8 из [коллекции примеров Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="b1f3c-106">See the StreamEffect Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="b1f3c-107">Вы можете выполнять потоковую передачу звуковых данных в XAudio2, создавая отдельный поток и выполняя операции чтения звуковых данных в потоке потоковой передачи, а затем используя обратные вызовы для управления этим потоком.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-107">You can stream audio data in XAudio2 by creating a separate thread and perform buffer reads of the audio data in the streaming thread, and then use callbacks to control that thread.</span></span>

-   [<span data-ttu-id="b1f3c-108">Выполнение операций чтения буфера в потоке потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="b1f3c-108">Performing buffer reads in the streaming thread</span></span>](#performing-buffer-reads-in-the-streaming-thread)
-   [<span data-ttu-id="b1f3c-109">Создание класса обратного вызова</span><span class="sxs-lookup"><span data-stu-id="b1f3c-109">Creating the callback class</span></span>](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a><span data-ttu-id="b1f3c-110">Выполнение операций чтения буфера в потоке потоковой передачи</span><span class="sxs-lookup"><span data-stu-id="b1f3c-110">Performing buffer reads in the streaming thread</span></span>

<span data-ttu-id="b1f3c-111">Чтобы выполнить операции чтения буфера в потоке потоковой передачи, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b1f3c-111">To perform buffer reads in the streaming thread follow these steps:</span></span>

1.  <span data-ttu-id="b1f3c-112">Создайте массив буферов чтения.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-112">Create an array of read buffers.</span></span>

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  <span data-ttu-id="b1f3c-113">Инициализация структуры с перекрытием.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-113">Initialize an OVERLAPPED structure.</span></span>

    <span data-ttu-id="b1f3c-114">Структура используется для проверки завершения асинхронного чтения с диска.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-114">The structure is used to check when an asynchronous disk read has finished.</span></span>

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  <span data-ttu-id="b1f3c-115">Вызовите функцию [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) для [**исходного голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) , который будет воспроизводить потоковую передачу звука.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-115">Call the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) that will be playing the streaming audio.</span></span>

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  <span data-ttu-id="b1f3c-116">Цикл, пока текущая точка чтения не прошла конец звукового файла.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-116">Loop while the current read position is not passed the end of the audio file.</span></span>

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    <span data-ttu-id="b1f3c-117">В цикле выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-117">In the loop, do the following:</span></span>

    1.  <span data-ttu-id="b1f3c-118">Считывает фрагмент данных с диска в текущий буфер чтения.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-118">Read a chunk of data from the disk into the current read buffer.</span></span>

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

        

    2.  <span data-ttu-id="b1f3c-119">Используйте функцию **GetOverlappedResult** для ожидания события, которое сигнализирует о завершении чтения.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-119">Use the **GetOverlappedResult** function to wait for the event that signals the read has finished.</span></span>

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  <span data-ttu-id="b1f3c-120">Подождите, пока количество буферов, помещенных в очередь [**исходного голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) , будет меньше числа буферов чтения.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-120">Wait for the number of buffers queued on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) to be less than the number of read buffers.</span></span>

        <span data-ttu-id="b1f3c-121">Состояние [**исходного голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) проверяется с помощью функции- [**State**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .</span><span class="sxs-lookup"><span data-stu-id="b1f3c-121">The state of the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) is checked with the [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) function.</span></span>

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  <span data-ttu-id="b1f3c-122">Отправьте текущий буфер чтения в [**Исходный голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) с помощью функции [**субмитсаурцебуффер**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .</span><span class="sxs-lookup"><span data-stu-id="b1f3c-122">Submit the current read buffer to the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) using the [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) function.</span></span>

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

        

    5.  <span data-ttu-id="b1f3c-123">Установите текущий индекс буфера чтения в следующий буфер.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-123">Set the current read buffer index to the next buffer.</span></span>

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  <span data-ttu-id="b1f3c-124">После завершения цикла дождитесь завершения воспроизведения оставшихся буферов в очереди.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-124">After the loop has finished, wait for the remaining queued buffers to finish playing.</span></span>

    <span data-ttu-id="b1f3c-125">Когда оставшиеся буферы завершают воспроизведение, звук останавливается, и поток может выйти из программы или повторно использовать для потоковой передачи другого звука.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-125">When the remaining buffers have finished playing, the sound stops, and the thread can exit or be reused to stream another sound.</span></span>

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a><span data-ttu-id="b1f3c-126">Создание класса обратного вызова</span><span class="sxs-lookup"><span data-stu-id="b1f3c-126">Creating the callback class</span></span>

<span data-ttu-id="b1f3c-127">Чтобы создать класс обратного вызова, создайте класс, наследующий от интерфейса [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="b1f3c-127">To create the callback class, create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span>

<span data-ttu-id="b1f3c-128">Класс должен задавать событие в методе [**онбуфференд**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) .</span><span class="sxs-lookup"><span data-stu-id="b1f3c-128">The class should set an event in its [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) method.</span></span> <span data-ttu-id="b1f3c-129">Это позволяет потоку потоковой передачи переключаться в спящий режим до тех пор, пока событие не выдает ему сигнал о том, что XAudio2 закончил чтение из буфера аудио.</span><span class="sxs-lookup"><span data-stu-id="b1f3c-129">This allows the streaming thread to put itself to sleep until the event signals it that XAudio2 has finished reading from an audio buffer.</span></span> <span data-ttu-id="b1f3c-130">Дополнительные сведения об использовании обратных вызовов с XAudio2 см. [в статье Использование исходных обратных вызовов](how-to--use-source-voice-callbacks.md).</span><span class="sxs-lookup"><span data-stu-id="b1f3c-130">For more information about using callbacks with XAudio2, see [How to: Use Source Voice Callbacks](how-to--use-source-voice-callbacks.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b1f3c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b1f3c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1f3c-132">Потоковая передача звуковых данных</span><span class="sxs-lookup"><span data-stu-id="b1f3c-132">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="b1f3c-133">Обратные вызовы в XAudio2</span><span class="sxs-lookup"><span data-stu-id="b1f3c-133">XAudio2 Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="b1f3c-134">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="b1f3c-134">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="b1f3c-135">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="b1f3c-135">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="b1f3c-136">Руководство: использование обратных вызовов речевых источников</span><span class="sxs-lookup"><span data-stu-id="b1f3c-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
