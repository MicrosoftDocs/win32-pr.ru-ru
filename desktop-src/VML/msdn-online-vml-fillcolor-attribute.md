---
title: Атрибут VML FillColor
description: Атрибут VML FillColor
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691654"
---
# <a name="vml-fillcolor-attribute"></a><span data-ttu-id="4a412-103">Атрибут VML FillColor</span><span class="sxs-lookup"><span data-stu-id="4a412-103">VML FillColor Attribute</span></span>

<span data-ttu-id="4a412-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4a412-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4a412-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="4a412-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4a412-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="4a412-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4a412-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4a412-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4a412-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4a412-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4a412-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4a412-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4a412-110">Определяет цвет кисти, которая заполняет замкнутый контур фигуры.</span><span class="sxs-lookup"><span data-stu-id="4a412-110">Defines the brush color that fills the closed path of a shape.</span></span> <span data-ttu-id="4a412-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="4a412-111">Read/write.</span></span> <span data-ttu-id="4a412-112">[Ивгколор](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="4a412-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="4a412-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="4a412-113">**Applies To**</span></span>

[<span data-ttu-id="4a412-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="4a412-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="4a412-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="4a412-115">**Tag Syntax**</span></span>

<span data-ttu-id="4a412-116"><v: *element* FillColor = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="4a412-116"><v: *element* fillcolor=" *expression* "></span></span>

<span data-ttu-id="4a412-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="4a412-117">**Script Syntax**</span></span>

<span data-ttu-id="4a412-118">*element* . FillColor = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="4a412-118">*element* .fillcolor="*expression*"</span></span>

<span data-ttu-id="4a412-119">*выражение* = *элемент*. FillColor</span><span class="sxs-lookup"><span data-stu-id="4a412-119">*expression*=*element*.fillcolor</span></span>

<span data-ttu-id="4a412-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="4a412-120">**Remarks**</span></span>

<span data-ttu-id="4a412-121">Значение **FillColor** дублируется из атрибута **Color** элемента **Fill** .</span><span class="sxs-lookup"><span data-stu-id="4a412-121">The **FillColor** value is duplicated from the **Color** attribute of the **Fill** element.</span></span>

<span data-ttu-id="4a412-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="4a412-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="4a412-123">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="4a412-123">**See Also**</span></span>

<span data-ttu-id="4a412-124">[Форма](shape-element--vml.md), [Заливка](msdn-online-vml-fill-element.md), [ивгколор](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="4a412-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span></span>

<span data-ttu-id="4a412-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="4a412-125">**Example**</span></span>

<span data-ttu-id="4a412-126">Цвет заливки прямоугольника — красный.</span><span class="sxs-lookup"><span data-stu-id="4a412-126">The fill color of the rectangle is red.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="4a412-127">[Пример атрибута FillColor](/previous-versions/bb229668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4a412-127">[FillColor Attribute Example](/previous-versions/bb229668(v=vs.85)).</span></span> <span data-ttu-id="4a412-128">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="4a412-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 