---
description: Шаблон класса Ккуеуе реализует простую, статично изменяемую очередь.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Класс Ккуеуе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679679"
---
# <a name="cqueue-class"></a><span data-ttu-id="e6f03-103">Класс Ккуеуе</span><span class="sxs-lookup"><span data-stu-id="e6f03-103">CQueue class</span></span>

<span data-ttu-id="e6f03-104">Шаблон класса **ккуеуе** реализует простую, статично изменяемую очередь.</span><span class="sxs-lookup"><span data-stu-id="e6f03-104">The **CQueue** class template implements a simple, statically sized queue.</span></span>



| <span data-ttu-id="e6f03-105">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="e6f03-105">Public Methods</span></span>                                  | <span data-ttu-id="e6f03-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e6f03-106">Description</span></span>                             |
|-------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="e6f03-107">**ккуеуе**</span><span class="sxs-lookup"><span data-stu-id="e6f03-107">**CQueue**</span></span>](cqueue-cqueue.md)                 | <span data-ttu-id="e6f03-108">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="e6f03-108">Constructor method.</span></span>                     |
| [<span data-ttu-id="e6f03-109">**~ Ккуеуе**</span><span class="sxs-lookup"><span data-stu-id="e6f03-109">**~CQueue**</span></span>](cqueue--cqueue.md)               | <span data-ttu-id="e6f03-110">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="e6f03-110">Destructor method.</span></span>                      |
| [<span data-ttu-id="e6f03-111">**жеткуеуеобжект**</span><span class="sxs-lookup"><span data-stu-id="e6f03-111">**GetQueueObject**</span></span>](cqueue-getqueueobject.md) | <span data-ttu-id="e6f03-112">Извлекает следующий элемент из очереди.</span><span class="sxs-lookup"><span data-stu-id="e6f03-112">Retrieves the next item from the queue.</span></span> |
| [<span data-ttu-id="e6f03-113">**путкуеуеобжект**</span><span class="sxs-lookup"><span data-stu-id="e6f03-113">**PutQueueObject**</span></span>](cqueue-putqueueobject.md) | <span data-ttu-id="e6f03-114">Помещает элемент в очередь.</span><span class="sxs-lookup"><span data-stu-id="e6f03-114">Puts an item onto the queue.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="e6f03-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6f03-115">Remarks</span></span>

<span data-ttu-id="e6f03-116">Конструктор класса задает размер очереди.</span><span class="sxs-lookup"><span data-stu-id="e6f03-116">The class constructor specifies the size of the queue.</span></span> <span data-ttu-id="e6f03-117">Используйте [**ккуеуе::P уткуеуеобжект**](cqueue-putqueueobject.md) , чтобы поместить элемент в очередь, и метод [**Ккуеуе:: жеткуеуеобжект**](cqueue-getqueueobject.md) для вывода элемента в очередь.</span><span class="sxs-lookup"><span data-stu-id="e6f03-117">Use the [**CQueue::PutQueueObject**](cqueue-putqueueobject.md) to put an item on the queue, and the [**CQueue::GetQueueObject**](cqueue-getqueueobject.md) method to dequeues an item.</span></span> <span data-ttu-id="e6f03-118">Если очередь заполнена, метод **путкуеуеобжект** блокируется до тех пор, пока не будет выведен элемент из очереди.</span><span class="sxs-lookup"><span data-stu-id="e6f03-118">If the queue is full, the **PutQueueObject** method blocks until an item is dequeued.</span></span> <span data-ttu-id="e6f03-119">Если очередь пуста, **жеткуеуеобжект** блокируется до постановки элемента в очередь.</span><span class="sxs-lookup"><span data-stu-id="e6f03-119">If the queue is empty, the **GetQueueObject** blocks until an item is queued.</span></span> <span data-ttu-id="e6f03-120">Параметр шаблона задает тип элемента.</span><span class="sxs-lookup"><span data-stu-id="e6f03-120">The template parameter specifies the type of item.</span></span> <span data-ttu-id="e6f03-121">Пример:</span><span class="sxs-lookup"><span data-stu-id="e6f03-121">For example:</span></span>


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



<span data-ttu-id="e6f03-122">Класс использует два семафора для управления операциями очереди, семафором Get и семафором "разместить".</span><span class="sxs-lookup"><span data-stu-id="e6f03-122">The class uses two semaphores to control queuing operations, a "get" semaphore and a "put" semaphore.</span></span> <span data-ttu-id="e6f03-123">Метод [**жеткуеуеобжект**](cqueue-getqueueobject.md) ожидает семафор "Get" (с помощью функции **WaitForSingleObject** ) и освобождает семафор "помещаемие" (с помощью функции **ReleaseSemaphore** ).</span><span class="sxs-lookup"><span data-stu-id="e6f03-123">The [**GetQueueObject**](cqueue-getqueueobject.md) method waits on the "get" semaphore (using the **WaitForSingleObject** function) and releases the "put" semaphore (using the **ReleaseSemaphore** function).</span></span> <span data-ttu-id="e6f03-124">Метод [**путкуеуеобжект**](cqueue-putqueueobject.md) ожидает семафора "помещает" и освобождает семафор "Get".</span><span class="sxs-lookup"><span data-stu-id="e6f03-124">The [**PutQueueObject**](cqueue-putqueueobject.md) method waits on the "put" semaphore and releases the "get" semaphore.</span></span> <span data-ttu-id="e6f03-125">Класс использует критическую секцию для сериализации операций очереди между несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="e6f03-125">The class uses a critical section to serialize queuing operations among multiple threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6f03-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e6f03-126">Requirements</span></span>



| <span data-ttu-id="e6f03-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e6f03-127">Requirement</span></span> | <span data-ttu-id="e6f03-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e6f03-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f03-129">Header</span><span class="sxs-lookup"><span data-stu-id="e6f03-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e6f03-130"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6f03-130"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e6f03-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6f03-131">Library</span></span><br/> | <dl> <span data-ttu-id="e6f03-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e6f03-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




