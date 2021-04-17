---
description: Метод Филлбуффер заполняет пример носителя данными.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Метод Ксаурцестреам. Филлбуффер (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685384"
---
# <a name="csourcestreamfillbuffer-method"></a><span data-ttu-id="0353b-103">Ксаурцестреам. Филлбуффер, метод</span><span class="sxs-lookup"><span data-stu-id="0353b-103">CSourceStream.FillBuffer method</span></span>

<span data-ttu-id="0353b-104">`FillBuffer`Метод заполняет пример носителя данными.</span><span class="sxs-lookup"><span data-stu-id="0353b-104">The `FillBuffer` method fills a media sample with data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0353b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0353b-105">Syntax</span></span>


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0353b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0353b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0353b-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="0353b-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0353b-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="0353b-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0353b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0353b-109">Return value</span></span>

<span data-ttu-id="0353b-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0353b-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0353b-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0353b-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0353b-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0353b-112">Return code</span></span>                                                                             | <span data-ttu-id="0353b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0353b-113">Description</span></span>              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="0353b-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0353b-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0353b-115">Конец потока</span><span class="sxs-lookup"><span data-stu-id="0353b-115">End of stream</span></span><br/> |
| <dl> <span data-ttu-id="0353b-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0353b-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0353b-117">Успешно</span><span class="sxs-lookup"><span data-stu-id="0353b-117">Success</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="0353b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0353b-118">Remarks</span></span>

<span data-ttu-id="0353b-119">Производный класс должен реализовывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="0353b-119">The derived class must implement this method.</span></span>

<span data-ttu-id="0353b-120">Образец носителя, указанный для этого метода, не имеет штампов времени.</span><span class="sxs-lookup"><span data-stu-id="0353b-120">The media sample given to this method has no time stamps.</span></span> <span data-ttu-id="0353b-121">Производный класс должен вызвать метод [**имедиасампле:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) , чтобы задать метки времени.</span><span class="sxs-lookup"><span data-stu-id="0353b-121">The derived class should call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method to set the time stamps.</span></span> <span data-ttu-id="0353b-122">При необходимости для типа мультимедиа производный класс также должен задавать время носителя, вызывая метод [**имедиасампле:: сетмедиатиме**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="0353b-122">If appropriate for the media type, the derived class should also set the media times, by calling the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span> <span data-ttu-id="0353b-123">Дополнительные сведения см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="0353b-123">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

<span data-ttu-id="0353b-124">Возвращает \_ значение false в конце потока.</span><span class="sxs-lookup"><span data-stu-id="0353b-124">Return S\_FALSE at the end of the stream.</span></span> <span data-ttu-id="0353b-125">В результате класс **ксаурцестреам** отправляет уведомление об окончании потока и останавливает цикл обработки буфера.</span><span class="sxs-lookup"><span data-stu-id="0353b-125">This causes the **CSourceStream** class to send the end-of-stream notification and halt the buffer processing loop.</span></span> <span data-ttu-id="0353b-126">Дополнительные сведения см. в разделе [**ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="0353b-126">See [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0353b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0353b-127">Requirements</span></span>



| <span data-ttu-id="0353b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0353b-128">Requirement</span></span> | <span data-ttu-id="0353b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0353b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0353b-130">Header</span><span class="sxs-lookup"><span data-stu-id="0353b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0353b-131"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0353b-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0353b-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0353b-132">Library</span></span><br/> | <dl> <span data-ttu-id="0353b-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0353b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0353b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0353b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0353b-135">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="0353b-135">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




