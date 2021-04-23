---
title: Атрибут VML Text-Decoration
description: Атрибут VML Text-Decoration
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987579"
---
# <a name="vml-text-decoration-attribute"></a><span data-ttu-id="5af72-103">Атрибут VML Text-Decoration</span><span class="sxs-lookup"><span data-stu-id="5af72-103">VML Text-Decoration Attribute</span></span>

<span data-ttu-id="5af72-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5af72-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5af72-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="5af72-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5af72-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="5af72-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5af72-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5af72-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5af72-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5af72-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5af72-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5af72-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5af72-110">Определяет стиль оформления текста.</span><span class="sxs-lookup"><span data-stu-id="5af72-110">Defines the style of text decoration.</span></span> <span data-ttu-id="5af72-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="5af72-111">Read/write.</span></span> <span data-ttu-id="5af72-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="5af72-112">**String**.</span></span>

<span data-ttu-id="5af72-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="5af72-113">**Applies To**</span></span>

[<span data-ttu-id="5af72-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="5af72-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="5af72-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="5af72-115">**Tag Syntax**</span></span>

<span data-ttu-id="5af72-116"><v: *element* Style = "Оформление текста: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="5af72-116"><v: *element* style="text-decoration: *expression* "></span></span>

<span data-ttu-id="5af72-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="5af72-117">**Script Syntax**</span></span>

<span data-ttu-id="5af72-118">*element* . Style. TextDecoration = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="5af72-118">*element* .style.textdecoration="*expression*"</span></span>

<span data-ttu-id="5af72-119">*выражение* = *element*. Style. TextDecoration</span><span class="sxs-lookup"><span data-stu-id="5af72-119">*expression*=*element*.style.textdecoration</span></span>

<span data-ttu-id="5af72-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="5af72-120">**Remarks**</span></span>

<span data-ttu-id="5af72-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="5af72-121">Values include:</span></span>

-   <span data-ttu-id="5af72-122">нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5af72-122">none (default)</span></span>
-   <span data-ttu-id="5af72-123">подчеркнутый</span><span class="sxs-lookup"><span data-stu-id="5af72-123">underline</span></span>
-   <span data-ttu-id="5af72-124">надчеркивание</span><span class="sxs-lookup"><span data-stu-id="5af72-124">overline</span></span>
-   <span data-ttu-id="5af72-125">со сквозной линией</span><span class="sxs-lookup"><span data-stu-id="5af72-125">line-through</span></span>
-   <span data-ttu-id="5af72-126">blink</span><span class="sxs-lookup"><span data-stu-id="5af72-126">blink</span></span>

<span data-ttu-id="5af72-127">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="5af72-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="5af72-128">**Пример**</span><span class="sxs-lookup"><span data-stu-id="5af72-128">**Example**</span></span>

<span data-ttu-id="5af72-129">Текст будет подчеркнут.</span><span class="sxs-lookup"><span data-stu-id="5af72-129">The text will be underlined.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 