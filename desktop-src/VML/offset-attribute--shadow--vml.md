---
title: Атрибут Offset (тень) (VML)
description: Атрибут Offset (тень) (VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61daaf3b311a87a3e3bcf064ceffc491e1134fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987574"
---
# <a name="offset-attribute-shadowvml"></a><span data-ttu-id="26b49-103">Атрибут Offset (тень) (VML)</span><span class="sxs-lookup"><span data-stu-id="26b49-103">Offset Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="26b49-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="26b49-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="26b49-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="26b49-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="26b49-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="26b49-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="26b49-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26b49-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="26b49-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="26b49-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="26b49-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="26b49-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="26b49-110">Определяет, насколько далеко тень расширяется после фигуры.</span><span class="sxs-lookup"><span data-stu-id="26b49-110">Defines how far the shadow extends past the shape.</span></span> <span data-ttu-id="26b49-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="26b49-111">Read/write.</span></span> <span data-ttu-id="26b49-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="26b49-112">**VgVector2D**.</span></span>

<span data-ttu-id="26b49-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="26b49-113">**Applies To**</span></span>

[<span data-ttu-id="26b49-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="26b49-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="26b49-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="26b49-115">**Tag Syntax**</span></span>

<span data-ttu-id="26b49-116"><v: смещение *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="26b49-116"><v: *element* offset=" *expression* "></span></span>

<span data-ttu-id="26b49-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="26b49-117">**Script Syntax**</span></span>

<span data-ttu-id="26b49-118">*element* . offset = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="26b49-118">*element* .offset="*expression*"</span></span>

<span data-ttu-id="26b49-119">*выражение* = *элемент*. offset</span><span class="sxs-lookup"><span data-stu-id="26b49-119">*expression*=*element*.offset</span></span>

<span data-ttu-id="26b49-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="26b49-120">**Remarks**</span></span>

<span data-ttu-id="26b49-121">Смещение по умолчанию для значения x равно 2pt, а значение по умолчанию для значения y — 2PT.</span><span class="sxs-lookup"><span data-stu-id="26b49-121">The default offset for the x value is 2pt and the default for the y value is 2pt.</span></span> <span data-ttu-id="26b49-122">Значения — это либо абсолютное измерение, либо дробное значение Shape.</span><span class="sxs-lookup"><span data-stu-id="26b49-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="26b49-123">Если дробная часть, они находятся в диапазоне от 50% до-50%.</span><span class="sxs-lookup"><span data-stu-id="26b49-123">If fractional, they range from 50% to -50%.</span></span>

<span data-ttu-id="26b49-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="26b49-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="26b49-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="26b49-125">**Example**</span></span>

<span data-ttu-id="26b49-126">Фигура имеет тень со смещением 5 пунктов вниз и 10 точками вправо.</span><span class="sxs-lookup"><span data-stu-id="26b49-126">The shape has a shadow with an offset of 5 points down and 10 points to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 