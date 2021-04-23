---
description: Метод Нотифевент отправляет уведомление о событии диспетчеру графа фильтров.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Кбасефилтер. Нотифевент, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657892"
---
# <a name="cbasefilternotifyevent-method"></a><span data-ttu-id="3ddd8-103">Кбасефилтер. Нотифевент, метод</span><span class="sxs-lookup"><span data-stu-id="3ddd8-103">CBaseFilter.NotifyEvent method</span></span>

<span data-ttu-id="3ddd8-104">`NotifyEvent`Метод отправляет уведомление о событии диспетчеру графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="3ddd8-104">The `NotifyEvent` method sends an event notification to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddd8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ddd8-105">Syntax</span></span>


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a><span data-ttu-id="3ddd8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ddd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ddd8-107">*EventCode*</span><span class="sxs-lookup"><span data-stu-id="3ddd8-107">*EventCode*</span></span> 
</dt> <dd>

<span data-ttu-id="3ddd8-108">Код уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="3ddd8-108">Event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="3ddd8-109">*EventParam1*</span><span class="sxs-lookup"><span data-stu-id="3ddd8-109">*EventParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3ddd8-110">Первый параметр события.</span><span class="sxs-lookup"><span data-stu-id="3ddd8-110">First parameter of the event.</span></span>

</dd> <dt>

<span data-ttu-id="3ddd8-111">*EventParam2*</span><span class="sxs-lookup"><span data-stu-id="3ddd8-111">*EventParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3ddd8-112">Второй параметр события.</span><span class="sxs-lookup"><span data-stu-id="3ddd8-112">Second parameter of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ddd8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ddd8-113">Return value</span></span>

<span data-ttu-id="3ddd8-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ddd8-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3ddd8-115">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3ddd8-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="3ddd8-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3ddd8-116">Return code</span></span>                                                                               | <span data-ttu-id="3ddd8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="3ddd8-117">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ddd8-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3ddd8-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="3ddd8-119">Диспетчер графов фильтров не принимает уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="3ddd8-119">The filter graph manager is not accepting event notifications.</span></span><br/>                              |
| <dl> <span data-ttu-id="3ddd8-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3ddd8-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3ddd8-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3ddd8-121">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="3ddd8-122"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="3ddd8-122"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="3ddd8-123">Фильтр не имеет указателя на интерфейс [**имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="3ddd8-123">Filter does not have a pointer to the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ddd8-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ddd8-124">Remarks</span></span>

<span data-ttu-id="3ddd8-125">Список кодов уведомлений и значений параметров см. в разделе [коды уведомлений о событиях](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3ddd8-125">For a list of notification codes and parameter values, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="3ddd8-126">В базовом классе, если код события является EC \_ завершен, метод устанавливает для параметра *EventParam2* указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) фильтра.</span><span class="sxs-lookup"><span data-stu-id="3ddd8-126">In the base class, if the event code is EC\_COMPLETE, the method sets the *EventParam2* parameter to a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddd8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="3ddd8-127">Requirements</span></span>



| <span data-ttu-id="3ddd8-128">Требование</span><span class="sxs-lookup"><span data-stu-id="3ddd8-128">Requirement</span></span> | <span data-ttu-id="3ddd8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="3ddd8-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddd8-130">Header</span><span class="sxs-lookup"><span data-stu-id="3ddd8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3ddd8-131"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ddd8-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3ddd8-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3ddd8-132">Library</span></span><br/> | <dl> <span data-ttu-id="3ddd8-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3ddd8-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ddd8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ddd8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddd8-135">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="3ddd8-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




