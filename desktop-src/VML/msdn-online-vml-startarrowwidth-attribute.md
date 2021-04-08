---
title: Атрибут Стартарроввидс VML
description: Атрибут Стартарроввидс VML
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792553"
---
# <a name="vml-startarrowwidth-attribute"></a><span data-ttu-id="1de64-103">Атрибут Стартарроввидс VML</span><span class="sxs-lookup"><span data-stu-id="1de64-103">VML StartArrowWidth Attribute</span></span>

<span data-ttu-id="1de64-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1de64-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1de64-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="1de64-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1de64-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="1de64-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1de64-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1de64-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1de64-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1de64-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1de64-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1de64-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1de64-110">Определяет ширину стрелки для начала строки.</span><span class="sxs-lookup"><span data-stu-id="1de64-110">Defines the arrowhead width for the start of a line.</span></span> <span data-ttu-id="1de64-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="1de64-111">Read/write.</span></span> <span data-ttu-id="1de64-112">**Вгарровхеадвидс**.</span><span class="sxs-lookup"><span data-stu-id="1de64-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="1de64-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="1de64-113">**Applies To**</span></span>

[<span data-ttu-id="1de64-114">Водок</span><span class="sxs-lookup"><span data-stu-id="1de64-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="1de64-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="1de64-115">**Tag Syntax**</span></span>

<span data-ttu-id="1de64-116"><v: *element* стартарроввидс = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="1de64-116"><v: *element* startarrowwidth=" *expression* "></span></span>

<span data-ttu-id="1de64-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="1de64-117">**Script Syntax**</span></span>

<span data-ttu-id="1de64-118">*element* . стартарроввидс = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="1de64-118">*element* .startarrowwidth="*expression*"</span></span>

<span data-ttu-id="1de64-119">*выражение* = *element*. стартарроввидс</span><span class="sxs-lookup"><span data-stu-id="1de64-119">*expression*=*element*.startarrowwidth</span></span>

<span data-ttu-id="1de64-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="1de64-120">**Remarks**</span></span>

<span data-ttu-id="1de64-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="1de64-121">Values include:</span></span>

-   <span data-ttu-id="1de64-122">Разрабатываем</span><span class="sxs-lookup"><span data-stu-id="1de64-122">Narrow</span></span>
-   <span data-ttu-id="1de64-123">Среднее (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1de64-123">Medium (default)</span></span>
-   <span data-ttu-id="1de64-124">Широкий</span><span class="sxs-lookup"><span data-stu-id="1de64-124">Wide</span></span>

<span data-ttu-id="1de64-125">Стандартный атрибут VML</span><span class="sxs-lookup"><span data-stu-id="1de64-125">VML Standard Attribute</span></span>

<span data-ttu-id="1de64-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="1de64-126">**Example**</span></span>

<span data-ttu-id="1de64-127">Линия рисуется с помощью широкой классической стрелки в начале штриха.</span><span class="sxs-lookup"><span data-stu-id="1de64-127">A line is drawn with a wide classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 