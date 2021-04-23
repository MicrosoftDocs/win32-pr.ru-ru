---
title: Атрибут скрытой VML
description: Атрибут скрытой VML
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070208"
---
# <a name="vml-obscured-attribute"></a><span data-ttu-id="1e2bf-103">Атрибут скрытой VML</span><span class="sxs-lookup"><span data-stu-id="1e2bf-103">VML Obscured Attribute</span></span>

<span data-ttu-id="1e2bf-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1e2bf-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1e2bf-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1e2bf-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1e2bf-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1e2bf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1e2bf-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1e2bf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1e2bf-110">Определяет, является ли тень прозрачной.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-110">Determines whether a shadow is transparent.</span></span> <span data-ttu-id="1e2bf-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-111">Read/write.</span></span> <span data-ttu-id="1e2bf-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-112">**VgTriState**.</span></span>

<span data-ttu-id="1e2bf-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="1e2bf-113">**Applies To**</span></span>

[<span data-ttu-id="1e2bf-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="1e2bf-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="1e2bf-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="1e2bf-115">**Tag Syntax**</span></span>

<span data-ttu-id="1e2bf-116"><v: *элемент* скрыт = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="1e2bf-116"><v: *element* obscured=" *expression* "></span></span>

<span data-ttu-id="1e2bf-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="1e2bf-117">**Script Syntax**</span></span>

<span data-ttu-id="1e2bf-118">*element* . скрыто = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="1e2bf-118">*element* .obscured="*expression*"</span></span>

<span data-ttu-id="1e2bf-119">*выражение* = *element*. замаскировано</span><span class="sxs-lookup"><span data-stu-id="1e2bf-119">*expression*=*element*.obscured</span></span>

<span data-ttu-id="1e2bf-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="1e2bf-120">**Remarks**</span></span>

<span data-ttu-id="1e2bf-121">Если **значение — true**, позволяет видеть сквозь тень, если в фигуре Нет заливки.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-121">If **True**, lets you see through the shadow if there is no fill on the shape.</span></span> <span data-ttu-id="1e2bf-122">Значение по умолчанию — **False**.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-122">Default is **False**.</span></span>

<span data-ttu-id="1e2bf-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="1e2bf-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="1e2bf-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="1e2bf-124">**Example**</span></span>

<span data-ttu-id="1e2bf-125">Фон отображается сквозь тень.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-125">The background shows through the shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 