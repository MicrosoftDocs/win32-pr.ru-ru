---
title: Атрибут Строкеок VML
description: Атрибут Строкеок VML
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a2875e3e6e8374238340ff2a596852e5ebce7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987720"
---
# <a name="vml-strokeok-attribute"></a><span data-ttu-id="ac524-103">Атрибут Строкеок VML</span><span class="sxs-lookup"><span data-stu-id="ac524-103">VML StrokeOK Attribute</span></span>

<span data-ttu-id="ac524-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ac524-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ac524-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ac524-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ac524-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ac524-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ac524-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ac524-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ac524-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ac524-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ac524-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ac524-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ac524-110">Определяет, будет ли отображаться штрих.</span><span class="sxs-lookup"><span data-stu-id="ac524-110">Determines whether a stroke will be displayed.</span></span> <span data-ttu-id="ac524-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ac524-111">Read/write.</span></span> <span data-ttu-id="ac524-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="ac524-112">**VgTriState**.</span></span>

<span data-ttu-id="ac524-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ac524-113">**Applies To**</span></span>

[<span data-ttu-id="ac524-114">Путь</span><span class="sxs-lookup"><span data-stu-id="ac524-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="ac524-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ac524-115">**Tag Syntax**</span></span>

<span data-ttu-id="ac524-116"><v: *element* строкеок = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ac524-116"><v: *element* strokeok=" *expression* "></span></span>

<span data-ttu-id="ac524-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ac524-117">**Script Syntax**</span></span>

<span data-ttu-id="ac524-118">*element* . строкеок = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ac524-118">*element* .strokeok="*expression*"</span></span>

<span data-ttu-id="ac524-119">*выражение* = *element*. строкеок</span><span class="sxs-lookup"><span data-stu-id="ac524-119">*expression*=*element*.strokeok</span></span>

<span data-ttu-id="ac524-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ac524-120">**Remarks**</span></span>

<span data-ttu-id="ac524-121">Если **значение равно false**, то контур не может быть обводкой.</span><span class="sxs-lookup"><span data-stu-id="ac524-121">If **False**, the path cannot be stroked.</span></span> <span data-ttu-id="ac524-122">Значение по умолчанию равно **True**.</span><span class="sxs-lookup"><span data-stu-id="ac524-122">The default is **True**.</span></span> <span data-ttu-id="ac524-123">Этот атрибут переопределяет все остальные атрибуты Stroke в родительском элементе или элементе **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="ac524-123">This attribute overrides all other stroke attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="ac524-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="ac524-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ac524-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ac524-125">**Example**</span></span>

<span data-ttu-id="ac524-126">Этот путь не будет обводкой.</span><span class="sxs-lookup"><span data-stu-id="ac524-126">The path will not be stroked.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 