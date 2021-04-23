---
description: Метод метода buffer извлекает пример носителя, содержащий буфер. Этот метод реализует метод Имемаллокатор::/buffer.
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Метод Кбасеаллокатор. WebMethod (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657853"
---
# <a name="cbaseallocatorgetbuffer-method"></a><span data-ttu-id="7fc79-104">Кбасеаллокатор. @ buffer, метод</span><span class="sxs-lookup"><span data-stu-id="7fc79-104">CBaseAllocator.GetBuffer method</span></span>

<span data-ttu-id="7fc79-105">`GetBuffer`Метод извлекает пример носителя, содержащий буфер.</span><span class="sxs-lookup"><span data-stu-id="7fc79-105">The `GetBuffer` method retrieves a media sample that contains a buffer.</span></span> <span data-ttu-id="7fc79-106">Этот метод реализует метод [**имемаллокатор::/buffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="7fc79-106">This method implements the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc79-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fc79-107">Syntax</span></span>


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7fc79-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fc79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc79-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="7fc79-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc79-110">Получает указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) буфера.</span><span class="sxs-lookup"><span data-stu-id="7fc79-110">Receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="7fc79-111">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7fc79-111">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7fc79-112">*пстарттиме*</span><span class="sxs-lookup"><span data-stu-id="7fc79-112">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc79-113">Указатель на время начала выборки.</span><span class="sxs-lookup"><span data-stu-id="7fc79-113">Pointer to the start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="7fc79-114">*пендтиме*</span><span class="sxs-lookup"><span data-stu-id="7fc79-114">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc79-115">Указатель на время окончания выборки.</span><span class="sxs-lookup"><span data-stu-id="7fc79-115">Pointer to the end time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="7fc79-116">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7fc79-116">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc79-117">Битовая комбинация нуля или более флагов.</span><span class="sxs-lookup"><span data-stu-id="7fc79-117">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="7fc79-118">Базовый класс поддерживает следующий флаг.</span><span class="sxs-lookup"><span data-stu-id="7fc79-118">The base class supports the following flag.</span></span>



| <span data-ttu-id="7fc79-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7fc79-119">Value</span></span>                                                                                                                                                          | <span data-ttu-id="7fc79-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7fc79-120">Meaning</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <span data-ttu-id="7fc79-121"><dt>**\_гбф \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc79-121"><dt>**AM\_GBF\_NOWAIT**</dt></span></span> </dl> | <span data-ttu-id="7fc79-122">Не дожидаться, пока буфер не станет доступным.</span><span class="sxs-lookup"><span data-stu-id="7fc79-122">Do not wait for a buffer to become available.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fc79-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fc79-123">Return value</span></span>

<span data-ttu-id="7fc79-124">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7fc79-124">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="7fc79-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7fc79-125">Return code</span></span>                                                                                           | <span data-ttu-id="7fc79-126">Описание</span><span class="sxs-lookup"><span data-stu-id="7fc79-126">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="7fc79-127"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc79-127"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="7fc79-128">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7fc79-128">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="7fc79-129"><dt>**VFW \_ E \_ не \_ зафиксирован**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc79-129"><dt>**VFW\_E\_NOT\_COMMITTED**</dt></span></span> </dl> | <span data-ttu-id="7fc79-130">Распределитель не зафиксирован.</span><span class="sxs-lookup"><span data-stu-id="7fc79-130">Allocator was not committed.</span></span><br/> |
| <dl> <span data-ttu-id="7fc79-131"><dt>**\_ \_ время ожидания VFW E**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc79-131"><dt>**VFW\_E\_TIMEOUT**</dt></span></span> </dl>        | <span data-ttu-id="7fc79-132">Истекло время ожидания.</span><span class="sxs-lookup"><span data-stu-id="7fc79-132">Timed out.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="7fc79-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fc79-133">Remarks</span></span>

<span data-ttu-id="7fc79-134">Если вызывающий объект не задает флаг **AM \_ \_ гбф** в *dwFlags*, этот метод блокируется до тех пор, пока не будет доступен следующий образец.</span><span class="sxs-lookup"><span data-stu-id="7fc79-134">Unless the caller specifies the **AM\_GBF\_NOWAIT** flag in *dwFlags*, this method blocks until the next sample is available.</span></span>

<span data-ttu-id="7fc79-135">Полученный пример носителя имеет допустимый указатель на выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="7fc79-135">The retrieved media sample has a valid pointer to the allocated buffer.</span></span> <span data-ttu-id="7fc79-136">Вызывающий объект отвечает за задание любых других свойств в образце, таких как отметки времени, время передачи мультимедиа или свойство точки синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7fc79-136">The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property.</span></span> <span data-ttu-id="7fc79-137">Дополнительные сведения см. в разделе [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span><span class="sxs-lookup"><span data-stu-id="7fc79-137">For more information, see [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span></span>

<span data-ttu-id="7fc79-138">В базовом классе параметры *пстарттиме* и *пендтиме* игнорируются.</span><span class="sxs-lookup"><span data-stu-id="7fc79-138">In the base class, the *pStartTime* and *pEndTime* parameters are ignored.</span></span> <span data-ttu-id="7fc79-139">Производные классы могут использовать эти значения.</span><span class="sxs-lookup"><span data-stu-id="7fc79-139">Derived classes can use these values.</span></span> <span data-ttu-id="7fc79-140">Например, распределитель для фильтра модуля [обработки видео](video-renderer-filter.md) использует эти значения для синхронизации переключения между областями DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="7fc79-140">For example, the allocator for the [Video Renderer](video-renderer-filter.md) filter uses these values to synchronize switching between DirectDraw surfaces.</span></span>

<span data-ttu-id="7fc79-141">Если метод должен ожидать выборки, он увеличивает число ожидающих объектов ([**кбасеаллокатор:: m \_ lCount**](cbaseallocator-m-lcount.md)) и вызывает функцию [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) для семафора ([**кбасеаллокатор:: m \_ хсем**](cbaseallocator-m-hsem.md)).</span><span class="sxs-lookup"><span data-stu-id="7fc79-141">If the method needs to wait on a sample, it increments the count of waiting objects ([**CBaseAllocator::m\_lCount**](cbaseallocator-m-lcount.md)) and the calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function on the semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)).</span></span> <span data-ttu-id="7fc79-142">Когда образец становится доступным, он вызывает метод [**кбасеаллокатор:: релеасебуффер**](cbaseallocator-releasebuffer.md) для распределителя, который увеличивает число семафоров на **m \_ lCount** (таким образом освобождает ожидающие потоки) и устанавливает **m \_ lCount** обратно в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="7fc79-142">When a sample becomes available, it calls the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method on the allocator, which increases the semaphore count by **m\_lCount** (thereby releasing the waiting threads) and sets **m\_lCount** back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc79-143">Требования</span><span class="sxs-lookup"><span data-stu-id="7fc79-143">Requirements</span></span>



| <span data-ttu-id="7fc79-144">Требование</span><span class="sxs-lookup"><span data-stu-id="7fc79-144">Requirement</span></span> | <span data-ttu-id="7fc79-145">Значение</span><span class="sxs-lookup"><span data-stu-id="7fc79-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc79-146">Header</span><span class="sxs-lookup"><span data-stu-id="7fc79-146">Header</span></span><br/>  | <dl> <span data-ttu-id="7fc79-147"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fc79-147"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7fc79-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7fc79-148">Library</span></span><br/> | <dl> <span data-ttu-id="7fc79-149"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7fc79-149"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc79-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fc79-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc79-151">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="7fc79-151">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

