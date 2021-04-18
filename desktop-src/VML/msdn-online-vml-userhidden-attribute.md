---
title: Атрибут Усерхидден VML
description: Атрибут Усерхидден VML
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 519857d53cbec985afae31a5e7dea8811773dc43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691542"
---
# <a name="vml-userhidden-attribute"></a><span data-ttu-id="5a2b2-103">Атрибут Усерхидден VML</span><span class="sxs-lookup"><span data-stu-id="5a2b2-103">VML UserHidden Attribute</span></span>

<span data-ttu-id="5a2b2-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5a2b2-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5a2b2-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5a2b2-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5a2b2-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5a2b2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5a2b2-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5a2b2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5a2b2-110">Определяет, скрыта ли привязка скрипта.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-110">Determines whether a script anchor is hidden.</span></span> <span data-ttu-id="5a2b2-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-111">Read/write.</span></span> <span data-ttu-id="5a2b2-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-112">**VgTriState**.</span></span>

<span data-ttu-id="5a2b2-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="5a2b2-113">**Applies To**</span></span>

[<span data-ttu-id="5a2b2-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="5a2b2-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="5a2b2-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="5a2b2-115">**Tag Syntax**</span></span>

<span data-ttu-id="5a2b2-116"><v: *element* о:усерхидден = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="5a2b2-116"><v: *element* o:userhidden=" *expression* "></span></span>

<span data-ttu-id="5a2b2-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="5a2b2-117">**Remarks**</span></span>

<span data-ttu-id="5a2b2-118">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-118">The default is **False**.</span></span> <span data-ttu-id="5a2b2-119">Если **значение равно true**, привязки сценариев остаются скрытыми, даже если фигура видима в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-119">If **True**, script anchors stay hidden even if the shape is otherwise visible.</span></span>

<span data-ttu-id="5a2b2-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="5a2b2-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="5a2b2-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="5a2b2-121">**Example**</span></span>

<span data-ttu-id="5a2b2-122">Привязка скрипта для фигуры скрыта.</span><span class="sxs-lookup"><span data-stu-id="5a2b2-122">The script anchor of the shape is hidden.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 