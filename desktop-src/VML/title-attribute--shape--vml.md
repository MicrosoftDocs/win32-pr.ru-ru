---
title: Атрибут Title (Shape) (VML)
description: Атрибут Title (Shape) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488240"
---
# <a name="title-attribute-shapevml"></a><span data-ttu-id="850b6-103">Атрибут Title (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="850b6-103">Title Attribute (Shape)(VML)</span></span>

<span data-ttu-id="850b6-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="850b6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="850b6-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="850b6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="850b6-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="850b6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="850b6-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="850b6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="850b6-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="850b6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="850b6-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="850b6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="850b6-110">Определяет текст, отображаемый при наведении указателя мыши на фигуру.</span><span class="sxs-lookup"><span data-stu-id="850b6-110">Defines the text displayed when the mouse pointer moves over the shape.</span></span> <span data-ttu-id="850b6-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="850b6-111">Read/write.</span></span> <span data-ttu-id="850b6-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="850b6-112">**String**.</span></span>

<span data-ttu-id="850b6-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="850b6-113">**Applies To**</span></span>

[<span data-ttu-id="850b6-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="850b6-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="850b6-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="850b6-115">**Tag Syntax**</span></span>

<span data-ttu-id="850b6-116"><v: *элемент* Title = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="850b6-116"><v: *element* title=" *expression* "></span></span>

<span data-ttu-id="850b6-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="850b6-117">**Script Syntax**</span></span>

<span data-ttu-id="850b6-118">*element* . Title = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="850b6-118">*element* .title="*expression*"</span></span>

<span data-ttu-id="850b6-119">*выражение* = *элемент*. Title</span><span class="sxs-lookup"><span data-stu-id="850b6-119">*expression*=*element*.title</span></span>

<span data-ttu-id="850b6-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="850b6-120">**Remarks**</span></span>

<span data-ttu-id="850b6-121">Атрибут **Title** аналогичен стандартному атрибуту **заголовка** HTML.</span><span class="sxs-lookup"><span data-stu-id="850b6-121">The **Title** attribute is similar to the standard HTML **Title** attribute.</span></span> <span data-ttu-id="850b6-122">Поведение заголовка аналогично подсказке Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="850b6-122">The behavior of a title is similar to a Microsoft Windows ToolTip.</span></span>

<span data-ttu-id="850b6-123">**Стандартный атрибут VML**</span><span class="sxs-lookup"><span data-stu-id="850b6-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="850b6-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="850b6-124">**Example**</span></span>

<span data-ttu-id="850b6-125">Заголовок фигуры — «отображение подсказки» и появляется при перемещении указателя мыши над фигурой.</span><span class="sxs-lookup"><span data-stu-id="850b6-125">The title of the shape is "ToolTip display" and will appear when the mouse pointer moves over the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="850b6-126">[Пример атрибута Title](/previous-versions/bb264097(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="850b6-126">[Title Attribute Example](/previous-versions/bb264097(v=vs.85)).</span></span> <span data-ttu-id="850b6-127">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="850b6-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 