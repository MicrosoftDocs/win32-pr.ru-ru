---
title: Атрибут Билевел VML
description: Атрибут Билевел VML
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792384"
---
# <a name="vml-bilevel-attribute"></a><span data-ttu-id="ada04-103">Атрибут Билевел VML</span><span class="sxs-lookup"><span data-stu-id="ada04-103">VML Bilevel Attribute</span></span>

<span data-ttu-id="ada04-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ada04-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ada04-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ada04-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ada04-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ada04-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ada04-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ada04-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ada04-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ada04-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ada04-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ada04-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ada04-110">Определяет, будет ли изображение отображаться черно-белым цветом.</span><span class="sxs-lookup"><span data-stu-id="ada04-110">Determines whether an image will be displayed in black and white.</span></span> <span data-ttu-id="ada04-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ada04-111">Read/write.</span></span> <span data-ttu-id="ada04-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="ada04-112">**VgTriState**.</span></span>

<span data-ttu-id="ada04-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ada04-113">**Applies To**</span></span>

[<span data-ttu-id="ada04-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="ada04-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="ada04-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ada04-115">**Tag Syntax**</span></span>

<span data-ttu-id="ada04-116"><v: *element* билевел = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ada04-116"><v: *element* bilevel=" *expression* "></span></span>

<span data-ttu-id="ada04-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ada04-117">**Script Syntax**</span></span>

<span data-ttu-id="ada04-118">*element* . билевел = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ada04-118">*element* .bilevel="*expression*"</span></span>

<span data-ttu-id="ada04-119">*выражение* = *element*. билевел</span><span class="sxs-lookup"><span data-stu-id="ada04-119">*expression*=*element*.bilevel</span></span>

<span data-ttu-id="ada04-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ada04-120">**Remarks**</span></span>

<span data-ttu-id="ada04-121">Если **значение — true**, изображение будет отображаться с использованием двух цветов (черный и белый).</span><span class="sxs-lookup"><span data-stu-id="ada04-121">If **True**, the image will be displayed using two colors (black and white).</span></span> <span data-ttu-id="ada04-122">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="ada04-122">The default is **False**.</span></span> <span data-ttu-id="ada04-123">При этом создается результат, аналогичный афише.</span><span class="sxs-lookup"><span data-stu-id="ada04-123">This creates an effect similar to posterization.</span></span>

<span data-ttu-id="ada04-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="ada04-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ada04-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ada04-125">**Example**</span></span>

<span data-ttu-id="ada04-126">Изображение будет отображаться только в черно-белом режиме.</span><span class="sxs-lookup"><span data-stu-id="ada04-126">The image will be displayed in black and white only.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 