---
description: Метод Жеталлокаторрекуирементс извлекает свойства распределителя, запрашиваемые входным закреплением.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Кбасеинпутпин. Жеталлокаторрекуирементс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657065"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a><span data-ttu-id="c4366-103">Кбасеинпутпин. Жеталлокаторрекуирементс, метод</span><span class="sxs-lookup"><span data-stu-id="c4366-103">CBaseInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="c4366-104">`GetAllocatorRequirements`Метод получает свойства распределителя, запрашиваемые входным закреплением.</span><span class="sxs-lookup"><span data-stu-id="c4366-104">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4366-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4366-105">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="c4366-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4366-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4366-107">*ппропс*</span><span class="sxs-lookup"><span data-stu-id="c4366-107">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="c4366-108">Указатель на структуру [**\_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая заполняется требованиями.</span><span class="sxs-lookup"><span data-stu-id="c4366-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4366-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4366-109">Return value</span></span>

<span data-ttu-id="c4366-110">Возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="c4366-110">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4366-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4366-111">Remarks</span></span>

<span data-ttu-id="c4366-112">Когда закрепление вывода инициализирует распределитель памяти, он может вызвать этот метод, чтобы определить, имеет ли входной ПИН-код требования к буферу.</span><span class="sxs-lookup"><span data-stu-id="c4366-112">When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements.</span></span> <span data-ttu-id="c4366-113">Дополнительные сведения см. в разделе [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="c4366-113">For more information, see [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="c4366-114">Реализация этого метода является необязательной.</span><span class="sxs-lookup"><span data-stu-id="c4366-114">Implementing this method is optional.</span></span> <span data-ttu-id="c4366-115">Если фильтр имеет особые требования выравнивания или префикса, Переопределите этот метод.</span><span class="sxs-lookup"><span data-stu-id="c4366-115">If the filter has specific alignment or prefix requirements, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4366-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c4366-116">Requirements</span></span>



| <span data-ttu-id="c4366-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c4366-117">Requirement</span></span> | <span data-ttu-id="c4366-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c4366-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4366-119">Header</span><span class="sxs-lookup"><span data-stu-id="c4366-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c4366-120"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4366-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c4366-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4366-121">Library</span></span><br/> | <dl> <span data-ttu-id="c4366-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c4366-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4366-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4366-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4366-124">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="c4366-124">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




