---
title: Атрибут Лимо VML
description: Атрибут Лимо VML
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413025"
---
# <a name="vml-limo-attribute"></a><span data-ttu-id="8cc5e-103">Атрибут Лимо VML</span><span class="sxs-lookup"><span data-stu-id="8cc5e-103">VML Limo Attribute</span></span>

<span data-ttu-id="8cc5e-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8cc5e-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8cc5e-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8cc5e-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8cc5e-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8cc5e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8cc5e-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8cc5e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8cc5e-110">Определяет точку растяжения на пути.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-110">Defines a stretch point on the path.</span></span> <span data-ttu-id="8cc5e-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-111">Read/write.</span></span> <span data-ttu-id="8cc5e-112">**Vector2D**.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-112">**Vector2D**.</span></span>

<span data-ttu-id="8cc5e-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="8cc5e-113">**Applies To**</span></span>

[<span data-ttu-id="8cc5e-114">Путь</span><span class="sxs-lookup"><span data-stu-id="8cc5e-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="8cc5e-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="8cc5e-115">**Tag Syntax**</span></span>

<span data-ttu-id="8cc5e-116"><v: *element* Лимо = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="8cc5e-116"><v: *element* limo=" *expression* "></span></span>

<span data-ttu-id="8cc5e-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="8cc5e-117">**Script Syntax**</span></span>

<span data-ttu-id="8cc5e-118">*element* . Лимо = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="8cc5e-118">*element* .limo="*expression*"</span></span>

<span data-ttu-id="8cc5e-119">*выражение* = *element*. Лимо</span><span class="sxs-lookup"><span data-stu-id="8cc5e-119">*expression*=*element*.limo</span></span>

<span data-ttu-id="8cc5e-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="8cc5e-120">**Remarks**</span></span>

<span data-ttu-id="8cc5e-121">Значение по умолчанию — "0 0".</span><span class="sxs-lookup"><span data-stu-id="8cc5e-121">The default value is "0 0".</span></span> <span data-ttu-id="8cc5e-122">Растягивание Лимо — это точки на границе фигуры, которые определяют, где и как можно растянуть фигуру пользователя в графическом редакторе.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-122">Limo stretches are points on a shape's edge that define where and how a shape may be stretched by a user in a graphical editor.</span></span>

<span data-ttu-id="8cc5e-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="8cc5e-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8cc5e-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="8cc5e-124">**Example**</span></span>

<span data-ttu-id="8cc5e-125">Точка растяжения Лимо определяется вдоль горизонтальной линии.</span><span class="sxs-lookup"><span data-stu-id="8cc5e-125">A limo stretch point is defined halfway along the horizontal line.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 