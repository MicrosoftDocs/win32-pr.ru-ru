---
title: Атрибут прорисовки VML
description: Атрибут прорисовки VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672351"
---
# <a name="vml-render-attribute"></a><span data-ttu-id="6c886-103">Атрибут прорисовки VML</span><span class="sxs-lookup"><span data-stu-id="6c886-103">VML Render Attribute</span></span>

<span data-ttu-id="6c886-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6c886-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6c886-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6c886-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6c886-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6c886-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6c886-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c886-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6c886-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6c886-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6c886-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6c886-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6c886-110">Определяет режим отрисовки для объема.</span><span class="sxs-lookup"><span data-stu-id="6c886-110">Defines the rendering mode of the extrusion.</span></span> <span data-ttu-id="6c886-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6c886-111">Read/write.</span></span> <span data-ttu-id="6c886-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="6c886-112">**String**.</span></span>

<span data-ttu-id="6c886-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6c886-113">**Applies To**</span></span>

[<span data-ttu-id="6c886-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="6c886-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="6c886-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6c886-115">**Tag Syntax**</span></span>

<span data-ttu-id="6c886-116"><o: Render для *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="6c886-116"><o: *element* render=" *expression* "></span></span>

<span data-ttu-id="6c886-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="6c886-117">**Script Syntax**</span></span>

<span data-ttu-id="6c886-118">*element* . Render = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="6c886-118">*element* .render="*expression*"</span></span>

<span data-ttu-id="6c886-119">*выражение* = *элемент*. Render</span><span class="sxs-lookup"><span data-stu-id="6c886-119">*expression*=*element*.render</span></span>

<span data-ttu-id="6c886-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6c886-120">**Remarks**</span></span>

<span data-ttu-id="6c886-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="6c886-121">Values include:</span></span>



| <span data-ttu-id="6c886-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6c886-122">Value</span></span>        | <span data-ttu-id="6c886-123">Описание</span><span class="sxs-lookup"><span data-stu-id="6c886-123">Description</span></span>                                                   |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="6c886-124">основ</span><span class="sxs-lookup"><span data-stu-id="6c886-124">solid</span></span>        | <span data-ttu-id="6c886-125">При отрисовке отображается сплошная фигура.</span><span class="sxs-lookup"><span data-stu-id="6c886-125">Rendering displays a solid shape.</span></span> <span data-ttu-id="6c886-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c886-126">Default.</span></span>                    |
| <span data-ttu-id="6c886-127">каркасной модели</span><span class="sxs-lookup"><span data-stu-id="6c886-127">wireframe</span></span>    | <span data-ttu-id="6c886-128">При отрисовке отображается каркасная фигура.</span><span class="sxs-lookup"><span data-stu-id="6c886-128">Rendering displays a wireframe shape.</span></span>                         |
| <span data-ttu-id="6c886-129">баундингкубе</span><span class="sxs-lookup"><span data-stu-id="6c886-129">boundingcube</span></span> | <span data-ttu-id="6c886-130">При отрисовке отображается связанный куб, содержащий фигуру.</span><span class="sxs-lookup"><span data-stu-id="6c886-130">Rendering displays the bounding cube that contains the shape.</span></span> |



 

<span data-ttu-id="6c886-131">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="6c886-131">*Microsoft Office Extensions Attribute*</span></span>

 

 