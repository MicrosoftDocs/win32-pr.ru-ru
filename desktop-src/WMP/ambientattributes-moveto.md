---
title: Амбиентаттрибутес. moveTo
description: Метод moveTo перемещает элемент управления в новое расположение с линейной скоростью.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. moveTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694917"
---
# <a name="ambientattributesmoveto"></a><span data-ttu-id="6402f-104">Амбиентаттрибутес. moveTo</span><span class="sxs-lookup"><span data-stu-id="6402f-104">AmbientAttributes.moveTo</span></span>

<span data-ttu-id="6402f-105">Метод **MoveTo** перемещает элемент управления в новое расположение с линейной скоростью.</span><span class="sxs-lookup"><span data-stu-id="6402f-105">The **moveTo** method moves the control to a new location at a linear speed.</span></span>

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a><span data-ttu-id="6402f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6402f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6402f-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*невлефт*</span><span class="sxs-lookup"><span data-stu-id="6402f-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span></span>
</dt> <dd>

<span data-ttu-id="6402f-108">**Число** (**длинное**), определяющее новое значение **левого** атрибута элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6402f-108">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="6402f-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*невтоп*</span><span class="sxs-lookup"><span data-stu-id="6402f-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span></span>
</dt> <dd>

<span data-ttu-id="6402f-110">**Число** (**длинное**), указывающее новое значение для **верхнего** атрибута элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6402f-110">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="6402f-111"><span id="time"></span><span id="TIME"></span>*Таймаут*</span><span class="sxs-lookup"><span data-stu-id="6402f-111"><span id="time"></span><span id="TIME"></span>*time*</span></span>
</dt> <dd>

<span data-ttu-id="6402f-112">**Число** (**длинное**), указывающее время в миллисекундах, которое требуется для перехода элемента управления в новое место.</span><span class="sxs-lookup"><span data-stu-id="6402f-112">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6402f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6402f-113">Return Value</span></span>

<span data-ttu-id="6402f-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6402f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6402f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6402f-115">Remarks</span></span>

<span data-ttu-id="6402f-116">Этот метод полезен для анимированных элементов вложенного **представления** (например, если пользователь щелкает табло и элементы управления просматриваются вниз).</span><span class="sxs-lookup"><span data-stu-id="6402f-116">This method is useful for animated **SUBVIEW** elements (for example, if the user clicks a tray and the controls slide down).</span></span>

<span data-ttu-id="6402f-117">Этот метод создает линейное движение при перемещении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6402f-117">This method creates a linear motion when moving the control.</span></span> <span data-ttu-id="6402f-118">Это отличается от **слидето**, который создает нелинейное движение.</span><span class="sxs-lookup"><span data-stu-id="6402f-118">This differs from **slideTo**, which creates a non-linear motion.</span></span>

## <a name="requirements"></a><span data-ttu-id="6402f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6402f-119">Requirements</span></span>



| <span data-ttu-id="6402f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6402f-120">Requirement</span></span> | <span data-ttu-id="6402f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6402f-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6402f-122">Версия</span><span class="sxs-lookup"><span data-stu-id="6402f-122">Version</span></span><br/> | <span data-ttu-id="6402f-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="6402f-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6402f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6402f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6402f-125">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="6402f-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="6402f-126">**Амбиентаттрибутес. Left**</span><span class="sxs-lookup"><span data-stu-id="6402f-126">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="6402f-127">**Амбиентаттрибутес. Слидето**</span><span class="sxs-lookup"><span data-stu-id="6402f-127">**AmbientAttributes.slideTo**</span></span>](ambientattributes-slideto.md)
</dt> <dt>

[<span data-ttu-id="6402f-128">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="6402f-128">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





