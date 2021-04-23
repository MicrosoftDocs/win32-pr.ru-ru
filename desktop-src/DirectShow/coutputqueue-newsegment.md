---
description: Метод Невсегмент доставляет новый сегмент входного ПИН-кода.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Каутпуткуеуе. Невсегмент, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675789"
---
# <a name="coutputqueuenewsegment-method"></a><span data-ttu-id="00fbf-103">Каутпуткуеуе. Невсегмент, метод</span><span class="sxs-lookup"><span data-stu-id="00fbf-103">COutputQueue.NewSegment method</span></span>

<span data-ttu-id="00fbf-104">`NewSegment`Метод доставляет новый сегмент для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="00fbf-104">The `NewSegment` method delivers a new segment to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="00fbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00fbf-105">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="00fbf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00fbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00fbf-107">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="00fbf-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="00fbf-108">Начальная координата носителя сегмента, в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="00fbf-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="00fbf-109">*тстоп*</span><span class="sxs-lookup"><span data-stu-id="00fbf-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="00fbf-110">Конечное расположение носителя сегмента в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="00fbf-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="00fbf-111">*драте*</span><span class="sxs-lookup"><span data-stu-id="00fbf-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="00fbf-112">Скорость обработки этого сегмента в процентах от исходной ставки.</span><span class="sxs-lookup"><span data-stu-id="00fbf-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00fbf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00fbf-113">Return value</span></span>

<span data-ttu-id="00fbf-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00fbf-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00fbf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00fbf-115">Remarks</span></span>

<span data-ttu-id="00fbf-116">Если объект использует поток, он помещает в очередь следующие элементы по порядку:</span><span class="sxs-lookup"><span data-stu-id="00fbf-116">If the object is using a thread, it queues the following items, in order:</span></span>

-   <span data-ttu-id="00fbf-117">НОВОЕ \_ сообщение управления сегментами.</span><span class="sxs-lookup"><span data-stu-id="00fbf-117">A NEW\_SEGMENT control message.</span></span>
-   <span data-ttu-id="00fbf-118">Данные сегмента.</span><span class="sxs-lookup"><span data-stu-id="00fbf-118">The segment data.</span></span>

<span data-ttu-id="00fbf-119">\_Сообщение о новом сегменте уведомляет поток о том, что следующий элемент в очереди будет содержать данные сегмента.</span><span class="sxs-lookup"><span data-stu-id="00fbf-119">The NEW\_SEGMENT message notifies the thread that the next item on the queue will contain segment data.</span></span> <span data-ttu-id="00fbf-120">Данные сегмента упаковываются в структуру, объявленную следующим образом:</span><span class="sxs-lookup"><span data-stu-id="00fbf-120">The segment data is bundled in a structure, declared as follows:</span></span>


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



<span data-ttu-id="00fbf-121">Поток вызывает метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) для входного ПИН-кода, используя данные, представленные в структуре.</span><span class="sxs-lookup"><span data-stu-id="00fbf-121">The thread calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin, using the data given in the structure.</span></span>

<span data-ttu-id="00fbf-122">Если объект не использует поток, он вызывает метод [**каутпуткуеуе:: сенданивай**](coutputqueue-sendanyway.md) для доставки всех ожидающих выборок.</span><span class="sxs-lookup"><span data-stu-id="00fbf-122">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="00fbf-123">Затем он вызывает **Ипин:: невсегмент** для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="00fbf-123">Then it calls **IPin::NewSegment** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="00fbf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="00fbf-124">Requirements</span></span>



| <span data-ttu-id="00fbf-125">Требование</span><span class="sxs-lookup"><span data-stu-id="00fbf-125">Requirement</span></span> | <span data-ttu-id="00fbf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="00fbf-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00fbf-127">Header</span><span class="sxs-lookup"><span data-stu-id="00fbf-127">Header</span></span><br/>  | <dl> <span data-ttu-id="00fbf-128"><dt>Аутпутк. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00fbf-128"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00fbf-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="00fbf-129">Library</span></span><br/> | <dl> <span data-ttu-id="00fbf-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="00fbf-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00fbf-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00fbf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00fbf-132">**Класс Каутпуткуеуе**</span><span class="sxs-lookup"><span data-stu-id="00fbf-132">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




