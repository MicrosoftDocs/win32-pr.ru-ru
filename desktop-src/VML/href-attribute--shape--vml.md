---
title: Атрибут HRef (Shape) (VML)
description: Атрибут HRef (Shape) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070530"
---
# <a name="href-attribute-shapevml"></a><span data-ttu-id="9b7f2-103">Атрибут HRef (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="9b7f2-103">HRef Attribute (Shape)(VML)</span></span>

<span data-ttu-id="9b7f2-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9b7f2-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9b7f2-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9b7f2-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9b7f2-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9b7f2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9b7f2-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9b7f2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9b7f2-110">Определяет URL-адрес для фигуры.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-110">Defines a URL for a shape.</span></span> <span data-ttu-id="9b7f2-111">Когда вы щелкните фигуру, браузер загрузит URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-111">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="9b7f2-112">Read/write.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-112">Read/write.</span></span> <span data-ttu-id="9b7f2-113">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-113">**String**.</span></span>

<span data-ttu-id="9b7f2-114">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="9b7f2-114">**Applies To**</span></span>

[<span data-ttu-id="9b7f2-115">Фигурная</span><span class="sxs-lookup"><span data-stu-id="9b7f2-115">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="9b7f2-116">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="9b7f2-116">**Tag Syntax**</span></span>

<span data-ttu-id="9b7f2-117"><v: *элемент* href = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="9b7f2-117"><v: *element* href=" *expression* "></span></span>

<span data-ttu-id="9b7f2-118">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="9b7f2-118">**Script Syntax**</span></span>

<span data-ttu-id="9b7f2-119">*element* . href = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="9b7f2-119">*element* .href="*expression*"</span></span>

<span data-ttu-id="9b7f2-120">*выражение* = *element*. href</span><span class="sxs-lookup"><span data-stu-id="9b7f2-120">*expression*=*element*.href</span></span>

<span data-ttu-id="9b7f2-121">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="9b7f2-121">**Remarks**</span></span>

<span data-ttu-id="9b7f2-122">Атрибут **href** аналогичен стандартному атрибуту HTML **href** привязок.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="9b7f2-123">Использование **href** упрощает создание интересных кнопок на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-123">Using **HRef** makes it easy to create interesting buttons on a Web page.</span></span>

<span data-ttu-id="9b7f2-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="9b7f2-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="9b7f2-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="9b7f2-125">**Example**</span></span>

<span data-ttu-id="9b7f2-126">Когда вы щелкните прямоугольник, браузер загрузит домашнюю страницу корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9b7f2-126">When the rectangle is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



<span data-ttu-id="9b7f2-127">[Пример атрибута href](/previous-versions/bb229672(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9b7f2-127">[HRef Attribute Example](/previous-versions/bb229672(v=vs.85)).</span></span> <span data-ttu-id="9b7f2-128">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="9b7f2-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 