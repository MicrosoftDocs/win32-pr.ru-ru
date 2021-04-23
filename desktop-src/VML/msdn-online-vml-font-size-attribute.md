---
title: Атрибут VML Font-Size
description: Атрибут VML Font-Size
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c02b2df8fb0076ed6df6342e40b980ed8aa248e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488252"
---
# <a name="vml-font-size-attribute"></a><span data-ttu-id="725cd-103">Атрибут VML Font-Size</span><span class="sxs-lookup"><span data-stu-id="725cd-103">VML Font-Size Attribute</span></span>

<span data-ttu-id="725cd-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="725cd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="725cd-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="725cd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="725cd-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="725cd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="725cd-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="725cd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="725cd-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="725cd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="725cd-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="725cd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="725cd-110">Определяет размер шрифта.</span><span class="sxs-lookup"><span data-stu-id="725cd-110">Defines the size of the font.</span></span> <span data-ttu-id="725cd-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="725cd-111">Read/write.</span></span> <span data-ttu-id="725cd-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="725cd-112">**String**.</span></span>

<span data-ttu-id="725cd-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="725cd-113">**Applies To**</span></span>

[<span data-ttu-id="725cd-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="725cd-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="725cd-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="725cd-115">**Tag Syntax**</span></span>

<span data-ttu-id="725cd-116"><v: Style *элемента* = "Font-Size: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="725cd-116"><v: *element* style="font-size: *expression* "></span></span>

<span data-ttu-id="725cd-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="725cd-117">**Script Syntax**</span></span>

<span data-ttu-id="725cd-118">*element* . Style. FontSize = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="725cd-118">*element* .style.fontsize="*expression*"</span></span>

<span data-ttu-id="725cd-119">*выражение* = *элемент*. Style. FontSize</span><span class="sxs-lookup"><span data-stu-id="725cd-119">*expression*=*element*.style.fontsize</span></span>

<span data-ttu-id="725cd-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="725cd-120">**Remarks**</span></span>

<span data-ttu-id="725cd-121">Размер шрифта определяется в пунктах.</span><span class="sxs-lookup"><span data-stu-id="725cd-121">The font size is defined in points.</span></span> <span data-ttu-id="725cd-122">Значения совпадают со стандартными атрибутами стиля HTML.</span><span class="sxs-lookup"><span data-stu-id="725cd-122">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="725cd-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="725cd-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="725cd-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="725cd-124">**Example**</span></span>

<span data-ttu-id="725cd-125">Размер шрифта — 36 точек.</span><span class="sxs-lookup"><span data-stu-id="725cd-125">The font size is 36 points.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 