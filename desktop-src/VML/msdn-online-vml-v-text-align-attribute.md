---
title: Атрибут VML V-Text-aligned
description: Атрибут VML V-Text-aligned
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6efb96bde980a4831f400ada7032f9ee37f1d976
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987629"
---
# <a name="vml-v-text-align-attribute"></a><span data-ttu-id="21f77-103">Атрибут VML V-Text-aligned</span><span class="sxs-lookup"><span data-stu-id="21f77-103">VML V-Text-Align Attribute</span></span>

<span data-ttu-id="21f77-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="21f77-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21f77-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="21f77-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21f77-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="21f77-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21f77-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21f77-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21f77-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21f77-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21f77-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21f77-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21f77-110">Определяет выравнивание текста.</span><span class="sxs-lookup"><span data-stu-id="21f77-110">Defines the alignment of text.</span></span> <span data-ttu-id="21f77-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="21f77-111">Read/write.</span></span> <span data-ttu-id="21f77-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="21f77-112">**String**.</span></span>

<span data-ttu-id="21f77-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="21f77-113">**Applies To**</span></span>

[<span data-ttu-id="21f77-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="21f77-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="21f77-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="21f77-115">**Tag Syntax**</span></span>

<span data-ttu-id="21f77-116"><v: Style *элемента* = "v-Text-aligned: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="21f77-116"><v: *element* style="v-text-align: *expression* "></span></span>

<span data-ttu-id="21f77-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="21f77-117">**Script Syntax**</span></span>

<span data-ttu-id="21f77-118">*element* . Style. v-Text-aligned = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="21f77-118">*element* .style.v-text-align="*expression*"</span></span>

<span data-ttu-id="21f77-119">*выражение* = *element*. Style. v-Text-aligned</span><span class="sxs-lookup"><span data-stu-id="21f77-119">*expression*=*element*.style.v-text-align</span></span>

<span data-ttu-id="21f77-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="21f77-120">**Remarks**</span></span>

<span data-ttu-id="21f77-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="21f77-121">Values include:</span></span>

-   <span data-ttu-id="21f77-122">**Left** (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21f77-122">**left** (default)</span></span>
-   <span data-ttu-id="21f77-123">**Правильно**</span><span class="sxs-lookup"><span data-stu-id="21f77-123">**right**</span></span>
-   <span data-ttu-id="21f77-124">**Center**</span><span class="sxs-lookup"><span data-stu-id="21f77-124">**center**</span></span>
-   <span data-ttu-id="21f77-125">**формат**</span><span class="sxs-lookup"><span data-stu-id="21f77-125">**justify**</span></span>
-   <span data-ttu-id="21f77-126">**Выравнивание по буквам**</span><span class="sxs-lookup"><span data-stu-id="21f77-126">**letter-justify**</span></span>
-   <span data-ttu-id="21f77-127">**растяжение по ширине**</span><span class="sxs-lookup"><span data-stu-id="21f77-127">**stretch-justify**</span></span>

<span data-ttu-id="21f77-128">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="21f77-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="21f77-129">**Пример**</span><span class="sxs-lookup"><span data-stu-id="21f77-129">**Example**</span></span>

<span data-ttu-id="21f77-130">Текст будет растянут по размеру пути, но дополнительное пространство будет размещаться между каждой буквой.</span><span class="sxs-lookup"><span data-stu-id="21f77-130">The text will be stretched out to fit the path, but the extra space will be put between each letter.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 