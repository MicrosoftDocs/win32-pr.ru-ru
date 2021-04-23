---
description: Неактивный метод уведомляет ПИН-код о том, что фильтр больше не активен.
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: Метод Кбасеаутпутпин. Inactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afec15e295e5c14cfb3d9efa6e733d1dc288b319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669205"
---
# <a name="cbaseoutputpininactive-method"></a><span data-ttu-id="de697-103">Кбасеаутпутпин. Inactive, метод</span><span class="sxs-lookup"><span data-stu-id="de697-103">CBaseOutputPin.Inactive method</span></span>

<span data-ttu-id="de697-104">`Inactive`Метод уведомляет ПИН-код о том, что фильтр больше не активен.</span><span class="sxs-lookup"><span data-stu-id="de697-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="de697-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de697-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="de697-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de697-106">Parameters</span></span>

<span data-ttu-id="de697-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="de697-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de697-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de697-108">Return value</span></span>

<span data-ttu-id="de697-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de697-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="de697-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="de697-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="de697-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="de697-111">Return code</span></span>                                                                                          | <span data-ttu-id="de697-112">Описание</span><span class="sxs-lookup"><span data-stu-id="de697-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="de697-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="de697-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="de697-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="de697-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="de697-115"><dt>**VFW \_ E \_ без \_ распределителя**</dt></span><span class="sxs-lookup"><span data-stu-id="de697-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="de697-116">Распределитель памяти недоступен.</span><span class="sxs-lookup"><span data-stu-id="de697-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de697-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de697-117">Remarks</span></span>

<span data-ttu-id="de697-118">Этот метод переопределяет метод [**кбасепин:: Inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="de697-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="de697-119">Он вызывает метод [**имемаллокатор::D екоммит**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) для дефиксации распределителя памяти.</span><span class="sxs-lookup"><span data-stu-id="de697-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="de697-120">При переопределении этого метода вызовите метод базового класса из переопределяющего метода.</span><span class="sxs-lookup"><span data-stu-id="de697-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="de697-121">Требования</span><span class="sxs-lookup"><span data-stu-id="de697-121">Requirements</span></span>



| <span data-ttu-id="de697-122">Требование</span><span class="sxs-lookup"><span data-stu-id="de697-122">Requirement</span></span> | <span data-ttu-id="de697-123">Значение</span><span class="sxs-lookup"><span data-stu-id="de697-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de697-124">Header</span><span class="sxs-lookup"><span data-stu-id="de697-124">Header</span></span><br/>  | <dl> <span data-ttu-id="de697-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de697-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="de697-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="de697-126">Library</span></span><br/> | <dl> <span data-ttu-id="de697-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="de697-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de697-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de697-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de697-129">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="de697-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




