---
description: Метод Среадпрок извлекает образцы из очереди и доставляет их во входной ПИН-код.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Каутпуткуеуе. Среадпрок, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665145"
---
# <a name="coutputqueuethreadproc-method"></a><span data-ttu-id="91f7a-103">Каутпуткуеуе. Среадпрок, метод</span><span class="sxs-lookup"><span data-stu-id="91f7a-103">COutputQueue.ThreadProc method</span></span>

<span data-ttu-id="91f7a-104">`ThreadProc`Метод извлекает образцы из очереди и доставляет их во входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="91f7a-104">The `ThreadProc` method retrieves samples from the queue and delivers them to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f7a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91f7a-105">Syntax</span></span>


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="91f7a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91f7a-106">Parameters</span></span>

<span data-ttu-id="91f7a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="91f7a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91f7a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91f7a-108">Return value</span></span>

<span data-ttu-id="91f7a-109">Возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="91f7a-109">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f7a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91f7a-110">Remarks</span></span>

<span data-ttu-id="91f7a-111">Метод [**каутпуткуеуе:: инитиалсреадпрок**](coutputqueue-initialthreadproc.md) вызывает этот метод, который реализует главный цикл потока.</span><span class="sxs-lookup"><span data-stu-id="91f7a-111">The [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) method calls this method, which implements the main thread loop.</span></span> <span data-ttu-id="91f7a-112">В цикле метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="91f7a-112">Within the loop, the method performs the following steps:</span></span>

1.  <span data-ttu-id="91f7a-113">Извлекает пример для очереди.</span><span class="sxs-lookup"><span data-stu-id="91f7a-113">Retrieves a sample for the queue.</span></span>
2.  <span data-ttu-id="91f7a-114">Если пример представляет собой управляющее сообщение, то поток выполняет действие элемента управления.</span><span class="sxs-lookup"><span data-stu-id="91f7a-114">If the sample is a control message, the thread executes the control action.</span></span> <span data-ttu-id="91f7a-115">В противном случае он помещает пример в массив [**каутпуткуеуе:: m \_ ппсамплес**](coutputqueue-m-ppsamples.md) .</span><span class="sxs-lookup"><span data-stu-id="91f7a-115">Otherwise, it places the sample into the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array.</span></span>
3.  <span data-ttu-id="91f7a-116">Если массив заполнен (или если [**каутпуткуеуе:: m \_ Ббатчексакт**](coutputqueue-m-bbatchexact.md) имеет **значение false**), поток вызывает метод [**имеминпутпин:: рецеивемултипле**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) для доставки образцов.</span><span class="sxs-lookup"><span data-stu-id="91f7a-116">When the array is full (or if [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) is **FALSE**), the thread calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method to deliver the samples.</span></span>
4.  <span data-ttu-id="91f7a-117">Если ни один из образцов не поставлен в очередь, поток ожидает семафор [**\_ хсем каутпуткуеуе:: m**](coutputqueue-m-hsem.md) .</span><span class="sxs-lookup"><span data-stu-id="91f7a-117">If no samples are queued, the thread waits on the [**COutputQueue::m\_hSem**](coutputqueue-m-hsem.md) semaphore.</span></span>

<span data-ttu-id="91f7a-118">Поток завершается, когда переменная члена [**каутпуткуеуе:: m \_ Бтерминате**](coutputqueue-m-bterminate.md) принимает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="91f7a-118">The thread terminates when the [**COutputQueue::m\_bTerminate**](coutputqueue-m-bterminate.md) member variable becomes **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="91f7a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="91f7a-119">Requirements</span></span>



| <span data-ttu-id="91f7a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="91f7a-120">Requirement</span></span> | <span data-ttu-id="91f7a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="91f7a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91f7a-122">Header</span><span class="sxs-lookup"><span data-stu-id="91f7a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="91f7a-123"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91f7a-123"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91f7a-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="91f7a-124">Library</span></span><br/> | <dl> <span data-ttu-id="91f7a-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="91f7a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f7a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91f7a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f7a-127">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="91f7a-127">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




