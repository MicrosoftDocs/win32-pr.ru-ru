---
title: Атрибут VML MSO-Mode
description: Атрибут VML MSO-Mode
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338092"
---
# <a name="vml-mso-wrap-mode-attribute"></a><span data-ttu-id="449a5-103">Атрибут VML MSO-Mode</span><span class="sxs-lookup"><span data-stu-id="449a5-103">VML MSO-Wrap-Mode Attribute</span></span>

<span data-ttu-id="449a5-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="449a5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="449a5-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="449a5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="449a5-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="449a5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="449a5-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="449a5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="449a5-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="449a5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="449a5-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="449a5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="449a5-110">Определяет режим переноса текста.</span><span class="sxs-lookup"><span data-stu-id="449a5-110">Defines the wrapping mode for text.</span></span> <span data-ttu-id="449a5-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="449a5-111">Read/write.</span></span> <span data-ttu-id="449a5-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="449a5-112">**String**.</span></span>

<span data-ttu-id="449a5-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="449a5-113">**Applies To**</span></span>

[<span data-ttu-id="449a5-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="449a5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="449a5-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="449a5-115">**Tag Syntax**</span></span>

<span data-ttu-id="449a5-116"><v: Style *элемента* = "MSO-Wrap-Mode: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="449a5-116"><v: *element* style="mso-wrap-mode: *expression* "></span></span>

<span data-ttu-id="449a5-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="449a5-117">**Remarks**</span></span>

<span data-ttu-id="449a5-118">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="449a5-118">Values include:</span></span>



| <span data-ttu-id="449a5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="449a5-119">Value</span></span>          | <span data-ttu-id="449a5-120">Описание</span><span class="sxs-lookup"><span data-stu-id="449a5-120">Description</span></span>                          |
|----------------|--------------------------------------|
| <span data-ttu-id="449a5-121">square</span><span class="sxs-lookup"><span data-stu-id="449a5-121">square</span></span>         | <span data-ttu-id="449a5-122">Заключает текст вокруг фигуры в квадрат.</span><span class="sxs-lookup"><span data-stu-id="449a5-122">Wraps text around shape in a square.</span></span> |
| <span data-ttu-id="449a5-123">тесная</span><span class="sxs-lookup"><span data-stu-id="449a5-123">tight</span></span>          | <span data-ttu-id="449a5-124">Текст переносится вблизи фигуры.</span><span class="sxs-lookup"><span data-stu-id="449a5-124">Text is wrapped close to the shape.</span></span>  |
| <span data-ttu-id="449a5-125">сверху вниз</span><span class="sxs-lookup"><span data-stu-id="449a5-125">top-and-bottom</span></span> | <span data-ttu-id="449a5-126">Текст переходит сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="449a5-126">Text jumps from top to bottom.</span></span>       |
| <span data-ttu-id="449a5-127">по</span><span class="sxs-lookup"><span data-stu-id="449a5-127">through</span></span>        | <span data-ttu-id="449a5-128">Текст отображается через фигуру.</span><span class="sxs-lookup"><span data-stu-id="449a5-128">Text displays through the shape.</span></span>     |
| <span data-ttu-id="449a5-129">нет</span><span class="sxs-lookup"><span data-stu-id="449a5-129">none</span></span>           | <span data-ttu-id="449a5-130">Текст не переносится.</span><span class="sxs-lookup"><span data-stu-id="449a5-130">Text doesn't wrap.</span></span>                   |



 

<span data-ttu-id="449a5-131">Используется в Microsoft PowerPoint для сохранения в формате HTML, чтобы указать, включено ли перетекание слов в автофигуре (**квадрат**) или выключено (**нет**).</span><span class="sxs-lookup"><span data-stu-id="449a5-131">Used by Microsoft PowerPoint for saving to HTML to indicate whether word wrap inside an AutoShape is on (**square**) or off (**none**).</span></span>

<span data-ttu-id="449a5-132">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="449a5-132">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="449a5-133">**Пример**</span><span class="sxs-lookup"><span data-stu-id="449a5-133">**Example**</span></span>

<span data-ttu-id="449a5-134">Следующий код показывает, что в PowerPoint включена функция переноса слов в автофигуре.</span><span class="sxs-lookup"><span data-stu-id="449a5-134">The following code indicates that wordwrap inside an AutoShape is turned on in PowerPoint.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 