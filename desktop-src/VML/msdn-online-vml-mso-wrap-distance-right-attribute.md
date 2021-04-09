---
title: Атрибут VML MSO-Wrap-Distance-right
description: Атрибут VML MSO-Wrap-Distance-right
ms.assetid: 2f0ec7a3-036e-4f45-a330-f8ddccb75791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf38fc62812b0ce300e4d18067a0f2497233f2e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890784"
---
# <a name="vml-mso-wrap-distance-right-attribute"></a><span data-ttu-id="181af-103">Атрибут VML MSO-Wrap-Distance-right</span><span class="sxs-lookup"><span data-stu-id="181af-103">VML MSO-Wrap-Distance-Right Attribute</span></span>

<span data-ttu-id="181af-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="181af-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="181af-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="181af-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="181af-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="181af-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="181af-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="181af-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="181af-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="181af-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="181af-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="181af-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="181af-110">Определяет расстояние от правой стороны фигуры до текста, который обтекает вокруг него.</span><span class="sxs-lookup"><span data-stu-id="181af-110">Defines the distance from the right side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="181af-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="181af-111">Read/write.</span></span> <span data-ttu-id="181af-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="181af-112">**String**.</span></span>

<span data-ttu-id="181af-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="181af-113">**Applies To**</span></span>

[<span data-ttu-id="181af-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="181af-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="181af-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="181af-115">**Tag Syntax**</span></span>

<span data-ttu-id="181af-116"><v: Style *элемента* = "MSO-Wrap-Distance-Right: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="181af-116"><v: *element* style="mso-wrap-distance-right: *expression* "></span></span>

<span data-ttu-id="181af-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="181af-117">**Remarks**</span></span>

<span data-ttu-id="181af-118">Обратите внимание, что этот атрибут отличается от атрибута **поля** CSS.</span><span class="sxs-lookup"><span data-stu-id="181af-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="181af-119">**Поле** изменяет источник фигуры, чтобы включить в него области полей, но расстояние по обтекания в Microsoft Office не изменяет происхождение фигуры.</span><span class="sxs-lookup"><span data-stu-id="181af-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="181af-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="181af-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="181af-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="181af-121">**Example**</span></span>

<span data-ttu-id="181af-122">Фигура имеет право на перенос в 10 пунктов.</span><span class="sxs-lookup"><span data-stu-id="181af-122">The shape has a right wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-right:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 