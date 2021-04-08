---
title: Атрибут объекта FillType VML
description: Атрибут объекта FillType VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987861"
---
# <a name="vml-filltype-attribute"></a><span data-ttu-id="83bbf-103">Атрибут объекта FillType VML</span><span class="sxs-lookup"><span data-stu-id="83bbf-103">VML FillType Attribute</span></span>

<span data-ttu-id="83bbf-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="83bbf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="83bbf-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="83bbf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="83bbf-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="83bbf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="83bbf-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="83bbf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="83bbf-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="83bbf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="83bbf-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="83bbf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="83bbf-110">Определяет тип заливки, используемый для фона штриха.</span><span class="sxs-lookup"><span data-stu-id="83bbf-110">Defines the type of fill used for the background of a stroke.</span></span> <span data-ttu-id="83bbf-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="83bbf-111">Read/write.</span></span> <span data-ttu-id="83bbf-112">**Вгфиллтипе**.</span><span class="sxs-lookup"><span data-stu-id="83bbf-112">**VgFillType**.</span></span>

<span data-ttu-id="83bbf-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="83bbf-113">**Applies To**</span></span>

[<span data-ttu-id="83bbf-114">Водок</span><span class="sxs-lookup"><span data-stu-id="83bbf-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="83bbf-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="83bbf-115">**Tag Syntax**</span></span>

<span data-ttu-id="83bbf-116"><v: *element* объекта FillType = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="83bbf-116"><v: *element* filltype=" *expression* "></span></span>

<span data-ttu-id="83bbf-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="83bbf-117">**Script Syntax**</span></span>

<span data-ttu-id="83bbf-118">*element* . объекта FillType = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="83bbf-118">*element* .filltype="*expression*"</span></span>

<span data-ttu-id="83bbf-119">*выражение* = *element*. объекта FillType</span><span class="sxs-lookup"><span data-stu-id="83bbf-119">*expression*=*element*.filltype</span></span>

<span data-ttu-id="83bbf-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="83bbf-120">**Remarks**</span></span>

<span data-ttu-id="83bbf-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="83bbf-121">Values include:</span></span>



| <span data-ttu-id="83bbf-122">DashStyle</span><span class="sxs-lookup"><span data-stu-id="83bbf-122">DashStyle</span></span> | <span data-ttu-id="83bbf-123">Описание</span><span class="sxs-lookup"><span data-stu-id="83bbf-123">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="83bbf-124">Сплошная</span><span class="sxs-lookup"><span data-stu-id="83bbf-124">Solid</span></span>     | <span data-ttu-id="83bbf-125">Шаблон заливки является сплошным.</span><span class="sxs-lookup"><span data-stu-id="83bbf-125">The fill pattern is solid.</span></span> <span data-ttu-id="83bbf-126">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83bbf-126">Default value.</span></span>      |
| <span data-ttu-id="83bbf-127">Tile</span><span class="sxs-lookup"><span data-stu-id="83bbf-127">Tile</span></span>      | <span data-ttu-id="83bbf-128">Изображение заливки заполняется мозаикой.</span><span class="sxs-lookup"><span data-stu-id="83bbf-128">The fill image is tiled.</span></span>                       |
| <span data-ttu-id="83bbf-129">Модель</span><span class="sxs-lookup"><span data-stu-id="83bbf-129">Pattern</span></span>   | <span data-ttu-id="83bbf-130">Изображение заливки растягивается для формирования шаблона.</span><span class="sxs-lookup"><span data-stu-id="83bbf-130">The fill image is stretched to form a pattern.</span></span> |
| <span data-ttu-id="83bbf-131">Frame</span><span class="sxs-lookup"><span data-stu-id="83bbf-131">Frame</span></span>     | <span data-ttu-id="83bbf-132">Изображение заливки превращается в границу фигуры.</span><span class="sxs-lookup"><span data-stu-id="83bbf-132">The fill image becomes a border for the shape.</span></span> |



 

<span data-ttu-id="83bbf-133">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="83bbf-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="83bbf-134">**Пример**</span><span class="sxs-lookup"><span data-stu-id="83bbf-134">**Example**</span></span>

<span data-ttu-id="83bbf-135">Штрих фигуры имеет мозаичную текстуру, созданную на основе изображения cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="83bbf-135">The stroke of the shape has a tiled texture created from the cylinder.gif image.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 