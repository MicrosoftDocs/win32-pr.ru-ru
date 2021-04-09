---
title: Атрибут VML Margin-Right
description: Атрибут VML Margin-Right
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070596"
---
# <a name="vml-margin-right-attribute"></a><span data-ttu-id="d2e06-103">Атрибут VML Margin-Right</span><span class="sxs-lookup"><span data-stu-id="d2e06-103">VML Margin-Right Attribute</span></span>

<span data-ttu-id="d2e06-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d2e06-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d2e06-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="d2e06-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d2e06-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="d2e06-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d2e06-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d2e06-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d2e06-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d2e06-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d2e06-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d2e06-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d2e06-110">Задает правый конец содержащего прямоугольника фигуры относительно привязки фигуры.</span><span class="sxs-lookup"><span data-stu-id="d2e06-110">Specifies the right edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="d2e06-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d2e06-111">Read/write.</span></span> <span data-ttu-id="d2e06-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="d2e06-112">**String**.</span></span>

<span data-ttu-id="d2e06-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="d2e06-113">**Applies To**</span></span>

[<span data-ttu-id="d2e06-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="d2e06-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d2e06-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="d2e06-115">**Tag Syntax**</span></span>

<span data-ttu-id="d2e06-116"><v: Style *элемента* = "поле-Right: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="d2e06-116"><v: *element* style="margin-right: *expression* "></span></span>

<span data-ttu-id="d2e06-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="d2e06-117">**Script Syntax**</span></span>

<span data-ttu-id="d2e06-118">*element* . Style. marginright = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="d2e06-118">*element* .style.marginright="*expression*"</span></span>

<span data-ttu-id="d2e06-119">*выражение* = *element*. Style. marginright</span><span class="sxs-lookup"><span data-stu-id="d2e06-119">*expression*=*element*.style.marginright</span></span>

<span data-ttu-id="d2e06-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="d2e06-120">**Remarks**</span></span>

<span data-ttu-id="d2e06-121">Атрибут **margin-right** аналогичен стандартному атрибуту HTML **margin-right** , используемому со таблицами стилей.</span><span class="sxs-lookup"><span data-stu-id="d2e06-121">The **Margin-Right** attribute is similar to the standard HTML **Margin-Right** attribute used with style sheets.</span></span>

<span data-ttu-id="d2e06-122">Обратите внимание, что для написания сценариев вместо **поля по правому** краю используется **marginright** .</span><span class="sxs-lookup"><span data-stu-id="d2e06-122">Note that **marginright** is used instead of **margin-right** for scripting.</span></span> <span data-ttu-id="d2e06-123">Также обратите внимание, что если **положение** **абсолютное**, поле не изменится.</span><span class="sxs-lookup"><span data-stu-id="d2e06-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="d2e06-124">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="d2e06-124">Values include:</span></span>



| <span data-ttu-id="d2e06-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d2e06-125">Value</span></span>      | <span data-ttu-id="d2e06-126">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e06-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e06-127">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="d2e06-127">Auto</span></span>       | <span data-ttu-id="d2e06-128">Расположение элемента по умолчанию в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="d2e06-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="d2e06-129">units</span><span class="sxs-lookup"><span data-stu-id="d2e06-129">units</span></span>      | <span data-ttu-id="d2e06-130">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2e06-130">Default.</span></span> <span data-ttu-id="d2e06-131">Число с абсолютными единицами измерения (cm, mm, in, PT, PC или px) или обозначение относительного числа единиц (EM или ex).</span><span class="sxs-lookup"><span data-stu-id="d2e06-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="d2e06-132">Если единицы не заданы, предполагается использование точек (ПКС).</span><span class="sxs-lookup"><span data-stu-id="d2e06-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="d2e06-133">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="d2e06-133">The default value is 0.</span></span> |
| <span data-ttu-id="d2e06-134">процент</span><span class="sxs-lookup"><span data-stu-id="d2e06-134">percentage</span></span> | <span data-ttu-id="d2e06-135">Значение, выраженное в процентах от высоты родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e06-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="d2e06-136">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="d2e06-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="d2e06-137">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="d2e06-137">**See Also**</span></span>

[<span data-ttu-id="d2e06-138">единиц(ы)</span><span class="sxs-lookup"><span data-stu-id="d2e06-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="d2e06-139">**Пример**</span><span class="sxs-lookup"><span data-stu-id="d2e06-139">**Example**</span></span>

<span data-ttu-id="d2e06-140">Правое поле имеет значение 25 пикселей.</span><span class="sxs-lookup"><span data-stu-id="d2e06-140">The right margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



<span data-ttu-id="d2e06-141">[Пример атрибута margin-right](/previous-versions/bb229677(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2e06-141">[Margin-Right Attribute Example](/previous-versions/bb229677(v=vs.85)).</span></span> <span data-ttu-id="d2e06-142">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="d2e06-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 