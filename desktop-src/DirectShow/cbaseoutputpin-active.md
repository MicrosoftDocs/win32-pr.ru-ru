---
description: Кбасеаутпутпин. Active Method — активный метод уведомляет ПИН-код о том, что фильтр активен.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Метод Кбасеаутпутпин. Active (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096212"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="dcc36-103">Кбасеаутпутпин. активный метод</span><span class="sxs-lookup"><span data-stu-id="dcc36-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="dcc36-104">`Active`Метод уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="dcc36-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc36-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcc36-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="dcc36-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcc36-106">Parameters</span></span>

<span data-ttu-id="dcc36-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dcc36-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcc36-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcc36-108">Return value</span></span>

<span data-ttu-id="dcc36-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dcc36-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dcc36-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="dcc36-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="dcc36-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dcc36-111">Return code</span></span>                                                                                          | <span data-ttu-id="dcc36-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dcc36-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="dcc36-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc36-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="dcc36-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="dcc36-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="dcc36-115"><dt>**VFW \_ E \_ без \_ распределителя**</dt></span><span class="sxs-lookup"><span data-stu-id="dcc36-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="dcc36-116">Распределитель недоступен.</span><span class="sxs-lookup"><span data-stu-id="dcc36-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dcc36-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="dcc36-117">Remarks</span></span>

<span data-ttu-id="dcc36-118">Этот метод переопределяет метод [**кбасепин:: Active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="dcc36-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="dcc36-119">Он вызывает метод [**имемаллокатор:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) для распределителя, чтобы выделить память для буферов.</span><span class="sxs-lookup"><span data-stu-id="dcc36-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="dcc36-120">При переопределении этого метода вызовите метод базового класса из переопределяющего метода.</span><span class="sxs-lookup"><span data-stu-id="dcc36-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc36-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dcc36-121">Requirements</span></span>



| <span data-ttu-id="dcc36-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dcc36-122">Requirement</span></span> | <span data-ttu-id="dcc36-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dcc36-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc36-124">Header</span><span class="sxs-lookup"><span data-stu-id="dcc36-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dcc36-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc36-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dcc36-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dcc36-126">Library</span></span><br/> | <dl> <span data-ttu-id="dcc36-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc36-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcc36-128">См. также</span><span class="sxs-lookup"><span data-stu-id="dcc36-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc36-129">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="dcc36-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




