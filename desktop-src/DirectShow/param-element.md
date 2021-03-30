---
description: Элемент Param указывает значение свойства для перехода, воздействия или другого подобъекта.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Элемент param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894910"
---
# <a name="param-element"></a><span data-ttu-id="ac6b4-103">Param, элемент</span><span class="sxs-lookup"><span data-stu-id="ac6b4-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="ac6b4-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-104">\[Deprecated.</span></span> <span data-ttu-id="ac6b4-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ac6b4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ac6b4-106">`param`Элемент указывает значение свойства для перехода, воздействия или другого подобъекта.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="ac6b4-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ac6b4-107">Attributes</span></span>

<span data-ttu-id="ac6b4-108">[**имя**](name-attribute.md), [ **значение**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="ac6b4-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="ac6b4-109">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="ac6b4-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6b4-110">Parent</span><span class="sxs-lookup"><span data-stu-id="ac6b4-110">Parent</span></span>   | <span data-ttu-id="ac6b4-111">[**клип**](clip-element.md), [**результат**](effect-element.md), [**Переход**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="ac6b4-111">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="ac6b4-112">Дети</span><span class="sxs-lookup"><span data-stu-id="ac6b4-112">Children</span></span> | <span data-ttu-id="ac6b4-113">[**в**](at-element.md), [ **Линейная**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="ac6b4-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="ac6b4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac6b4-114">Remarks</span></span>

<span data-ttu-id="ac6b4-115">Атрибут **value** задает значение свойства в начале перехода или воздействия.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-115">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="ac6b4-116">Для указания изменяющихся значений используйте элемент **at** или **линейный** .</span><span class="sxs-lookup"><span data-stu-id="ac6b4-116">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="ac6b4-117">Если элемент **param** **не содержит ни одного** или **линейного** элемента, значение остается постоянным в течение действия или перехода.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-117">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="ac6b4-118">Элемент **param** внутри элемента **Clip** не **может содержать** **линейные** элементы или.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-118">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="ac6b4-119">Многие переходы поддерживают стандартное свойство **Progress** , которое находится в диапазоне от 0 до 1,0, указывая, какой процент перехода отражается в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-119">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="ac6b4-120">**Выполняется** = 0,0, переход находится в начале последовательности (всего лишь первое изображение видео).</span><span class="sxs-lookup"><span data-stu-id="ac6b4-120">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="ac6b4-121">Время **выполнения** = 0,5, переход на половину завершен.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-121">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="ac6b4-122">(Например, при очистке, **выполняется** = 0,5 граница перехода находится в центре изображения). **Выполняется** = 1,0, переход выполнен (целиком — второе изображение).</span><span class="sxs-lookup"><span data-stu-id="ac6b4-122">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="ac6b4-123">По умолчанию переходы переходят в **состояние Progress** = 0,0 в начале перехода на **Progress** = 1,0 в конце.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-123">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="ac6b4-124">Другие свойства обычно относятся к одному конкретному переходу или результату.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-124">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="ac6b4-125">Например, переход от очистки поддерживает свойство **градиентсизе** , которое управляет шириной области переходов.</span><span class="sxs-lookup"><span data-stu-id="ac6b4-125">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="ac6b4-126">Чтобы выполнить переход назад, задайте для свойства **Progress** значение 1,0 в начале перехода и используйте **линейный** элемент для изменения значения на 0,0, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="ac6b4-126">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="ac6b4-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="ac6b4-127">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="ac6b4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac6b4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac6b4-129">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="ac6b4-129">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



