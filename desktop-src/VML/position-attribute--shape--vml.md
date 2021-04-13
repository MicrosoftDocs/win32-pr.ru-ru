---
title: Атрибут расположения (Shape) (VML)
description: Атрибут расположения (Shape) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413633"
---
# <a name="position-attribute-shapevml"></a><span data-ttu-id="7e004-103">Атрибут расположения (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="7e004-103">Position Attribute (Shape)(VML)</span></span>

<span data-ttu-id="7e004-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7e004-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7e004-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7e004-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7e004-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7e004-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7e004-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7e004-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7e004-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7e004-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7e004-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7e004-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7e004-110">Определяет тип позиционирования, используемый для размещения элемента.</span><span class="sxs-lookup"><span data-stu-id="7e004-110">Defines the type of positioning used to place an element.</span></span> <span data-ttu-id="7e004-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="7e004-111">Read/write.</span></span> <span data-ttu-id="7e004-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="7e004-112">**String**.</span></span>

<span data-ttu-id="7e004-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="7e004-113">**Applies To**</span></span>

[<span data-ttu-id="7e004-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="7e004-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="7e004-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="7e004-115">**Tag Syntax**</span></span>

<span data-ttu-id="7e004-116"><v: Style *элемента* = "Расположение: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="7e004-116"><v: *element* style="position: *expression* "></span></span>

<span data-ttu-id="7e004-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="7e004-117">**Script Syntax**</span></span>

<span data-ttu-id="7e004-118">*element* . Style. Disposition = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="7e004-118">*element* .style.position="*expression*"</span></span>

<span data-ttu-id="7e004-119">*выражение* = *element*. Style. положением</span><span class="sxs-lookup"><span data-stu-id="7e004-119">*expression*=*element*.style.position</span></span>

<span data-ttu-id="7e004-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="7e004-120">**Remarks**</span></span>

<span data-ttu-id="7e004-121">Атрибут « **позиционирование** » аналогичен стандартному атрибуту « **позиционирование** HTML», используемому со таблицами стилей.</span><span class="sxs-lookup"><span data-stu-id="7e004-121">The **Position** attribute is similar to the standard HTML **Position** attribute used with style sheets.</span></span>

<span data-ttu-id="7e004-122">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="7e004-122">Values include:</span></span>



| <span data-ttu-id="7e004-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7e004-123">Value</span></span>    | <span data-ttu-id="7e004-124">Описание</span><span class="sxs-lookup"><span data-stu-id="7e004-124">Description</span></span>                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e004-125">static</span><span class="sxs-lookup"><span data-stu-id="7e004-125">static</span></span>   | <span data-ttu-id="7e004-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e004-126">Default.</span></span> <span data-ttu-id="7e004-127">Элемент располагается в соответствии с нормальным потоком страницы.</span><span class="sxs-lookup"><span data-stu-id="7e004-127">The element is positioned according to the normal flow of the page.</span></span> <span data-ttu-id="7e004-128">Атрибуты **верхнего** и **левого угла** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="7e004-128">The **Top** and **Left** attributes are ignored.</span></span> <span data-ttu-id="7e004-129">Если объект привязан встроенным, который происходит только в Microsoft Word, используется это значение.</span><span class="sxs-lookup"><span data-stu-id="7e004-129">If the object is anchored inline, which only happens in Microsoft Word, this value is used.</span></span> |
| <span data-ttu-id="7e004-130">absolute</span><span class="sxs-lookup"><span data-stu-id="7e004-130">absolute</span></span> | <span data-ttu-id="7e004-131">Элемент располагается относительно родителя с использованием атрибутов **верхнего** и **левого** элементов.</span><span class="sxs-lookup"><span data-stu-id="7e004-131">The element is positioned relative to the parent, using the **Top** and **Left** attributes.</span></span> <span data-ttu-id="7e004-132">Это значение используется для перемещаемых объектов Microsoft Word и Microsoft Excel и слайдов Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="7e004-132">This value is used by Microsoft Word and Microsoft Excel floating objects, and Microsoft PowerPoint slides.</span></span>                  |
| <span data-ttu-id="7e004-133">relative</span><span class="sxs-lookup"><span data-stu-id="7e004-133">relative</span></span> | <span data-ttu-id="7e004-134">Элемент располагается в соответствии с нормальным потоком страницы, но используются **верхние** и **левые** атрибуты.</span><span class="sxs-lookup"><span data-stu-id="7e004-134">The element is positioned according to the normal flow of the page, but the **Top** and **Left** attributes are used.</span></span> <span data-ttu-id="7e004-135">Перекрытие перекрывающихся элементов регулируется атрибутом **Z-Index** .</span><span class="sxs-lookup"><span data-stu-id="7e004-135">The overlap of overlapping elements is governed by the **Z-Index** attribute.</span></span>                       |



 

<span data-ttu-id="7e004-136">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="7e004-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="7e004-137">**Пример**</span><span class="sxs-lookup"><span data-stu-id="7e004-137">**Example**</span></span>

<span data-ttu-id="7e004-138">Расположение прямоугольника отображается с использованием *относительного* стиля.</span><span class="sxs-lookup"><span data-stu-id="7e004-138">The position of the rectangle is displayed using the *relative* style.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="7e004-139">[Пример атрибута позиционирования](/previous-versions/bb264090(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7e004-139">[Position Attribute Example](/previous-versions/bb264090(v=vs.85)).</span></span> <span data-ttu-id="7e004-140">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="7e004-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 