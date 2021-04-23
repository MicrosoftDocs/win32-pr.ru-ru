---
description: Вы можете уведомить код клиента XAudio2 о событиях ядра, зарегистрировав экземпляр класса, реализующего интерфейс IXAudio2EngineCallback с подсистемой XAudio2.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 'Руководство: использование обратных вызовов модуля'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424013"
---
# <a name="how-to-use-engine-callbacks"></a><span data-ttu-id="2a1e0-103">Руководство: использование обратных вызовов модуля</span><span class="sxs-lookup"><span data-stu-id="2a1e0-103">How to: Use Engine Callbacks</span></span>

<span data-ttu-id="2a1e0-104">Вы можете уведомить код клиента XAudio2 о событиях ядра, зарегистрировав экземпляр класса, реализующего интерфейс [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) с подсистемой XAudio2.</span><span class="sxs-lookup"><span data-stu-id="2a1e0-104">You can notify the XAudio2 client code of engine events by registering an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface with the XAudio2 engine.</span></span> <span data-ttu-id="2a1e0-105">Это позволяет коду клиента XAudio2 отследить время обработки звука и перезапустить подсистему в случае возникновения критической ошибки.</span><span class="sxs-lookup"><span data-stu-id="2a1e0-105">This allows the XAudio2 client code to keep track of when audio processing is occurring, and when to restart the engine in the event of a critical error.</span></span>

## <a name="to-use-an-engine-callback"></a><span data-ttu-id="2a1e0-106">Использование обратного вызова подсистемы</span><span class="sxs-lookup"><span data-stu-id="2a1e0-106">To use an engine callback</span></span>

<span data-ttu-id="2a1e0-107">Следующие шаги регистрируют объект для обработки событий обработчика.</span><span class="sxs-lookup"><span data-stu-id="2a1e0-107">The following steps register an object to handle engine events.</span></span>

1.  <span data-ttu-id="2a1e0-108">Создайте класс, наследующий от интерфейса [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .</span><span class="sxs-lookup"><span data-stu-id="2a1e0-108">Create a class that inherits from the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface.</span></span>

    <span data-ttu-id="2a1e0-109">Все методы [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) являются исключительно виртуальными и должны быть определены.</span><span class="sxs-lookup"><span data-stu-id="2a1e0-109">All methods of [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) are purely virtual and must be defined.</span></span> <span data-ttu-id="2a1e0-110">В этом примере метод является [**IXAudio2EngineCallback:: онкритикалеррор**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), который устанавливает флаг для сигнализации основного цикла игры о том, что произошла критическая ошибка.</span><span class="sxs-lookup"><span data-stu-id="2a1e0-110">The method of interest in this example is [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), which sets a flag to signal the main game loop that a critical error has occurred.</span></span> <span data-ttu-id="2a1e0-111">Остальные методы, [**IXAudio2EngineCallback:: онпроцессингпассстарт**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) и [**IXAudio2EngineCallback:: онпроцессингпассенд**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), являются заглушками в этом примере.</span><span class="sxs-lookup"><span data-stu-id="2a1e0-111">The remaining methods, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) and [**IXAudio2EngineCallback::OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), are stubs in this example.</span></span>

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  <span data-ttu-id="2a1e0-112">Используйте [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) для создания экземпляра подсистемы XAudio2.</span><span class="sxs-lookup"><span data-stu-id="2a1e0-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) to create an instance of the XAudio2 engine.</span></span>

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="2a1e0-113">Чтобы зарегистрировать обратный вызов модуля, используйте [**IXAudio2:: регистерфоркаллбаккс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) .</span><span class="sxs-lookup"><span data-stu-id="2a1e0-113">Use [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) to register the engine callback.</span></span>

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  <span data-ttu-id="2a1e0-114">Если обратный вызов подсистемы больше не требуется, вызовите [**IXAudio2:: унрегистерфоркаллбаккс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span><span class="sxs-lookup"><span data-stu-id="2a1e0-114">If you don't need the engine callback any more, call [**IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span></span>

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="2a1e0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="2a1e0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a1e0-116">Обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="2a1e0-116">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="2a1e0-117">Обратные вызовы в XAudio2</span><span class="sxs-lookup"><span data-stu-id="2a1e0-117">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="2a1e0-118">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="2a1e0-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="2a1e0-119">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="2a1e0-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="2a1e0-120">Руководство: организация звукового потока с диска</span><span class="sxs-lookup"><span data-stu-id="2a1e0-120">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
