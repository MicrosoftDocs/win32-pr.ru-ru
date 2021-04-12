---
title: Атрибут DashStyle VML
description: Атрибут DashStyle VML
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337716"
---
# <a name="vml-dashstyle-attribute"></a><span data-ttu-id="5840a-103">Атрибут DashStyle VML</span><span class="sxs-lookup"><span data-stu-id="5840a-103">VML DashStyle Attribute</span></span>

<span data-ttu-id="5840a-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5840a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5840a-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="5840a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5840a-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="5840a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5840a-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5840a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5840a-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5840a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5840a-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5840a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5840a-110">Задает шаблон точки и штриха для штриха.</span><span class="sxs-lookup"><span data-stu-id="5840a-110">Specifies the dot and dash pattern for a stroke.</span></span> <span data-ttu-id="5840a-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="5840a-111">Read/write.</span></span> <span data-ttu-id="5840a-112">**Вглинедашстиле**.</span><span class="sxs-lookup"><span data-stu-id="5840a-112">**VgLineDashStyle**.</span></span>

<span data-ttu-id="5840a-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="5840a-113">**Applies To**</span></span>

[<span data-ttu-id="5840a-114">Водок</span><span class="sxs-lookup"><span data-stu-id="5840a-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="5840a-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="5840a-115">**Tag Syntax**</span></span>

<span data-ttu-id="5840a-116"><v: *element* DashStyle = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="5840a-116"><v: *element* dashstyle=" *expression* "></span></span>

<span data-ttu-id="5840a-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="5840a-117">**Script Syntax**</span></span>

<span data-ttu-id="5840a-118">*element* . DashStyle = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="5840a-118">*element* .dashstyle="*expression*"</span></span>

<span data-ttu-id="5840a-119">*выражение* = *element*. DashStyle</span><span class="sxs-lookup"><span data-stu-id="5840a-119">*expression*=*element*.dashstyle</span></span>

<span data-ttu-id="5840a-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="5840a-120">**Remarks**</span></span>

<span data-ttu-id="5840a-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="5840a-121">Values include:</span></span>

-   <span data-ttu-id="5840a-122">Solid (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5840a-122">Solid (default)</span></span>
-   <span data-ttu-id="5840a-123">шортдаш</span><span class="sxs-lookup"><span data-stu-id="5840a-123">ShortDash</span></span>
-   <span data-ttu-id="5840a-124">шортдот</span><span class="sxs-lookup"><span data-stu-id="5840a-124">ShortDot</span></span>
-   <span data-ttu-id="5840a-125">шортдашдот</span><span class="sxs-lookup"><span data-stu-id="5840a-125">ShortDashDot</span></span>
-   <span data-ttu-id="5840a-126">шортдашдотдот</span><span class="sxs-lookup"><span data-stu-id="5840a-126">ShortDashDotDot</span></span>
-   <span data-ttu-id="5840a-127">Точки</span><span class="sxs-lookup"><span data-stu-id="5840a-127">Dot</span></span>
-   <span data-ttu-id="5840a-128">Штрих</span><span class="sxs-lookup"><span data-stu-id="5840a-128">Dash</span></span>
-   <span data-ttu-id="5840a-129">лонгдаш</span><span class="sxs-lookup"><span data-stu-id="5840a-129">LongDash</span></span>
-   <span data-ttu-id="5840a-130">DashDot</span><span class="sxs-lookup"><span data-stu-id="5840a-130">DashDot</span></span>
-   <span data-ttu-id="5840a-131">лонгдашдот</span><span class="sxs-lookup"><span data-stu-id="5840a-131">LongDashDot</span></span>
-   <span data-ttu-id="5840a-132">лонгдашдотдот</span><span class="sxs-lookup"><span data-stu-id="5840a-132">LongDashDotDot</span></span>

<span data-ttu-id="5840a-133">Атрибут **DashStyle** позволяет пользователю указать пользовательский шаблон штриха.</span><span class="sxs-lookup"><span data-stu-id="5840a-133">The **DashStyle** attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="5840a-134">Это делается с помощью ряда чисел.</span><span class="sxs-lookup"><span data-stu-id="5840a-134">This is done using a series of numbers.</span></span> <span data-ttu-id="5840a-135">Стили штриха определяются с точки зрения длины тире (рисуемой части штриха) и длины пробела между тире.</span><span class="sxs-lookup"><span data-stu-id="5840a-135">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="5840a-136">Длины задаются относительно толщины линии: длина "1" равна толщине линии.</span><span class="sxs-lookup"><span data-stu-id="5840a-136">The lengths are relative to the line width: a length of "1" is equal to the line width.</span></span> <span data-ttu-id="5840a-137">Стиль **ендкап** применяется к каждому штриху, а стиль стрелки — нет.</span><span class="sxs-lookup"><span data-stu-id="5840a-137">The **EndCap** style is applied to each dash, the arrow style is not.</span></span> <span data-ttu-id="5840a-138">Строка сначала определяет длину тире, а затем длину пробела.</span><span class="sxs-lookup"><span data-stu-id="5840a-138">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="5840a-139">Это может повторяться для формирования сложных стилей штрихов.</span><span class="sxs-lookup"><span data-stu-id="5840a-139">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="5840a-140">Строка всегда должна содержать пару цифр. Если оно содержит нечетное число чисел, Последнее может быть не учитывается.</span><span class="sxs-lookup"><span data-stu-id="5840a-140">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span>

<span data-ttu-id="5840a-141">В следующей таблице перечислены некоторые типичные значения и описание предполагаемого воздействия.</span><span class="sxs-lookup"><span data-stu-id="5840a-141">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="5840a-142">"0" означает точку, которая должна быть фаурфолд симметричной (при этом круглые концы должны быть кругом).</span><span class="sxs-lookup"><span data-stu-id="5840a-142">"0" implies a dot that should be fourfold symmetrical (with round end caps it should be a circle).</span></span> <span data-ttu-id="5840a-143">Если конец строки имеет значение «Flat», средство просмотра должно выбрать по возможности встроенный штрих по операционной системе (иными словами).</span><span class="sxs-lookup"><span data-stu-id="5840a-143">If the line end cap is "flat," a viewer should choose a built-in operating system dash where possible (in other words.</span></span> <span data-ttu-id="5840a-144">что быстро нарисовано.)</span><span class="sxs-lookup"><span data-stu-id="5840a-144">something that is fast to draw.).</span></span> <span data-ttu-id="5840a-145">В следующей таблице приведены некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="5840a-145">The following table shows some examples.</span></span>



| <span data-ttu-id="5840a-146">DashStyle</span><span class="sxs-lookup"><span data-stu-id="5840a-146">DashStyle</span></span>     | <span data-ttu-id="5840a-147">Описание</span><span class="sxs-lookup"><span data-stu-id="5840a-147">Description</span></span>                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5840a-148">"2 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-148">"2 2"</span></span>         | <span data-ttu-id="5840a-149">Короткие тире.</span><span class="sxs-lookup"><span data-stu-id="5840a-149">Short-dashes.</span></span> <span data-ttu-id="5840a-150">Каждое тире и расстояние между ними вдвое больше ширины строки.</span><span class="sxs-lookup"><span data-stu-id="5840a-150">Each dash and the space between is twice the width of the line.</span></span>                        |
| <span data-ttu-id="5840a-151">"0 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-151">"0 2"</span></span>         | <span data-ttu-id="5840a-152">Количество.</span><span class="sxs-lookup"><span data-stu-id="5840a-152">Dots.</span></span> <span data-ttu-id="5840a-153">Расстояние между вдвое больше ширины строки.</span><span class="sxs-lookup"><span data-stu-id="5840a-153">Space between is twice the width of the line.</span></span>                                                  |
| <span data-ttu-id="5840a-154">"2 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-154">"2 2 0 2"</span></span>     | <span data-ttu-id="5840a-155">Короткий штрих пунктир.</span><span class="sxs-lookup"><span data-stu-id="5840a-155">Short dash dot.</span></span>                                                                                      |
| <span data-ttu-id="5840a-156">"2 2 0 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-156">"2 2 0 2 0 2"</span></span> | <span data-ttu-id="5840a-157">Короткий Штрих пунктирная точка.</span><span class="sxs-lookup"><span data-stu-id="5840a-157">Short dash dot dot.</span></span>                                                                                  |
| <span data-ttu-id="5840a-158">"1 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-158">"1 2"</span></span>         | <span data-ttu-id="5840a-159">Оператор.</span><span class="sxs-lookup"><span data-stu-id="5840a-159">Dot.</span></span> <span data-ttu-id="5840a-160">Каждое тире — это ширина линии, а ширина каждого пробела вдвое превышает ширину строки.</span><span class="sxs-lookup"><span data-stu-id="5840a-160">Each dash is the width of the line, while each space is twice the width of the line.</span></span>            |
| <span data-ttu-id="5840a-161">"4 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-161">"4 2"</span></span>         | <span data-ttu-id="5840a-162">Черточками.</span><span class="sxs-lookup"><span data-stu-id="5840a-162">Dash.</span></span> <span data-ttu-id="5840a-163">Каждое тире в четыре раза превышает ширину строки, тогда как каждое пространство вдвое превышает ширину строки.</span><span class="sxs-lookup"><span data-stu-id="5840a-163">Each dash is four times the width of the line while each space is twice the width of the line.</span></span> |
| <span data-ttu-id="5840a-164">"8 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-164">"8 2"</span></span>         | <span data-ttu-id="5840a-165">Длинный тире.</span><span class="sxs-lookup"><span data-stu-id="5840a-165">Long dash.</span></span>                                                                                           |
| <span data-ttu-id="5840a-166">"4 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-166">"4 2 1 2"</span></span>     | <span data-ttu-id="5840a-167">Тире, точка.</span><span class="sxs-lookup"><span data-stu-id="5840a-167">Dash dot.</span></span>                                                                                            |
| <span data-ttu-id="5840a-168">"8 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-168">"8 2 1 2"</span></span>     | <span data-ttu-id="5840a-169">Длинный штрих пунктир.</span><span class="sxs-lookup"><span data-stu-id="5840a-169">Long dash dot.</span></span>                                                                                       |
| <span data-ttu-id="5840a-170">"8 2 1 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="5840a-170">"8 2 1 2 1 2"</span></span> | <span data-ttu-id="5840a-171">Длинный штрихпунктир с точкой.</span><span class="sxs-lookup"><span data-stu-id="5840a-171">Long dash dot dot.</span></span>                                                                                   |



 

<span data-ttu-id="5840a-172">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="5840a-172">*VML Standard Attribute*</span></span>

<span data-ttu-id="5840a-173">**Пример**</span><span class="sxs-lookup"><span data-stu-id="5840a-173">**Example**</span></span>

<span data-ttu-id="5840a-174">Фигура имеет стиль пунктира для чередующихся штрихов и точек.</span><span class="sxs-lookup"><span data-stu-id="5840a-174">The shape has a dash style of alternating dashes and dots.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 