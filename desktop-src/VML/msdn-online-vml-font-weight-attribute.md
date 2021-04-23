---
title: Атрибут VML Font-Weight
description: Атрибут VML Font-Weight
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e4de8a1bb4132c75d4520dcacc661fbbc97eef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413175"
---
# <a name="vml-font-weight-attribute"></a><span data-ttu-id="e59be-103">Атрибут VML Font-Weight</span><span class="sxs-lookup"><span data-stu-id="e59be-103">VML Font-Weight Attribute</span></span>

<span data-ttu-id="e59be-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e59be-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e59be-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e59be-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e59be-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e59be-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e59be-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e59be-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e59be-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e59be-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e59be-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e59be-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e59be-110">Определяет толщину букв шрифта.</span><span class="sxs-lookup"><span data-stu-id="e59be-110">Defines the thickness of the letters of the font.</span></span> <span data-ttu-id="e59be-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="e59be-111">Read/write.</span></span> <span data-ttu-id="e59be-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="e59be-112">**String**.</span></span>

<span data-ttu-id="e59be-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="e59be-113">**Applies To**</span></span>

[<span data-ttu-id="e59be-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="e59be-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="e59be-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="e59be-115">**Tag Syntax**</span></span>

<span data-ttu-id="e59be-116"><v: Style *элемента* = "Font-весом: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e59be-116"><v: *element* style="font-weight: *expression* "></span></span>

<span data-ttu-id="e59be-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="e59be-117">**Script Syntax**</span></span>

<span data-ttu-id="e59be-118">*element* . Style. FontWeight = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="e59be-118">*element* .style.fontweight="*expression*"</span></span>

<span data-ttu-id="e59be-119">*выражение* = *element*. Style. FontWeight</span><span class="sxs-lookup"><span data-stu-id="e59be-119">*expression*=*element*.style.fontweight</span></span>

<span data-ttu-id="e59be-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="e59be-120">**Remarks**</span></span>

<span data-ttu-id="e59be-121">Значения совпадают со стандартными атрибутами стиля HTML.</span><span class="sxs-lookup"><span data-stu-id="e59be-121">The values are the same as the standard HTML style attributes.</span></span> <span data-ttu-id="e59be-122">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="e59be-122">Values include:</span></span>



| <span data-ttu-id="e59be-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e59be-123">Value</span></span>   | <span data-ttu-id="e59be-124">Описание</span><span class="sxs-lookup"><span data-stu-id="e59be-124">Description</span></span>                                                                 |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="e59be-125">нормальный</span><span class="sxs-lookup"><span data-stu-id="e59be-125">normal</span></span>  | <span data-ttu-id="e59be-126">Нормальный.</span><span class="sxs-lookup"><span data-stu-id="e59be-126">Normal.</span></span> <span data-ttu-id="e59be-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e59be-127">Default.</span></span>                                                            |
| <span data-ttu-id="e59be-128">полужирный</span><span class="sxs-lookup"><span data-stu-id="e59be-128">bold</span></span>    | <span data-ttu-id="e59be-129">Делять.</span><span class="sxs-lookup"><span data-stu-id="e59be-129">Bold.</span></span>                                                                       |
| <span data-ttu-id="e59be-130">bolder</span><span class="sxs-lookup"><span data-stu-id="e59be-130">bolder</span></span>  | <span data-ttu-id="e59be-131">Более тяжелее обычного.</span><span class="sxs-lookup"><span data-stu-id="e59be-131">Heavier than normal.</span></span>                                                        |
| <span data-ttu-id="e59be-132">lighter</span><span class="sxs-lookup"><span data-stu-id="e59be-132">lighter</span></span> | <span data-ttu-id="e59be-133">Светлее обычного.</span><span class="sxs-lookup"><span data-stu-id="e59be-133">Lighter than normal.</span></span>                                                        |
| <span data-ttu-id="e59be-134">100</span><span class="sxs-lookup"><span data-stu-id="e59be-134">100</span></span>     | <span data-ttu-id="e59be-135">По крайней мере, в качестве веса 200.</span><span class="sxs-lookup"><span data-stu-id="e59be-135">At least as light as the 200 weight.</span></span>                                        |
| <span data-ttu-id="e59be-136">200</span><span class="sxs-lookup"><span data-stu-id="e59be-136">200</span></span>     | <span data-ttu-id="e59be-137">По крайней мере выделены полужирным шрифтом, равным 100, и, по крайней мере, в качестве веса 300.</span><span class="sxs-lookup"><span data-stu-id="e59be-137">At least as bold as the 100 weight and at least as light as the 300 weight.</span></span> |
| <span data-ttu-id="e59be-138">300</span><span class="sxs-lookup"><span data-stu-id="e59be-138">300</span></span>     | <span data-ttu-id="e59be-139">По крайней мере выделены полужирным шрифтом, равным 200, и, по крайней мере, в качестве веса 400.</span><span class="sxs-lookup"><span data-stu-id="e59be-139">At least as bold as the 200 weight and at least as light as the 400 weight.</span></span> |
| <span data-ttu-id="e59be-140">400</span><span class="sxs-lookup"><span data-stu-id="e59be-140">400</span></span>     | <span data-ttu-id="e59be-141">Нормальный.</span><span class="sxs-lookup"><span data-stu-id="e59be-141">Normal.</span></span>                                                                     |
| <span data-ttu-id="e59be-142">500</span><span class="sxs-lookup"><span data-stu-id="e59be-142">500</span></span>     | <span data-ttu-id="e59be-143">По крайней мере выделены полужирным шрифтом, равным 400, и, по крайней мере, в качестве веса 600.</span><span class="sxs-lookup"><span data-stu-id="e59be-143">At least as bold as the 400 weight and at least as light as the 600 weight.</span></span> |
| <span data-ttu-id="e59be-144">600</span><span class="sxs-lookup"><span data-stu-id="e59be-144">600</span></span>     | <span data-ttu-id="e59be-145">По крайней мере выделены полужирным шрифтом, равным 500, и, по крайней мере, в качестве веса 700.</span><span class="sxs-lookup"><span data-stu-id="e59be-145">At least as bold as the 500 weight and at least as light as the 700 weight.</span></span> |
| <span data-ttu-id="e59be-146">700</span><span class="sxs-lookup"><span data-stu-id="e59be-146">700</span></span>     | <span data-ttu-id="e59be-147">Делять.</span><span class="sxs-lookup"><span data-stu-id="e59be-147">Bold.</span></span>                                                                       |
| <span data-ttu-id="e59be-148">800</span><span class="sxs-lookup"><span data-stu-id="e59be-148">800</span></span>     | <span data-ttu-id="e59be-149">По крайней мере выделены полужирным шрифтом, равным 700, и, по крайней мере, в качестве веса 900.</span><span class="sxs-lookup"><span data-stu-id="e59be-149">At least as bold as the 700 weight and at least as light as the 900 weight.</span></span> |
| <span data-ttu-id="e59be-150">900</span><span class="sxs-lookup"><span data-stu-id="e59be-150">900</span></span>     | <span data-ttu-id="e59be-151">По крайней мере, выделено полужирным шрифтом 800.</span><span class="sxs-lookup"><span data-stu-id="e59be-151">At least as bold as the 800 weight.</span></span>                                         |



 

<span data-ttu-id="e59be-152">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="e59be-152">*VML Standard Attribute*</span></span>

<span data-ttu-id="e59be-153">**Пример**</span><span class="sxs-lookup"><span data-stu-id="e59be-153">**Example**</span></span>

<span data-ttu-id="e59be-154">Плотность шрифта выделена полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="e59be-154">The font weight is bold.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 