---
description: Функция CreateTimerQueue создает очередь для таймеров.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Очереди таймера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663412"
---
# <a name="timer-queues"></a><span data-ttu-id="2e587-103">Очереди таймера</span><span class="sxs-lookup"><span data-stu-id="2e587-103">Timer Queues</span></span>

<span data-ttu-id="2e587-104">Функция [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) создает очередь для таймеров.</span><span class="sxs-lookup"><span data-stu-id="2e587-104">The [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) function creates a queue for timers.</span></span> <span data-ttu-id="2e587-105">Таймеры в этой очереди, известные как *таймеры очереди*, — это простые объекты, которые позволяют указать функцию обратного вызова, которая будет вызываться при наступлении указанного времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="2e587-105">Timers in this queue, known as *timer-queue timers*, are lightweight objects that enable you to specify a callback function to be called when the specified due time arrives.</span></span> <span data-ttu-id="2e587-106">Операция ожидания выполняется потоком в [пуле потоков](../procthread/thread-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="2e587-106">The wait operation is performed by a thread in the [thread pool](../procthread/thread-pooling.md).</span></span>

<span data-ttu-id="2e587-107">Чтобы добавить таймер в очередь, вызовите функцию [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="2e587-107">To add a timer to the queue, call the [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function.</span></span> <span data-ttu-id="2e587-108">Чтобы обновить таймер очереди таймера, вызовите функцию [**чанжетимеркуеуетимер**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="2e587-108">To update a timer-queue timer, call the [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) function.</span></span> <span data-ttu-id="2e587-109">Вы можете указать функцию обратного вызова, которая будет выполняться рабочим потоком из пула потоков по истечении срока действия таймера.</span><span class="sxs-lookup"><span data-stu-id="2e587-109">You can specify a callback function to be executed by a worker thread from the thread pool when the timer expires.</span></span>

<span data-ttu-id="2e587-110">Чтобы отменить ожидающий таймер, вызовите функцию [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="2e587-110">To cancel a pending timer, call the [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) function.</span></span> <span data-ttu-id="2e587-111">По завершении работы с очередью таймеров вызовите функцию [**делететимеркуеуикс**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) , чтобы удалить очередь таймера.</span><span class="sxs-lookup"><span data-stu-id="2e587-111">When you are finished with the queue of timers, call the [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) function to delete the timer queue.</span></span> <span data-ttu-id="2e587-112">Все ожидающие таймеры в очереди отменяются и удаляются.</span><span class="sxs-lookup"><span data-stu-id="2e587-112">Any pending timers in the queue are canceled and deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e587-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2e587-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e587-114">Использование очередей таймера</span><span class="sxs-lookup"><span data-stu-id="2e587-114">Using Timer Queues</span></span>](using-timer-queues.md)
</dt> </dl>

 

 
