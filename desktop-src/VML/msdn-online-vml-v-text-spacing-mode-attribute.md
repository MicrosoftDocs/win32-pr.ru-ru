---
title: Атрибут "режим пробельного текста" VML V
description: Атрибут "режим пробельного текста" VML V
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488248"
---
# <a name="vml-v-text-spacing-mode-attribute"></a><span data-ttu-id="c984f-103">Атрибут "режим пробельного текста" VML V</span><span class="sxs-lookup"><span data-stu-id="c984f-103">VML V-Text-Spacing-Mode Attribute</span></span>

<span data-ttu-id="c984f-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c984f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c984f-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c984f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c984f-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c984f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c984f-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c984f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c984f-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c984f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c984f-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c984f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c984f-110">Определяет режим для леттерспаЦинг.</span><span class="sxs-lookup"><span data-stu-id="c984f-110">Defines the mode for letterspacing.</span></span> <span data-ttu-id="c984f-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c984f-111">Read/write.</span></span> <span data-ttu-id="c984f-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="c984f-112">**String**.</span></span>

<span data-ttu-id="c984f-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c984f-113">**Applies To**</span></span>

[<span data-ttu-id="c984f-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="c984f-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="c984f-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c984f-115">**Tag Syntax**</span></span>

<span data-ttu-id="c984f-116"><v: Style *элемента* = "v-Text-просвет-Mode: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c984f-116"><v: *element* style="v-text-spacing-mode: *expression* "></span></span>

<span data-ttu-id="c984f-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c984f-117">**Script Syntax**</span></span>

<span data-ttu-id="c984f-118">*element* . Style. v-Text-просвет-Mode = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c984f-118">*element* .style.v-text-spacing-mode="*expression*"</span></span>

<span data-ttu-id="c984f-119">*выражение* = Text. Style. v-режим пробельных текстовых *элементов*</span><span class="sxs-lookup"><span data-stu-id="c984f-119">*expression*=*element*.style.v-text-spacing-mode</span></span>

<span data-ttu-id="c984f-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c984f-120">**Remarks**</span></span>

<span data-ttu-id="c984f-121">Значения включают</span><span class="sxs-lookup"><span data-stu-id="c984f-121">Values include</span></span>

-   <span data-ttu-id="c984f-122">**усиление** (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c984f-122">**tightening** (default)</span></span>
-   <span data-ttu-id="c984f-123">**отслеживающ**</span><span class="sxs-lookup"><span data-stu-id="c984f-123">**tracking**</span></span>

<span data-ttu-id="c984f-124">Этот атрибут определяет, будет ли удалено место между каждой буквой (с сужением) или добавляться между каждой буквой (отслеживание).</span><span class="sxs-lookup"><span data-stu-id="c984f-124">This attribute determines whether space will be removed between each letter (tightening) or added between each letter (tracking).</span></span> <span data-ttu-id="c984f-125">Объем леттерспаЦинг изменения определяется атрибутом « [интервалы по тексту](msdn-online-vml-v-text-spacing-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="c984f-125">The amount of letterspacing change is defined by the [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) attribute.</span></span>

<span data-ttu-id="c984f-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="c984f-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="c984f-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c984f-127">**Example**</span></span>

<span data-ttu-id="c984f-128">ЛеттерспаЦинг между каждой буквой увеличивается на 200 единиц.</span><span class="sxs-lookup"><span data-stu-id="c984f-128">The letterspacing between each letter is increased by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 