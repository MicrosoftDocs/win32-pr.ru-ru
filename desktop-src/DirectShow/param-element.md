---
description: Элемент Param указывает значение свойства для перехода, воздействия или другого подобъекта.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Элемент param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909042"
---
# <a name="param-element"></a><span data-ttu-id="aa08e-103">Param, элемент</span><span class="sxs-lookup"><span data-stu-id="aa08e-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="aa08e-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="aa08e-104">\[Deprecated.</span></span> <span data-ttu-id="aa08e-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aa08e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aa08e-106">`param`Элемент указывает значение свойства для перехода, воздействия или другого подобъекта.</span><span class="sxs-lookup"><span data-stu-id="aa08e-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="aa08e-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="aa08e-107">Attributes</span></span>

<span data-ttu-id="aa08e-108">[**имя**](name-attribute.md), [ **значение**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="aa08e-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="aa08e-109">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="aa08e-109">Parent/Child Information</span></span>



| <span data-ttu-id="aa08e-110">Метка</span><span class="sxs-lookup"><span data-stu-id="aa08e-110">Label</span></span> | <span data-ttu-id="aa08e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="aa08e-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa08e-112">Parent</span><span class="sxs-lookup"><span data-stu-id="aa08e-112">Parent</span></span>   | <span data-ttu-id="aa08e-113">[**клип**](clip-element.md), [**результат**](effect-element.md), [**Переход**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="aa08e-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="aa08e-114">Дети</span><span class="sxs-lookup"><span data-stu-id="aa08e-114">Children</span></span> | <span data-ttu-id="aa08e-115">[**в**](at-element.md), [ **Линейная**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="aa08e-115">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="aa08e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa08e-116">Remarks</span></span>

<span data-ttu-id="aa08e-117">Атрибут **value** задает значение свойства в начале перехода или воздействия.</span><span class="sxs-lookup"><span data-stu-id="aa08e-117">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="aa08e-118">Для указания изменяющихся значений используйте элемент **at** или **линейный** .</span><span class="sxs-lookup"><span data-stu-id="aa08e-118">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="aa08e-119">Если элемент **param** **не содержит ни одного** или **линейного** элемента, значение остается постоянным в течение действия или перехода.</span><span class="sxs-lookup"><span data-stu-id="aa08e-119">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="aa08e-120">Элемент **param** внутри элемента **Clip** не **может содержать** **линейные** элементы или.</span><span class="sxs-lookup"><span data-stu-id="aa08e-120">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="aa08e-121">Многие переходы поддерживают стандартное свойство **Progress** , которое находится в диапазоне от 0 до 1,0, указывая, какой процент перехода отражается в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="aa08e-121">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="aa08e-122">**Выполняется** = 0,0, переход находится в начале последовательности (всего лишь первое изображение видео).</span><span class="sxs-lookup"><span data-stu-id="aa08e-122">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="aa08e-123">Время **выполнения** = 0,5, переход на половину завершен.</span><span class="sxs-lookup"><span data-stu-id="aa08e-123">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="aa08e-124">(Например, при очистке, **выполняется** = 0,5 граница перехода находится в центре изображения). **Выполняется** = 1,0, переход выполнен (целиком — второе изображение).</span><span class="sxs-lookup"><span data-stu-id="aa08e-124">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="aa08e-125">По умолчанию переходы переходят в **состояние Progress** = 0,0 в начале перехода на **Progress** = 1,0 в конце.</span><span class="sxs-lookup"><span data-stu-id="aa08e-125">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="aa08e-126">Другие свойства обычно относятся к одному конкретному переходу или результату.</span><span class="sxs-lookup"><span data-stu-id="aa08e-126">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="aa08e-127">Например, переход от очистки поддерживает свойство **градиентсизе** , которое управляет шириной области переходов.</span><span class="sxs-lookup"><span data-stu-id="aa08e-127">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="aa08e-128">Чтобы выполнить переход назад, задайте для свойства **Progress** значение 1,0 в начале перехода и используйте **линейный** элемент для изменения значения на 0,0, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="aa08e-128">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="aa08e-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="aa08e-129">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="aa08e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="aa08e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa08e-131">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="aa08e-131">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



