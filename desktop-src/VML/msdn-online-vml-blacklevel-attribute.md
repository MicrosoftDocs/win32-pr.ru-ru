---
title: Атрибут Блакклевел VML
description: Атрибут Блакклевел VML
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070215"
---
# <a name="vml-blacklevel-attribute"></a><span data-ttu-id="eda46-103">Атрибут Блакклевел VML</span><span class="sxs-lookup"><span data-stu-id="eda46-103">VML BlackLevel Attribute</span></span>

<span data-ttu-id="eda46-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="eda46-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eda46-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="eda46-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eda46-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="eda46-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eda46-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eda46-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eda46-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="eda46-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eda46-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="eda46-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eda46-110">Определяет интенсивность черного цвета в изображении.</span><span class="sxs-lookup"><span data-stu-id="eda46-110">Defines the intensity of black in an image.</span></span> <span data-ttu-id="eda46-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="eda46-111">Read/write.</span></span> <span data-ttu-id="eda46-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="eda46-112">**VgNumber**.</span></span>

<span data-ttu-id="eda46-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="eda46-113">**Applies To**</span></span>

[<span data-ttu-id="eda46-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="eda46-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="eda46-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="eda46-115">**Tag Syntax**</span></span>

<span data-ttu-id="eda46-116"><v: *element* блакклевел = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="eda46-116"><v: *element* blacklevel=" *expression* "></span></span>

<span data-ttu-id="eda46-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="eda46-117">**Script Syntax**</span></span>

<span data-ttu-id="eda46-118">*element* . блакклевел = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="eda46-118">*element* .blacklevel="*expression*"</span></span>

<span data-ttu-id="eda46-119">*выражение* = *element*. блакклевел</span><span class="sxs-lookup"><span data-stu-id="eda46-119">*expression*=*element*.blacklevel</span></span>

<span data-ttu-id="eda46-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="eda46-120">**Remarks**</span></span>

<span data-ttu-id="eda46-121">Позволяет изменить уровень цвета таким образом, чтобы черный цвет отображался как истинный черный, а все остальные цвета отображались как оттенки выше черного цвета.</span><span class="sxs-lookup"><span data-stu-id="eda46-121">Allows the color level to be modified so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span> <span data-ttu-id="eda46-122">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="eda46-122">The default value is 0.</span></span> <span data-ttu-id="eda46-123">Хотя разрешено любое число между положительной и отрицательной бесконечностью, значения меньше-0,5 будут отображаться как все черные, а значения больше 0,5 будут отображаться как все белые.</span><span class="sxs-lookup"><span data-stu-id="eda46-123">While any number between positive and negative infinity is permitted, values less than -0.5 will display as all black and values greater than 0.5 will display as all white.</span></span>

<span data-ttu-id="eda46-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="eda46-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="eda46-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="eda46-125">**Example**</span></span>

<span data-ttu-id="eda46-126">Изображение будет отображаться с очень темными тонами.</span><span class="sxs-lookup"><span data-stu-id="eda46-126">The image will be displayed with very dark tones.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 