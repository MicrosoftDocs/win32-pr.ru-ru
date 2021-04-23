---
title: Атрибут аспекта VML
description: Атрибут аспекта VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792402"
---
# <a name="vml-aspect-attribute"></a><span data-ttu-id="6f83e-103">Атрибут аспекта VML</span><span class="sxs-lookup"><span data-stu-id="6f83e-103">VML Aspect Attribute</span></span>

<span data-ttu-id="6f83e-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6f83e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6f83e-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6f83e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6f83e-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6f83e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6f83e-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6f83e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6f83e-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6f83e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6f83e-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6f83e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6f83e-110">Указывает, как будет сохраняться пропорции изображения заливки.</span><span class="sxs-lookup"><span data-stu-id="6f83e-110">Specifies how the fill image aspect ratio will be preserved.</span></span> <span data-ttu-id="6f83e-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6f83e-111">Read/write.</span></span> <span data-ttu-id="6f83e-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="6f83e-112">**String**.</span></span>

<span data-ttu-id="6f83e-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6f83e-113">**Applies To**</span></span>

[<span data-ttu-id="6f83e-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="6f83e-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="6f83e-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6f83e-115">**Tag Syntax**</span></span>

<span data-ttu-id="6f83e-116"><v: аспект *element* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="6f83e-116"><v: *element* aspect=" *expression* "></span></span>

<span data-ttu-id="6f83e-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="6f83e-117">**Script Syntax**</span></span>

<span data-ttu-id="6f83e-118">*element* . аспект = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="6f83e-118">*element* .aspect="*expression*"</span></span>

<span data-ttu-id="6f83e-119">*выражение* = *element*. аспект</span><span class="sxs-lookup"><span data-stu-id="6f83e-119">*expression*=*element*.aspect</span></span>

<span data-ttu-id="6f83e-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6f83e-120">**Remarks**</span></span>

<span data-ttu-id="6f83e-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="6f83e-121">Values include:</span></span>



| <span data-ttu-id="6f83e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6f83e-122">Value</span></span>   | <span data-ttu-id="6f83e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="6f83e-123">Description</span></span>                           |
|---------|---------------------------------------|
| <span data-ttu-id="6f83e-124">ignore</span><span class="sxs-lookup"><span data-stu-id="6f83e-124">ignore</span></span>  | <span data-ttu-id="6f83e-125">Пропускать проблемы с аспектами.</span><span class="sxs-lookup"><span data-stu-id="6f83e-125">Ignore aspect issues.</span></span> <span data-ttu-id="6f83e-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f83e-126">Default.</span></span>        |
| <span data-ttu-id="6f83e-127">задать</span><span class="sxs-lookup"><span data-stu-id="6f83e-127">atleast</span></span> | <span data-ttu-id="6f83e-128">Размер изображения не меньше **размера**.</span><span class="sxs-lookup"><span data-stu-id="6f83e-128">Image is at least as big as **Size**.</span></span> |
| <span data-ttu-id="6f83e-129">атмост</span><span class="sxs-lookup"><span data-stu-id="6f83e-129">atmost</span></span>  | <span data-ttu-id="6f83e-130">**Размер** изображения не превышает.</span><span class="sxs-lookup"><span data-stu-id="6f83e-130">Image is no bigger than **Size**.</span></span>     |



 

<span data-ttu-id="6f83e-131">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="6f83e-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="6f83e-132">**Пример**</span><span class="sxs-lookup"><span data-stu-id="6f83e-132">**Example**</span></span>

<span data-ttu-id="6f83e-133">Изображение, составляющее заливку, больше или равно размеру 10 пунктов на 10 пунктов.</span><span class="sxs-lookup"><span data-stu-id="6f83e-133">The image that makes up the fill is greater than or equal to a size of 10 points by 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 