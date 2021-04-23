---
description: 'Метод Сетсинк задает внешний диспетчер качества. Этот метод реализует метод Икуалитиконтрол:: Сетсинк.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Кбасепин. Сетсинк, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657204"
---
# <a name="cbasepinsetsink-method"></a><span data-ttu-id="52a57-104">Кбасепин. Сетсинк, метод</span><span class="sxs-lookup"><span data-stu-id="52a57-104">CBasePin.SetSink method</span></span>

<span data-ttu-id="52a57-105">`SetSink`Метод задает внешний диспетчер качества.</span><span class="sxs-lookup"><span data-stu-id="52a57-105">The `SetSink` method sets an external quality manager.</span></span> <span data-ttu-id="52a57-106">Этот метод реализует метод [**икуалитиконтрол:: сетсинк**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .</span><span class="sxs-lookup"><span data-stu-id="52a57-106">This method implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a57-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52a57-107">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="52a57-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52a57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a57-109">*пикк*</span><span class="sxs-lookup"><span data-stu-id="52a57-109">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="52a57-110">Указатель на интерфейс [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) диспетчера качества.</span><span class="sxs-lookup"><span data-stu-id="52a57-110">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface of the quality manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a57-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52a57-111">Return value</span></span>

<span data-ttu-id="52a57-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="52a57-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="52a57-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52a57-113">Remarks</span></span>

<span data-ttu-id="52a57-114">Вызовите этот метод, чтобы перенаправить сообщения контроля качества внешнему диспетчеру качества.</span><span class="sxs-lookup"><span data-stu-id="52a57-114">Call this method to redirect quality-control messages to an external quality manager.</span></span> <span data-ttu-id="52a57-115">Дополнительные сведения см. в разделе [Управление качеством](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="52a57-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52a57-116">Требования</span><span class="sxs-lookup"><span data-stu-id="52a57-116">Requirements</span></span>



| <span data-ttu-id="52a57-117">Требование</span><span class="sxs-lookup"><span data-stu-id="52a57-117">Requirement</span></span> | <span data-ttu-id="52a57-118">Значение</span><span class="sxs-lookup"><span data-stu-id="52a57-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52a57-119">Header</span><span class="sxs-lookup"><span data-stu-id="52a57-119">Header</span></span><br/>  | <dl> <span data-ttu-id="52a57-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52a57-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="52a57-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52a57-121">Library</span></span><br/> | <dl> <span data-ttu-id="52a57-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="52a57-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a57-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52a57-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a57-124">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="52a57-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




