---
description: Метод QueueSample ставит в очередь пример.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Каутпуткуеуе. QueueSample, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8efe0ec3b2326d1af0d0075770bdc6443ab9dcad
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910072"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="bb1d5-103">Каутпуткуеуе. QueueSample, метод</span><span class="sxs-lookup"><span data-stu-id="bb1d5-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="bb1d5-104">`QueueSample`Метод помещает пример в очередь.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb1d5-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="bb1d5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb1d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb1d5-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="bb1d5-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="bb1d5-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb1d5-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb1d5-109">Return value</span></span>

<span data-ttu-id="bb1d5-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb1d5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb1d5-111">Remarks</span></span>

<span data-ttu-id="bb1d5-112">Этот метод добавляет пример в конец очереди.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="bb1d5-113">Перед вызовом этого метода следует удерживать критическую секцию и вызывать его только в том случае, если объект использует поток для доставки образцов.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="bb1d5-114">Чтобы определить, использует ли объект поток, вызовите метод [**каутпуткуеуе::**](coutputqueue-isqueued.md) GetObject.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="bb1d5-115">Этот метод можно также использовать для помещения управляющих сообщений в очередь.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="bb1d5-116">Управляющее сообщение — это определенная константа (приведение к \_ типу данных типа Long), которая указывает потоку выполнить какое-либо действие.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="bb1d5-117">Класс **каутпуткуеуе** определяет управляющие сообщения, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



| <span data-ttu-id="bb1d5-118">Метка</span><span class="sxs-lookup"><span data-stu-id="bb1d5-118">Label</span></span> | <span data-ttu-id="bb1d5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bb1d5-119">Value</span></span> |
|---------------|----------------------------------------|
| <span data-ttu-id="bb1d5-120">Сообщение</span><span class="sxs-lookup"><span data-stu-id="bb1d5-120">Message</span></span>       | <span data-ttu-id="bb1d5-121">Действие</span><span class="sxs-lookup"><span data-stu-id="bb1d5-121">Action</span></span>                                 |
| <span data-ttu-id="bb1d5-122">\_пакет EOS</span><span class="sxs-lookup"><span data-stu-id="bb1d5-122">EOS\_PACKET</span></span>   | <span data-ttu-id="bb1d5-123">Доставка уведомления об окончании потока.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-123">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="bb1d5-124">НОВЫЙ \_ сегмент</span><span class="sxs-lookup"><span data-stu-id="bb1d5-124">NEW\_SEGMENT</span></span>  | <span data-ttu-id="bb1d5-125">Доставьте новый сегмент.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-125">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="bb1d5-126">СБРОСИТЬ \_ пакет</span><span class="sxs-lookup"><span data-stu-id="bb1d5-126">RESET\_PACKET</span></span> | <span data-ttu-id="bb1d5-127">Сброс состояния очереди.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-127">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="bb1d5-128">Отправить \_ пакет</span><span class="sxs-lookup"><span data-stu-id="bb1d5-128">SEND\_PACKET</span></span>  | <span data-ttu-id="bb1d5-129">Отправляет частичный пакет примеров.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-129">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="bb1d5-130">Это защищенный метод, который класс **каутпуткуеуе** использует для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="bb1d5-130">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb1d5-131">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="bb1d5-131">Requirements</span></span>



| <span data-ttu-id="bb1d5-132">Требование</span><span class="sxs-lookup"><span data-stu-id="bb1d5-132">Requirement</span></span> | <span data-ttu-id="bb1d5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bb1d5-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1d5-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bb1d5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="bb1d5-135"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb1d5-135"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb1d5-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb1d5-136">Library</span></span><br/> | <dl> <span data-ttu-id="bb1d5-137"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bb1d5-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb1d5-138">См. также</span><span class="sxs-lookup"><span data-stu-id="bb1d5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb1d5-139">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="bb1d5-139">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




