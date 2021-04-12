---
title: Атрибут Градиентшапеок VML
description: Атрибут Градиентшапеок VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413566"
---
# <a name="vml-gradientshapeok-attribute"></a><span data-ttu-id="6a9b5-103">Атрибут Градиентшапеок VML</span><span class="sxs-lookup"><span data-stu-id="6a9b5-103">VML GradientShapeOK Attribute</span></span>

<span data-ttu-id="6a9b5-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6a9b5-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6a9b5-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6a9b5-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6a9b5-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6a9b5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6a9b5-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6a9b5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6a9b5-110">Определяет, будет ли путь градиента состоять из повторяющихся концентрических путей.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-110">Determines whether a gradient path will be made up of repeated concentric paths.</span></span> <span data-ttu-id="6a9b5-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-111">Read/write.</span></span> <span data-ttu-id="6a9b5-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-112">**VgTriState**.</span></span>

<span data-ttu-id="6a9b5-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6a9b5-113">**Applies To**</span></span>

[<span data-ttu-id="6a9b5-114">Путь</span><span class="sxs-lookup"><span data-stu-id="6a9b5-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="6a9b5-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6a9b5-115">**Tag Syntax**</span></span>

<span data-ttu-id="6a9b5-116"><v: *element* градиентшапеок = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="6a9b5-116"><v: *element* gradientshapeok=" *expression* "></span></span>

<span data-ttu-id="6a9b5-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="6a9b5-117">**Script Syntax**</span></span>

<span data-ttu-id="6a9b5-118">*element* . градиентшапеок = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="6a9b5-118">*element* .gradientshapeok="*expression*"</span></span>

<span data-ttu-id="6a9b5-119">*выражение* = *element*. градиентшапеок</span><span class="sxs-lookup"><span data-stu-id="6a9b5-119">*expression*=*element*.gradientshapeok</span></span>

<span data-ttu-id="6a9b5-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6a9b5-120">**Remarks**</span></span>

<span data-ttu-id="6a9b5-121">Если **значение — true**, путь будет заполнен концентрическим градиентным заполнением с использованием пути как повторяющейся формы градиента. Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-121">If **True**, the path will be filled with a concentric gradient fill using the path as the repeated shape of the gradient.The default is **False**.</span></span>

<span data-ttu-id="6a9b5-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="6a9b5-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="6a9b5-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="6a9b5-123">**Example**</span></span>

<span data-ttu-id="6a9b5-124">Путь будет заполнен концентрическим градиентным заполнением, который состоит из повторяющихся прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="6a9b5-124">The path will be filled with a concentric gradient fill made up of repeated rectangles.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 