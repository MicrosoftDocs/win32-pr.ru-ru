---
title: Запуск одного события таймера
description: Запуск одного события таймера
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- Таймеры мультимедиа, события
- таймеры, события
- Таймеры мультимедиа, начальные события
- таймеры, события запуска
- Функция Тимесетевент
- Запуск событий таймера
- события с одним таймером
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9d0024e3dfa9b0bda79f209abd9b81e89ad11c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412840"
---
# <a name="starting-a-single-timer-event"></a><span data-ttu-id="14936-110">Запуск одного события таймера</span><span class="sxs-lookup"><span data-stu-id="14936-110">Starting a Single Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="14936-111">В этом разделе описывается устаревшая функция.</span><span class="sxs-lookup"><span data-stu-id="14936-111">This topic describes an obsolete function.</span></span> <span data-ttu-id="14936-112">Новые приложения должны использовать функцию [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) для создания таймеров.</span><span class="sxs-lookup"><span data-stu-id="14936-112">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="14936-113">Чтобы запустить одно событие таймера, вызовите функцию [**тимесетевент**](/previous-versions//dd757634(v=vs.85)) , указав период времени перед обратным вызовом, разрешение, адрес функции обратного вызова (см. [**тимепрок**](/previous-versions//dd757631(v=vs.85))) и данные пользователя, которые необходимо передать функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="14936-113">To start a single timer event, call the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function, specifying the amount of time before the callback occurs, the resolution, the address of the callback function (see [**TimeProc**](/previous-versions//dd757631(v=vs.85))), and the user data to supply with the callback function.</span></span> <span data-ttu-id="14936-114">Приложение может использовать функцию, подобную приведенной ниже, для запуска одного события таймера.</span><span class="sxs-lookup"><span data-stu-id="14936-114">An application can use a function like the following to start a single timer event.</span></span>


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



<span data-ttu-id="14936-115">Пример функции обратного вызова Онешоткаллбакк см. в разделе [написание функции обратного вызова таймера](writing-a-timer-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="14936-115">For an example of the callback function OneShotCallback, see [Writing a Timer Callback Function](writing-a-timer-callback-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14936-116">См. также</span><span class="sxs-lookup"><span data-stu-id="14936-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14936-117">Использование таймеров мультимедиа</span><span class="sxs-lookup"><span data-stu-id="14936-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 