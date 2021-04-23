---
title: Начальный атрибут (Fill) (VML)
description: Начальный атрибут (Fill) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413640"
---
# <a name="origin-attribute-fillvml"></a><span data-ttu-id="eb553-103">Начальный атрибут (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="eb553-103">Origin Attribute (Fill)(VML)</span></span>

<span data-ttu-id="eb553-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="eb553-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eb553-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="eb553-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eb553-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="eb553-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eb553-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb553-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eb553-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="eb553-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eb553-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="eb553-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eb553-110">Определяет центр изображения заливки.</span><span class="sxs-lookup"><span data-stu-id="eb553-110">Defines the center of a fill image.</span></span> <span data-ttu-id="eb553-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="eb553-111">Read/write.</span></span> <span data-ttu-id="eb553-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="eb553-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="eb553-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="eb553-113">**Applies To**</span></span>

[<span data-ttu-id="eb553-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="eb553-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="eb553-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="eb553-115">**Tag Syntax**</span></span>

<span data-ttu-id="eb553-116"><v: *элемент* Origin = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="eb553-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="eb553-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="eb553-117">**Script Syntax**</span></span>

<span data-ttu-id="eb553-118">*element* . Origin = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="eb553-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="eb553-119">*выражение* = *элемент*. Origin</span><span class="sxs-lookup"><span data-stu-id="eb553-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="eb553-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="eb553-120">**Remarks**</span></span>

<span data-ttu-id="eb553-121">Задает точку относительно верхнего левого угла изображения; Этот момент рассматривается как источник изображения.</span><span class="sxs-lookup"><span data-stu-id="eb553-121">Specifies a point relative to the upper left corner of the image; this point is treated as the origin of the image.</span></span> <span data-ttu-id="eb553-122">По умолчанию используется центр изображения.</span><span class="sxs-lookup"><span data-stu-id="eb553-122">Default is the center of the image.</span></span> <span data-ttu-id="eb553-123">Вектор представляет собой часть ширины и высоты изображения.</span><span class="sxs-lookup"><span data-stu-id="eb553-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="eb553-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="eb553-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="eb553-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="eb553-125">**Example**</span></span>

<span data-ttu-id="eb553-126">Изображение заливки смещается влево до точки 50% ширины фигуры.</span><span class="sxs-lookup"><span data-stu-id="eb553-126">The image of the fill is shifted left to a point 50% of the width of the shape .</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 