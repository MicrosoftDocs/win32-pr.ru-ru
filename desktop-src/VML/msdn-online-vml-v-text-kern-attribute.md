---
title: Атрибут VML V-Text-кернинг
description: Атрибут VML V-Text-кернинг
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987719"
---
# <a name="vml-v-text-kern-attribute"></a><span data-ttu-id="49bc2-103">Атрибут VML V-Text-кернинг</span><span class="sxs-lookup"><span data-stu-id="49bc2-103">VML V-Text-Kern Attribute</span></span>

<span data-ttu-id="49bc2-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="49bc2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49bc2-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="49bc2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49bc2-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="49bc2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49bc2-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="49bc2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49bc2-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="49bc2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49bc2-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="49bc2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49bc2-110">Определяет, включен ли кернинг.</span><span class="sxs-lookup"><span data-stu-id="49bc2-110">Determines whether kerning is turned on.</span></span> <span data-ttu-id="49bc2-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="49bc2-111">Read/write.</span></span> <span data-ttu-id="49bc2-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="49bc2-112">**VgTriState**.</span></span>

<span data-ttu-id="49bc2-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="49bc2-113">**Applies To**</span></span>

[<span data-ttu-id="49bc2-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="49bc2-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="49bc2-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="49bc2-115">**Tag Syntax**</span></span>

<span data-ttu-id="49bc2-116"><v: Style *элемента* = "v-Text-кернинг: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="49bc2-116"><v: *element* style="v-text-kern: *expression* "></span></span>

<span data-ttu-id="49bc2-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="49bc2-117">**Script Syntax**</span></span>

<span data-ttu-id="49bc2-118">*element* . Style. v-Text-кернинг = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="49bc2-118">*element* .style.v-text-kern="*expression*"</span></span>

<span data-ttu-id="49bc2-119">*выражение* = *element*. Style. v-Text-кернинг</span><span class="sxs-lookup"><span data-stu-id="49bc2-119">*expression*=*element*.style.v-text-kern</span></span>

<span data-ttu-id="49bc2-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="49bc2-120">**Remarks**</span></span>

<span data-ttu-id="49bc2-121">Если **значение равно true**, кернинг включен.</span><span class="sxs-lookup"><span data-stu-id="49bc2-121">If **True**, the kerning is turned on.</span></span> <span data-ttu-id="49bc2-122">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="49bc2-122">The default is **False**.</span></span> <span data-ttu-id="49bc2-123">Кернинг — это удаление пробела между определенными парами букв, чтобы компенсировать нечетные леттерформс.</span><span class="sxs-lookup"><span data-stu-id="49bc2-123">Kerning is the removal of space between certain letter pairs to compensate for uneven letterforms.</span></span> <span data-ttu-id="49bc2-124">Например, если кернинг включен, дополнительное пространство между заглавной буквой «T» и строчной буквой «i» будет удалено.</span><span class="sxs-lookup"><span data-stu-id="49bc2-124">For example, if kerning is turned on, extra space between a capital "T" and a lowercase "i" would be removed.</span></span>

<span data-ttu-id="49bc2-125">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="49bc2-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="49bc2-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="49bc2-126">**Example**</span></span>

<span data-ttu-id="49bc2-127">Кернинг включен.</span><span class="sxs-lookup"><span data-stu-id="49bc2-127">Kerning is turned on.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 