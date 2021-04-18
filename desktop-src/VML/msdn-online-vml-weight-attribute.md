---
title: Атрибут веса VML
description: Атрибут веса VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691559"
---
# <a name="vml-weight-attribute"></a><span data-ttu-id="8f030-103">Атрибут веса VML</span><span class="sxs-lookup"><span data-stu-id="8f030-103">VML Weight Attribute</span></span>

<span data-ttu-id="8f030-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8f030-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8f030-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="8f030-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8f030-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="8f030-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8f030-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f030-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8f030-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8f030-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8f030-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8f030-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8f030-110">Определяет толщину штриха.</span><span class="sxs-lookup"><span data-stu-id="8f030-110">Defines the thickness of a stroke.</span></span> <span data-ttu-id="8f030-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="8f030-111">Read/write.</span></span> <span data-ttu-id="8f030-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="8f030-112">**String**.</span></span>

<span data-ttu-id="8f030-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="8f030-113">**Applies To**</span></span>

[<span data-ttu-id="8f030-114">Водок</span><span class="sxs-lookup"><span data-stu-id="8f030-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="8f030-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="8f030-115">**Tag Syntax**</span></span>

<span data-ttu-id="8f030-116"><v: вес *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="8f030-116"><v: *element* weight=" *expression* "></span></span>

<span data-ttu-id="8f030-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="8f030-117">**Script Syntax**</span></span>

<span data-ttu-id="8f030-118">*element* . Weight = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="8f030-118">*element* .weight="*expression*"</span></span>

<span data-ttu-id="8f030-119">*выражение* = *элемент*. вес</span><span class="sxs-lookup"><span data-stu-id="8f030-119">*expression*=*element*.weight</span></span>

<span data-ttu-id="8f030-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="8f030-120">**Remarks**</span></span>

<span data-ttu-id="8f030-121">Этот атрибут совпадает с атрибутом **Строкевеигхт** **фигуры** и переопределяет его.</span><span class="sxs-lookup"><span data-stu-id="8f030-121">This attribute is the same as the **StrokeWeight** attribute of **Shape** and overrides it.</span></span> <span data-ttu-id="8f030-122">Значение по умолчанию — 1 точка.</span><span class="sxs-lookup"><span data-stu-id="8f030-122">The default value is 1 point.</span></span>

<span data-ttu-id="8f030-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="8f030-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8f030-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="8f030-124">**Example**</span></span>

<span data-ttu-id="8f030-125">Штрих имеет толщину 5 очков, а не 2 точки.</span><span class="sxs-lookup"><span data-stu-id="8f030-125">The stroke has a thickness of 5 points, not 2 points.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 