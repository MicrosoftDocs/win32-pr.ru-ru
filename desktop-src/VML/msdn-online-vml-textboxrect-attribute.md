---
title: Атрибут Текстбоксрект VML
description: Атрибут Текстбоксрект VML
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070072"
---
# <a name="vml-textboxrect-attribute"></a><span data-ttu-id="c1bd0-103">Атрибут Текстбоксрект VML</span><span class="sxs-lookup"><span data-stu-id="c1bd0-103">VML TextBoxRect Attribute</span></span>

<span data-ttu-id="c1bd0-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c1bd0-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c1bd0-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c1bd0-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c1bd0-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c1bd0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c1bd0-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c1bd0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c1bd0-110">Определяет одно или несколько текстовых полей внутри фигуры.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-110">Defines one or more text boxes inside a shape.</span></span> <span data-ttu-id="c1bd0-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-111">Read/write.</span></span> <span data-ttu-id="c1bd0-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-112">**String**.</span></span>

<span data-ttu-id="c1bd0-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c1bd0-113">**Applies To**</span></span>

[<span data-ttu-id="c1bd0-114">Путь</span><span class="sxs-lookup"><span data-stu-id="c1bd0-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="c1bd0-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c1bd0-115">**Tag Syntax**</span></span>

<span data-ttu-id="c1bd0-116"><v: *element* текстбоксрект = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c1bd0-116"><v: *element* textboxrect=" *expression* "></span></span>

<span data-ttu-id="c1bd0-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c1bd0-117">**Script Syntax**</span></span>

<span data-ttu-id="c1bd0-118">*element* . текстбоксрект = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c1bd0-118">*element* .textboxrect="*expression*"</span></span>

<span data-ttu-id="c1bd0-119">*выражение* = *element*. текстбоксрект</span><span class="sxs-lookup"><span data-stu-id="c1bd0-119">*expression*=*element*.textboxrect</span></span>

<span data-ttu-id="c1bd0-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c1bd0-120">**Remarks**</span></span>

<span data-ttu-id="c1bd0-121">Текстовое поле определяется одним или несколькими наборами чисел, которые указывают (по порядку) левую, верхнюю, правую и нижнюю точки прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-121">A textbox is defined by one or more sets of numbers specifying (in order) the left, top, right, and bottom points of the rectangle.</span></span> <span data-ttu-id="c1bd0-122">Несколько наборов разделяются точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-122">Multiple sets are delimited by a semicolon.</span></span> <span data-ttu-id="c1bd0-123">Значением по умолчанию является то же значение измерения, что и содержащий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-123">The default value is the same dimension value as the containing rectangle.</span></span> <span data-ttu-id="c1bd0-124">Если определено более одного текстового поля, разделенные запятыми наборы, определяющие каждое текстовое поле, разделяются точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-124">If more than one textbox is defined, the comma-delimited quadruple sets that define each textbox are separated by semicolons.</span></span> <span data-ttu-id="c1bd0-125">Обычно текстовые поля поступают в виде наборов из 1, 2, 3 или 6 прямоугольников на фигуре.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-125">Normally textboxes come in sets of 1, 2, 3, or 6 rectangles on a shape.</span></span>

<span data-ttu-id="c1bd0-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="c1bd0-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="c1bd0-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c1bd0-127">**Example**</span></span>

<span data-ttu-id="c1bd0-128">В левом верхнем углу фигуры определяется и помещается 5 единиц в поле с 95 единиц на 95 единиц.</span><span class="sxs-lookup"><span data-stu-id="c1bd0-128">A textbox of 95 units by 95 units is defined and placed 5 units inside the top left corner of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 