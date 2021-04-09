---
title: Атрибут VML Font-Family
description: Атрибут VML Font-Family
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070598"
---
# <a name="vml-font-family-attribute"></a><span data-ttu-id="5b61f-103">Атрибут VML Font-Family</span><span class="sxs-lookup"><span data-stu-id="5b61f-103">VML Font-Family Attribute</span></span>

<span data-ttu-id="5b61f-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5b61f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5b61f-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="5b61f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5b61f-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="5b61f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5b61f-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5b61f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5b61f-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5b61f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5b61f-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5b61f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5b61f-110">Определяет семейство шрифта текстпас.</span><span class="sxs-lookup"><span data-stu-id="5b61f-110">Defines the family of the textpath font.</span></span> <span data-ttu-id="5b61f-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="5b61f-111">Read/write.</span></span> <span data-ttu-id="5b61f-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="5b61f-112">**String**.</span></span>

<span data-ttu-id="5b61f-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="5b61f-113">**Applies To**</span></span>

[<span data-ttu-id="5b61f-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="5b61f-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="5b61f-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="5b61f-115">**Tag Syntax**</span></span>

<span data-ttu-id="5b61f-116"><v: Style *элемента* = "Font-Family: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5b61f-116"><v: *element* style="font-family: *expression* "></span></span>

<span data-ttu-id="5b61f-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="5b61f-117">**Script Syntax**</span></span>

<span data-ttu-id="5b61f-118">*element* . Style. FontFamily = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="5b61f-118">*element* .style.fontfamily="*expression*"</span></span>

<span data-ttu-id="5b61f-119">*выражение* = *элемент*. Style. FontFamily</span><span class="sxs-lookup"><span data-stu-id="5b61f-119">*expression*=*element*.style.fontfamily</span></span>

<span data-ttu-id="5b61f-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="5b61f-120">**Remarks**</span></span>

<span data-ttu-id="5b61f-121">Определяет имя шрифта.</span><span class="sxs-lookup"><span data-stu-id="5b61f-121">Defines the font name.</span></span> <span data-ttu-id="5b61f-122">Можно использовать специальные имена, такие как Arial, или универсальные типы, такие как serif, sans-serif, рукописный ввод, фэнтези или моноширинная.</span><span class="sxs-lookup"><span data-stu-id="5b61f-122">Specific names such as Arial can be used or generic types such as serif, sans-serif, cursive, fantasy, or monospace.</span></span> <span data-ttu-id="5b61f-123">Значения совпадают со стандартными атрибутами стиля HTML.</span><span class="sxs-lookup"><span data-stu-id="5b61f-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="5b61f-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="5b61f-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="5b61f-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="5b61f-125">**Example**</span></span>

<span data-ttu-id="5b61f-126">Семейство шрифтов текста — Arial.</span><span class="sxs-lookup"><span data-stu-id="5b61f-126">The font family of the text is Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 