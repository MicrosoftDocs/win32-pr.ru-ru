---
title: Атрибут Фитшапе VML
description: Атрибут Фитшапе VML
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672411"
---
# <a name="vml-fitshape-attribute"></a><span data-ttu-id="e409b-103">Атрибут Фитшапе VML</span><span class="sxs-lookup"><span data-stu-id="e409b-103">VML FitShape Attribute</span></span>

<span data-ttu-id="e409b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e409b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e409b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e409b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e409b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e409b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e409b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e409b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e409b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e409b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e409b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e409b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e409b-110">Определяет, умещается ли текст в ограничивающем прямоугольнике фигуры.</span><span class="sxs-lookup"><span data-stu-id="e409b-110">Defines whether the text fits bounding box of a shape.</span></span> <span data-ttu-id="e409b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="e409b-111">Read/write.</span></span> <span data-ttu-id="e409b-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="e409b-112">**VgTriState**.</span></span>

<span data-ttu-id="e409b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="e409b-113">**Applies To**</span></span>

[<span data-ttu-id="e409b-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="e409b-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="e409b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="e409b-115">**Tag Syntax**</span></span>

<span data-ttu-id="e409b-116"><v: *element* фитшапе = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="e409b-116"><v: *element* fitshape=" *expression* "></span></span>

<span data-ttu-id="e409b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="e409b-117">**Script Syntax**</span></span>

<span data-ttu-id="e409b-118">*element* . фитшапе = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="e409b-118">*element* .fitshape="*expression*"</span></span>

<span data-ttu-id="e409b-119">*выражение* = *element*. фитшапе</span><span class="sxs-lookup"><span data-stu-id="e409b-119">*expression*=*element*.fitshape</span></span>

<span data-ttu-id="e409b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="e409b-120">**Remarks**</span></span>

<span data-ttu-id="e409b-121">Если **значение равно true**, растягивает текст до краев прямоугольника, определяющего всю фигуру.</span><span class="sxs-lookup"><span data-stu-id="e409b-121">If **True**, stretches the text out to the edges of the box that defines the entire shape.</span></span> <span data-ttu-id="e409b-122">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="e409b-122">The default is **False**.</span></span>

<span data-ttu-id="e409b-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="e409b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="e409b-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="e409b-124">**Example**</span></span>

<span data-ttu-id="e409b-125">Текст будет растянут по размеру фигуры.</span><span class="sxs-lookup"><span data-stu-id="e409b-125">The text will stretch to fit the shape.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 