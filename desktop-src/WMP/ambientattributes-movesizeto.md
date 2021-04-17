---
title: Амбиентаттрибутес. Мовесизето
description: Метод Мовесизето перемещает элемент управления и задает новый размер элемента управления в новом расположении. Элемент управления перемещается и изменяет размер в анимированном виде за указанный период времени.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Мовесизето
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694770"
---
# <a name="ambientattributesmovesizeto"></a><span data-ttu-id="8231b-105">Амбиентаттрибутес. Мовесизето</span><span class="sxs-lookup"><span data-stu-id="8231b-105">AmbientAttributes.moveSizeTo</span></span>

<span data-ttu-id="8231b-106">Метод **мовесизето** перемещает элемент управления и задает новый размер элемента управления в новом расположении.</span><span class="sxs-lookup"><span data-stu-id="8231b-106">The **moveSizeTo** method moves the control and specifies a new size for the control in the new location.</span></span> <span data-ttu-id="8231b-107">Элемент управления перемещается и изменяет размер в анимированном виде за указанный период времени.</span><span class="sxs-lookup"><span data-stu-id="8231b-107">The control moves and resizes in an animated fashion over the specified time period.</span></span>

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a><span data-ttu-id="8231b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8231b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8231b-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*невкс*</span><span class="sxs-lookup"><span data-stu-id="8231b-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="8231b-110">**Число** (**длинное**), определяющее новое значение **левого** атрибута элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8231b-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="8231b-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*неви*</span><span class="sxs-lookup"><span data-stu-id="8231b-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="8231b-112">**Число** (**длинное**), указывающее новое значение для **верхнего** атрибута элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8231b-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="8231b-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*неввидс*</span><span class="sxs-lookup"><span data-stu-id="8231b-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span></span>
</dt> <dd>

<span data-ttu-id="8231b-114">**Число** (**длинное**), определяющее новое значение атрибута **Width** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8231b-114">**Number** (**long**) specifying the new value for the **width** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="8231b-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*невхеигхт*</span><span class="sxs-lookup"><span data-stu-id="8231b-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span></span>
</dt> <dd>

<span data-ttu-id="8231b-116">**Число** (**длинное**), указывающее новое значение для атрибута **Height** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8231b-116">**Number** (**long**) specifying the new value for the **height** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="8231b-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*моветиме*</span><span class="sxs-lookup"><span data-stu-id="8231b-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="8231b-118">**Число** (**длинное**), указывающее время в миллисекундах, которое требуется для перехода элемента управления в новое место.</span><span class="sxs-lookup"><span data-stu-id="8231b-118">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> <dt>

<span data-ttu-id="8231b-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*фслиде*</span><span class="sxs-lookup"><span data-stu-id="8231b-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span></span>
</dt> <dd>

<span data-ttu-id="8231b-120">**Логическое значение** , указывающее тип движения, создаваемого при перемещении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="8231b-120">**Boolean** specifying the type of motion created when moving the control.</span></span>



| <span data-ttu-id="8231b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8231b-121">Value</span></span> | <span data-ttu-id="8231b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="8231b-122">Description</span></span>                                                             |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="8231b-123">true</span><span class="sxs-lookup"><span data-stu-id="8231b-123">true</span></span>  | <span data-ttu-id="8231b-124">Движение является нелинейным (скользящее движение, которое ускоряется и замедляется).</span><span class="sxs-lookup"><span data-stu-id="8231b-124">Motion is non-linear (sliding motion that accelerates and decelerates).</span></span> |
| <span data-ttu-id="8231b-125">false</span><span class="sxs-lookup"><span data-stu-id="8231b-125">false</span></span> | <span data-ttu-id="8231b-126">Движение является линейным.</span><span class="sxs-lookup"><span data-stu-id="8231b-126">Motion is linear.</span></span>                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8231b-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8231b-127">Return Value</span></span>

<span data-ttu-id="8231b-128">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8231b-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8231b-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8231b-129">Remarks</span></span>

<span data-ttu-id="8231b-130">Движение элемента управления может быть линейным или нелинейным.</span><span class="sxs-lookup"><span data-stu-id="8231b-130">The motion of the control can be linear or non-linear.</span></span> <span data-ttu-id="8231b-131">Линейное движение означает, что элемент управления перемещается по постоянной скорости в новое место, что приводит к внезапному запуску и остановке.</span><span class="sxs-lookup"><span data-stu-id="8231b-131">Linear motion means the control moves at a constant speed to its new location, starting and stopping abruptly.</span></span> <span data-ttu-id="8231b-132">Если указано нелинейное движение, создается скользящее движение, которое ускоряется от нуля в начале движения и замедляется до нуля в конце, что достигается гладкой остановкой.</span><span class="sxs-lookup"><span data-stu-id="8231b-132">When non-linear motion is specified, a sliding motion is created that accelerates from zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="8231b-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8231b-133">Requirements</span></span>



| <span data-ttu-id="8231b-134">Требование</span><span class="sxs-lookup"><span data-stu-id="8231b-134">Requirement</span></span> | <span data-ttu-id="8231b-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8231b-135">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="8231b-136">Версия</span><span class="sxs-lookup"><span data-stu-id="8231b-136">Version</span></span><br/> | <span data-ttu-id="8231b-137">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="8231b-137">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8231b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8231b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8231b-139">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="8231b-139">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="8231b-140">**Амбиентаттрибутес. Height**</span><span class="sxs-lookup"><span data-stu-id="8231b-140">**AmbientAttributes.height**</span></span>](ambientattributes-height.md)
</dt> <dt>

[<span data-ttu-id="8231b-141">**Амбиентаттрибутес. Left**</span><span class="sxs-lookup"><span data-stu-id="8231b-141">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="8231b-142">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="8231b-142">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> <dt>

[<span data-ttu-id="8231b-143">**Амбиентаттрибутес. Width**</span><span class="sxs-lookup"><span data-stu-id="8231b-143">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> </dl>

 

 





