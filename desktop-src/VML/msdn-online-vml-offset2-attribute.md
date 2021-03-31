---
title: Атрибут Offset2 VML
description: Атрибут Offset2 VML
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533437"
---
# <a name="vml-offset2-attribute"></a><span data-ttu-id="7d2fc-103">Атрибут Offset2 VML</span><span class="sxs-lookup"><span data-stu-id="7d2fc-103">VML Offset2 Attribute</span></span>

<span data-ttu-id="7d2fc-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7d2fc-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7d2fc-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7d2fc-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7d2fc-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7d2fc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7d2fc-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7d2fc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7d2fc-110">Определяет второе смещение.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-110">Determines a second offset.</span></span> <span data-ttu-id="7d2fc-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-111">Read/write.</span></span> <span data-ttu-id="7d2fc-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-112">**VgVector2D**.</span></span>

<span data-ttu-id="7d2fc-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="7d2fc-113">**Applies To**</span></span>

[<span data-ttu-id="7d2fc-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="7d2fc-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="7d2fc-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="7d2fc-115">**Tag Syntax**</span></span>

<span data-ttu-id="7d2fc-116"><v: *element* offset2 = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="7d2fc-116"><v: *element* offset2=" *expression* "></span></span>

<span data-ttu-id="7d2fc-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="7d2fc-117">**Script Syntax**</span></span>

<span data-ttu-id="7d2fc-118">*element* . offset2 = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="7d2fc-118">*element* .offset2="*expression*"</span></span>

<span data-ttu-id="7d2fc-119">*выражение* = *element*. offset2</span><span class="sxs-lookup"><span data-stu-id="7d2fc-119">*expression*=*element*.offset2</span></span>

<span data-ttu-id="7d2fc-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="7d2fc-120">**Remarks**</span></span>

<span data-ttu-id="7d2fc-121">Значение по умолчанию для второго смещения для значения x равно 0, а значение по умолчанию для значения y равно 0.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-121">The default for a second offset for the x value is 0 and the default for the y value is 0.</span></span> <span data-ttu-id="7d2fc-122">Значения — это либо абсолютное измерение, либо дробное значение Shape.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="7d2fc-123">Если дробная часть, значения находятся в диапазоне от 50% до-50%.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-123">If fractional, the values range from 50% to -50%.</span></span>

<span data-ttu-id="7d2fc-124">Используйте второе смещение для создания специальных эффектов тени.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-124">Use a second offset to create special shadow effects.</span></span> <span data-ttu-id="7d2fc-125">Дополнительные сведения о втором смещении см. в описании атрибута [Type](type-attribute--shadow--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="7d2fc-125">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second offsets.</span></span>

<span data-ttu-id="7d2fc-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="7d2fc-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="7d2fc-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="7d2fc-127">**Example**</span></span>

<span data-ttu-id="7d2fc-128">Для фигуры создается двойная тень.</span><span class="sxs-lookup"><span data-stu-id="7d2fc-128">A double shadow is created for the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 