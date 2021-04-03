---
title: Атрибут src (Stroke) (VML)
description: Атрибут src (Stroke) (VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791808"
---
# <a name="src-attribute-strokevml"></a><span data-ttu-id="82b02-103">Атрибут src (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="82b02-103">Src Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="82b02-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="82b02-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="82b02-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="82b02-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="82b02-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="82b02-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="82b02-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82b02-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="82b02-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="82b02-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="82b02-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="82b02-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="82b02-110">Определяет исходное изображение для загрузки для заливки штриха.</span><span class="sxs-lookup"><span data-stu-id="82b02-110">Defines the source image to load for a stroke fill.</span></span> <span data-ttu-id="82b02-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="82b02-111">Read/write.</span></span> <span data-ttu-id="82b02-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="82b02-112">**String**.</span></span>

<span data-ttu-id="82b02-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="82b02-113">**Applies To**</span></span>

[<span data-ttu-id="82b02-114">Водок</span><span class="sxs-lookup"><span data-stu-id="82b02-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="82b02-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="82b02-115">**Tag Syntax**</span></span>

<span data-ttu-id="82b02-116"><v: *элемент* src = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="82b02-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="82b02-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="82b02-117">**Script Syntax**</span></span>

<span data-ttu-id="82b02-118">*element* . src = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="82b02-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="82b02-119">*выражение* = *элемент*. src</span><span class="sxs-lookup"><span data-stu-id="82b02-119">*expression*=*element*.src</span></span>

<span data-ttu-id="82b02-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="82b02-120">**Remarks**</span></span>

<span data-ttu-id="82b02-121">URL-адрес изображения, загружаемого для изображений и узорных заливок.</span><span class="sxs-lookup"><span data-stu-id="82b02-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="82b02-122">Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="82b02-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="82b02-123">Если этот атрибут встречается отдельно, то есть без **href** или **Title**, то изображение связывается.</span><span class="sxs-lookup"><span data-stu-id="82b02-123">If this attribute appears alone, that is, no **HRef** or **Title**, then the image is linked.</span></span>

<span data-ttu-id="82b02-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="82b02-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="82b02-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="82b02-125">**Example**</span></span>

<span data-ttu-id="82b02-126">Штрих создается с изображением, указанным в файле cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="82b02-126">The stroke is created with the image specified by the cylinder.gif file.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 