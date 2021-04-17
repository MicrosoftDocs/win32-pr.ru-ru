---
title: Атрибут VML MSO-Wrap-Distance-Top
description: Атрибут VML MSO-Wrap-Distance-Top
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a16898733ead7bf3728d8f520888c8a05ef5fe6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691571"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a><span data-ttu-id="9a53c-103">Атрибут VML MSO-Wrap-Distance-Top</span><span class="sxs-lookup"><span data-stu-id="9a53c-103">VML MSO-Wrap-Distance-Top Attribute</span></span>

<span data-ttu-id="9a53c-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9a53c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9a53c-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="9a53c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9a53c-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="9a53c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9a53c-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9a53c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9a53c-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9a53c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9a53c-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9a53c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9a53c-110">Определяет расстояние от фигуры до текста, вокруг которого производится оболочка.</span><span class="sxs-lookup"><span data-stu-id="9a53c-110">Defines the distance from the shape top to the text that wraps around it.</span></span> <span data-ttu-id="9a53c-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="9a53c-111">Read/write.</span></span> <span data-ttu-id="9a53c-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="9a53c-112">**String**.</span></span>

<span data-ttu-id="9a53c-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="9a53c-113">**Applies To**</span></span>

[<span data-ttu-id="9a53c-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="9a53c-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="9a53c-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="9a53c-115">**Tag Syntax**</span></span>

<span data-ttu-id="9a53c-116"><v: Style *элемента* = "MSO-Wrap-Distance-Top: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="9a53c-116"><v: *element* style="mso-wrap-distance-top: *expression* "></span></span>

<span data-ttu-id="9a53c-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="9a53c-117">**Remarks**</span></span>

<span data-ttu-id="9a53c-118">Обратите внимание, что этот атрибут отличается от атрибута **поля** CSS.</span><span class="sxs-lookup"><span data-stu-id="9a53c-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="9a53c-119">**Поле** изменяет источник фигуры, чтобы включить в него области полей, но расстояние по обтекания в Microsoft Office не изменяет происхождение фигуры.</span><span class="sxs-lookup"><span data-stu-id="9a53c-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="9a53c-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="9a53c-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="9a53c-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="9a53c-121">**Example**</span></span>

<span data-ttu-id="9a53c-122">Фигура имеет верхнее заданное расстояние в 10 пунктов.</span><span class="sxs-lookup"><span data-stu-id="9a53c-122">The shape has a top wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 