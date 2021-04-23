---
description: Ожидание обхода цепочки (WCT) позволяет отладчикам диагностировать зависания приложений и взаимоблокировки.
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: Ожидание обхода цепочки
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 842beb7d5470bc2b3e6e9c7c1150ff2aa1a4cf76
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/04/2021
ms.locfileid: "103894014"
---
# <a name="wait-chain-traversal"></a><span data-ttu-id="1cc5c-103">Ожидание обхода цепочки</span><span class="sxs-lookup"><span data-stu-id="1cc5c-103">Wait Chain Traversal</span></span>

<span data-ttu-id="1cc5c-104">Ожидание обхода цепочки (WCT) позволяет отладчикам диагностировать зависания приложений и взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-104">Wait Chain Traversal (WCT) enables debuggers to diagnose application hangs and deadlocks.</span></span>

<span data-ttu-id="1cc5c-105">*Цепочка ожидания* — это последовательность потоков и объектов синхронизации, в которой каждый поток ожидает объект, следующий за ним.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-105">A *wait chain* is an alternating sequence of threads and synchronization objects where each thread waits for the object that follows.</span></span> <span data-ttu-id="1cc5c-106">Каждый следующий объект, в свою очередь, принадлежит следующему потоку в цепочке.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-106">Each object that follows is, in turn, owned by the subsequent thread in the chain.</span></span>

<span data-ttu-id="1cc5c-107">Поток ожидает объект синхронизации от времени, когда поток запрашивает объект, пока поток не получит его.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-107">A thread waits for a synchronization object from the time the thread requests the object until the thread has acquired it.</span></span> <span data-ttu-id="1cc5c-108">Это "Блокировка" принадлежит потоку от момента его получения потоком, пока поток не освободит его.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-108">This "lock" is owned by a thread from the time the thread acquires it, until the thread releases it.</span></span> <span data-ttu-id="1cc5c-109">Иными словами, когда поток 1 ожидает блокировку, принадлежащую потоку 2, поток 1 находится в состоянии ожидания для потока 2.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-109">In other words, when thread 1 is waiting for a lock that is owned by thread 2, thread 1 is "waiting" for thread 2.</span></span>

<span data-ttu-id="1cc5c-110">WCT поддерживает следующие примитивы синхронизации:</span><span class="sxs-lookup"><span data-stu-id="1cc5c-110">WCT supports the following synchronization primitives:</span></span>

- [<span data-ttu-id="1cc5c-111">Расширенный вызов локальной процедуры (ALPC)</span><span class="sxs-lookup"><span data-stu-id="1cc5c-111">Advanced Local Procedure Call (ALPC)</span></span>](../etw/alpc.md)
- [<span data-ttu-id="1cc5c-112">Модель COM</span><span class="sxs-lookup"><span data-stu-id="1cc5c-112">Component Object Model (COM)</span></span>](../com/the-component-object-model.md)
- [<span data-ttu-id="1cc5c-113">Критические секции</span><span class="sxs-lookup"><span data-stu-id="1cc5c-113">Critical sections</span></span>](../sync/critical-section-objects.md)
- [<span data-ttu-id="1cc5c-114">Мьютексы</span><span class="sxs-lookup"><span data-stu-id="1cc5c-114">Mutexes</span></span>](../sync/mutex-objects.md)
- [<span data-ttu-id="1cc5c-115">SendMessage</span><span class="sxs-lookup"><span data-stu-id="1cc5c-115">SendMessage</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
- <span data-ttu-id="1cc5c-116">Операции [ожидания](../sync/wait-functions.md) для [процессов и потоков](../procthread/processes-and-threads.md)</span><span class="sxs-lookup"><span data-stu-id="1cc5c-116">[Wait](../sync/wait-functions.md) operations on [processes and threads](../procthread/processes-and-threads.md)</span></span>

<span data-ttu-id="1cc5c-117">Чтобы получить цепочку ожидания для одного или нескольких потоков, создайте сеанс WCT с помощью функций [опенсреадваитчаинсессион](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) и [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) .</span><span class="sxs-lookup"><span data-stu-id="1cc5c-117">To retrieve the wait chain for one or more threads, create a WCT session using the [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) and [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) functions.</span></span> <span data-ttu-id="1cc5c-118">Сеансы WCT представлены с помощью маркера типа **хвкт**.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-118">WCT sessions are represented by a handle of type **HWCT**.</span></span>

## <a name="sessions-can-be-synchronous-or-asynchronous"></a><span data-ttu-id="1cc5c-119">Сеансы могут быть синхронными или асинхронными</span><span class="sxs-lookup"><span data-stu-id="1cc5c-119">Sessions can be synchronous or asynchronous</span></span>

<span data-ttu-id="1cc5c-120">Синхронные сеансы нельзя отменить и заблокировать вызывающий поток до получения цепочки ожидания.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-120">Synchronous sessions cannot be canceled, and block the calling thread, until a wait chain has been retrieved.</span></span>

<span data-ttu-id="1cc5c-121">Асинхронные сеансы не блокируют вызывающий поток и могут быть отменены приложением с помощью функции [клосесреадваитчаинсессион](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) .</span><span class="sxs-lookup"><span data-stu-id="1cc5c-121">Asynchronous sessions do not block the calling thread, and can be canceled by the application using the [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) function.</span></span> <span data-ttu-id="1cc5c-122">Результаты асинхронных операций становятся доступными через функцию обратного вызова [ваитчаинкаллбакк](/windows/win32/api/wct/nc-wct-pwaitchaincallback) , предоставляемую приложением.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-122">Results from asynchronous operations are made available through a [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) callback function provided by the application.</span></span>

<span data-ttu-id="1cc5c-123">Для асинхронных сеансов вызывающий объект может указать указатель на структуру данных контекста через [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (этот же указатель передается функции обратного вызова [ваитчаинкаллбакк](/windows/win32/api/wct/nc-wct-pwaitchaincallback) ).</span><span class="sxs-lookup"><span data-stu-id="1cc5c-123">For asynchronous sessions, the caller can specify a pointer to a context data structure through [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (this same pointer is passed to the [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) callback function).</span></span>

<span data-ttu-id="1cc5c-124">Структура контекстных данных определяется пользователем и непрозрачна для WCT.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-124">The context data structure is user-defined and opaque to WCT.</span></span> <span data-ttu-id="1cc5c-125">Оно может использоваться приложением для обмена контекстом между запросом WCT и функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-125">It can be used by the application to communicate context between a WCT query and a callback function.</span></span> <span data-ttu-id="1cc5c-126">Как правило, обработчик событий передается через эту структуру, и при выполнении обратного вызова это событие сообщается, и поток мониторинга сообщает о завершении запроса.</span><span class="sxs-lookup"><span data-stu-id="1cc5c-126">Typically, you pass an event handle through this structure and, when the callback is executed, this event is signalled and a monitoring thread is informed that the query has been completed.</span></span>

<span data-ttu-id="1cc5c-127">Пример обхода цепочки ожидания см. [в разделе Использование WCT](using-wct.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc5c-127">See [Using WCT](using-wct.md) for an example of wait chain traversal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cc5c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1cc5c-128">Related topics</span></span>

<span data-ttu-id="1cc5c-129">[С помощью WCT](using-wct.md), [справочника по WCT](wct-reference.md), [MSDN Magazine 2007 Июль-Bugslayer: ожидание цепочки ожидания](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)</span><span class="sxs-lookup"><span data-stu-id="1cc5c-129">[Using WCT](using-wct.md), [WCT Reference](wct-reference.md), [MSDN Magazine 2007 July - Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)</span></span>