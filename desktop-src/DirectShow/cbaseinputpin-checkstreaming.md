---
description: Определяет, может ли ПИН-код принимать выборки.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Кбасеинпутпин. Чеккстреаминг, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656867"
---
# <a name="cbaseinputpincheckstreaming-method"></a><span data-ttu-id="cd9f3-103">Кбасеинпутпин. Чеккстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="cd9f3-103">CBaseInputPin.CheckStreaming method</span></span>

<span data-ttu-id="cd9f3-104">Определяет, может ли ПИН-код принимать выборки.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-104">Determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9f3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd9f3-105">Syntax</span></span>


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="cd9f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd9f3-106">Parameters</span></span>

<span data-ttu-id="cd9f3-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd9f3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd9f3-108">Return value</span></span>

<span data-ttu-id="cd9f3-109">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="cd9f3-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cd9f3-110">Return code</span></span>                                                                                           | <span data-ttu-id="cd9f3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cd9f3-111">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="cd9f3-112"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cd9f3-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="cd9f3-113">Успешно.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-113">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="cd9f3-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cd9f3-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="cd9f3-115">ПИН-код в данный момент очищается.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-115">Pin is currently flushing.</span></span><br/> |
| <dl> <span data-ttu-id="cd9f3-116"><dt>**\_ \_ ошибка среды выполнения VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cd9f3-116"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="cd9f3-117">Произошла ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-117">A run-time error occurred.</span></span><br/> |
| <dl> <span data-ttu-id="cd9f3-118"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="cd9f3-118"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="cd9f3-119">ПИН-код остановлен.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-119">The pin is stopped.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="cd9f3-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd9f3-120">Remarks</span></span>

<span data-ttu-id="cd9f3-121">Производный класс может переопределить этот метод для выполнения дальнейших проверок.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-121">The derived class can override this method to perform further checks.</span></span> <span data-ttu-id="cd9f3-122">В переопределяющем методе также вызывается реализация базового класса.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-122">In the overriding method, also call the base class implementation.</span></span>

<span data-ttu-id="cd9f3-123">Метод [**кбасеинпутпин:: Receive**](cbaseinputpin-receive.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-123">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method calls this method.</span></span> <span data-ttu-id="cd9f3-124">Для вызова этого метода следует переопределить метод [**кбасепин:: EndOfStream**](cbasepin-endofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="cd9f3-124">You should override the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method to call this method as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9f3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="cd9f3-125">Requirements</span></span>



| <span data-ttu-id="cd9f3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="cd9f3-126">Requirement</span></span> | <span data-ttu-id="cd9f3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cd9f3-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9f3-128">Header</span><span class="sxs-lookup"><span data-stu-id="cd9f3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="cd9f3-129"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd9f3-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cd9f3-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd9f3-130">Library</span></span><br/> | <dl> <span data-ttu-id="cd9f3-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cd9f3-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd9f3-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd9f3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9f3-133">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="cd9f3-133">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




