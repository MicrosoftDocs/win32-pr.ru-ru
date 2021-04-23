---
title: Атрибут размера (Fill) (VML)
description: Атрибут размера (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987573"
---
# <a name="size-attribute-fillvml"></a><span data-ttu-id="3bbd8-103">Атрибут размера (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="3bbd8-103">Size Attribute (Fill)(VML)</span></span>

<span data-ttu-id="3bbd8-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3bbd8-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3bbd8-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3bbd8-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3bbd8-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3bbd8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3bbd8-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3bbd8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3bbd8-110">Определяет размер изображения для заливки.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-110">Defines the size of the image for the fill.</span></span> <span data-ttu-id="3bbd8-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-111">Read/write.</span></span> <span data-ttu-id="3bbd8-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbd8-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="3bbd8-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="3bbd8-113">**Applies To**</span></span>

[<span data-ttu-id="3bbd8-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="3bbd8-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="3bbd8-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="3bbd8-115">**Tag Syntax**</span></span>

<span data-ttu-id="3bbd8-116"><v: size *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="3bbd8-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="3bbd8-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="3bbd8-117">**Script Syntax**</span></span>

<span data-ttu-id="3bbd8-118">*element* . size = "*выражение \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="3bbd8-118">*element* .size="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="3bbd8-119">*выражение* = *элемент*. размер</span><span class="sxs-lookup"><span data-stu-id="3bbd8-119">*expression*=*element*.size</span></span>

<span data-ttu-id="3bbd8-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3bbd8-120">**Remarks**</span></span>

<span data-ttu-id="3bbd8-121">Значение по умолчанию — размер исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-121">The default is the size of the original image.</span></span> <span data-ttu-id="3bbd8-122">Размеры, превышающие размер шапевилл, отображают увеличенную, но обрезанную версию изображения.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-122">Sizes that are larger than the shapewill display a magnified but clipped version of the image.</span></span>

<span data-ttu-id="3bbd8-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="3bbd8-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3bbd8-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="3bbd8-124">**Example**</span></span>

<span data-ttu-id="3bbd8-125">Несмотря на то, что исходный размер изображения составляет 50 точек по 50, изображение будет отображаться в центре заливки в виде 10-на 10 изображений.</span><span class="sxs-lookup"><span data-stu-id="3bbd8-125">Even though the original size of the image is 50-by-50 points, the image will be displayed as a 10-by-10 image in the center of the fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 