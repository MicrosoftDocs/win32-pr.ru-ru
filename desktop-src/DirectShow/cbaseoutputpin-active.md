---
description: Активный метод уведомляет ПИН-код о том, что фильтр активен.
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
ms.openlocfilehash: 249cddac4027fa434996b1118cc692937b686a83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657523"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="32d3f-103">Кбасеаутпутпин. активный метод</span><span class="sxs-lookup"><span data-stu-id="32d3f-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="32d3f-104">`Active`Метод уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="32d3f-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d3f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32d3f-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="32d3f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32d3f-106">Parameters</span></span>

<span data-ttu-id="32d3f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="32d3f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32d3f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32d3f-108">Return value</span></span>

<span data-ttu-id="32d3f-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32d3f-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="32d3f-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="32d3f-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="32d3f-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="32d3f-111">Return code</span></span>                                                                                          | <span data-ttu-id="32d3f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="32d3f-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="32d3f-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="32d3f-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="32d3f-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="32d3f-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="32d3f-115"><dt>**VFW \_ E \_ без \_ распределителя**</dt></span><span class="sxs-lookup"><span data-stu-id="32d3f-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="32d3f-116">Распределитель недоступен.</span><span class="sxs-lookup"><span data-stu-id="32d3f-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32d3f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32d3f-117">Remarks</span></span>

<span data-ttu-id="32d3f-118">Этот метод переопределяет метод [**кбасепин:: Active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="32d3f-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="32d3f-119">Он вызывает метод [**имемаллокатор:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) для распределителя, чтобы выделить память для буферов.</span><span class="sxs-lookup"><span data-stu-id="32d3f-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="32d3f-120">При переопределении этого метода вызовите метод базового класса из переопределяющего метода.</span><span class="sxs-lookup"><span data-stu-id="32d3f-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32d3f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="32d3f-121">Requirements</span></span>



| <span data-ttu-id="32d3f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="32d3f-122">Requirement</span></span> | <span data-ttu-id="32d3f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="32d3f-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d3f-124">Header</span><span class="sxs-lookup"><span data-stu-id="32d3f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="32d3f-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32d3f-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="32d3f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32d3f-126">Library</span></span><br/> | <dl> <span data-ttu-id="32d3f-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="32d3f-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32d3f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32d3f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d3f-129">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="32d3f-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




