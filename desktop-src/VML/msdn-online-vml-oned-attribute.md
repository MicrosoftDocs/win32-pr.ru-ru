---
title: Атрибут Онед VML
description: Атрибут Онед VML
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339017"
---
# <a name="vml-oned-attribute"></a><span data-ttu-id="6c140-103">Атрибут Онед VML</span><span class="sxs-lookup"><span data-stu-id="6c140-103">VML OnEd Attribute</span></span>

<span data-ttu-id="6c140-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6c140-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6c140-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6c140-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6c140-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6c140-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6c140-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c140-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6c140-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6c140-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6c140-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6c140-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6c140-110">Определяет, скрываются ли дополнительные дескрипторы фигуры.</span><span class="sxs-lookup"><span data-stu-id="6c140-110">Determines whether the extra handles of a shape are hidden.</span></span> <span data-ttu-id="6c140-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6c140-111">Read/write.</span></span> <span data-ttu-id="6c140-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="6c140-112">**VgTriState**.</span></span>

<span data-ttu-id="6c140-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6c140-113">**Applies To**</span></span>

[<span data-ttu-id="6c140-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="6c140-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="6c140-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6c140-115">**Tag Syntax**</span></span>

<span data-ttu-id="6c140-116"><v: *element* о:онед = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="6c140-116"><v: *element* o:oned=" *expression* "></span></span>

<span data-ttu-id="6c140-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6c140-117">**Remarks**</span></span>

<span data-ttu-id="6c140-118">Скрывает все маркеры фигур, кроме левого верхнего и нижнего правого. то есть те же маркеры, которые используются для сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="6c140-118">Hides all shape handles except the top left and bottom right; that is, the same handles that are used for a straight line segment.</span></span> <span data-ttu-id="6c140-119">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="6c140-119">The default is **False**.</span></span>

<span data-ttu-id="6c140-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="6c140-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="6c140-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="6c140-121">**Example**</span></span>

<span data-ttu-id="6c140-122">Все маркеры фигуры, кроме верхнего левого и нижнего правого угла, скрыты.</span><span class="sxs-lookup"><span data-stu-id="6c140-122">All but the top left and bottom right handles of the shape are hidden.</span></span>


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 