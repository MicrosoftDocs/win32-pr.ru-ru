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
# <a name="how-to-use-source-voice-callbacks"></a><span data-ttu-id="e7324-104">Руководство: использование обратных вызовов речевых источников</span><span class="sxs-lookup"><span data-stu-id="e7324-104">How to: Use Source Voice Callbacks</span></span>

<span data-ttu-id="e7324-105">При создании исходного голоса можно передать ему структуру, которая определяет обратные вызовы для определенных событий аудио.</span><span class="sxs-lookup"><span data-stu-id="e7324-105">When you create a source voice, you can pass a structure to it that defines callbacks for certain audio events.</span></span> <span data-ttu-id="e7324-106">Эти обратные вызовы можно использовать для выполнения действий или для сигнализации другого кода.</span><span class="sxs-lookup"><span data-stu-id="e7324-106">You can use these callbacks to perform actions or to signal other code.</span></span>

1.  <span data-ttu-id="e7324-107">Создайте класс, наследующий от интерфейса [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="e7324-107">Create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span> <span data-ttu-id="e7324-108">Все функции элементов **IXAudio2VoiceCallback** являются исключительно виртуальными и должны быть определены.</span><span class="sxs-lookup"><span data-stu-id="e7324-108">All member functions of **IXAudio2VoiceCallback** are purely virtual, and must be defined.</span></span> <span data-ttu-id="e7324-109">Единственная интересная функция в этом примере — [**онстреаменд**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span><span class="sxs-lookup"><span data-stu-id="e7324-109">The only function of interest in this example is [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span></span> <span data-ttu-id="e7324-110">Поэтому остальные функции являются заглушками.</span><span class="sxs-lookup"><span data-stu-id="e7324-110">Therefore, the rest of the functions are stubs.</span></span> <span data-ttu-id="e7324-111">Функция **онстреаменд** запускает событие, показывающее, что воспроизведение звука завершено.</span><span class="sxs-lookup"><span data-stu-id="e7324-111">The **OnStreamEnd** function triggers an event that indicates the sound is done playing.</span></span>

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

    

2.  <span data-ttu-id="e7324-112">Создайте [**Исходный голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) с помощью [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) , используя экземпляр класса обратного вызова, созданный ранее в качестве параметра пкаллбакк.</span><span class="sxs-lookup"><span data-stu-id="e7324-112">Create a [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) with [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) using an instance of the callback class created previously as the pCallback parameter.</span></span>

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  <span data-ttu-id="e7324-113">После запуска голоса используйте метод [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) , чтобы дождаться срабатывания события.</span><span class="sxs-lookup"><span data-stu-id="e7324-113">After starting the voice, use the [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) method to wait for the event to be triggered.</span></span>

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e7324-114">См. также</span><span class="sxs-lookup"><span data-stu-id="e7324-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7324-115">Обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="e7324-115">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="e7324-116">Обратные вызовы в XAudio2</span><span class="sxs-lookup"><span data-stu-id="e7324-116">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="e7324-117">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="e7324-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="e7324-118">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="e7324-118">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="e7324-119">Руководство: организация звукового потока с диска</span><span class="sxs-lookup"><span data-stu-id="e7324-119">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
