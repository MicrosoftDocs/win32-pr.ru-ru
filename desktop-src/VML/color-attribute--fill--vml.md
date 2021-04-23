---
title: Атрибут цвета (Fill) (VML)
description: Атрибут цвета (Fill) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487773"
---
# <a name="color-attribute-fillvml"></a><span data-ttu-id="37d89-103">Атрибут цвета (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="37d89-103">Color Attribute (Fill)(VML)</span></span>

<span data-ttu-id="37d89-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="37d89-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="37d89-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="37d89-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="37d89-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="37d89-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="37d89-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="37d89-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="37d89-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="37d89-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="37d89-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="37d89-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="37d89-110">Определяет цвет заливки.</span><span class="sxs-lookup"><span data-stu-id="37d89-110">Defines the color of a fill.</span></span> <span data-ttu-id="37d89-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="37d89-111">Read/write.</span></span> <span data-ttu-id="37d89-112">**Вгколор**.</span><span class="sxs-lookup"><span data-stu-id="37d89-112">**VgColor**.</span></span>

<span data-ttu-id="37d89-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="37d89-113">**Applies To**</span></span>

[<span data-ttu-id="37d89-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="37d89-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="37d89-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="37d89-115">**Tag Syntax**</span></span>

<span data-ttu-id="37d89-116"><v: Color *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="37d89-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="37d89-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="37d89-117">**Script Syntax**</span></span>

<span data-ttu-id="37d89-118">*element* . Color = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="37d89-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="37d89-119">*выражение* = *элемент*. Color</span><span class="sxs-lookup"><span data-stu-id="37d89-119">*expression*=*element*.color</span></span>

<span data-ttu-id="37d89-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="37d89-120">**Remarks**</span></span>

<span data-ttu-id="37d89-121">Переопределяет атрибут **FillColor** фигуры.</span><span class="sxs-lookup"><span data-stu-id="37d89-121">Overrides the **FillColor** attribute of a shape.</span></span> <span data-ttu-id="37d89-122">Значение по умолчанию — **белый**.</span><span class="sxs-lookup"><span data-stu-id="37d89-122">The default value is **White**.</span></span>

<span data-ttu-id="37d89-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="37d89-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="37d89-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="37d89-124">**Example**</span></span>

<span data-ttu-id="37d89-125">Цвет заливки фигуры — зеленый.</span><span class="sxs-lookup"><span data-stu-id="37d89-125">The fill color of the shape is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 