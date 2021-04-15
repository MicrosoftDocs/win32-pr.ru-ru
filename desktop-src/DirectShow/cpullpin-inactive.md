---
description: Неактивный метод завершает работу рабочего потока, который извлекает данные из выходного ПИН-кода. Этот метод также отменяет выделение распределителя.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Метод Кпуллпин. Inactive (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669054"
---
# <a name="cpullpininactive-method"></a><span data-ttu-id="0b42f-104">Кпуллпин. Inactive, метод</span><span class="sxs-lookup"><span data-stu-id="0b42f-104">CPullPin.Inactive method</span></span>

<span data-ttu-id="0b42f-105">`Inactive`Метод завершает работу рабочего потока, который извлекает данные из выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="0b42f-105">The `Inactive` method shuts down the worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="0b42f-106">Этот метод также отменяет выделение распределителя.</span><span class="sxs-lookup"><span data-stu-id="0b42f-106">This method also decommits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b42f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b42f-107">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="0b42f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b42f-108">Parameters</span></span>

<span data-ttu-id="0b42f-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0b42f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b42f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b42f-110">Return value</span></span>

<span data-ttu-id="0b42f-111">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0b42f-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b42f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b42f-112">Remarks</span></span>

<span data-ttu-id="0b42f-113">Вызывайте этот метод, когда фильтр владельца станет неактивным.</span><span class="sxs-lookup"><span data-stu-id="0b42f-113">Call this method when the owning filter becomes inactive.</span></span> <span data-ttu-id="0b42f-114">(Если входной ПИН-код является производным от [**кбасепин**](cbasepin.md), переопределите метод [**Кбасепин:: Inactive**](cbasepin-inactive.md) .)</span><span class="sxs-lookup"><span data-stu-id="0b42f-114">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Inactive**](cbasepin-inactive.md) method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="0b42f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0b42f-115">Requirements</span></span>



| <span data-ttu-id="0b42f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0b42f-116">Requirement</span></span> | <span data-ttu-id="0b42f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0b42f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b42f-118">Header</span><span class="sxs-lookup"><span data-stu-id="0b42f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0b42f-119"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b42f-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="0b42f-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0b42f-120">Library</span></span><br/> | <dl> <span data-ttu-id="0b42f-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0b42f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b42f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b42f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b42f-123">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="0b42f-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




