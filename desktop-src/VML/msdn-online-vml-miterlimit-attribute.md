---
title: Атрибут Митерлимит VML
description: Атрибут Митерлимит VML
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487877"
---
# <a name="vml-miterlimit-attribute"></a><span data-ttu-id="83965-103">Атрибут Митерлимит VML</span><span class="sxs-lookup"><span data-stu-id="83965-103">VML MiterLimit Attribute</span></span>

<span data-ttu-id="83965-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="83965-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="83965-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="83965-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="83965-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="83965-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="83965-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="83965-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="83965-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="83965-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="83965-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="83965-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="83965-110">Определяет гладкость соединения типа «уголок».</span><span class="sxs-lookup"><span data-stu-id="83965-110">Defines the smoothness of the miter joint.</span></span> <span data-ttu-id="83965-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="83965-111">Read/write.</span></span> <span data-ttu-id="83965-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="83965-112">**VgNumber**.</span></span>

<span data-ttu-id="83965-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="83965-113">**Applies To**</span></span>

[<span data-ttu-id="83965-114">Водок</span><span class="sxs-lookup"><span data-stu-id="83965-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="83965-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="83965-115">**Tag Syntax**</span></span>

<span data-ttu-id="83965-116"><v: *element* митерлимит = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="83965-116"><v: *element* miterlimit=" *expression* "></span></span>

<span data-ttu-id="83965-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="83965-117">**Script Syntax**</span></span>

<span data-ttu-id="83965-118">*element* . митерлимит = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="83965-118">*element* .miterlimit="*expression*"</span></span>

<span data-ttu-id="83965-119">*выражение* = *element*. митерлимит</span><span class="sxs-lookup"><span data-stu-id="83965-119">*expression*=*element*.miterlimit</span></span>

<span data-ttu-id="83965-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="83965-120">**Remarks**</span></span>

<span data-ttu-id="83965-121">Максимальное расстояние между внутренней точкой и внешней точкой соединения.</span><span class="sxs-lookup"><span data-stu-id="83965-121">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="83965-122">Это число является кратным ширине линии.</span><span class="sxs-lookup"><span data-stu-id="83965-122">This number is a multiple of the thickness of the line.</span></span>

<span data-ttu-id="83965-123">Значение по умолчанию: 8.</span><span class="sxs-lookup"><span data-stu-id="83965-123">The default value is 8.</span></span>

<span data-ttu-id="83965-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="83965-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="83965-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="83965-125">**Example**</span></span>

<span data-ttu-id="83965-126">Соединения в ломаной линии размещаются с ограничением 10, то есть 5 раз в две точки.</span><span class="sxs-lookup"><span data-stu-id="83965-126">The joints on the polyline are mitered with a limit of 10, that is, 5 times 2 points.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 