---
description: Метод Стартусингаутпутпин получает доступ к ПИН-коду для операции потоковой передачи.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Кдинамикаутпутпин. Стартусингаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657923"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a><span data-ttu-id="cbb84-103">Кдинамикаутпутпин. Стартусингаутпутпин, метод</span><span class="sxs-lookup"><span data-stu-id="cbb84-103">CDynamicOutputPin.StartUsingOutputPin method</span></span>

<span data-ttu-id="cbb84-104">`StartUsingOutputPin`Метод получает доступ к ПИН-коду для потоковой операции.</span><span class="sxs-lookup"><span data-stu-id="cbb84-104">The `StartUsingOutputPin` method obtains access to the pin for a streaming operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb84-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbb84-105">Syntax</span></span>


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="cbb84-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbb84-106">Parameters</span></span>

<span data-ttu-id="cbb84-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cbb84-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbb84-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbb84-108">Return value</span></span>

<span data-ttu-id="cbb84-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cbb84-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cbb84-110">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cbb84-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="cbb84-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cbb84-111">Return code</span></span>                                                                                           | <span data-ttu-id="cbb84-112">Описание</span><span class="sxs-lookup"><span data-stu-id="cbb84-112">Description</span></span>                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbb84-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cbb84-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="cbb84-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="cbb84-114">Success.</span></span><br/>                                               |
| <dl> <span data-ttu-id="cbb84-115"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="cbb84-115"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>          | <span data-ttu-id="cbb84-116">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="cbb84-116">Unexpected error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="cbb84-117"><dt>**\_ \_ изменение состояния VFW \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="cbb84-117"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="cbb84-118">Фильтр был остановлен, или ПИН-код начал запись на диск.</span><span class="sxs-lookup"><span data-stu-id="cbb84-118">The filter was stopped, or the pin has begun flushing.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbb84-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbb84-119">Remarks</span></span>

<span data-ttu-id="cbb84-120">Вызовите этот метод перед вызовом методов, которые доставляют данные в подключенный входной ПИН-код или изменяют тип носителя соединения.</span><span class="sxs-lookup"><span data-stu-id="cbb84-120">Call this method before calling any methods that deliver data to the connected input pin or that change the connection's media type.</span></span> <span data-ttu-id="cbb84-121">Например, это правило применяется к следующим методам:</span><span class="sxs-lookup"><span data-stu-id="cbb84-121">For example, this rule applies to the following methods:</span></span>

-   [<span data-ttu-id="cbb84-122">**Кдинамикаутпутпин:: Чанжеаутпутформат**</span><span class="sxs-lookup"><span data-stu-id="cbb84-122">**CDynamicOutputPin::ChangeOutputFormat**</span></span>](cdynamicoutputpin-changeoutputformat.md)
-   [<span data-ttu-id="cbb84-123">**Кдинамикаутпутпин:: Чанжемедиатипе**</span><span class="sxs-lookup"><span data-stu-id="cbb84-123">**CDynamicOutputPin::ChangeMediaType**</span></span>](cdynamicoutputpin-changemediatype.md)
-   [<span data-ttu-id="cbb84-124">**Кдинамикаутпутпин::D Инамикреконнект**</span><span class="sxs-lookup"><span data-stu-id="cbb84-124">**CDynamicOutputPin::DynamicReconnect**</span></span>](cdynamicoutputpin-dynamicreconnect.md)
-   [<span data-ttu-id="cbb84-125">**Кбасеаутпутпин::D еливер**</span><span class="sxs-lookup"><span data-stu-id="cbb84-125">**CBaseOutputPin::Deliver**</span></span>](cbaseoutputpin-deliver.md)
-   [<span data-ttu-id="cbb84-126">**Кбасеаутпутпин::D Еливерендофстреам**</span><span class="sxs-lookup"><span data-stu-id="cbb84-126">**CBaseOutputPin::DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md)
-   [<span data-ttu-id="cbb84-127">**Кбасеаутпутпин::D Еливерневсегмент**</span><span class="sxs-lookup"><span data-stu-id="cbb84-127">**CBaseOutputPin::DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)
-   [<span data-ttu-id="cbb84-128">**Имеминпутпин:: Receive**</span><span class="sxs-lookup"><span data-stu-id="cbb84-128">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="cbb84-129">**Имеминпутпин:: Рецеивемултипле**</span><span class="sxs-lookup"><span data-stu-id="cbb84-129">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="cbb84-130">**Ипин:: EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="cbb84-130">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="cbb84-131">**Ипин:: Невсегмент**</span><span class="sxs-lookup"><span data-stu-id="cbb84-131">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

<span data-ttu-id="cbb84-132">После этого вызовите метод [**кдинамикаутпутпин:: стопусингаутпутпин**](cdynamicoutputpin-stopusingoutputpin.md) , чтобы освободить доступ к ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="cbb84-132">Afterward, call the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method to release the access to the pin.</span></span>

<span data-ttu-id="cbb84-133">Если ПИН-код заблокирован, `StartUsingOutputPin` ожидает, пока ПИН-код не будет разблокирован.</span><span class="sxs-lookup"><span data-stu-id="cbb84-133">If the pin is blocked, `StartUsingOutputPin` waits for the pin to become unblocked.</span></span> <span data-ttu-id="cbb84-134">Если фильтр останавливается во время ожидания метода, метод немедленно возвращает \_ \_ изменение состояния VFW E \_ .</span><span class="sxs-lookup"><span data-stu-id="cbb84-134">If the filter stops while the method is waiting, the method immediately returns VFW\_E\_STATE\_CHANGED.</span></span> <span data-ttu-id="cbb84-135">ПИН-код содержит количество вызовов, которые `StartUsingOutputPin` были вызваны без соответствующего вызова **стопусингаутпутпин**.</span><span class="sxs-lookup"><span data-stu-id="cbb84-135">The pin maintains a count of how many times `StartUsingOutputPin` has been called without a corresponding call to **StopUsingOutputPin**.</span></span> <span data-ttu-id="cbb84-136">Если другой поток попытается заблокировать ПИН-код, пока этот счетчик не равен нулю, ПИН-код устанавливает состояние блокировки "Pending".</span><span class="sxs-lookup"><span data-stu-id="cbb84-136">If another thread tries to block the pin while this count is non-zero, the pin sets its blocking status to "pending."</span></span> <span data-ttu-id="cbb84-137">ПИН-код будет заблокирован после завершения всех операций потоковой передачи, в последнем вызове **стопусингаутпутпин**.</span><span class="sxs-lookup"><span data-stu-id="cbb84-137">The pin becomes blocked once all of the streaming operations have completed, in the final call to **StopUsingOutputPin**.</span></span>

<span data-ttu-id="cbb84-138">Не держите в [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) критическую секцию при вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="cbb84-138">Do not hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section when you call this method.</span></span> <span data-ttu-id="cbb84-139">В противном случае, если ПИН-код заблокирован, он не может быть разблокирован, что приведет к взаимоблокировке.</span><span class="sxs-lookup"><span data-stu-id="cbb84-139">Otherwise, if the pin is blocked, it can never become unblocked, causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbb84-140">Требования</span><span class="sxs-lookup"><span data-stu-id="cbb84-140">Requirements</span></span>



| <span data-ttu-id="cbb84-141">Требование</span><span class="sxs-lookup"><span data-stu-id="cbb84-141">Requirement</span></span> | <span data-ttu-id="cbb84-142">Значение</span><span class="sxs-lookup"><span data-stu-id="cbb84-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb84-143">Header</span><span class="sxs-lookup"><span data-stu-id="cbb84-143">Header</span></span><br/>  | <dl> <span data-ttu-id="cbb84-144"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbb84-144"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cbb84-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbb84-145">Library</span></span><br/> | <dl> <span data-ttu-id="cbb84-146"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cbb84-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbb84-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbb84-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb84-148">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="cbb84-148">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




