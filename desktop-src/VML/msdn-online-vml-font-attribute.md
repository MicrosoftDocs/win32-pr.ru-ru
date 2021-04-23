---
title: Атрибут шрифта VML
description: Атрибут шрифта VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691652"
---
# <a name="vml-font-attribute"></a><span data-ttu-id="84c5a-103">Атрибут шрифта VML</span><span class="sxs-lookup"><span data-stu-id="84c5a-103">VML Font Attribute</span></span>

<span data-ttu-id="84c5a-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="84c5a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="84c5a-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="84c5a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="84c5a-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="84c5a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="84c5a-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="84c5a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="84c5a-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="84c5a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="84c5a-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="84c5a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="84c5a-110">Задает составное значение атрибутов шрифта.</span><span class="sxs-lookup"><span data-stu-id="84c5a-110">Specifies a compound value of font attributes.</span></span> <span data-ttu-id="84c5a-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="84c5a-111">Read/write.</span></span> <span data-ttu-id="84c5a-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="84c5a-112">**String**.</span></span>

<span data-ttu-id="84c5a-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="84c5a-113">**Applies To**</span></span>

[<span data-ttu-id="84c5a-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="84c5a-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="84c5a-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="84c5a-115">**Tag Syntax**</span></span>

<span data-ttu-id="84c5a-116"><v: Style *элемента* = "Font: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="84c5a-116"><v: *element* style="font: *expression* "></span></span>

<span data-ttu-id="84c5a-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="84c5a-117">**Script Syntax**</span></span>

<span data-ttu-id="84c5a-118">*element* . Style. Font = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="84c5a-118">*element* .style.font="*expression*"</span></span>

<span data-ttu-id="84c5a-119">*выражение* = *элемент*. Style. Font</span><span class="sxs-lookup"><span data-stu-id="84c5a-119">*expression*=*element*.style.font</span></span>

<span data-ttu-id="84c5a-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="84c5a-120">**Remarks**</span></span>

<span data-ttu-id="84c5a-121">Определяет атрибуты шрифта, включая семейство, стиль, вес, размер и вариант.</span><span class="sxs-lookup"><span data-stu-id="84c5a-121">Defines the attributes of a font, including family, style, weight, size, and variant.</span></span> <span data-ttu-id="84c5a-122">Порядок следования определений в строке: **Шрифт** **, начертание шрифта, начертание** **шрифта**, шрифт, **Размер шрифта**, **линия** и **семейство шрифтов**.</span><span class="sxs-lookup"><span data-stu-id="84c5a-122">The order of definitions in the string is: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height**, and **font-family**.</span></span> <span data-ttu-id="84c5a-123">Значения совпадают со стандартными атрибутами стиля HTML.</span><span class="sxs-lookup"><span data-stu-id="84c5a-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="84c5a-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="84c5a-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="84c5a-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="84c5a-125">**Example**</span></span>

<span data-ttu-id="84c5a-126">Шрифт текста текстпас имеет курсив, капитель, полужирный шрифт, 36 пт, Arial.</span><span class="sxs-lookup"><span data-stu-id="84c5a-126">The font of the textpath text is italic, small-caps, bold, 36 point Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 