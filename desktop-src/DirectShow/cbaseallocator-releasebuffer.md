---
description: 'Метод Релеасебуффер возвращает пример носителя в список примеров бесплатных носителей. Этот метод реализует метод Имемаллокатор:: Релеасебуффер.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Кбасеаллокатор. Релеасебуффер, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689233"
---
# <a name="cbaseallocatorreleasebuffer-method"></a><span data-ttu-id="13124-104">Кбасеаллокатор. Релеасебуффер, метод</span><span class="sxs-lookup"><span data-stu-id="13124-104">CBaseAllocator.ReleaseBuffer method</span></span>

<span data-ttu-id="13124-105">`ReleaseBuffer`Метод возвращает пример носителя в список примеров бесплатных носителей.</span><span class="sxs-lookup"><span data-stu-id="13124-105">The `ReleaseBuffer` method returns a media sample to the list of free media samples.</span></span> <span data-ttu-id="13124-106">Этот метод реализует метод [**имемаллокатор:: релеасебуффер**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="13124-106">This method implements the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="13124-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13124-107">Syntax</span></span>


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="13124-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="13124-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13124-109">*псампле*</span><span class="sxs-lookup"><span data-stu-id="13124-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="13124-110">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) объекта Sample мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="13124-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13124-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13124-111">Return value</span></span>

<span data-ttu-id="13124-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="13124-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="13124-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13124-113">Remarks</span></span>

<span data-ttu-id="13124-114">Когда число ссылок в образце носителя достигает нуля, пример вызывает **релеасебуффер** в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="13124-114">When a media sample's reference count reaches zero, the sample calls **ReleaseBuffer** with itself as the parameter.</span></span> <span data-ttu-id="13124-115">Этот метод выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="13124-115">This method performs the following actions.</span></span>

-   <span data-ttu-id="13124-116">Возвращает пример носителя в свободный список ([**кбасеаллокатор:: m \_ лфри**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="13124-116">Returns the media sample to the free list ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>
-   <span data-ttu-id="13124-117">Вызывает метод [**кбасеаллокатор:: нотифисампле**](cbaseallocator-notifysample.md) , который освобождает все потоки, заблокированные при вызове метода [**кбасеаллокатор::**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="13124-117">Calls the [**CBaseAllocator::NotifySample**](cbaseallocator-notifysample.md) method, which releases any threads that are blocked on calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>
-   <span data-ttu-id="13124-118">Если метод [**кбасеаллокатор:: сетнотифи**](cbaseallocator-setnotify.md) был вызван ранее, вызывается метод **Имемаллокаторнотификаллбакктемп:: нотифирелеасе** .</span><span class="sxs-lookup"><span data-stu-id="13124-118">If the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method was called previously, calls the **IMemAllocatorNotifyCallbackTemp::NotifyRelease** method.</span></span>
-   <span data-ttu-id="13124-119">При освобождении последней выборки, если имеется ожидающий вызов [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) , вызывает метод [**Кбасеаллокатор:: Free**](cbaseallocator-free.md) для освобождения буферной памяти.</span><span class="sxs-lookup"><span data-stu-id="13124-119">When the last sample is released, if there is a pending [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) call, calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method to release the buffer memory.</span></span> <span data-ttu-id="13124-120">(В базовом классе **Free** является чисто виртуальным методом.)</span><span class="sxs-lookup"><span data-stu-id="13124-120">(In the base class, **Free** is a pure virtual method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="13124-121">Требования</span><span class="sxs-lookup"><span data-stu-id="13124-121">Requirements</span></span>



| <span data-ttu-id="13124-122">Требование</span><span class="sxs-lookup"><span data-stu-id="13124-122">Requirement</span></span> | <span data-ttu-id="13124-123">Значение</span><span class="sxs-lookup"><span data-stu-id="13124-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13124-124">Header</span><span class="sxs-lookup"><span data-stu-id="13124-124">Header</span></span><br/>  | <dl> <span data-ttu-id="13124-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13124-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="13124-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13124-126">Library</span></span><br/> | <dl> <span data-ttu-id="13124-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="13124-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13124-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13124-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13124-129">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="13124-129">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




