---
title: Атрибут видимости VML
description: Атрибут видимости VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691560"
---
# <a name="vml-visibility-attribute"></a><span data-ttu-id="6bb83-103">Атрибут видимости VML</span><span class="sxs-lookup"><span data-stu-id="6bb83-103">VML Visibility Attribute</span></span>

<span data-ttu-id="6bb83-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6bb83-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6bb83-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6bb83-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6bb83-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6bb83-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6bb83-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6bb83-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6bb83-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6bb83-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6bb83-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6bb83-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6bb83-110">Определяет, отображается ли фигура.</span><span class="sxs-lookup"><span data-stu-id="6bb83-110">Determines whether a shape is displayed.</span></span> <span data-ttu-id="6bb83-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6bb83-111">Read/write.</span></span> <span data-ttu-id="6bb83-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="6bb83-112">**String**.</span></span>

<span data-ttu-id="6bb83-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6bb83-113">**Applies To**</span></span>

[<span data-ttu-id="6bb83-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="6bb83-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="6bb83-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6bb83-115">**Tag Syntax**</span></span>

<span data-ttu-id="6bb83-116"><v: Style *элемента* = "Visibility: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="6bb83-116"><v: *element* style="visibility: *expression* "></span></span>

<span data-ttu-id="6bb83-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="6bb83-117">**Script Syntax**</span></span>

<span data-ttu-id="6bb83-118">*element* . Style. Visibility = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="6bb83-118">*element* .style.visibility="*expression*"</span></span>

<span data-ttu-id="6bb83-119">*выражение* = *элемент*. Style. Visibility</span><span class="sxs-lookup"><span data-stu-id="6bb83-119">*expression*=*element*.style.visibility</span></span>

<span data-ttu-id="6bb83-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6bb83-120">**Remarks**</span></span>

<span data-ttu-id="6bb83-121">Атрибут **видимости** аналогичен стандартному атрибуту **видимости** HTML для стилей.</span><span class="sxs-lookup"><span data-stu-id="6bb83-121">The **Visibility** attribute is similar to the standard HTML **Visibility** attribute for styles.</span></span>

<span data-ttu-id="6bb83-122">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="6bb83-122">Values include:</span></span>



| <span data-ttu-id="6bb83-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6bb83-123">Value</span></span>    | <span data-ttu-id="6bb83-124">Описание</span><span class="sxs-lookup"><span data-stu-id="6bb83-124">Description</span></span>                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb83-125">visible</span><span class="sxs-lookup"><span data-stu-id="6bb83-125">visible</span></span>  | <span data-ttu-id="6bb83-126">Фигура является видимой.</span><span class="sxs-lookup"><span data-stu-id="6bb83-126">The shape is visible.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="6bb83-127">hidden</span><span class="sxs-lookup"><span data-stu-id="6bb83-127">hidden</span></span>   | <span data-ttu-id="6bb83-128">Фигура не видна, но по-прежнему является частью последовательности объектов в браузере.</span><span class="sxs-lookup"><span data-stu-id="6bb83-128">The shape is not visible, but is still part of the flow of the objects in the browser.</span></span> <span data-ttu-id="6bb83-129">События мыши не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="6bb83-129">Mouse events are not processed.</span></span>                                                                  |
| <span data-ttu-id="6bb83-130">inherit</span><span class="sxs-lookup"><span data-stu-id="6bb83-130">inherit</span></span>  | <span data-ttu-id="6bb83-131">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6bb83-131">Default.</span></span> <span data-ttu-id="6bb83-132">Состояние видимости наследуется от родителя фигуры.</span><span class="sxs-lookup"><span data-stu-id="6bb83-132">The visibility state is inherited from the parent of the shape.</span></span> <span data-ttu-id="6bb83-133">Microsoft Office приложения используют только **наследование** и **Скрытие**; все остальные значения сопоставляются с **наследованием**.</span><span class="sxs-lookup"><span data-stu-id="6bb83-133">Microsoft Office applications only use **inherit** and **hidden**; any other values are mapped to **inherit**.</span></span> |
| <span data-ttu-id="6bb83-134">Свертывание</span><span class="sxs-lookup"><span data-stu-id="6bb83-134">collapse</span></span> | <span data-ttu-id="6bb83-135">Используется для графических редакторов, которые могут сворачивать группы фигур; Например, «вкладыши».</span><span class="sxs-lookup"><span data-stu-id="6bb83-135">Used for graphical editing applications that can collapse groups of shapes; for example, outliners.</span></span>                                                                                     |



 

<span data-ttu-id="6bb83-136">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="6bb83-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="6bb83-137">**Пример**</span><span class="sxs-lookup"><span data-stu-id="6bb83-137">**Example**</span></span>

<span data-ttu-id="6bb83-138">Следующий код создает фигуру, но делает ее скрытой.</span><span class="sxs-lookup"><span data-stu-id="6bb83-138">The following code creates a shape but makes it hidden.</span></span> <span data-ttu-id="6bb83-139">Другие объекты в документе будут обтекать его, и в нем останется пробел, равный размеру фигуры.</span><span class="sxs-lookup"><span data-stu-id="6bb83-139">Other objects in the document will flow around it, leaving a space the same size as the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



<span data-ttu-id="6bb83-140">[Пример атрибута видимости](/previous-versions/bb264100(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6bb83-140">[Visibility Attribute Example](/previous-versions/bb264100(v=vs.85)).</span></span> <span data-ttu-id="6bb83-141">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="6bb83-141">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 