---
title: Атрибут VML Margin-Bottom
description: Атрибут VML Margin-Bottom
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792768"
---
# <a name="vml-margin-bottom-attribute"></a><span data-ttu-id="4039b-103">Атрибут VML Margin-Bottom</span><span class="sxs-lookup"><span data-stu-id="4039b-103">VML Margin-Bottom Attribute</span></span>

<span data-ttu-id="4039b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4039b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4039b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="4039b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4039b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="4039b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4039b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4039b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4039b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4039b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4039b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4039b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4039b-110">Задает нижнюю границу содержащего прямоугольника фигуры относительно привязки фигуры.</span><span class="sxs-lookup"><span data-stu-id="4039b-110">Specifies the bottom edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="4039b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="4039b-111">Read/write.</span></span> <span data-ttu-id="4039b-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="4039b-112">**String**.</span></span>

<span data-ttu-id="4039b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="4039b-113">**Applies To**</span></span>

[<span data-ttu-id="4039b-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="4039b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="4039b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="4039b-115">**Tag Syntax**</span></span>

<span data-ttu-id="4039b-116"><v: поле *элемента* -Bottom = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="4039b-116"><v: *element* margin-bottom=" *expression* "></span></span>

<span data-ttu-id="4039b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="4039b-117">**Script Syntax**</span></span>

<span data-ttu-id="4039b-118">*element* . marginbottom = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="4039b-118">*element* .marginbottom="*expression*"</span></span>

<span data-ttu-id="4039b-119">*выражение* = *element*. marginbottom</span><span class="sxs-lookup"><span data-stu-id="4039b-119">*expression*=*element*.marginbottom</span></span>

<span data-ttu-id="4039b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="4039b-120">**Remarks**</span></span>

<span data-ttu-id="4039b-121">Атрибут **Margin-Bottom** аналогичен стандартному атрибуту **поля** HTML, используемому в таблицах стилей.</span><span class="sxs-lookup"><span data-stu-id="4039b-121">The **Margin-Bottom** attribute is similar to the standard HTML **Margin-Bottom** attribute used with style sheets.</span></span>

<span data-ttu-id="4039b-122">Обратите внимание, что для написания скрипта вместо **поля по нижнему** краю используется **marginbottom** .</span><span class="sxs-lookup"><span data-stu-id="4039b-122">Note that **marginbottom** is used instead of **margin-bottom** for scripting.</span></span> <span data-ttu-id="4039b-123">Также обратите внимание, что если **положение** **абсолютное**, поле не изменится.</span><span class="sxs-lookup"><span data-stu-id="4039b-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="4039b-124">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="4039b-124">Values include:</span></span>



| <span data-ttu-id="4039b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4039b-125">Value</span></span>      | <span data-ttu-id="4039b-126">Описание</span><span class="sxs-lookup"><span data-stu-id="4039b-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4039b-127">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="4039b-127">Auto</span></span>       | <span data-ttu-id="4039b-128">Расположение элемента по умолчанию в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="4039b-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="4039b-129">units</span><span class="sxs-lookup"><span data-stu-id="4039b-129">units</span></span>      | <span data-ttu-id="4039b-130">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4039b-130">Default.</span></span> <span data-ttu-id="4039b-131">Число с абсолютными единицами измерения (cm, mm, in, PT, PC или px) или обозначение относительного числа единиц (EM или ex).</span><span class="sxs-lookup"><span data-stu-id="4039b-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="4039b-132">Если единицы не заданы, предполагается использование точек (ПКС).</span><span class="sxs-lookup"><span data-stu-id="4039b-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="4039b-133">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="4039b-133">The default value is 0.</span></span> |
| <span data-ttu-id="4039b-134">процент</span><span class="sxs-lookup"><span data-stu-id="4039b-134">percentage</span></span> | <span data-ttu-id="4039b-135">Значение, выраженное в процентах от высоты родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="4039b-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="4039b-136">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="4039b-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="4039b-137">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="4039b-137">**See Also**</span></span>

[<span data-ttu-id="4039b-138">единиц(ы)</span><span class="sxs-lookup"><span data-stu-id="4039b-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="4039b-139">**Пример**</span><span class="sxs-lookup"><span data-stu-id="4039b-139">**Example**</span></span>

<span data-ttu-id="4039b-140">Для нижнего поля задается значение 25 пикселей.</span><span class="sxs-lookup"><span data-stu-id="4039b-140">The bottom margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



<span data-ttu-id="4039b-141">[Пример атрибута Margin-Bottom](/previous-versions/bb229675(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4039b-141">[Margin-Bottom Attribute Example](/previous-versions/bb229675(v=vs.85)).</span></span> <span data-ttu-id="4039b-142">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="4039b-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 