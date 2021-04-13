---
title: Атрибут строки VML
description: Атрибут строки VML
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6c172b4ca1f5049a3e89528a2333378164f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413230"
---
# <a name="vml-string-attribute"></a><span data-ttu-id="c869f-103">Атрибут строки VML</span><span class="sxs-lookup"><span data-stu-id="c869f-103">VML String Attribute</span></span>

<span data-ttu-id="c869f-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c869f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c869f-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c869f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c869f-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c869f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c869f-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c869f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c869f-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c869f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c869f-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c869f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c869f-110">Определяет текст текстового пути.</span><span class="sxs-lookup"><span data-stu-id="c869f-110">Defines the text of the text path.</span></span> <span data-ttu-id="c869f-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c869f-111">Read/write.</span></span> <span data-ttu-id="c869f-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="c869f-112">**String**.</span></span>

<span data-ttu-id="c869f-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c869f-113">**Applies To**</span></span>

[<span data-ttu-id="c869f-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="c869f-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="c869f-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c869f-115">**Tag Syntax**</span></span>

<span data-ttu-id="c869f-116"><v: *элемент* String = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c869f-116"><v: *element* string=" *expression* "></span></span>

<span data-ttu-id="c869f-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c869f-117">**Script Syntax**</span></span>

<span data-ttu-id="c869f-118">*element* . String = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c869f-118">*element* .string="*expression*"</span></span>

<span data-ttu-id="c869f-119">*выражение* = *элемент*. String</span><span class="sxs-lookup"><span data-stu-id="c869f-119">*expression*=*element*.string</span></span>

<span data-ttu-id="c869f-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c869f-120">**Remarks**</span></span>

<span data-ttu-id="c869f-121">Для вывода текста по текстовому пути необходимо назначить текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="c869f-121">You must assign a text string to display text on a text path.</span></span>

<span data-ttu-id="c869f-122">Стандартный атрибут VML</span><span class="sxs-lookup"><span data-stu-id="c869f-122">VML Standard Attribute</span></span>

<span data-ttu-id="c869f-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c869f-123">**Example**</span></span>

<span data-ttu-id="c869f-124">Строка, которая будет отображаться, имеет текст VML.</span><span class="sxs-lookup"><span data-stu-id="c869f-124">The string that will be displayed is "VML Text".</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 