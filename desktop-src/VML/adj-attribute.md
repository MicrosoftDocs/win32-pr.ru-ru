---
title: Атрибут "года"
description: Атрибут "года"
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672314"
---
# <a name="adj-attribute"></a><span data-ttu-id="395a5-103">Атрибут "года"</span><span class="sxs-lookup"><span data-stu-id="395a5-103">Adj Attribute</span></span>

<span data-ttu-id="395a5-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="395a5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="395a5-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="395a5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="395a5-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="395a5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="395a5-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="395a5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="395a5-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="395a5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="395a5-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="395a5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="395a5-110">Задает значение корректировки, используемое для определения значений формулы.</span><span class="sxs-lookup"><span data-stu-id="395a5-110">Specifies an adjustment value used to define values for a formula.</span></span> <span data-ttu-id="395a5-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="395a5-111">Read/write.</span></span> <span data-ttu-id="395a5-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="395a5-112">**String**.</span></span>

<span data-ttu-id="395a5-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="395a5-113">**Applies To**</span></span>

[<span data-ttu-id="395a5-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="395a5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="395a5-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="395a5-115">**Tag Syntax**</span></span>

<span data-ttu-id="395a5-116"><v: поправка *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="395a5-116"><v: *element* adj=" *expression* "></span></span>

<span data-ttu-id="395a5-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="395a5-117">**Script Syntax**</span></span>

<span data-ttu-id="395a5-118">*element* . прилагательные = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="395a5-118">*element* .adj="*expression*"</span></span>

<span data-ttu-id="395a5-119">*выражение* = *element*. прилагательный</span><span class="sxs-lookup"><span data-stu-id="395a5-119">*expression*=*element*.adj</span></span>

<span data-ttu-id="395a5-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="395a5-120">**Remarks**</span></span>

<span data-ttu-id="395a5-121">**Прилагательное** используется для предоставления настраиваемых точек для формулы.</span><span class="sxs-lookup"><span data-stu-id="395a5-121">**Adj** is used to provide adjustable points for a formula.</span></span> <span data-ttu-id="395a5-122">Если **используется в тегах, то** результатом является строка с разделителями-запятыми длиной до 8 значений.</span><span class="sxs-lookup"><span data-stu-id="395a5-122">If used in tags, **Adj** is a comma-delimited string of up to 8 values.</span></span> <span data-ttu-id="395a5-123">Некоторые значения могут быть опущены.</span><span class="sxs-lookup"><span data-stu-id="395a5-123">Some values may be omitted.</span></span> <span data-ttu-id="395a5-124">Например, "0, 1, 2,, 4, 5,, 7" является допустимой строкой, но четвертый и седьмой элементы не будут иметь значений (элементы считаются начиная с 0).</span><span class="sxs-lookup"><span data-stu-id="395a5-124">For example, "0,1,2,,4,5,,7" would be a valid string but the fourth and seventh items would not have values (items are counted starting from 0).</span></span>

<span data-ttu-id="395a5-125">Для написания **сценариев используется тип** данных [ивгаджустментс](msdn-online-vml-ivgadjustments-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="395a5-125">For scripting, **Adj** uses the [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) data type.</span></span>

<span data-ttu-id="395a5-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="395a5-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="395a5-127">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="395a5-127">**See Also**</span></span>

[<span data-ttu-id="395a5-128">Формула</span><span class="sxs-lookup"><span data-stu-id="395a5-128">Formula</span></span>](msdn-online-vml-formulas-element.md)

<span data-ttu-id="395a5-129">**Пример**</span><span class="sxs-lookup"><span data-stu-id="395a5-129">**Example**</span></span>

<span data-ttu-id="395a5-130">Простой квадрат создается с корректировками.</span><span class="sxs-lookup"><span data-stu-id="395a5-130">A simple square is created with adjustments.</span></span> <span data-ttu-id="395a5-131">Сначала создается **строка с** указанием восьми значений коррекции.</span><span class="sxs-lookup"><span data-stu-id="395a5-131">First the **Adj** string is created to define eight adjustment values.</span></span> <span data-ttu-id="395a5-132">Затем каждое значение корректировки ссылается на одну из восьми формул, при этом каждое значение коррекции буква символом решетки ( \# ).</span><span class="sxs-lookup"><span data-stu-id="395a5-132">Then each adjustment value is referenced by one of the eight formulas, with each adjustment value preceeded by a number sign (\#) symbol.</span></span> <span data-ttu-id="395a5-133">Наконец, путь определяется строкой, которая ссылается на формулы, при этом каждая формула буква символом "at" (@).</span><span class="sxs-lookup"><span data-stu-id="395a5-133">Finally a path is defined by a string that references the formulas, with each formula preceeded by the "at" sign (@) symbol.</span></span>


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



<span data-ttu-id="395a5-134">[Пример атрибута](/previous-versions/bb229662(v=vs.85)) "поправка" (требуется Microsoft Internet Explorer 5 или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="395a5-134">[Adj Attribute Example](/previous-versions/bb229662(v=vs.85)) (Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 