---
title: Атрибут VML Layout-Flow
description: Атрибут VML Layout-Flow
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987672"
---
# <a name="vml-layout-flow-attribute"></a><span data-ttu-id="b7d6c-103">Атрибут VML Layout-Flow</span><span class="sxs-lookup"><span data-stu-id="b7d6c-103">VML Layout-Flow Attribute</span></span>

<span data-ttu-id="b7d6c-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b7d6c-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b7d6c-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b7d6c-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b7d6c-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b7d6c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b7d6c-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b7d6c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b7d6c-110">Определяет поток макета текста в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-110">Determines the flow of the text layout in a textbox.</span></span> <span data-ttu-id="b7d6c-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-111">Read/write.</span></span> <span data-ttu-id="b7d6c-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-112">**String**.</span></span>

<span data-ttu-id="b7d6c-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b7d6c-113">**Applies To**</span></span>

[<span data-ttu-id="b7d6c-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="b7d6c-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="b7d6c-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b7d6c-115">**Tag Syntax**</span></span>

<span data-ttu-id="b7d6c-116"><v: Style *элемента* = "макет-Flow: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b7d6c-116"><v: *element* style="layout-flow: *expression* "></span></span>

<span data-ttu-id="b7d6c-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b7d6c-117">**Remarks**</span></span>

<span data-ttu-id="b7d6c-118">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-118">Values include:</span></span>



| <span data-ttu-id="b7d6c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b7d6c-119">Value</span></span>                  | <span data-ttu-id="b7d6c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b7d6c-120">Description</span></span>                                 |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b7d6c-121">horizontal</span><span class="sxs-lookup"><span data-stu-id="b7d6c-121">horizontal</span></span>             | <span data-ttu-id="b7d6c-122">Текст отображается горизонтально.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-122">Text is displayed horizontally.</span></span> <span data-ttu-id="b7d6c-123">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-123">Default.</span></span>    |
| <span data-ttu-id="b7d6c-124">Вертикаль</span><span class="sxs-lookup"><span data-stu-id="b7d6c-124">vertical</span></span>               | <span data-ttu-id="b7d6c-125">Текст отображается вертикально.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-125">Text is displayed vertically.</span></span>               |
| <span data-ttu-id="b7d6c-126">по вертикали-идеографические</span><span class="sxs-lookup"><span data-stu-id="b7d6c-126">vertical-ideographic</span></span>   | <span data-ttu-id="b7d6c-127">Идеографическая текст отображается вертикально.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-127">Ideographic text is displayed vertically.</span></span>   |
| <span data-ttu-id="b7d6c-128">горизонтально-идеографические</span><span class="sxs-lookup"><span data-stu-id="b7d6c-128">horizontal-ideographic</span></span> | <span data-ttu-id="b7d6c-129">Идеографическая текст отображается горизонтально.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-129">Ideographic text is displayed horizontally.</span></span> |



 

<span data-ttu-id="b7d6c-130">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="b7d6c-130">*VML Standard Attribute*</span></span>

<span data-ttu-id="b7d6c-131">**Пример**</span><span class="sxs-lookup"><span data-stu-id="b7d6c-131">**Example**</span></span>

<span data-ttu-id="b7d6c-132">Поток текста в текстовом поле будет передаваться по вертикали.</span><span class="sxs-lookup"><span data-stu-id="b7d6c-132">The text flow in the textbox will flow vertically.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 