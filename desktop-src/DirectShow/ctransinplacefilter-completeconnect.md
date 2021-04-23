---
description: Метод Комплетеконнект завершает подключение ПИН-кода.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Ктрансинплацефилтер. Комплетеконнект, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdc9d1d5567cda2e4b0fd4a351136405493ef61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657982"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a><span data-ttu-id="1220c-103">Ктрансинплацефилтер. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="1220c-103">CTransInPlaceFilter.CompleteConnect method</span></span>

<span data-ttu-id="1220c-104">`CompleteConnect`Метод завершает соединение с закреплением.</span><span class="sxs-lookup"><span data-stu-id="1220c-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1220c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1220c-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="1220c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1220c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1220c-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="1220c-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="1220c-108">Член перечисленного типа с [**\_ направлением ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий, какой ПИН-код фильтра делает соединение.</span><span class="sxs-lookup"><span data-stu-id="1220c-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1220c-109">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="1220c-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="1220c-110">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода в этой попытке подключения.</span><span class="sxs-lookup"><span data-stu-id="1220c-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1220c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1220c-111">Return value</span></span>

<span data-ttu-id="1220c-112">Возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1220c-112">Returns an **HRESULT**.</span></span> <span data-ttu-id="1220c-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1220c-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1220c-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1220c-114">Return code</span></span>                                                                                           | <span data-ttu-id="1220c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1220c-115">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1220c-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1220c-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="1220c-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="1220c-117">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="1220c-118"><dt>**VFW \_ E \_ не \_ в \_ графе**</dt></span><span class="sxs-lookup"><span data-stu-id="1220c-118"><dt>**VFW\_E\_NOT\_IN\_GRAPH**</dt></span></span> </dl> | <span data-ttu-id="1220c-119">Фильтр не находится на графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="1220c-119">The filter is not in a filter graph.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1220c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1220c-120">Remarks</span></span>

<span data-ttu-id="1220c-121">Этот метод переопределяет метод [**ктрансформфилтер:: комплетеконнект**](ctransformfilter-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="1220c-121">This method overrides the [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method.</span></span>

<span data-ttu-id="1220c-122">Поведение фильтра зависит от порядка подключения ПИН-кода:</span><span class="sxs-lookup"><span data-stu-id="1220c-122">The behavior of the filter depends on the order of the pin connections:</span></span>

-   <span data-ttu-id="1220c-123">Если входной ПИН-код подключен первым, подключение использует временный распределитель.</span><span class="sxs-lookup"><span data-stu-id="1220c-123">If the input pin is connected first, the connection uses a temporary allocator.</span></span> <span data-ttu-id="1220c-124">Когда выходной ПИН-код подключен, фильтр повторно подключает входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="1220c-124">When the output pin is connected, the filter reconnects the input pin.</span></span> <span data-ttu-id="1220c-125">Повторное подключение входного ПИН-кода вызывает повторное согласование распределителя в вышестоящем фильтре.</span><span class="sxs-lookup"><span data-stu-id="1220c-125">Reconnecting the input pin causes the upstream filter to renegotiate the allocator.</span></span> <span data-ttu-id="1220c-126">На этом этапе входной ПИН-код предлагает распределитель из подчиненного фильтра.</span><span class="sxs-lookup"><span data-stu-id="1220c-126">At that point, the input pin proposes an allocator from the downstream filter.</span></span> <span data-ttu-id="1220c-127">Дополнительные сведения см. в разделе [**ктрансинплацеинпутпин:: распределителе**](ctransinplaceinputpin-getallocator.md).</span><span class="sxs-lookup"><span data-stu-id="1220c-127">For more information, see [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span></span>
-   <span data-ttu-id="1220c-128">Если выходной ПИН-код подключен первым, то закрепление вывода не выбирает распределитель.</span><span class="sxs-lookup"><span data-stu-id="1220c-128">If the output pin is connected first, the output pin does not select an allocator.</span></span> <span data-ttu-id="1220c-129">Когда входной ПИН-код подключен, он согласовывает распределитель для обоих подключений.</span><span class="sxs-lookup"><span data-stu-id="1220c-129">When the input pin is connected, it negotiates an allocator for both connections.</span></span> <span data-ttu-id="1220c-130">Если входные и выходные типы носителей не совпадают, фильтр повторно подключает выходной ПИН-код с помощью входного типа.</span><span class="sxs-lookup"><span data-stu-id="1220c-130">If the input and output media types are not the same, the filter reconnects the output pin using the input type.</span></span>

<span data-ttu-id="1220c-131">Фильтр выполняет все пересоединения ПИН-кода, вызывая метод [**кбасефилтер:: реконнектпин**](cbasefilter-reconnectpin.md) .</span><span class="sxs-lookup"><span data-stu-id="1220c-131">The filter performs all pin reconnections by calling the [**CBaseFilter::ReconnectPin**](cbasefilter-reconnectpin.md) method.</span></span> <span data-ttu-id="1220c-132">Метод **реконнектпин** , в свою очередь, вызывает метод [**IFilterGraph2:: реконнектекс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="1220c-132">The **ReconnectPin** method, in turn, calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="1220c-133">Требования</span><span class="sxs-lookup"><span data-stu-id="1220c-133">Requirements</span></span>



| <span data-ttu-id="1220c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="1220c-134">Requirement</span></span> | <span data-ttu-id="1220c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="1220c-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1220c-136">Header</span><span class="sxs-lookup"><span data-stu-id="1220c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1220c-137"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1220c-137"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1220c-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1220c-138">Library</span></span><br/> | <dl> <span data-ttu-id="1220c-139"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1220c-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1220c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1220c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1220c-141">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="1220c-141">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




