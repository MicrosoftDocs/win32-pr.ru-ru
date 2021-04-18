---
description: Метод Сендкуалити отправляет сообщение с качеством, чтобы указать, что должен делать поставщик в отношении качества.
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: Кбасевидеорендерер. Сендкуалити, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656961"
---
# <a name="cbasevideorenderersendquality-method"></a><span data-ttu-id="f130b-103">Кбасевидеорендерер. Сендкуалити, метод</span><span class="sxs-lookup"><span data-stu-id="f130b-103">CBaseVideoRenderer.SendQuality method</span></span>

<span data-ttu-id="f130b-104">`SendQuality`Метод отправляет сообщение с качеством, чтобы указать, что должен сделать поставщик о качестве качества.</span><span class="sxs-lookup"><span data-stu-id="f130b-104">The `SendQuality` method sends a quality message to indicate what the supplier should do about quality.</span></span>

## <a name="syntax"></a><span data-ttu-id="f130b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f130b-105">Syntax</span></span>


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a><span data-ttu-id="f130b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f130b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f130b-107">*трлате*</span><span class="sxs-lookup"><span data-stu-id="f130b-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="f130b-108">Время, в течение которого кадр находится в конце.</span><span class="sxs-lookup"><span data-stu-id="f130b-108">Amount of time by which the frame is late.</span></span>

</dd> <dt>

<span data-ttu-id="f130b-109">*трреалстреам*</span><span class="sxs-lookup"><span data-stu-id="f130b-109">*trRealStream*</span></span> 
</dt> <dd>

<span data-ttu-id="f130b-110">Время куррентстреам.</span><span class="sxs-lookup"><span data-stu-id="f130b-110">Currentstream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f130b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f130b-111">Return value</span></span>

<span data-ttu-id="f130b-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f130b-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f130b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f130b-113">Remarks</span></span>

<span data-ttu-id="f130b-114">Эта функция-член отправляет поток сообщений контроля качества в Управление качеством.</span><span class="sxs-lookup"><span data-stu-id="f130b-114">This member function sends a quality control message upstream to control quality management.</span></span> <span data-ttu-id="f130b-115">Характер качественного сообщения (то есть необходимость уменьшить или увеличить количество выборок) определяется в реализации управления качеством в этом производном классе (см. [**кбасевидеорендерер:: шаулддравсампленов**](cbasevideorenderer-shoulddrawsamplenow.md)).</span><span class="sxs-lookup"><span data-stu-id="f130b-115">The nature of the quality message (that is, whether to reduce or increase the number of samples) is determined in the quality management implementation in this derived class (see [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f130b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f130b-116">Requirements</span></span>



| <span data-ttu-id="f130b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f130b-117">Requirement</span></span> | <span data-ttu-id="f130b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f130b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f130b-119">Header</span><span class="sxs-lookup"><span data-stu-id="f130b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f130b-120"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f130b-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f130b-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f130b-121">Library</span></span><br/> | <dl> <span data-ttu-id="f130b-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f130b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f130b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f130b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f130b-124">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="f130b-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




