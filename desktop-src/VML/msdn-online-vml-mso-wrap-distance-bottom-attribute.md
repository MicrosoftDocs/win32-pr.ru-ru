---
title: Атрибут VML MSO-Wrap-Distance-Bottom
description: Атрибут VML MSO-Wrap-Distance-Bottom
ms.assetid: b096fc67-dd99-4833-bb82-73de7b06f43c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c3ec66ae23994184227d857e269318606d9ea4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987670"
---
# <a name="vml-mso-wrap-distance-bottom-attribute"></a><span data-ttu-id="27406-103">Атрибут VML MSO-Wrap-Distance-Bottom</span><span class="sxs-lookup"><span data-stu-id="27406-103">VML MSO-Wrap-Distance-Bottom Attribute</span></span>

<span data-ttu-id="27406-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="27406-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="27406-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="27406-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="27406-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="27406-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="27406-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="27406-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="27406-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="27406-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="27406-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="27406-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="27406-110">Определяет расстояние от нижней стороны фигуры до текста, который обтекает вокруг него.</span><span class="sxs-lookup"><span data-stu-id="27406-110">Defines the distance from the bottom side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="27406-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="27406-111">Read/write.</span></span> <span data-ttu-id="27406-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="27406-112">**String**.</span></span>

<span data-ttu-id="27406-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="27406-113">**Applies To**</span></span>

[<span data-ttu-id="27406-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="27406-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="27406-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="27406-115">**Tag Syntax**</span></span>

<span data-ttu-id="27406-116"><v: Style *элемента* = "MSO-Wrap-Distance-Bottom: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="27406-116"><v: *element* style="mso-wrap-distance-bottom: *expression* "></span></span>

<span data-ttu-id="27406-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="27406-117">**Remarks**</span></span>

<span data-ttu-id="27406-118">Обратите внимание, что этот атрибут отличается от атрибута **поля** CSS.</span><span class="sxs-lookup"><span data-stu-id="27406-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="27406-119">**Поле** изменяет источник фигуры, добавляя области полей, но расстояние по переносу в Microsoft Office не изменяет происхождение фигуры.</span><span class="sxs-lookup"><span data-stu-id="27406-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="27406-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="27406-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="27406-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="27406-121">**Example**</span></span>

<span data-ttu-id="27406-122">Фигура имеет нижнюю границу обтекания в 10 пунктов.</span><span class="sxs-lookup"><span data-stu-id="27406-122">The shape has a bottom wrap distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-bottom:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 