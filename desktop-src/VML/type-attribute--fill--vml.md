---
title: Атрибут Type (Fill) (VML)
description: Атрибут Type (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792756"
---
# <a name="type-attribute-fillvml"></a><span data-ttu-id="358c0-103">Атрибут Type (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="358c0-103">Type Attribute (Fill)(VML)</span></span>

<span data-ttu-id="358c0-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="358c0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="358c0-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="358c0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="358c0-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="358c0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="358c0-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="358c0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="358c0-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="358c0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="358c0-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="358c0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="358c0-110">Определяет тип заливки.</span><span class="sxs-lookup"><span data-stu-id="358c0-110">Determines the type of fill.</span></span> <span data-ttu-id="358c0-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="358c0-111">Read/write.</span></span> <span data-ttu-id="358c0-112">**Вгфиллтипе**.</span><span class="sxs-lookup"><span data-stu-id="358c0-112">**VgFillType**.</span></span>

<span data-ttu-id="358c0-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="358c0-113">**Applies To**</span></span>

[<span data-ttu-id="358c0-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="358c0-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="358c0-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="358c0-115">**Tag Syntax**</span></span>

<span data-ttu-id="358c0-116"><v: *element* Type = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="358c0-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="358c0-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="358c0-117">**Script Syntax**</span></span>

<span data-ttu-id="358c0-118">*element* . Type = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="358c0-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="358c0-119">*выражение* = *element*. Type</span><span class="sxs-lookup"><span data-stu-id="358c0-119">*expression*=*element*.type</span></span>

<span data-ttu-id="358c0-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="358c0-120">**Remarks**</span></span>

<span data-ttu-id="358c0-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="358c0-121">Values include:</span></span>



| <span data-ttu-id="358c0-122">Тип</span><span class="sxs-lookup"><span data-stu-id="358c0-122">Type</span></span>           | <span data-ttu-id="358c0-123">Описание</span><span class="sxs-lookup"><span data-stu-id="358c0-123">Description</span></span>                                                             |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="358c0-124">основ</span><span class="sxs-lookup"><span data-stu-id="358c0-124">solid</span></span>          | <span data-ttu-id="358c0-125">Шаблон заливки является сплошным.</span><span class="sxs-lookup"><span data-stu-id="358c0-125">The fill pattern is solid.</span></span> <span data-ttu-id="358c0-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="358c0-126">Default.</span></span>                                     |
| <span data-ttu-id="358c0-127">градиент</span><span class="sxs-lookup"><span data-stu-id="358c0-127">gradient</span></span>       | <span data-ttu-id="358c0-128">Цвета заливки смешиваются вместе в линейном градиенте от нижнего к верхнему.</span><span class="sxs-lookup"><span data-stu-id="358c0-128">The fill colors blend together in a linear gradient from bottom to top.</span></span> |
| <span data-ttu-id="358c0-129">градиентрадиал</span><span class="sxs-lookup"><span data-stu-id="358c0-129">gradientradial</span></span> | <span data-ttu-id="358c0-130">Цвета заливки смешиваются вместе в радиальном градиенте.</span><span class="sxs-lookup"><span data-stu-id="358c0-130">The fill colors blend together in a radial gradient.</span></span>                    |
| <span data-ttu-id="358c0-131">tile</span><span class="sxs-lookup"><span data-stu-id="358c0-131">tile</span></span>           | <span data-ttu-id="358c0-132">Изображение заливки заполняется мозаикой.</span><span class="sxs-lookup"><span data-stu-id="358c0-132">The fill image is tiled.</span></span>                                                |
| <span data-ttu-id="358c0-133">pattern</span><span class="sxs-lookup"><span data-stu-id="358c0-133">pattern</span></span>        | <span data-ttu-id="358c0-134">Изображение используется для создания узора с использованием цветов заливки.</span><span class="sxs-lookup"><span data-stu-id="358c0-134">The image is used to create a pattern using the fill colors.</span></span>            |
| <span data-ttu-id="358c0-135">frame</span><span class="sxs-lookup"><span data-stu-id="358c0-135">frame</span></span>          | <span data-ttu-id="358c0-136">Изображение растягивается для заполнения фигуры.</span><span class="sxs-lookup"><span data-stu-id="358c0-136">The image is stretched to fill the shape.</span></span>                               |



 

<span data-ttu-id="358c0-137">**Стандартный атрибут VML**</span><span class="sxs-lookup"><span data-stu-id="358c0-137">**VML Standard Attribute**</span></span>

<span data-ttu-id="358c0-138">**Пример**</span><span class="sxs-lookup"><span data-stu-id="358c0-138">**Example**</span></span>

<span data-ttu-id="358c0-139">Красный цвет фона и синяя заливка создаются с использованием шаблона myimage.gif изображения.</span><span class="sxs-lookup"><span data-stu-id="358c0-139">A red foreground and blue background fill is created using the pattern of the image myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 