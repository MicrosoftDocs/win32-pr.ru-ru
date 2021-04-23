---
title: Атрибут VML Font-Style
description: Атрибут VML Font-Style
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f4fc2f299d78c3ccd8b194b8506cfce07abceb7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070078"
---
# <a name="vml-font-style-attribute"></a><span data-ttu-id="3f621-103">Атрибут VML Font-Style</span><span class="sxs-lookup"><span data-stu-id="3f621-103">VML Font-Style Attribute</span></span>

<span data-ttu-id="3f621-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3f621-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3f621-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="3f621-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3f621-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="3f621-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3f621-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3f621-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3f621-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3f621-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3f621-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3f621-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3f621-110">Определяет величину наклона для шрифта.</span><span class="sxs-lookup"><span data-stu-id="3f621-110">Defines the amount of slant for a font.</span></span> <span data-ttu-id="3f621-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="3f621-111">Read/write.</span></span> <span data-ttu-id="3f621-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="3f621-112">**String**.</span></span>

<span data-ttu-id="3f621-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="3f621-113">**Applies To**</span></span>

[<span data-ttu-id="3f621-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="3f621-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="3f621-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="3f621-115">**Tag Syntax**</span></span>

<span data-ttu-id="3f621-116"><v: Style *элемента* = "Font-Style: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3f621-116"><v: *element* style="font-style: *expression* "></span></span>

<span data-ttu-id="3f621-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="3f621-117">**Script Syntax**</span></span>

<span data-ttu-id="3f621-118">*element* . Style. FontStyle = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="3f621-118">*element* .style.fontstyle="*expression*"</span></span>

<span data-ttu-id="3f621-119">*выражение* = *element*. Style. FontStyle</span><span class="sxs-lookup"><span data-stu-id="3f621-119">*expression*=*element*.style.fontstyle</span></span>

<span data-ttu-id="3f621-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3f621-120">**Remarks**</span></span>

<span data-ttu-id="3f621-121">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="3f621-121">The values are:</span></span>

-   <span data-ttu-id="3f621-122">Обычная (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f621-122">normal (default)</span></span>
-   <span data-ttu-id="3f621-123">наклонный</span><span class="sxs-lookup"><span data-stu-id="3f621-123">oblique</span></span>
-   <span data-ttu-id="3f621-124">курсив</span><span class="sxs-lookup"><span data-stu-id="3f621-124">italic</span></span>

<span data-ttu-id="3f621-125">Большинство браузеров отображаются наклонным курсивом.</span><span class="sxs-lookup"><span data-stu-id="3f621-125">Most browsers render oblique as italic.</span></span> <span data-ttu-id="3f621-126">Значения совпадают со стандартными атрибутами стиля HTML.</span><span class="sxs-lookup"><span data-stu-id="3f621-126">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="3f621-127">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="3f621-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="3f621-128">**Пример**</span><span class="sxs-lookup"><span data-stu-id="3f621-128">**Example**</span></span>

<span data-ttu-id="3f621-129">Шрифт имеет курсивное начертание (наклонное).</span><span class="sxs-lookup"><span data-stu-id="3f621-129">The font is italic (slanted).</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 