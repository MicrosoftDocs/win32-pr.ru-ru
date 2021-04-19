---
title: Амбиентаттрибутес. Слидето
description: Метод Слидето перемещает элемент управления в новое расположение. Элемент управления перемещается нелинейным способом за указанный период времени.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Слидето
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699060"
---
# <a name="ambientattributesslideto"></a><span data-ttu-id="6d4b2-105">Амбиентаттрибутес. Слидето</span><span class="sxs-lookup"><span data-stu-id="6d4b2-105">AmbientAttributes.slideTo</span></span>

<span data-ttu-id="6d4b2-106">Метод **слидето** перемещает элемент управления в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="6d4b2-106">The **slideTo** method moves the control to a new location.</span></span> <span data-ttu-id="6d4b2-107">Элемент управления перемещается нелинейным способом за указанный период времени.</span><span class="sxs-lookup"><span data-stu-id="6d4b2-107">The control moves in a non-linear fashion over the specified time period.</span></span>

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a><span data-ttu-id="6d4b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d4b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d4b2-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*невкс*</span><span class="sxs-lookup"><span data-stu-id="6d4b2-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="6d4b2-110">**Число** (**длинное**), определяющее новое значение **левого** атрибута элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6d4b2-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="6d4b2-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*неви*</span><span class="sxs-lookup"><span data-stu-id="6d4b2-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="6d4b2-112">**Число** (**длинное**), указывающее новое значение для **верхнего** атрибута элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6d4b2-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="6d4b2-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*моветиме*</span><span class="sxs-lookup"><span data-stu-id="6d4b2-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="6d4b2-114">**Число** (**длинное**), указывающее время в миллисекундах, которое требуется для перехода элемента управления в новое место.</span><span class="sxs-lookup"><span data-stu-id="6d4b2-114">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d4b2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d4b2-115">Return Value</span></span>

<span data-ttu-id="6d4b2-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6d4b2-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d4b2-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d4b2-117">Remarks</span></span>

<span data-ttu-id="6d4b2-118">Этот метод отличается от **MoveTo**, который создает линейное движение при перемещении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6d4b2-118">This method is different from **moveTo**, which creates a linear motion when moving the control.</span></span> <span data-ttu-id="6d4b2-119">Нелинейное движение, созданное этим методом, является скользящим движением, которое ускоряется от нуля в начале движения и замедляется до нуля в конце, что достигается плавной остановкой.</span><span class="sxs-lookup"><span data-stu-id="6d4b2-119">The non-linear motion created by this method is a sliding motion that accelerates from a speed of zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4b2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6d4b2-120">Requirements</span></span>



| <span data-ttu-id="6d4b2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6d4b2-121">Requirement</span></span> | <span data-ttu-id="6d4b2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6d4b2-122">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="6d4b2-123">Версия</span><span class="sxs-lookup"><span data-stu-id="6d4b2-123">Version</span></span><br/> | <span data-ttu-id="6d4b2-124">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="6d4b2-124">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d4b2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d4b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4b2-126">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="6d4b2-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d4b2-127">**Амбиентаттрибутес. Left**</span><span class="sxs-lookup"><span data-stu-id="6d4b2-127">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="6d4b2-128">**Амбиентаттрибутес. moveTo**</span><span class="sxs-lookup"><span data-stu-id="6d4b2-128">**AmbientAttributes.moveTo**</span></span>](ambientattributes-moveto.md)
</dt> <dt>

[<span data-ttu-id="6d4b2-129">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="6d4b2-129">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





