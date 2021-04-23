---
title: Атрибут ID (Stroke) (VML)
description: Атрибут ID (Stroke) (VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792403"
---
# <a name="id-attribute-strokevml"></a><span data-ttu-id="2fe7a-103">Атрибут ID (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="2fe7a-103">ID Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="2fe7a-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2fe7a-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2fe7a-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2fe7a-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2fe7a-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2fe7a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2fe7a-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2fe7a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2fe7a-110">Имя, которое предоставляет уникальный идентификатор для штриха.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-110">A name that provides a unique identifier for a stroke.</span></span> <span data-ttu-id="2fe7a-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-111">Read/write.</span></span> <span data-ttu-id="2fe7a-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-112">**String**.</span></span>

<span data-ttu-id="2fe7a-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="2fe7a-113">**Applies To**</span></span>

[<span data-ttu-id="2fe7a-114">Водок</span><span class="sxs-lookup"><span data-stu-id="2fe7a-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="2fe7a-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="2fe7a-115">**Tag Syntax**</span></span>

<span data-ttu-id="2fe7a-116"><v: *element* ID = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="2fe7a-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="2fe7a-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="2fe7a-117">**Script Syntax**</span></span>

<span data-ttu-id="2fe7a-118">*element* . ID = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="2fe7a-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="2fe7a-119">*выражение* = *element*. ID</span><span class="sxs-lookup"><span data-stu-id="2fe7a-119">*expression*=*element*.id</span></span>

<span data-ttu-id="2fe7a-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="2fe7a-120">**Remarks**</span></span>

<span data-ttu-id="2fe7a-121">Используйте **ID** для ссылки на конкретный штрих.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-121">Use **ID** to refer to a specific stroke.</span></span> <span data-ttu-id="2fe7a-122">После создания штриха и присвоения ему идентификатора можно использовать имя идентификатора, если требуется управлять обводкой.</span><span class="sxs-lookup"><span data-stu-id="2fe7a-122">Once you have created a stroke and given it an ID, you can use the ID name when you want to manipulate the stroke.</span></span>

<span data-ttu-id="2fe7a-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="2fe7a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="2fe7a-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="2fe7a-124">**Example**</span></span>

<span data-ttu-id="2fe7a-125">Фигура имеет идентификатор Stroke с именем «мистроке».</span><span class="sxs-lookup"><span data-stu-id="2fe7a-125">The shape has a stroke ID called "mystroke".</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 