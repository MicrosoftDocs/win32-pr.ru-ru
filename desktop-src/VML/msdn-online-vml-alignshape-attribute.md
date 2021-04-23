---
title: Атрибут Алигншапе VML
description: Атрибут Алигншапе VML
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339028"
---
# <a name="vml-alignshape-attribute"></a><span data-ttu-id="605ca-103">Атрибут Алигншапе VML</span><span class="sxs-lookup"><span data-stu-id="605ca-103">VML AlignShape Attribute</span></span>

<span data-ttu-id="605ca-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="605ca-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="605ca-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="605ca-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="605ca-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="605ca-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="605ca-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="605ca-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="605ca-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="605ca-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="605ca-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="605ca-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="605ca-110">Определяет, будет ли изображение согласовываться с фигурой.</span><span class="sxs-lookup"><span data-stu-id="605ca-110">Determines whether an image will align with a shape.</span></span> <span data-ttu-id="605ca-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="605ca-111">Read/write.</span></span> <span data-ttu-id="605ca-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="605ca-112">**VgTriState**.</span></span>

<span data-ttu-id="605ca-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="605ca-113">**Applies To**</span></span>

[<span data-ttu-id="605ca-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="605ca-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="605ca-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="605ca-115">**Tag Syntax**</span></span>

<span data-ttu-id="605ca-116"><v: *element* алигншапе = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="605ca-116"><v: *element* alignshape=" *expression* "></span></span>

<span data-ttu-id="605ca-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="605ca-117">**Script Syntax**</span></span>

<span data-ttu-id="605ca-118">*element* . алигншапе = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="605ca-118">*element* .alignshape="*expression*"</span></span>

<span data-ttu-id="605ca-119">*выражение* = *element*. алигншапе</span><span class="sxs-lookup"><span data-stu-id="605ca-119">*expression*=*element*.alignshape</span></span>

<span data-ttu-id="605ca-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="605ca-120">**Remarks**</span></span>

<span data-ttu-id="605ca-121">Если **значение — true**, изображение, используемое для создания заливки, будет согласовываться с фигурой.</span><span class="sxs-lookup"><span data-stu-id="605ca-121">If **True**, the image used to create the fill is aligned with the shape.</span></span> <span data-ttu-id="605ca-122">Если задано **значение false**, то изображение, используемое для создания заливки, будет согласовываться с окном.</span><span class="sxs-lookup"><span data-stu-id="605ca-122">If **False**, the image used to create the fill is aligned with the window.</span></span> <span data-ttu-id="605ca-123">Значение по умолчанию — **True**.</span><span class="sxs-lookup"><span data-stu-id="605ca-123">Default is **True**.</span></span>

<span data-ttu-id="605ca-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="605ca-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="605ca-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="605ca-125">**Example**</span></span>

<span data-ttu-id="605ca-126">Изображение мозаичной заливки, созданное из myimage.gif, согласуется с окном, а не с фигурой. Несмотря на то, что фигура поворачивается, изображение — нет.</span><span class="sxs-lookup"><span data-stu-id="605ca-126">The tiled fill image created from myimage.gif is aligned with the window, not the shape; even though the shape is rotated, the image is not.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 