---
description: XAudio2 может вызывать функции, предоставляемые клиентом, чтобы уведомить его асинхронно о некоторых событиях, происходящих в потоке обработки звука.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: Обратные вызовы в XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee191ad8c15d238a065c837c6fb192befbe7a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349812"
---
# <a name="xaudio2-callbacks"></a><span data-ttu-id="80f3c-103">Обратные вызовы в XAudio2</span><span class="sxs-lookup"><span data-stu-id="80f3c-103">XAudio2 Callbacks</span></span>

<span data-ttu-id="80f3c-104">XAudio2 может вызывать функции, предоставляемые клиентом, чтобы уведомить его асинхронно о некоторых событиях, происходящих в потоке обработки звука.</span><span class="sxs-lookup"><span data-stu-id="80f3c-104">XAudio2 can call functions provided by the client to notify it asynchronously of certain events taking place in the audio processing thread.</span></span> <span data-ttu-id="80f3c-105">Эти обратные вызовы могут быть глобальными или конкретными для заданного исходного голоса.</span><span class="sxs-lookup"><span data-stu-id="80f3c-105">These callbacks can be global or specific to a given source voice.</span></span> <span data-ttu-id="80f3c-106">Чтобы получить вызовы глобальной подсистемы, клиент должен предоставить экземпляр класса, реализующего интерфейс [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) при инициализации XAudio2.</span><span class="sxs-lookup"><span data-stu-id="80f3c-106">To receive global engine callbacks, the client must provide an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface when initializing XAudio2.</span></span> <span data-ttu-id="80f3c-107">Чтобы получить исходные голосовые обратные вызовы, клиент должен предоставить экземпляр класса, реализующего интерфейс [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) при создании исходных голосов.</span><span class="sxs-lookup"><span data-stu-id="80f3c-107">To receive source voice callbacks, the client must provide an instance of a class implementing the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface when creating source voices.</span></span> <span data-ttu-id="80f3c-108">Дополнительные сведения см. в разделе **IXAudio2EngineCallback** и **IXAudio2VoiceCallback**.</span><span class="sxs-lookup"><span data-stu-id="80f3c-108">For more details, see **IXAudio2EngineCallback** and **IXAudio2VoiceCallback**.</span></span>

<span data-ttu-id="80f3c-109">Необходимо тщательно реализовать обратные вызовы, чтобы избежать возникновения перерывов в аудио.</span><span class="sxs-lookup"><span data-stu-id="80f3c-109">You must implement callbacks carefully to avoid causing breaks in the audio.</span></span> <span data-ttu-id="80f3c-110">При каждом выполнении обратного вызова XAudio2 не может создать звук.</span><span class="sxs-lookup"><span data-stu-id="80f3c-110">Whenever a callback is running, XAudio2 cannot generate any audio.</span></span> <span data-ttu-id="80f3c-111">Задержка более чем на несколько миллисекунд может вызвать проблему со звуком.</span><span class="sxs-lookup"><span data-stu-id="80f3c-111">Delays of more than a few milliseconds can cause an audio problem.</span></span> <span data-ttu-id="80f3c-112">Задержки этой природы также создают выходные данные отладчика.</span><span class="sxs-lookup"><span data-stu-id="80f3c-112">Delays of this nature also generate debugger output.</span></span> <span data-ttu-id="80f3c-113">Это указывает на потенциальные проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="80f3c-113">This indicates potential performance issues.</span></span> <span data-ttu-id="80f3c-114">Как минимум функции обратного вызова не должны выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="80f3c-114">At a minimum, callback functions must not do the following:</span></span>

-   <span data-ttu-id="80f3c-115">Доступ к жесткому диску или другому постоянному хранилищу</span><span class="sxs-lookup"><span data-stu-id="80f3c-115">Access the hard disk or other permanent storage</span></span>
-   <span data-ttu-id="80f3c-116">Создание ресурсоемких или блокирующих вызовов API</span><span class="sxs-lookup"><span data-stu-id="80f3c-116">Make expensive or blocking API calls</span></span>
-   <span data-ttu-id="80f3c-117">Синхронизация с другими частями клиентского кода</span><span class="sxs-lookup"><span data-stu-id="80f3c-117">Synchronize with other parts of client code</span></span>
-   <span data-ttu-id="80f3c-118">Требовать значительный уровень загрузки ЦП</span><span class="sxs-lookup"><span data-stu-id="80f3c-118">Require significant CPU usage</span></span>

<span data-ttu-id="80f3c-119">Если при проектировании клиента требуется обратный вызов для активации действий, например перечисленных выше, обратный вызов должен сообщить другому клиентскому потоку о выполнении работы.</span><span class="sxs-lookup"><span data-stu-id="80f3c-119">If the client design requires a callback to trigger actions such as those listed previously, the callback should signal a different client thread to do the work.</span></span> <span data-ttu-id="80f3c-120">Это можно сделать с помощью простого механизма **выполнить SetEvent** или более сложных механизмов, например неблокирующей очереди команд, которая используется другим потоком.</span><span class="sxs-lookup"><span data-stu-id="80f3c-120">You can do this with a simple **SetEvent** mechanism or more sophisticated mechanisms like a nonblocking command queue that is consumed by another thread.</span></span>

## <a name="ixaudio2enginecallback"></a><span data-ttu-id="80f3c-121">IXAudio2EngineCallback</span><span class="sxs-lookup"><span data-stu-id="80f3c-121">IXAudio2EngineCallback</span></span>

<span data-ttu-id="80f3c-122">Класс [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) содержит методы, которые уведомляют клиента при возникновении определенных событий в подсистеме XAudio2.</span><span class="sxs-lookup"><span data-stu-id="80f3c-122">The [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) class contains methods that notify the client when certain events happen in the XAudio2 engine.</span></span> <span data-ttu-id="80f3c-123">Эти методы должны быть реализованы клиентом XAudio2.</span><span class="sxs-lookup"><span data-stu-id="80f3c-123">These methods should be implemented by the XAudio2 client.</span></span> <span data-ttu-id="80f3c-124">XAudio2 вызывает эти методы посредством указателя интерфейса, предоставленного клиентом, с помощью метода [**IXAudio2:: регистерфоркаллбаккс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) .</span><span class="sxs-lookup"><span data-stu-id="80f3c-124">XAudio2 calls these methods by means of an interface pointer provided by the client using the [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) method.</span></span> <span data-ttu-id="80f3c-125">Все эти методы возвращают **значение void**, а не **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="80f3c-125">All these methods return **void**, rather than an **HRESULT**.</span></span>

## <a name="ixaudio2voicecallback"></a><span data-ttu-id="80f3c-126">IXAudio2VoiceCallback</span><span class="sxs-lookup"><span data-stu-id="80f3c-126">IXAudio2VoiceCallback</span></span>

<span data-ttu-id="80f3c-127">Класс [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) содержит методы, которые уведомляют клиента при возникновении определенных событий в определенном исходном голосовом XAudio2.</span><span class="sxs-lookup"><span data-stu-id="80f3c-127">The [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) class contains methods that notify the client when certain events happen in a specific XAudio2 source voice.</span></span> <span data-ttu-id="80f3c-128">XAudio2 вызывает эти методы с помощью указателя интерфейса, предоставленного клиентом в [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).</span><span class="sxs-lookup"><span data-stu-id="80f3c-128">XAudio2 calls these methods by means of an interface pointer provided by the client in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).</span></span> <span data-ttu-id="80f3c-129">Как и в случае с [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback), эти методы должны быть реализованы клиентом XAudio2 и возвращать **значение void** , а не **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="80f3c-129">As with [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback), these methods should be implemented by the XAudio2 client, and return **void** rather than an **HRESULT**.</span></span>

<span data-ttu-id="80f3c-130">Как упоминалось ранее, важно, чтобы предоставляемые клиентом реализации этих обратных вызовов возвращались как можно быстрее, желательно в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="80f3c-130">As mentioned previously, it is crucial that the client-provided implementations of these callbacks return as quickly as possible, preferably within a millisecond.</span></span> <span data-ttu-id="80f3c-131">Обратные вызовы выполняются в потоке обработки звука, и вся обработка прерывается до возвращения обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="80f3c-131">The callbacks are executed in the audio processing thread, and all processing is interrupted until the callback returns.</span></span> <span data-ttu-id="80f3c-132">Задержка в обратном вызове может легко вызвать проблему со звуком.</span><span class="sxs-lookup"><span data-stu-id="80f3c-132">A delay in a callback can easily cause an audio problem.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80f3c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="80f3c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80f3c-134">Обратные вызовы</span><span class="sxs-lookup"><span data-stu-id="80f3c-134">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="80f3c-135">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="80f3c-135">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="80f3c-136">Руководство: использование обратных вызовов речевых источников</span><span class="sxs-lookup"><span data-stu-id="80f3c-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> <dt>

[<span data-ttu-id="80f3c-137">Руководство: использование обратных вызовов модуля</span><span class="sxs-lookup"><span data-stu-id="80f3c-137">How to: Use Engine Callbacks</span></span>](how-to--use-engine-callbacks.md)
</dt> <dt>

[<span data-ttu-id="80f3c-138">Руководство: организация звукового потока с диска</span><span class="sxs-lookup"><span data-stu-id="80f3c-138">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
