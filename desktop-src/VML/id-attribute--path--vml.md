---
title: Атрибут ID (Path) (VML)
description: Атрибут ID (Path) (VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133899"
---
# <a name="id-attribute-pathvml"></a><span data-ttu-id="11bbd-103">Атрибут ID (Path) (VML)</span><span class="sxs-lookup"><span data-stu-id="11bbd-103">ID Attribute (Path)(VML)</span></span>

<span data-ttu-id="11bbd-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="11bbd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="11bbd-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="11bbd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="11bbd-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="11bbd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="11bbd-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="11bbd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="11bbd-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="11bbd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="11bbd-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="11bbd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="11bbd-110">Имя, которое предоставляет уникальный идентификатор для пути.</span><span class="sxs-lookup"><span data-stu-id="11bbd-110">A name that provides a unique identifier for a path.</span></span> <span data-ttu-id="11bbd-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="11bbd-111">Read/write.</span></span> <span data-ttu-id="11bbd-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="11bbd-112">**String**.</span></span>

<span data-ttu-id="11bbd-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="11bbd-113">**Applies To**</span></span>

[<span data-ttu-id="11bbd-114">Путь</span><span class="sxs-lookup"><span data-stu-id="11bbd-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="11bbd-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="11bbd-115">**Tag Syntax**</span></span>

<span data-ttu-id="11bbd-116"><v: *element* ID = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="11bbd-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="11bbd-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="11bbd-117">**Script Syntax**</span></span>

<span data-ttu-id="11bbd-118">*element* . ID = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="11bbd-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="11bbd-119">*выражение* = *element*. ID</span><span class="sxs-lookup"><span data-stu-id="11bbd-119">*expression*=*element*.id</span></span>

<span data-ttu-id="11bbd-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="11bbd-120">**Remarks**</span></span>

<span data-ttu-id="11bbd-121">Используйте **ID** для ссылки на конкретный путь.</span><span class="sxs-lookup"><span data-stu-id="11bbd-121">Use **ID** to refer to a specific path.</span></span> <span data-ttu-id="11bbd-122">После создания пути и присвоения ему идентификатора можно использовать имя идентификатора, если требуется управлять путем.</span><span class="sxs-lookup"><span data-stu-id="11bbd-122">Once you have created a path and given it an ID, you can use the ID name when you want to manipulate the path.</span></span>

<span data-ttu-id="11bbd-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="11bbd-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="11bbd-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="11bbd-124">**Example**</span></span>

<span data-ttu-id="11bbd-125">Фигура имеет идентификатор Path с именем «myPath».</span><span class="sxs-lookup"><span data-stu-id="11bbd-125">The shape has a path ID called "myPath".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 