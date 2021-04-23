---
description: Метод Чанжеаутпутформат динамически изменяет тип носителя для соединения и доставляет сведения о новом сегменте.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Кдинамикаутпутпин. Чанжеаутпутформат, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669426"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a><span data-ttu-id="366a8-103">Кдинамикаутпутпин. Чанжеаутпутформат, метод</span><span class="sxs-lookup"><span data-stu-id="366a8-103">CDynamicOutputPin.ChangeOutputFormat method</span></span>

<span data-ttu-id="366a8-104">`ChangeOutputFormat`Метод динамически изменяет тип носителя для соединения и доставляет сведения о новом сегменте.</span><span class="sxs-lookup"><span data-stu-id="366a8-104">The `ChangeOutputFormat` method dynamically changes the media type for the connection, and delivers new segment information.</span></span> <span data-ttu-id="366a8-105">Это изменение может произойти при выполнении графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="366a8-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="366a8-106">После вызова этого метода не удается доставить образцы со старым типом носителя.</span><span class="sxs-lookup"><span data-stu-id="366a8-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="366a8-107">Вызывающий объект должен гарантировать, что старые примеры не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="366a8-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="366a8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="366a8-108">Syntax</span></span>


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a><span data-ttu-id="366a8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="366a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="366a8-110">*состоит*</span><span class="sxs-lookup"><span data-stu-id="366a8-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="366a8-111">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , указывающую тип носителя.</span><span class="sxs-lookup"><span data-stu-id="366a8-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> <dt>

<span data-ttu-id="366a8-112">*тсегментстарт*</span><span class="sxs-lookup"><span data-stu-id="366a8-112">*tSegmentStart*</span></span> 
</dt> <dd>

<span data-ttu-id="366a8-113">Время начала сегмента.</span><span class="sxs-lookup"><span data-stu-id="366a8-113">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="366a8-114">*тсегментстоп*</span><span class="sxs-lookup"><span data-stu-id="366a8-114">*tSegmentStop*</span></span> 
</dt> <dd>

<span data-ttu-id="366a8-115">Время окончания сегмента.</span><span class="sxs-lookup"><span data-stu-id="366a8-115">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="366a8-116">*дсегментрате*</span><span class="sxs-lookup"><span data-stu-id="366a8-116">*dSegmentRate*</span></span> 
</dt> <dd>

<span data-ttu-id="366a8-117">Частота сегментов.</span><span class="sxs-lookup"><span data-stu-id="366a8-117">Segment rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="366a8-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="366a8-118">Return value</span></span>

<span data-ttu-id="366a8-119">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="366a8-119">Returns an **HRESULT** value.</span></span> <span data-ttu-id="366a8-120">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="366a8-120">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="366a8-121">Код возврата</span><span class="sxs-lookup"><span data-stu-id="366a8-121">Return code</span></span>                                                                                           | <span data-ttu-id="366a8-122">Описание</span><span class="sxs-lookup"><span data-stu-id="366a8-122">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="366a8-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="366a8-123"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="366a8-124">Успешно.</span><span class="sxs-lookup"><span data-stu-id="366a8-124">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="366a8-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="366a8-125"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="366a8-126">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="366a8-126">Failure.</span></span> <span data-ttu-id="366a8-127">Возможно, фильтр-владелец не вызывал [**кдинамикаутпутпин:: сетконфигинфо**](cdynamicoutputpin-setconfiginfo.md).</span><span class="sxs-lookup"><span data-stu-id="366a8-127">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="366a8-128"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="366a8-128"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="366a8-129">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="366a8-129">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="366a8-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="366a8-130">Remarks</span></span>

<span data-ttu-id="366a8-131">Этот метод изменяет тип формата во время выполнения фильтра.</span><span class="sxs-lookup"><span data-stu-id="366a8-131">This method changes the format type while the filter is running.</span></span> <span data-ttu-id="366a8-132">Если подчиненный ПИН-код принимает новый формат, повторное подключение не требуется.</span><span class="sxs-lookup"><span data-stu-id="366a8-132">If the downstream pin accepts the new format, no reconnection is necessary.</span></span> <span data-ttu-id="366a8-133">В противном случае метод пытается повторно подключить ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="366a8-133">Otherwise, the method attempts to reconnect the pin.</span></span> <span data-ttu-id="366a8-134">Если метод успешно изменяет формат, он доставляет сведения о новом сегменте.</span><span class="sxs-lookup"><span data-stu-id="366a8-134">If the method successfully changes the format, it delivers the new segment information.</span></span> <span data-ttu-id="366a8-135">Этот метод вызывает метод [**кдинамикаутпутпин:: чанжемедиатипе**](cdynamicoutputpin-changemediatype.md) для изменения формата.</span><span class="sxs-lookup"><span data-stu-id="366a8-135">This method calls the [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) method to perform the format change.</span></span>

<span data-ttu-id="366a8-136">Перед вызовом этого метода необходимо вызвать метод [**кдинамикаутпутпин:: стартусингаутпутпин**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="366a8-136">You must call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="366a8-137">Требования</span><span class="sxs-lookup"><span data-stu-id="366a8-137">Requirements</span></span>



| <span data-ttu-id="366a8-138">Требование</span><span class="sxs-lookup"><span data-stu-id="366a8-138">Requirement</span></span> | <span data-ttu-id="366a8-139">Значение</span><span class="sxs-lookup"><span data-stu-id="366a8-139">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="366a8-140">Header</span><span class="sxs-lookup"><span data-stu-id="366a8-140">Header</span></span><br/>  | <dl> <span data-ttu-id="366a8-141"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="366a8-141"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="366a8-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="366a8-142">Library</span></span><br/> | <dl> <span data-ttu-id="366a8-143"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="366a8-143"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="366a8-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="366a8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="366a8-145">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="366a8-145">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




