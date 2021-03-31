---
title: Регистрация функции-обработчика
description: Клиентские приложения получают Виневентс в функции обратного вызова Виневентпрок. Действия, выполняемые функцией обратного вызова, определяются приложением, но синтаксис должен быть указан в прототипе.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888015"
---
# <a name="registering-a-hook-function"></a><span data-ttu-id="3f77c-104">Регистрация функции-обработчика</span><span class="sxs-lookup"><span data-stu-id="3f77c-104">Registering a Hook Function</span></span>

<span data-ttu-id="3f77c-105">Клиентские приложения получают Виневентс в функции обратного вызова [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) .</span><span class="sxs-lookup"><span data-stu-id="3f77c-105">Client applications receive WinEvents in a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function.</span></span> <span data-ttu-id="3f77c-106">Действия, выполняемые функцией обратного вызова, определяются приложением, но синтаксис должен быть указан в прототипе.</span><span class="sxs-lookup"><span data-stu-id="3f77c-106">The actions performed by the callback function are defined by the application, but the syntax must be as specified in the prototype.</span></span>

<span data-ttu-id="3f77c-107">Прежде чем он сможет получать события, необходимо зарегистрировать функцию, вызвав [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span><span class="sxs-lookup"><span data-stu-id="3f77c-107">Before it can receive events, the function must be registered by calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span></span> <span data-ttu-id="3f77c-108">Клиент может вызвать **сетвиневенсук** несколько раз, чтобы зарегистрировать различные функции-обработчики, или задать дополнительные события для ранее зарегистрированной функции обработчика.</span><span class="sxs-lookup"><span data-stu-id="3f77c-108">The client can call **SetWinEventHook** more than once to register different hook functions, or to set additional events for a previously registered hook function.</span></span>

<span data-ttu-id="3f77c-109">При вызове [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) клиент указывает, какие события должны быть получены, и как их получить.</span><span class="sxs-lookup"><span data-stu-id="3f77c-109">When calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) the client specifies which events to receive and how to receive them.</span></span> <span data-ttu-id="3f77c-110">Клиент может выбрать:</span><span class="sxs-lookup"><span data-stu-id="3f77c-110">The client can choose to:</span></span>

-   <span data-ttu-id="3f77c-111">Получение всех событий или определенного набора событий.</span><span class="sxs-lookup"><span data-stu-id="3f77c-111">Receive all events or a specific set of events.</span></span>
-   <span data-ttu-id="3f77c-112">Получение событий из всех потоков или из определенного потока.</span><span class="sxs-lookup"><span data-stu-id="3f77c-112">Receive events from all threads or from a specific thread.</span></span>
-   <span data-ttu-id="3f77c-113">Получение событий из всех процессов или из определенного процесса.</span><span class="sxs-lookup"><span data-stu-id="3f77c-113">Receive events from all processes or from a specific process.</span></span>
-   <span data-ttu-id="3f77c-114">Обработка событий в процессе или вне процесса.</span><span class="sxs-lookup"><span data-stu-id="3f77c-114">Handle events in process or out of process.</span></span>

<span data-ttu-id="3f77c-115">При создании события, удовлетворяющего заданным критериям, система вызывает функцию обратного вызова [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) клиента (или "процедура обработчика").</span><span class="sxs-lookup"><span data-stu-id="3f77c-115">When an event is generated that matches the specified criteria, the system calls the client's [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function (or "hook procedure").</span></span> <span data-ttu-id="3f77c-116">Параметры, получаемые функцией-обработчиком, сообщают клиенту о окне, объекте и возможном дочернем элементе, создавшем событие.</span><span class="sxs-lookup"><span data-stu-id="3f77c-116">The parameters that the hook function receives tell the client about the window, object, and possible child element that generated the event.</span></span> <span data-ttu-id="3f77c-117">Клиент использует эти параметры в вызове получения объекта, например [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="3f77c-117">A client uses these parameters in an object retrieval call, such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

 

 




