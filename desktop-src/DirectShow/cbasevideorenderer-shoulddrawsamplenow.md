---
description: Метод Шаулддравсампленов определяет, следует ли рисовать видео без установки связи таймера с часами.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Кбасевидеорендерер. Шаулддравсампленов, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674999"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a><span data-ttu-id="a911c-103">Кбасевидеорендерер. Шаулддравсампленов, метод</span><span class="sxs-lookup"><span data-stu-id="a911c-103">CBaseVideoRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="a911c-104">`ShouldDrawSampleNow`Метод определяет, следует ли рисовать видео без установки связи таймера с часами.</span><span class="sxs-lookup"><span data-stu-id="a911c-104">The `ShouldDrawSampleNow` method determines if the video should be drawn without setting a timer advise link with the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="a911c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a911c-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a><span data-ttu-id="a911c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a911c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a911c-107">*пмедиасампле*</span><span class="sxs-lookup"><span data-stu-id="a911c-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a911c-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) для образца.</span><span class="sxs-lookup"><span data-stu-id="a911c-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface for the sample.</span></span>

</dd> <dt>

<span data-ttu-id="a911c-109">*птрстарт*</span><span class="sxs-lookup"><span data-stu-id="a911c-109">*ptrStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a911c-110">Указатель на время начала подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="a911c-110">Pointer to the time to begin rendering.</span></span>

</dd> <dt>

<span data-ttu-id="a911c-111">*птренд*</span><span class="sxs-lookup"><span data-stu-id="a911c-111">*ptrEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a911c-112">Указатель на время, когда нужно прерывать отрисовку.</span><span class="sxs-lookup"><span data-stu-id="a911c-112">Pointer to the time to stop rendering.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a911c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a911c-113">Return value</span></span>

<span data-ttu-id="a911c-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a911c-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a911c-115">Возвращает \_ «ОК», означая, что рисуется один раз без ожидания, «ложь», \_ означающий прорисовку во времени *птрстарт*, или ошибка, означающая, что не Нарисуйте пример, то есть пропустите его, чтобы сэкономить время.</span><span class="sxs-lookup"><span data-stu-id="a911c-115">Returns S\_OK to mean draw at once without waiting, S\_FALSE to mean draw at time *ptrStart*, or an error to mean do not draw the sample; that is, skip it to save time.</span></span>

## <a name="remarks"></a><span data-ttu-id="a911c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a911c-116">Remarks</span></span>

<span data-ttu-id="a911c-117">Эта функция члена переопределяет [**кбасерендерер:: шаулддравсампленов**](cbaserenderer-shoulddrawsamplenow.md).</span><span class="sxs-lookup"><span data-stu-id="a911c-117">This member function overrides [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a911c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a911c-118">Requirements</span></span>



| <span data-ttu-id="a911c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a911c-119">Requirement</span></span> | <span data-ttu-id="a911c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a911c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a911c-121">Header</span><span class="sxs-lookup"><span data-stu-id="a911c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a911c-122"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a911c-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a911c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a911c-123">Library</span></span><br/> | <dl> <span data-ttu-id="a911c-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a911c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a911c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a911c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a911c-126">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="a911c-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




