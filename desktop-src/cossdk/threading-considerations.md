---
description: Особенности работы с потоками
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Особенности работы с потоками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072538"
---
# <a name="threading-considerations"></a><span data-ttu-id="2a8b7-103">Особенности работы с потоками</span><span class="sxs-lookup"><span data-stu-id="2a8b7-103">Threading Considerations</span></span>

<span data-ttu-id="2a8b7-104">Средство записи очередей компонентов COM+ может выполняться в многопоточном апартаменте процесса (MTA) или в однопотоковом подразделении (STA).</span><span class="sxs-lookup"><span data-stu-id="2a8b7-104">The COM+ queued components recorder is capable of running in the process's multithreaded apartment (MTA) or in a single-threaded apartment (STA).</span></span> <span data-ttu-id="2a8b7-105">Когда средство записи запускается в STA, для каждого подразделения, содержащего объекты, должна быть очередь [очереди сообщений](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) для обработки вызовов из других процессов и подразделений в рамках одного процесса.</span><span class="sxs-lookup"><span data-stu-id="2a8b7-105">When the recorder is run in the STA, COM+ requires that each apartment containing objects must have a [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) queue to handle calls from other processes and apartments within the same process.</span></span> <span data-ttu-id="2a8b7-106">Это означает, что Рабочая функция потока должна иметь цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="2a8b7-106">This means that the thread's work function must have a message loop.</span></span> <span data-ttu-id="2a8b7-107">При создании экземпляра компонента в очереди возвращаемый указатель интерфейса всегда является указателем интерфейса прокси, а не прямым указателем интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a8b7-107">When a queued component is instantiated, the interface pointer returned is always a proxy interface pointer rather than a direct interface pointer.</span></span> <span data-ttu-id="2a8b7-108">Указатель на самом деле является ссылкой на экземпляр средства записи.</span><span class="sxs-lookup"><span data-stu-id="2a8b7-108">The pointer is actually a reference to an instance of the recorder.</span></span> <span data-ttu-id="2a8b7-109">Если ссылка на интерфейс записи передается другому потоку, исходный поток по-прежнему должен выполнять цикл обработки сообщений Windows, чтобы принимающий поток мог распаковать интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2a8b7-109">If this recorder interface reference is passed to another thread, the original thread must still be running the Windows message loop so that the receiving thread can unmarshal the interface.</span></span> <span data-ttu-id="2a8b7-110">Если это не так, принимающий поток зависает в вызове [**каунмаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="2a8b7-110">If this is not the case, the receiving thread hangs in a call to [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span>

<span data-ttu-id="2a8b7-111">Если для синхронизации потоков используются примитивы, рассмотрите возможность использования [**мсгваитформултиплеобжектс**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) вместо других функций синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2a8b7-111">If you are using primitives to synchronize the threads, consider using [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) instead of other synchronization functions.</span></span> <span data-ttu-id="2a8b7-112">Это проверяет наличие сообщений в очереди, а также состояния объекта синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2a8b7-112">This checks for messages in the queue as well as the state of the synchronization object.</span></span>

 

 
