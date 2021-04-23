---
title: Атрибут Имажеаспект VML
description: Атрибут Имажеаспект VML
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338116"
---
# <a name="vml-imageaspect-attribute"></a><span data-ttu-id="0597d-103">Атрибут Имажеаспект VML</span><span class="sxs-lookup"><span data-stu-id="0597d-103">VML ImageAspect Attribute</span></span>

<span data-ttu-id="0597d-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0597d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0597d-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="0597d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0597d-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="0597d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0597d-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0597d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0597d-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0597d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0597d-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0597d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0597d-110">Определяет, как будет сохраняться пропорции изображения обводки.</span><span class="sxs-lookup"><span data-stu-id="0597d-110">Defines how the stroke image aspect ratio will be preserved.</span></span> <span data-ttu-id="0597d-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="0597d-111">Read/write.</span></span> <span data-ttu-id="0597d-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="0597d-112">**String**.</span></span>

<span data-ttu-id="0597d-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="0597d-113">**Applies To**</span></span>

[<span data-ttu-id="0597d-114">Водок</span><span class="sxs-lookup"><span data-stu-id="0597d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="0597d-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="0597d-115">**Tag Syntax**</span></span>

<span data-ttu-id="0597d-116"><v:</span><span class="sxs-lookup"><span data-stu-id="0597d-116"><v:</span></span>

<span data-ttu-id="0597d-117">element *имажеаспект = "* выражение *" >*</span><span class="sxs-lookup"><span data-stu-id="0597d-117">element *imageaspect="* expression *">*</span></span>

<span data-ttu-id="0597d-118">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="0597d-118">**Script Syntax**</span></span>

<span data-ttu-id="0597d-119">element *. имажеаспект = "* выражение *"*</span><span class="sxs-lookup"><span data-stu-id="0597d-119">element *.imageaspect="* expression *"*</span></span>

<span data-ttu-id="0597d-120">*=* элемент Expression *. имажеаспект*</span><span class="sxs-lookup"><span data-stu-id="0597d-120">expression *=* element *.imageaspect*</span></span>

<span data-ttu-id="0597d-121">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="0597d-121">**Remarks**</span></span>

<span data-ttu-id="0597d-122">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="0597d-122">Values include:</span></span>



| <span data-ttu-id="0597d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0597d-123">Value</span></span>   | <span data-ttu-id="0597d-124">Описание</span><span class="sxs-lookup"><span data-stu-id="0597d-124">Description</span></span>                                |
|---------|--------------------------------------------|
| <span data-ttu-id="0597d-125">Игнорировать</span><span class="sxs-lookup"><span data-stu-id="0597d-125">Ignore</span></span>  | <span data-ttu-id="0597d-126">Пропускать проблемы с аспектами.</span><span class="sxs-lookup"><span data-stu-id="0597d-126">Ignore aspect issues.</span></span>                      |
| <span data-ttu-id="0597d-127">Задать</span><span class="sxs-lookup"><span data-stu-id="0597d-127">AtLeast</span></span> | <span data-ttu-id="0597d-128">Размер изображения по меньшей мере равен **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="0597d-128">Image is at least as big as **ImageSize**.</span></span> |
| <span data-ttu-id="0597d-129">атмост</span><span class="sxs-lookup"><span data-stu-id="0597d-129">AtMost</span></span>  | <span data-ttu-id="0597d-130">Размер изображения не превышает **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="0597d-130">Image is no bigger than **ImageSize**.</span></span>     |



 

<span data-ttu-id="0597d-131">В каждом случае атрибут **ImageSize** будет скорректирован для сохранения аспекта изображения.</span><span class="sxs-lookup"><span data-stu-id="0597d-131">In each case, the **ImageSize** attribute will be adjusted to preserve the aspect of the image.</span></span>

<span data-ttu-id="0597d-132">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="0597d-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="0597d-133">**Пример**</span><span class="sxs-lookup"><span data-stu-id="0597d-133">**Example**</span></span>

<span data-ttu-id="0597d-134">Изображение обводки будет по крайней мере большим, чем размер изображения.</span><span class="sxs-lookup"><span data-stu-id="0597d-134">The stroke image will be at least as big as the image size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 