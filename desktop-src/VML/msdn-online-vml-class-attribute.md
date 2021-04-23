---
title: Атрибут класса VML
description: Атрибут класса VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987674"
---
# <a name="vml-class-attribute"></a><span data-ttu-id="cefd5-103">Атрибут класса VML</span><span class="sxs-lookup"><span data-stu-id="cefd5-103">VML Class Attribute</span></span>

<span data-ttu-id="cefd5-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cefd5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cefd5-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="cefd5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cefd5-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="cefd5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cefd5-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cefd5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cefd5-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cefd5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cefd5-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cefd5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cefd5-110">Ссылается на определение стиля CSS.</span><span class="sxs-lookup"><span data-stu-id="cefd5-110">Refers to a definition of a CSS style.</span></span> <span data-ttu-id="cefd5-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="cefd5-111">Read/write.</span></span> <span data-ttu-id="cefd5-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="cefd5-112">**String**.</span></span>

<span data-ttu-id="cefd5-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="cefd5-113">**Applies To**</span></span>

[<span data-ttu-id="cefd5-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="cefd5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="cefd5-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="cefd5-115">**Tag Syntax**</span></span>

<span data-ttu-id="cefd5-116"><v: *element* Class = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="cefd5-116"><v: *element* class=" *expression* "></span></span>

<span data-ttu-id="cefd5-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="cefd5-117">**Script Syntax**</span></span>

<span data-ttu-id="cefd5-118">*element* . ClassName = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="cefd5-118">*element* .classname="*expression*"</span></span>

<span data-ttu-id="cefd5-119">*выражение* = *element*. classname</span><span class="sxs-lookup"><span data-stu-id="cefd5-119">*expression*=*element*.classname</span></span>

<span data-ttu-id="cefd5-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="cefd5-120">**Remarks**</span></span>

<span data-ttu-id="cefd5-121">Атрибут **Class** аналогичен стандартному атрибуту **класса** HTML, используемому в таблицах стилей CSS.</span><span class="sxs-lookup"><span data-stu-id="cefd5-121">The **class** attribute is similar to the standard HTML **class** attribute used with CSS style sheets.</span></span>

<span data-ttu-id="cefd5-122">Обратите внимание, что вместо **класса** для создания скриптов используется **className** .</span><span class="sxs-lookup"><span data-stu-id="cefd5-122">Note that **classname** is used instead of **class** for scripting.</span></span> <span data-ttu-id="cefd5-123">Кроме того, обратите внимание, что для сценариев можно только прочитать **className** . изменение значения **className** не приведет к изменению отрисовки фигуры.</span><span class="sxs-lookup"><span data-stu-id="cefd5-123">Also note that for scripting, the **classname** can only be read; changing the value of **classname** will not change the rendering of the shape.</span></span>

<span data-ttu-id="cefd5-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="cefd5-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="cefd5-125">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="cefd5-125">**See Also**</span></span>

[<span data-ttu-id="cefd5-126">Фигурная</span><span class="sxs-lookup"><span data-stu-id="cefd5-126">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="cefd5-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="cefd5-127">**Example**</span></span>

<span data-ttu-id="cefd5-128">Класс для **Width** создается с использованием стиля</span><span class="sxs-lookup"><span data-stu-id="cefd5-128">A class for **width** is created with the style</span></span>


```HTML
   .narrowstyle {width:50;height:100}
```



<span data-ttu-id="cefd5-129">Затем на ширину добавляется ссылка, включающая стиль.</span><span class="sxs-lookup"><span data-stu-id="cefd5-129">Then the width is referenced by including the style.</span></span> <span data-ttu-id="cefd5-130">Обратите внимание, что ширина андхеигхт не определена в атрибуте **Style** , но будет определяться стилем.</span><span class="sxs-lookup"><span data-stu-id="cefd5-130">Note that the width andheight is not defined in the **style** attribute, but will be defined by the style.</span></span>


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="cefd5-131">Обратите внимание, что **класс** применяется только к атрибутам типа CSS.</span><span class="sxs-lookup"><span data-stu-id="cefd5-131">Note that **Class** only applies to CSS-type attributes.</span></span>

 

 