---
title: Атрибут оттенков VML
description: Атрибут оттенков VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413174"
---
# <a name="vml-grayscale-attribute"></a><span data-ttu-id="19d92-103">Атрибут оттенков VML</span><span class="sxs-lookup"><span data-stu-id="19d92-103">VML GrayScale Attribute</span></span>

<span data-ttu-id="19d92-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="19d92-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="19d92-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="19d92-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="19d92-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="19d92-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="19d92-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="19d92-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="19d92-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="19d92-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="19d92-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="19d92-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="19d92-110">Определяет, будет ли изображение отображаться в режиме градаций серого.</span><span class="sxs-lookup"><span data-stu-id="19d92-110">Determines whether a picture will be displayed in grayscale mode.</span></span> <span data-ttu-id="19d92-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="19d92-111">Read/write.</span></span> <span data-ttu-id="19d92-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="19d92-112">**VgTriState**.</span></span>

<span data-ttu-id="19d92-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="19d92-113">**Applies To**</span></span>

[<span data-ttu-id="19d92-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="19d92-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="19d92-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="19d92-115">**Tag Syntax**</span></span>

<span data-ttu-id="19d92-116"><v: градации серого *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="19d92-116"><v: *element* grayscale=" *expression* "></span></span>

<span data-ttu-id="19d92-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="19d92-117">**Script Syntax**</span></span>

<span data-ttu-id="19d92-118">*element* . градации серого = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="19d92-118">*element* .grayscale="*expression*"</span></span>

<span data-ttu-id="19d92-119">*выражение* = *element*. оттенки серого</span><span class="sxs-lookup"><span data-stu-id="19d92-119">*expression*=*element*.grayscale</span></span>

<span data-ttu-id="19d92-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="19d92-120">**Remarks**</span></span>

<span data-ttu-id="19d92-121">Если **значение — true**, изображение будет отображаться в оттенках серого вместо цвета.</span><span class="sxs-lookup"><span data-stu-id="19d92-121">If **True**, the picture will be displayed in grayscale instead of color.</span></span> <span data-ttu-id="19d92-122">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="19d92-122">The default is **False**.</span></span>

<span data-ttu-id="19d92-123">Значение основано на КЦИР рекомендации 709, что соответствует более зеленому весу и дает более привлекательные результаты для естественного цвета.</span><span class="sxs-lookup"><span data-stu-id="19d92-123">The value is based according to CCIR recommendation 709, which favors more green weight and produces more pleasing results for natural color.</span></span>

<span data-ttu-id="19d92-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="19d92-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="19d92-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="19d92-125">**Example**</span></span>

<span data-ttu-id="19d92-126">Изображение будет отображаться в оттенках серого вместо цвета.</span><span class="sxs-lookup"><span data-stu-id="19d92-126">The image will be displayed in grayscale instead of color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 