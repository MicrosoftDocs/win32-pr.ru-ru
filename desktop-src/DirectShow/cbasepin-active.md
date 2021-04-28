---
description: Кбасепин. Active Method — активный метод уведомляет ПИН-код о том, что фильтр активен.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Метод Кбасепин. Active (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096111"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="0ef28-103">Кбасепин. активный метод</span><span class="sxs-lookup"><span data-stu-id="0ef28-103">CBasePin.Active method</span></span>

<span data-ttu-id="0ef28-104">`Active`Метод уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="0ef28-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ef28-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="0ef28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ef28-106">Parameters</span></span>

<span data-ttu-id="0ef28-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ef28-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ef28-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ef28-108">Return value</span></span>

<span data-ttu-id="0ef28-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0ef28-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef28-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="0ef28-110">Remarks</span></span>

<span data-ttu-id="0ef28-111">Когда фильтр переходит из остановленного в приостановленный, класс [**кбасефилтер**](cbasefilter.md) вызывает этот метод для всех подключенных контактов фильтра.</span><span class="sxs-lookup"><span data-stu-id="0ef28-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="0ef28-112">Этот метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="0ef28-112">This method does nothing in the base class.</span></span> <span data-ttu-id="0ef28-113">Производные классы могут переопределять этот метод; Например, ПИН-код может зафиксировать распределительы или получить аппаратные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0ef28-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="0ef28-114">Внутреннее состояние диспетчера графа фильтра не обновляется до тех пор, пока эта функция-член не вернет значение, поэтому не проверяйте состояние из этого метода.</span><span class="sxs-lookup"><span data-stu-id="0ef28-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef28-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0ef28-115">Requirements</span></span>



| <span data-ttu-id="0ef28-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0ef28-116">Requirement</span></span> | <span data-ttu-id="0ef28-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0ef28-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef28-118">Header</span><span class="sxs-lookup"><span data-stu-id="0ef28-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef28-119"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef28-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ef28-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ef28-120">Library</span></span><br/> | <dl> <span data-ttu-id="0ef28-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef28-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef28-122">См. также</span><span class="sxs-lookup"><span data-stu-id="0ef28-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef28-123">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="0ef28-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




