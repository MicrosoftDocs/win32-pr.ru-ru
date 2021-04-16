---
description: Неактивный метод уведомляет ПИН-код о том, что фильтр больше не активен.
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Метод Кбасеинпутпин. Inactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52bf7efa352e8a73d562c61c3833a051ee860d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657064"
---
# <a name="cbaseinputpininactive-method"></a><span data-ttu-id="f683c-103">Кбасеинпутпин. Inactive, метод</span><span class="sxs-lookup"><span data-stu-id="f683c-103">CBaseInputPin.Inactive method</span></span>

<span data-ttu-id="f683c-104">`Inactive`Метод уведомляет ПИН-код о том, что фильтр больше не активен.</span><span class="sxs-lookup"><span data-stu-id="f683c-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="f683c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f683c-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="f683c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f683c-106">Parameters</span></span>

<span data-ttu-id="f683c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f683c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f683c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f683c-108">Return value</span></span>

<span data-ttu-id="f683c-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f683c-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f683c-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f683c-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="f683c-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f683c-111">Return code</span></span>                                                                                          | <span data-ttu-id="f683c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f683c-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f683c-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f683c-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="f683c-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="f683c-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="f683c-115"><dt>**VFW \_ E \_ без \_ распределителя**</dt></span><span class="sxs-lookup"><span data-stu-id="f683c-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="f683c-116">Распределитель памяти недоступен.</span><span class="sxs-lookup"><span data-stu-id="f683c-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f683c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f683c-117">Remarks</span></span>

<span data-ttu-id="f683c-118">Этот метод переопределяет метод [**кбасепин:: Inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="f683c-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="f683c-119">Он вызывает метод [**имемаллокатор::D екоммит**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) для дефиксации распределителя памяти.</span><span class="sxs-lookup"><span data-stu-id="f683c-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="f683c-120">При переопределении этого метода вызовите метод базового класса из переопределяющего метода.</span><span class="sxs-lookup"><span data-stu-id="f683c-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f683c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f683c-121">Requirements</span></span>



| <span data-ttu-id="f683c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f683c-122">Requirement</span></span> | <span data-ttu-id="f683c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f683c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f683c-124">Header</span><span class="sxs-lookup"><span data-stu-id="f683c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f683c-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f683c-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f683c-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f683c-126">Library</span></span><br/> | <dl> <span data-ttu-id="f683c-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f683c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f683c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f683c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f683c-129">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="f683c-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




