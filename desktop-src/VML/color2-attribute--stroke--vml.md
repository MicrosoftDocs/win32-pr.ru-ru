---
title: Атрибут color2 (Stroke) (VML)
description: Атрибут color2 (Stroke) (VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d577843b7d65de4f6197beabc877c308cf00154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488044"
---
# <a name="color2-attribute-strokevml"></a><span data-ttu-id="6eab5-103">Атрибут color2 (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="6eab5-103">Color2 Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="6eab5-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6eab5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6eab5-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6eab5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6eab5-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6eab5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6eab5-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6eab5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6eab5-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6eab5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6eab5-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6eab5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6eab5-110">Определяет второй цвет для штрихов.</span><span class="sxs-lookup"><span data-stu-id="6eab5-110">Defines a second color for strokes.</span></span> <span data-ttu-id="6eab5-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6eab5-111">Read/write.</span></span> <span data-ttu-id="6eab5-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="6eab5-112">**String**.</span></span>

<span data-ttu-id="6eab5-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6eab5-113">**Applies To**</span></span>

[<span data-ttu-id="6eab5-114">Водок</span><span class="sxs-lookup"><span data-stu-id="6eab5-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="6eab5-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6eab5-115">**Tag Syntax**</span></span>

<span data-ttu-id="6eab5-116"><v: *element* color2 = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="6eab5-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="6eab5-117">Синтаксис сценария</span><span class="sxs-lookup"><span data-stu-id="6eab5-117">Script Syntax</span></span>

<span data-ttu-id="6eab5-118">*element* . color2 = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="6eab5-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="6eab5-119">*выражение* = *element*. color2</span><span class="sxs-lookup"><span data-stu-id="6eab5-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="6eab5-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6eab5-120">**Remarks**</span></span>

<span data-ttu-id="6eab5-121">Второй цвет используется, если тип заливки обводки является шаблоном.</span><span class="sxs-lookup"><span data-stu-id="6eab5-121">A second color is used when a stroke's fill type is a pattern.</span></span>

<span data-ttu-id="6eab5-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="6eab5-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="6eab5-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="6eab5-123">**Example**</span></span>

<span data-ttu-id="6eab5-124">Обводка фигуры — это заливка узором, где заливка определяется исходным изображением, но прозрачный фон определяется вторым цветом.</span><span class="sxs-lookup"><span data-stu-id="6eab5-124">The shape's stroke is a pattern fill where the fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 