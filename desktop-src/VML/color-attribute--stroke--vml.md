---
title: Атрибут цвета (Stroke) (VML)
description: Атрибут цвета (Stroke) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691614"
---
# <a name="color-attribute-strokevml"></a><span data-ttu-id="f793c-103">Атрибут цвета (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="f793c-103">Color Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="f793c-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f793c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f793c-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f793c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f793c-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f793c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f793c-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f793c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f793c-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f793c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f793c-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f793c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f793c-110">Определяет цвет штриха.</span><span class="sxs-lookup"><span data-stu-id="f793c-110">Defines the color of a stroke.</span></span> <span data-ttu-id="f793c-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f793c-111">Read/write.</span></span> <span data-ttu-id="f793c-112">**Вгколор**.</span><span class="sxs-lookup"><span data-stu-id="f793c-112">**VgColor**.</span></span>

<span data-ttu-id="f793c-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="f793c-113">**Applies To**</span></span>

[<span data-ttu-id="f793c-114">Водок</span><span class="sxs-lookup"><span data-stu-id="f793c-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="f793c-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="f793c-115">**Tag Syntax**</span></span>

<span data-ttu-id="f793c-116"><v: Color *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="f793c-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="f793c-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="f793c-117">**Script Syntax**</span></span>

<span data-ttu-id="f793c-118">*element* . Color = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="f793c-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="f793c-119">*выражение* = *элемент*. Color</span><span class="sxs-lookup"><span data-stu-id="f793c-119">*expression*=*element*.color</span></span>

<span data-ttu-id="f793c-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="f793c-120">**Remarks**</span></span>

<span data-ttu-id="f793c-121">Переопределяет атрибут **строкеколор** фигуры.</span><span class="sxs-lookup"><span data-stu-id="f793c-121">Overrides the **StrokeColor** attribute of a shape.</span></span> <span data-ttu-id="f793c-122">Значение по умолчанию — **Black**.</span><span class="sxs-lookup"><span data-stu-id="f793c-122">The default value is **black**.</span></span>

<span data-ttu-id="f793c-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="f793c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f793c-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="f793c-124">**Example**</span></span>

<span data-ttu-id="f793c-125">Фигура имеет **зеленый** цвет обводки, а не **красный**.</span><span class="sxs-lookup"><span data-stu-id="f793c-125">The shape has a stroke color of **green**, not **red**.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 