---
title: Использование элемента «формулы»
description: Использование элемента «формулы»
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Веб-семинар, элемент формул
- Разработка веб-страниц, элементы формул
- Язык VML (VML), элемент формул
- VML (язык VML), элемент формул
- Векторная графика, элемент формул
- элемент формул
- Элементы VML, формулы
- Фигуры VML, элемент формул
- Язык VML (VML), определение контуров для фигур
- VML (язык VML), определение контуров для фигур
- Векторная графика, определение контуров для фигур
- Фигуры VML, определение путей
- определение контуров для фигур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070063"
---
# <a name="using-the-formulas-element"></a><span data-ttu-id="ad29d-116">Использование элемента «формулы»</span><span class="sxs-lookup"><span data-stu-id="ad29d-116">Using the Formulas Element</span></span>

<span data-ttu-id="ad29d-117">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ad29d-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ad29d-118">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ad29d-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ad29d-119">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ad29d-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ad29d-120">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad29d-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ad29d-121">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ad29d-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ad29d-122">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ad29d-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ad29d-123">В этом разделе показано, как использовать `<formulas>` вложенный элемент для определения изменяемого пути к фигуре.</span><span class="sxs-lookup"><span data-stu-id="ad29d-123">In this topic, we will illustrate how to use the `<formulas>` sub-element to define an adjustable path for a shape.</span></span>

<span data-ttu-id="ad29d-124"><formulas>Вложенный элемент можно поместить внутри или, `<shape>` `<shapetype>` чтобы определить формулы, которые могут варьировать путь к фигуре.</span><span class="sxs-lookup"><span data-stu-id="ad29d-124">You can place the <formulas> sub-element inside `<shape>` or `<shapetype>` to define formulas that can vary the path of a shape.</span></span> <span data-ttu-id="ad29d-125">Внутри `<formulas>` вложенного элемента один вложенный элемент **f** определяет одну формулу таким образом, чтобы одно значение вычисляется на основе этой формулы.</span><span class="sxs-lookup"><span data-stu-id="ad29d-125">Inside the `<formulas>` sub-element, one **f** sub-element defines one formula so that one value is evaluated based upon that formula.</span></span> <span data-ttu-id="ad29d-126">Например, формула `<v:f eqn="prod 10 4 5"/>` определяет значение, эквивалентное "10 x 4/5".</span><span class="sxs-lookup"><span data-stu-id="ad29d-126">For example, the formula, `<v:f eqn="prod 10 4 5"/>` defines a value that is equivalent to "10 x 4 / 5".</span></span>

<span data-ttu-id="ad29d-127">Можно разместить множество вложенных элементов **f** внутри одного `<formulas>` вложенного элемента.</span><span class="sxs-lookup"><span data-stu-id="ad29d-127">You can place many **f** sub-elements inside one`<formulas>` sub-element.</span></span> <span data-ttu-id="ad29d-128">Формулы могут ссылаться на значения, определенные ранее в других формулах внутри того же `<formulas>` вложенного элемента.</span><span class="sxs-lookup"><span data-stu-id="ad29d-128">Formulas can reference the values that are defined earlier in other formulas within the same `<formulas>` sub-element.</span></span> <span data-ttu-id="ad29d-129">Значение, определенное в первой формуле, может называться @0 , а значение, определенное во второй формуле, можно называть @1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="ad29d-129">The value that is defined in the first formula can be referred to as @0, the value that is defined in the second formula can be referred to as @1, and so on.</span></span>

<span data-ttu-id="ad29d-130">Кроме того, можно указать атрибут свойства « **года** » `<shape>` элемента, например «прилагательные», «100, 200, 150».</span><span class="sxs-lookup"><span data-stu-id="ad29d-130">In addition, you can specify the **adj** property attribute of the `<shape>` element, such as adj="100, 200, 150".</span></span> <span data-ttu-id="ad29d-131">Внутри `<formulas>` элемента можно ссылаться на эти значения из списка назначений. </span><span class="sxs-lookup"><span data-stu-id="ad29d-131">Inside the `<formulas>` element, you can then reference those values in the **adj** list.</span></span> <span data-ttu-id="ad29d-132">Первое значение (100) **в списке** назначений может называться \# 0, а второе значение (200) — как \# 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="ad29d-132">The first value (100) in the **adj** list can be referred to as \#0, the second value (200) can be referred to as \#1, and so on.</span></span>

<span data-ttu-id="ad29d-133">Например, чтобы нарисовать улыбающаяся рожица, можно ввести следующее представление VML:</span><span class="sxs-lookup"><span data-stu-id="ad29d-133">For example, to draw a smiling face, you can type the following VML representation:</span></span>

![shape1.gif (735 байт)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   <span data-ttu-id="ad29d-135">`adj="17520"` Определяет значение (= 17520).</span><span class="sxs-lookup"><span data-stu-id="ad29d-135">`adj="17520"` defines a value (= 17520).</span></span> <span data-ttu-id="ad29d-136">На это значение можно ссылаться как на \# 0.</span><span class="sxs-lookup"><span data-stu-id="ad29d-136">This value can be referenced as \#0.</span></span>
-   <span data-ttu-id="ad29d-137">Первая формула, `<v:f eqn="sum 33030 0 #0"/>` , определяет значение (= 33030 + 0- \# 0).</span><span class="sxs-lookup"><span data-stu-id="ad29d-137">The first formula, `<v:f eqn="sum 33030 0 #0"/>`, defines the value (= 33030 + 0 - \#0).</span></span> <span data-ttu-id="ad29d-138">На это значение можно ссылаться как @0 .</span><span class="sxs-lookup"><span data-stu-id="ad29d-138">This value can be referenced as @0.</span></span>
-   <span data-ttu-id="ad29d-139">Вторая формула, `<v:f eqn="prod #0 4 3"/>` , определяет значение (= \# 0 \* 4/3).</span><span class="sxs-lookup"><span data-stu-id="ad29d-139">The second formula, `<v:f eqn="prod #0 4 3"/>`, defines the value (= \#0 \* 4 / 3).</span></span> <span data-ttu-id="ad29d-140">На это значение можно ссылаться как @1 .</span><span class="sxs-lookup"><span data-stu-id="ad29d-140">This value can be referenced as @1.</span></span>
-   <span data-ttu-id="ad29d-141">Третья формула, `<v:f eqn="prod @0 1 3"/>` , определяет значение (= @0 \* 1/3).</span><span class="sxs-lookup"><span data-stu-id="ad29d-141">The third formula, `<v:f eqn="prod @0 1 3"/>`, defines the value (= @0 \* 1 / 3).</span></span> <span data-ttu-id="ad29d-142">На это значение можно ссылаться как @2 .</span><span class="sxs-lookup"><span data-stu-id="ad29d-142">This value can be referenced as @2.</span></span>
-   <span data-ttu-id="ad29d-143">Четвертая формула, `<v:f eqn="sum @1 0 @2"/>` , определяет значение (= @1 + 0 -@2 ).</span><span class="sxs-lookup"><span data-stu-id="ad29d-143">The fourth formula, `<v:f eqn="sum @1 0 @2"/>`, defines the value (=@1 + 0 -@2).</span></span> <span data-ttu-id="ad29d-144">На это значение можно ссылаться как @3 .</span><span class="sxs-lookup"><span data-stu-id="ad29d-144">This value can be referenced as @3.</span></span>
-   <span data-ttu-id="ad29d-145">Внутри `<path>` элемента значения, определенные в первой ( @0 ) и четвертой ( @3 ) формулах, используются для определения контура фигуры.</span><span class="sxs-lookup"><span data-stu-id="ad29d-145">Inside the `<path>` element, the values defined in the first (@0) and the fourth (@3) formulas are used to determine the outline of the shape.</span></span>

<span data-ttu-id="ad29d-146">Если **изменить список** `adj="20000"` назначений, например, то значения формул, ссылающихся на список « **года** », будут также изменены, что повлияет на улыбку следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad29d-146">If you change the **adj** list, such as `adj="20000"`, the values of the formulas that reference the **adj** list will be changed as well, affecting the smiling face as follows:</span></span>

![shape2.gif (765 байт)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





<span data-ttu-id="ad29d-148">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span><span class="sxs-lookup"><span data-stu-id="ad29d-148">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span></span>

 

 