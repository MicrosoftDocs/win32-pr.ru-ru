---
title: Атрибут Angle (Заливка) (VML)
description: Атрибут Angle (Заливка) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070532"
---
# <a name="angle-attribute-fillvml"></a><span data-ttu-id="bcce2-103">Атрибут Angle (Заливка) (VML)</span><span class="sxs-lookup"><span data-stu-id="bcce2-103">Angle Attribute (Fill)(VML)</span></span>

<span data-ttu-id="bcce2-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bcce2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bcce2-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="bcce2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bcce2-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="bcce2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bcce2-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bcce2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bcce2-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bcce2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bcce2-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bcce2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bcce2-110">Определяет угол градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="bcce2-110">Defines the angle of a gradient fill.</span></span> <span data-ttu-id="bcce2-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="bcce2-111">Read/write.</span></span> <span data-ttu-id="bcce2-112">[Вгангле](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="bcce2-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="bcce2-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="bcce2-113">**Applies To**</span></span>

[<span data-ttu-id="bcce2-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="bcce2-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="bcce2-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="bcce2-115">**Tag Syntax**</span></span>

<span data-ttu-id="bcce2-116"><v: Angle *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="bcce2-116"><v: *element* angle=" *expression* "></span></span>

<span data-ttu-id="bcce2-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="bcce2-117">**Script Syntax**</span></span>

<span data-ttu-id="bcce2-118">*element* . Angle = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="bcce2-118">*element* .angle="*expression*"</span></span>

<span data-ttu-id="bcce2-119">*выражение* = *элемент*. угол</span><span class="sxs-lookup"><span data-stu-id="bcce2-119">*expression*=*element*.angle</span></span>

<span data-ttu-id="bcce2-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="bcce2-120">**Remarks**</span></span>

<span data-ttu-id="bcce2-121">Вектор градиента перпендикулярен вектору направления смешения от одного цвета к другому.</span><span class="sxs-lookup"><span data-stu-id="bcce2-121">The vector of a gradient is perpendicular to the vector of the blend direction from one color to another.</span></span> <span data-ttu-id="bcce2-122">Значение по умолчанию — 0 (нуль) градусов, то есть горизонтальный вектор слева направо.</span><span class="sxs-lookup"><span data-stu-id="bcce2-122">The default value is 0 (zero) degrees, which is a horizontal vector from left to right.</span></span> <span data-ttu-id="bcce2-123">Положительные углы поворачивают градиент в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="bcce2-123">Positive angles rotate the gradient in a counter-clockwise direction.</span></span>

<span data-ttu-id="bcce2-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="bcce2-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="bcce2-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="bcce2-125">**Example**</span></span>

<span data-ttu-id="bcce2-126">Заливка фигуры состоит из градиента двух цветов: от синего к красному по углу 45 градусов.</span><span class="sxs-lookup"><span data-stu-id="bcce2-126">The fill of the shape is composed of a gradient of two colors, running from blue to red at an angle of 45 degrees.</span></span> <span data-ttu-id="bcce2-127">Красный будет находиться в левом верхнем углу, а синий — в нижнем правом углу.</span><span class="sxs-lookup"><span data-stu-id="bcce2-127">Red will be in the top left corner and blue will be in the bottom right corner.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 