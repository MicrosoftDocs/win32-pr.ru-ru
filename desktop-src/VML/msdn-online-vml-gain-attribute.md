---
title: Атрибут усиления VML
description: Атрибут усиления VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413316"
---
# <a name="vml-gain-attribute"></a><span data-ttu-id="c155a-103">Атрибут усиления VML</span><span class="sxs-lookup"><span data-stu-id="c155a-103">VML Gain Attribute</span></span>

<span data-ttu-id="c155a-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c155a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c155a-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c155a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c155a-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c155a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c155a-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c155a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c155a-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c155a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c155a-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c155a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c155a-110">Определяет интенсивность всех цветов в изображении.</span><span class="sxs-lookup"><span data-stu-id="c155a-110">Defines the intensity of all colors in an image.</span></span> <span data-ttu-id="c155a-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c155a-111">Read/write.</span></span> <span data-ttu-id="c155a-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="c155a-112">**VgNumber**.</span></span>

<span data-ttu-id="c155a-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c155a-113">**Applies To**</span></span>

[<span data-ttu-id="c155a-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="c155a-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="c155a-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c155a-115">**Tag Syntax**</span></span>

<span data-ttu-id="c155a-116"><v: *element* прибыль = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c155a-116"><v: *element* gain=" *expression* "></span></span>

<span data-ttu-id="c155a-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c155a-117">**Script Syntax**</span></span>

<span data-ttu-id="c155a-118">*element* . прибыль = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c155a-118">*element* .gain="*expression*"</span></span>

<span data-ttu-id="c155a-119">*выражение* = *element*. выигрыш</span><span class="sxs-lookup"><span data-stu-id="c155a-119">*expression*=*element*.gain</span></span>

<span data-ttu-id="c155a-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c155a-120">**Remarks**</span></span>

<span data-ttu-id="c155a-121">Этот атрибут определяет степень яркости белого цвета, влияя на все остальные цвета.</span><span class="sxs-lookup"><span data-stu-id="c155a-121">This attribute defines how bright the color white is, affecting all other colors.</span></span> <span data-ttu-id="c155a-122">Диапазон значений — от 0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="c155a-122">Values range from 0 to infinity.</span></span> <span data-ttu-id="c155a-123">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="c155a-123">The default value is 1.0.</span></span> <span data-ttu-id="c155a-124">Значение 0 показывает отсутствие изображения.</span><span class="sxs-lookup"><span data-stu-id="c155a-124">A value of 0 displays no image.</span></span> <span data-ttu-id="c155a-125">Значения, превышающие 1, доменяют изображение, а значения меньше 1 делают изображение серым.</span><span class="sxs-lookup"><span data-stu-id="c155a-125">Values greater than 1 lighten the picture and values less than 1 make the picture seem grayer.</span></span>

<span data-ttu-id="c155a-126">Этот атрибут можно использовать для создания интересных эффектов.</span><span class="sxs-lookup"><span data-stu-id="c155a-126">This attribute can be used to create interesting effects.</span></span>

<span data-ttu-id="c155a-127">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="c155a-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="c155a-128">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c155a-128">**Example**</span></span>

<span data-ttu-id="c155a-129">Изображение будет отображаться со всеми цветами, которые будут относиться к серому.</span><span class="sxs-lookup"><span data-stu-id="c155a-129">The image will be displayed with all the colors tending toward gray.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 