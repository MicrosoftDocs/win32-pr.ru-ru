---
title: Атрибут Фокуспоситион VML
description: Атрибут Фокуспоситион VML
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134551"
---
# <a name="vml-focusposition-attribute"></a><span data-ttu-id="e1876-103">Атрибут Фокуспоситион VML</span><span class="sxs-lookup"><span data-stu-id="e1876-103">VML FocusPosition Attribute</span></span>

<span data-ttu-id="e1876-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e1876-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e1876-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e1876-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e1876-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e1876-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e1876-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e1876-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e1876-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e1876-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e1876-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e1876-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e1876-110">Определяет центр радиального градиента.</span><span class="sxs-lookup"><span data-stu-id="e1876-110">Defines the center of a radial gradient.</span></span> <span data-ttu-id="e1876-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="e1876-111">Read/write.</span></span> <span data-ttu-id="e1876-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="e1876-112">**VgVector2D**.</span></span>

<span data-ttu-id="e1876-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="e1876-113">**Applies To**</span></span>

[<span data-ttu-id="e1876-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="e1876-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="e1876-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="e1876-115">**Tag Syntax**</span></span>

<span data-ttu-id="e1876-116"><v: *element* фокуспоситион = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="e1876-116"><v: *element* focusposition=" *expression* "></span></span>

<span data-ttu-id="e1876-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="e1876-117">**Script Syntax**</span></span>

<span data-ttu-id="e1876-118">*element* . фокуспоситион = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="e1876-118">*element* .focusposition="*expression*"</span></span>

<span data-ttu-id="e1876-119">*выражение* = *element*. фокуспоситион</span><span class="sxs-lookup"><span data-stu-id="e1876-119">*expression*=*element*.focusposition</span></span>

<span data-ttu-id="e1876-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="e1876-120">**Remarks**</span></span>

<span data-ttu-id="e1876-121">Указывает радиальные градиенты Центральной поситионфор.</span><span class="sxs-lookup"><span data-stu-id="e1876-121">Specifies the center positionfor radial gradients.</span></span> <span data-ttu-id="e1876-122">Вектор представляет собой часть ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="e1876-122">The vector is a fraction of the width and height of the shape.</span></span> <span data-ttu-id="e1876-123">Первый — это процентная доля от заполнения до левого края; Второй — это процентная доля от заполнения до верха.</span><span class="sxs-lookup"><span data-stu-id="e1876-123">The first is a percentage of the fill to the left edge; the second is a percentage of the fill to the top.</span></span> <span data-ttu-id="e1876-124">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="e1876-124">The default value is 0,0.</span></span> <span data-ttu-id="e1876-125">Чтобы поместить радиальную заливку в центре фигуры, используйте значение 50%, 50%.</span><span class="sxs-lookup"><span data-stu-id="e1876-125">To position a radial fill at the center of a shape, use the value of 50%,50%.</span></span>

<span data-ttu-id="e1876-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="e1876-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="e1876-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="e1876-127">**Example**</span></span>

<span data-ttu-id="e1876-128">Радиальная заливка будет центрирована таким образом, что синий цвет будет начинаться в центре и истекает наружу, постепенно меняя его на красную, на время достижения внешних краев и углов.</span><span class="sxs-lookup"><span data-stu-id="e1876-128">The radial fill will be centered so that blue will start in the center and radiate outward, gradually changing to red by the time it reaches the outside edges and corners.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 