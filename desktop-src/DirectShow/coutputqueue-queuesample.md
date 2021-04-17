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
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674883"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="ee1ea-103">Каутпуткуеуе. QueueSample, метод</span><span class="sxs-lookup"><span data-stu-id="ee1ea-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="ee1ea-104">`QueueSample`Метод помещает пример в очередь.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee1ea-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="ee1ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee1ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1ea-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="ee1ea-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ee1ea-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1ea-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee1ea-109">Return value</span></span>

<span data-ttu-id="ee1ea-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee1ea-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee1ea-111">Remarks</span></span>

<span data-ttu-id="ee1ea-112">Этот метод добавляет пример в конец очереди.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="ee1ea-113">Перед вызовом этого метода следует удерживать критическую секцию и вызывать его только в том случае, если объект использует поток для доставки образцов.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="ee1ea-114">Чтобы определить, использует ли объект поток, вызовите метод [**каутпуткуеуе::**](coutputqueue-isqueued.md) GetObject.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="ee1ea-115">Этот метод можно также использовать для помещения управляющих сообщений в очередь.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="ee1ea-116">Управляющее сообщение — это определенная константа (приведение к \_ типу данных типа Long), которая указывает потоку выполнить какое-либо действие.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="ee1ea-117">Класс **каутпуткуеуе** определяет управляющие сообщения, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



|               |                                        |
|---------------|----------------------------------------|
| <span data-ttu-id="ee1ea-118">Сообщение</span><span class="sxs-lookup"><span data-stu-id="ee1ea-118">Message</span></span>       | <span data-ttu-id="ee1ea-119">Действие</span><span class="sxs-lookup"><span data-stu-id="ee1ea-119">Action</span></span>                                 |
| <span data-ttu-id="ee1ea-120">\_пакет EOS</span><span class="sxs-lookup"><span data-stu-id="ee1ea-120">EOS\_PACKET</span></span>   | <span data-ttu-id="ee1ea-121">Доставка уведомления об окончании потока.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-121">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="ee1ea-122">НОВЫЙ \_ сегмент</span><span class="sxs-lookup"><span data-stu-id="ee1ea-122">NEW\_SEGMENT</span></span>  | <span data-ttu-id="ee1ea-123">Доставьте новый сегмент.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-123">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="ee1ea-124">СБРОСИТЬ \_ пакет</span><span class="sxs-lookup"><span data-stu-id="ee1ea-124">RESET\_PACKET</span></span> | <span data-ttu-id="ee1ea-125">Сброс состояния очереди.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-125">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="ee1ea-126">Отправить \_ пакет</span><span class="sxs-lookup"><span data-stu-id="ee1ea-126">SEND\_PACKET</span></span>  | <span data-ttu-id="ee1ea-127">Отправляет частичный пакет примеров.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-127">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="ee1ea-128">Это защищенный метод, который класс **каутпуткуеуе** использует для внутренних целей.</span><span class="sxs-lookup"><span data-stu-id="ee1ea-128">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee1ea-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ee1ea-129">Requirements</span></span>



| <span data-ttu-id="ee1ea-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ee1ea-130">Requirement</span></span> | <span data-ttu-id="ee1ea-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ee1ea-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1ea-132">Header</span><span class="sxs-lookup"><span data-stu-id="ee1ea-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ee1ea-133"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee1ea-133"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee1ea-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee1ea-134">Library</span></span><br/> | <dl> <span data-ttu-id="ee1ea-135"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ee1ea-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee1ea-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee1ea-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1ea-137">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="ee1ea-137">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




