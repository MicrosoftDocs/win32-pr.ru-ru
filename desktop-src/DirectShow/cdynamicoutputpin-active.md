---
description: Активный метод уведомляет ПИН-код о том, что фильтр активен.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Метод Кдинамикаутпутпин. Active (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669431"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="fbaaf-103">Кдинамикаутпутпин. активный метод</span><span class="sxs-lookup"><span data-stu-id="fbaaf-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="fbaaf-104">`Active`Метод уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="fbaaf-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbaaf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbaaf-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="fbaaf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbaaf-106">Parameters</span></span>

<span data-ttu-id="fbaaf-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fbaaf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbaaf-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbaaf-108">Return value</span></span>

<span data-ttu-id="fbaaf-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbaaf-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fbaaf-110">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fbaaf-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="fbaaf-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fbaaf-111">Return code</span></span>                                                                            | <span data-ttu-id="fbaaf-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fbaaf-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbaaf-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="fbaaf-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="fbaaf-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fbaaf-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="fbaaf-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="fbaaf-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="fbaaf-116">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="fbaaf-116">Failure.</span></span> <span data-ttu-id="fbaaf-117">[**Кдинамикаутпутпин:: сетконфигинфо**](cdynamicoutputpin-setconfiginfo.md) не был вызван.</span><span class="sxs-lookup"><span data-stu-id="fbaaf-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fbaaf-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbaaf-118">Remarks</span></span>

<span data-ttu-id="fbaaf-119">Этот метод переопределяет метод [**кбасеаутпутпин:: Active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="fbaaf-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="fbaaf-120">Он сбрасывает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="fbaaf-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="fbaaf-121">Если фильтр-владелец не вызвал **сетконфигинфо**, этот метод возвращает значение E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="fbaaf-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbaaf-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fbaaf-122">Requirements</span></span>



| <span data-ttu-id="fbaaf-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fbaaf-123">Requirement</span></span> | <span data-ttu-id="fbaaf-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fbaaf-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbaaf-125">Header</span><span class="sxs-lookup"><span data-stu-id="fbaaf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fbaaf-126"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbaaf-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fbaaf-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fbaaf-127">Library</span></span><br/> | <dl> <span data-ttu-id="fbaaf-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fbaaf-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbaaf-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbaaf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbaaf-130">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="fbaaf-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




