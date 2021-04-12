---
description: Приложение может отказаться от интерфейса Дуккинг по умолчанию, обрабатываемого системой, и заменить его пользовательской реализацией.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Предоставление пользовательского поведения Дуккинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142415"
---
# <a name="providing-a-custom-ducking-behavior"></a><span data-ttu-id="b8614-103">Предоставление пользовательского поведения Дуккинг</span><span class="sxs-lookup"><span data-stu-id="b8614-103">Providing a Custom Ducking Behavior</span></span>

<span data-ttu-id="b8614-104">Приложение может отказаться от [интерфейса Дуккинг по умолчанию](stream-attenuation.md) , обрабатываемого системой, и заменить его пользовательской реализацией.</span><span class="sxs-lookup"><span data-stu-id="b8614-104">An application can opt out of the [Default Ducking Experience](stream-attenuation.md) handled by the system and replace it with a custom implementation.</span></span>

<span data-ttu-id="b8614-105">Приложение может предоставить пользовательский интерфейс дуккинг.</span><span class="sxs-lookup"><span data-stu-id="b8614-105">An application can provide a custom ducking experience.</span></span> <span data-ttu-id="b8614-106">Например, проигрыватель Windows Media предоставляет собственный интерфейс дуккинг, приостанавливая текущий поток мультимедиа во время сеанса связи и возобновляя воспроизведение при закрытии сеанса.</span><span class="sxs-lookup"><span data-stu-id="b8614-106">For example, Windows Media Player provides its own ducking experience by pausing the current media stream during a communication session and resuming playback when the session is closed.</span></span> <span data-ttu-id="b8614-107">Пример приложения мультимедиа, реализующего дуккинг, входит в состав примеров Windows SDK; Дополнительные сведения см. в разделе [дуккингмедиаплайер](duckingmediaplayer.md).</span><span class="sxs-lookup"><span data-stu-id="b8614-107">A sample media application that implements ducking is included with Windows SDK samples; for more information, see [DuckingMediaPlayer](duckingmediaplayer.md).</span></span> <span data-ttu-id="b8614-108">Чтобы имитировать взаимодействие между открытием и закрытием потоков связи и созданием событий дуккинг, см. раздел [дуккингкаптуресампле](duckingcapturesample.md), который также входит в состав примеров Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b8614-108">To simulate the experience of opening and closing communication streams, and generating ducking events, see [DuckingCaptureSample](duckingcapturesample.md), which is also included with Windows SDK samples.</span></span>

<span data-ttu-id="b8614-109">Приложение мультимедиа, которое воспроизводит звуки для ослабления, должно учитывать коммуникационные потоки, когда они открываются и закрываются в системе.</span><span class="sxs-lookup"><span data-stu-id="b8614-109">A media application that plays sounds to be attenuated must be aware of the communication streams, when they are opened and closed in the system.</span></span> <span data-ttu-id="b8614-110">Пользовательская реализация может предоставляться с помощью Медиафаундатион, DirectShow или DirectSound, использующих основные API аудио.</span><span class="sxs-lookup"><span data-stu-id="b8614-110">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="b8614-111">Прямой ВАСАПИ клиент может также переопределить обработку по умолчанию, если он знает, когда начинается и заканчивается сеанс связи.</span><span class="sxs-lookup"><span data-stu-id="b8614-111">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="b8614-112">**Чтобы обеспечить пользовательский интерфейс дуккинг, клиент ВАСАПИ должен выполнить следующие задачи:**</span><span class="sxs-lookup"><span data-stu-id="b8614-112">**To provide a custom ducking experience, a WASAPI client must perform the following tasks:**</span></span>

1.  <span data-ttu-id="b8614-113">Зарегистрируйтесь для получения событий дуккинг из *дуккинг Manager*— компонента звуковой системы, который обрабатывает уведомления, связанные с изменениями потока связи.</span><span class="sxs-lookup"><span data-stu-id="b8614-113">Register to receive ducking events from the *ducking manager*—a component of the audio system that handles notifications related to communication stream changes.</span></span> <span data-ttu-id="b8614-114">Дополнительные сведения см. в [Поддуккинг событий](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b8614-114">For more information, [Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="b8614-115">Если клиент зарегистрирован для получения уведомлений дуккинг, диспетчер дуккинг отключает поведение по умолчанию, предоставляемое системой.</span><span class="sxs-lookup"><span data-stu-id="b8614-115">If the client is gets registered to receive ducking notifications, the ducking manager disables the default behavior provided by the system.</span></span> <span data-ttu-id="b8614-116">Если поведение по умолчанию отключено неявно (см. раздел [Отключение интерфейса Дуккинг по умолчанию](disabling-the-ducking-experience.md)), а клиент не обеспечивает никаких действий по замене, приложение не будет работать в дуккинг.</span><span class="sxs-lookup"><span data-stu-id="b8614-116">If the default behavior is disabled explictly (see [Disabling the Default Ducking Experience](disabling-the-ducking-experience.md)) and the client does not provide a substitute behavior, the application does not experience any ducking behavior.</span></span>

     

2.  <span data-ttu-id="b8614-117">Прослушивать уведомления о событиях утка, отправленные диспетчером дуккинг, и выполнять требуемое поведение дуккинг.</span><span class="sxs-lookup"><span data-stu-id="b8614-117">Listen for the duck event notifications sent by the ducking manager and perform the desired ducking behavior.</span></span> <span data-ttu-id="b8614-118">Дополнительные сведения о реализации поведения дуккинг см. в статье [рекомендации по реализации для уведомлений дуккинг](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b8614-118">For more information about implementing a ducking behavior, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8614-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b8614-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8614-120">Использование коммуникационного устройства</span><span class="sxs-lookup"><span data-stu-id="b8614-120">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="b8614-121">Интерфейс Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b8614-121">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="b8614-122">Отключение интерфейса Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b8614-122">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="b8614-123">Рекомендации по реализации для уведомлений Дуккинг</span><span class="sxs-lookup"><span data-stu-id="b8614-123">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="b8614-124">Получение событий Дуккинг</span><span class="sxs-lookup"><span data-stu-id="b8614-124">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



