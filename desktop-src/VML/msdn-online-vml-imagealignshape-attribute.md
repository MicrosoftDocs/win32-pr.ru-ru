---
title: Атрибут Имажеалигншапе VML
description: Атрибут Имажеалигншапе VML
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82aaab9c4c470b41bcf9fdb96ee2c048a7d0b81d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338121"
---
# <a name="vml-imagealignshape-attribute"></a><span data-ttu-id="695c4-103">Атрибут Имажеалигншапе VML</span><span class="sxs-lookup"><span data-stu-id="695c4-103">VML ImageAlignShape Attribute</span></span>

<span data-ttu-id="695c4-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="695c4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="695c4-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="695c4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="695c4-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="695c4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="695c4-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="695c4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="695c4-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="695c4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="695c4-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="695c4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="695c4-110">Определяет выравнивание изображения обводки.</span><span class="sxs-lookup"><span data-stu-id="695c4-110">Determines the alignment of the stroke image.</span></span> <span data-ttu-id="695c4-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="695c4-111">Read/write.</span></span> <span data-ttu-id="695c4-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="695c4-112">**VgTriState**.</span></span>

<span data-ttu-id="695c4-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="695c4-113">**Applies To**</span></span>

[<span data-ttu-id="695c4-114">Водок</span><span class="sxs-lookup"><span data-stu-id="695c4-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="695c4-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="695c4-115">**Tag Syntax**</span></span>

<span data-ttu-id="695c4-116"><v:</span><span class="sxs-lookup"><span data-stu-id="695c4-116"><v:</span></span>

<span data-ttu-id="695c4-117">element *имажеалигншапе = "* выражение *" >*</span><span class="sxs-lookup"><span data-stu-id="695c4-117">element *imagealignshape="* expression *">*</span></span>

<span data-ttu-id="695c4-118">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="695c4-118">**Script Syntax**</span></span>

<span data-ttu-id="695c4-119">element *. имажеалигншапе = "* выражение *"*</span><span class="sxs-lookup"><span data-stu-id="695c4-119">element *.imagealignshape="* expression *"*</span></span>

<span data-ttu-id="695c4-120">*=* элемент Expression *. имажеалигншапе*</span><span class="sxs-lookup"><span data-stu-id="695c4-120">expression *=* element *.imagealignshape*</span></span>

<span data-ttu-id="695c4-121">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="695c4-121">**Remarks**</span></span>

<span data-ttu-id="695c4-122">Если **значение равно true**, выровняйте изображение с фигурой, в противном случае выровняйте изображение с помощью окна.</span><span class="sxs-lookup"><span data-stu-id="695c4-122">If **True**, align the image with the shape, else align the image with the window.</span></span> <span data-ttu-id="695c4-123">Значение по умолчанию равно **True**.</span><span class="sxs-lookup"><span data-stu-id="695c4-123">The default is **True**.</span></span>

<span data-ttu-id="695c4-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="695c4-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="695c4-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="695c4-125">**Example**</span></span>

<span data-ttu-id="695c4-126">Изображение будет согласовано с окном.</span><span class="sxs-lookup"><span data-stu-id="695c4-126">The image is aligned with the window.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 