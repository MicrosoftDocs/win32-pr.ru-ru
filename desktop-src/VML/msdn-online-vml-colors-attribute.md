---
title: Атрибут Colors VML
description: Атрибут Colors VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533350"
---
# <a name="vml-colors-attribute"></a><span data-ttu-id="6b2c4-103">Атрибут Colors VML</span><span class="sxs-lookup"><span data-stu-id="6b2c4-103">VML Colors Attribute</span></span>

<span data-ttu-id="6b2c4-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6b2c4-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6b2c4-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6b2c4-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6b2c4-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6b2c4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6b2c4-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6b2c4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6b2c4-110">Определяет несколько цветов для градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-110">Defines multiple colors for a gradient fill.</span></span> <span data-ttu-id="6b2c4-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-111">Read/write.</span></span> <span data-ttu-id="6b2c4-112">**Ивгградиентколораррай**.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-112">**IVgGradientColorArray**.</span></span>

<span data-ttu-id="6b2c4-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6b2c4-113">**Applies To**</span></span>

[<span data-ttu-id="6b2c4-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="6b2c4-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="6b2c4-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6b2c4-115">**Tag Syntax**</span></span>

<span data-ttu-id="6b2c4-116"><v: Colors *Elements* = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="6b2c4-116"><v: *element* colors=" *expression* "></span></span>

<span data-ttu-id="6b2c4-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="6b2c4-117">**Script Syntax**</span></span>

<span data-ttu-id="6b2c4-118">*element* . Colors = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="6b2c4-118">*element* .colors="*expression*"</span></span>

<span data-ttu-id="6b2c4-119">*выражение* = *element*. Colors</span><span class="sxs-lookup"><span data-stu-id="6b2c4-119">*expression*=*element*.colors</span></span>

<span data-ttu-id="6b2c4-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6b2c4-120">**Remarks**</span></span>

<span data-ttu-id="6b2c4-121">Используется для определения массива, состоящего из парных значений процентов ([вгфрактион](msdn-online-vml-vgfraction-data-type.md)) и Color ([вгколор](msdn-online-vml-ivgcolor.md)).</span><span class="sxs-lookup"><span data-stu-id="6b2c4-121">Used to define an array consisting of paired values of percentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) and color ([VgColor](msdn-online-vml-ivgcolor.md)).</span></span> <span data-ttu-id="6b2c4-122">Массив создает наложенную заливку с использованием каждой точки в массиве, начиная с 0% (определяется **цветом**) и заканчивая 100% (определяется с помощью **color2**).</span><span class="sxs-lookup"><span data-stu-id="6b2c4-122">The array creates a blended fill using each point in the array, starting at 0% (defined by **Color**) and ending at 100% (defined by **Color2**).</span></span> <span data-ttu-id="6b2c4-123">Промежуточные цвета, определяемые способом, можно определить, назначив значение цвета в процентах.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-123">Intermediate colors along the way can be defined by assigning a color value to a percentage.</span></span> <span data-ttu-id="6b2c4-124">Пара "процент и цвет" отделяется запятой, но пары разделяются друг от друга запятыми.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-124">The percent and color pair are not separated by a comma, but pairs are separated from each other by commas.</span></span>

<span data-ttu-id="6b2c4-125">Стандартный атрибут VML</span><span class="sxs-lookup"><span data-stu-id="6b2c4-125">VML Standard Attribute</span></span>

<span data-ttu-id="6b2c4-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="6b2c4-126">**Example**</span></span>

<span data-ttu-id="6b2c4-127">Фигура имеет градиентную заливку, состоящую из четырех цветов, начинающихся с красного цвета, смешения к желтому, зеленому и финаллиблуе.</span><span class="sxs-lookup"><span data-stu-id="6b2c4-127">The shape has a gradient fill consisting of four colors, starting with red, blending to yellow, then green, and finallyblue.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 