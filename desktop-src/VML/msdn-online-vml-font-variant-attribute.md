---
title: Атрибут VML Font-Variant
description: Атрибут VML Font-Variant
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413029"
---
# <a name="vml-font-variant-attribute"></a><span data-ttu-id="4e79d-103">Атрибут VML Font-Variant</span><span class="sxs-lookup"><span data-stu-id="4e79d-103">VML Font-Variant Attribute</span></span>

<span data-ttu-id="4e79d-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4e79d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4e79d-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="4e79d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4e79d-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="4e79d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4e79d-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4e79d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4e79d-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4e79d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4e79d-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4e79d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4e79d-110">Определяет вариант начертания шрифта.</span><span class="sxs-lookup"><span data-stu-id="4e79d-110">Defines the variant style of a font.</span></span> <span data-ttu-id="4e79d-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="4e79d-111">Read/write.</span></span> <span data-ttu-id="4e79d-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="4e79d-112">**String**.</span></span>

<span data-ttu-id="4e79d-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="4e79d-113">**Applies To**</span></span>

[<span data-ttu-id="4e79d-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="4e79d-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="4e79d-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="4e79d-115">**Tag Syntax**</span></span>

<span data-ttu-id="4e79d-116"><v: Style *элемента* = "Font-Variant: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="4e79d-116"><v: *element* style="font-variant: *expression* "></span></span>

<span data-ttu-id="4e79d-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="4e79d-117">**Script Syntax**</span></span>

<span data-ttu-id="4e79d-118">*element* . Style. фонтвариант = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="4e79d-118">*element* .style.fontvariant="*expression*"</span></span>

<span data-ttu-id="4e79d-119">*выражение* = *element*. Style. фонтвариант</span><span class="sxs-lookup"><span data-stu-id="4e79d-119">*expression*=*element*.style.fontvariant</span></span>

<span data-ttu-id="4e79d-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="4e79d-120">**Remarks**</span></span>

<span data-ttu-id="4e79d-121">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="4e79d-121">The values are:</span></span>

-   <span data-ttu-id="4e79d-122">Обычная (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e79d-122">normal (default)</span></span>
-   <span data-ttu-id="4e79d-123">малые прописные</span><span class="sxs-lookup"><span data-stu-id="4e79d-123">small-caps</span></span>

<span data-ttu-id="4e79d-124">Значения совпадают со стандартными атрибутами стиля HTML.</span><span class="sxs-lookup"><span data-stu-id="4e79d-124">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="4e79d-125">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="4e79d-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="4e79d-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="4e79d-126">**Example**</span></span>

<span data-ttu-id="4e79d-127">Шрифт подготавливается к просмотру как небольшие прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="4e79d-127">The font is rendered as small capital letters.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 