---
title: Атрибут Даублекликкнотифи VML
description: Атрибут Даублекликкнотифи VML
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337609"
---
# <a name="vml-doubleclicknotify-attribute"></a><span data-ttu-id="2b0c8-103">Атрибут Даублекликкнотифи VML</span><span class="sxs-lookup"><span data-stu-id="2b0c8-103">VML DoubleClickNotify Attribute</span></span>

<span data-ttu-id="2b0c8-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2b0c8-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2b0c8-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2b0c8-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2b0c8-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2b0c8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2b0c8-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2b0c8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2b0c8-110">Отправляет сообщение о событии при двойном щелчке фигуры.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-110">Sends an event message when a shape is double-clicked.</span></span> <span data-ttu-id="2b0c8-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-111">Read/write.</span></span> <span data-ttu-id="2b0c8-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-112">**VgTriState**.</span></span>

<span data-ttu-id="2b0c8-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="2b0c8-113">**Applies To**</span></span>

[<span data-ttu-id="2b0c8-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="2b0c8-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="2b0c8-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-115">**Tag Syntax**</span></span>

<span data-ttu-id="2b0c8-116"><v: *element* о:даублекликкнотифи = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="2b0c8-116"><v: *element* o:doubleclicknotify=" *expression* "></span></span>

<span data-ttu-id="2b0c8-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-117">**Remarks**</span></span>

<span data-ttu-id="2b0c8-118">Значение по умолчанию — **false**, что означает, что событие не будет запущено.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-118">The default value is **False**, indicating that the event will not be fired.</span></span>

<span data-ttu-id="2b0c8-119">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="2b0c8-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="2b0c8-120">**Пример**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-120">**Example**</span></span>

<span data-ttu-id="2b0c8-121">Фигура активирует событие двойного щелчка при двойном щелчке.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-121">The shape will trigger a double-click event when double-clicked.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 