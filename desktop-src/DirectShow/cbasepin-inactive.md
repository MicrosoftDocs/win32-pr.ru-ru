---
description: Кбасепин. Inactive-метод. неактивный метод уведомляет ПИН-код о том, что фильтр больше не активен.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Метод Кбасепин. Inactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c0d9ec403b53c3197c001e966ce7efd5eb8bed2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099342"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="4a08b-103">Кбасепин. Inactive, метод</span><span class="sxs-lookup"><span data-stu-id="4a08b-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="4a08b-104">`Inactive`Метод уведомляет ПИН-код о том, что фильтр больше не активен.</span><span class="sxs-lookup"><span data-stu-id="4a08b-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a08b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a08b-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="4a08b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a08b-106">Parameters</span></span>

<span data-ttu-id="4a08b-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4a08b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a08b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a08b-108">Return value</span></span>

<span data-ttu-id="4a08b-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4a08b-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a08b-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="4a08b-110">Remarks</span></span>

<span data-ttu-id="4a08b-111">При остановке фильтра класс [**кбасефилтер**](cbasefilter.md) вызывает этот метод для всех подключенных контактов фильтра.</span><span class="sxs-lookup"><span data-stu-id="4a08b-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="4a08b-112">Этот метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="4a08b-112">This method does nothing in the base class.</span></span> <span data-ttu-id="4a08b-113">Производные классы должны переопределять этот метод, чтобы освободить все ресурсы, полученные методом [**кбасепин:: Active**](cbasepin-active.md) ; Например, для дефиксации распределителя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="4a08b-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="4a08b-114">Внутреннее состояние диспетчера графа фильтра не обновляется до тех пор, пока этот метод не возвратит значение, поэтому не проверяйте состояние из этого метода.</span><span class="sxs-lookup"><span data-stu-id="4a08b-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a08b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4a08b-115">Requirements</span></span>



| <span data-ttu-id="4a08b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4a08b-116">Requirement</span></span> | <span data-ttu-id="4a08b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4a08b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a08b-118">Header</span><span class="sxs-lookup"><span data-stu-id="4a08b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4a08b-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a08b-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4a08b-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a08b-120">Library</span></span><br/> | <dl> <span data-ttu-id="4a08b-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4a08b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a08b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4a08b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a08b-123">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="4a08b-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




