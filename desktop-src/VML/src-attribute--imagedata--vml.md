---
title: Атрибут src (Имажедата) (VML)
description: Атрибут src (Имажедата) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070067"
---
# <a name="src-attribute-imagedatavml"></a><span data-ttu-id="92beb-103">Атрибут src (Имажедата) (VML)</span><span class="sxs-lookup"><span data-stu-id="92beb-103">Src Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="92beb-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="92beb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="92beb-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="92beb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="92beb-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="92beb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="92beb-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="92beb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="92beb-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="92beb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="92beb-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="92beb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="92beb-110">Определяет источник изображения.</span><span class="sxs-lookup"><span data-stu-id="92beb-110">Defines a source for the image.</span></span> <span data-ttu-id="92beb-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="92beb-111">Read/write.</span></span> <span data-ttu-id="92beb-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="92beb-112">**String**.</span></span>

<span data-ttu-id="92beb-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="92beb-113">**Applies To**</span></span>

[<span data-ttu-id="92beb-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="92beb-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="92beb-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="92beb-115">**Tag Syntax**</span></span>

<span data-ttu-id="92beb-116"><v: *элемент* src = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="92beb-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="92beb-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="92beb-117">**Script Syntax**</span></span>

<span data-ttu-id="92beb-118">*element* . src = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="92beb-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="92beb-119">*выражение* = *элемент*. src</span><span class="sxs-lookup"><span data-stu-id="92beb-119">*expression*=*element*.src</span></span>

<span data-ttu-id="92beb-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="92beb-120">**Remarks**</span></span>

<span data-ttu-id="92beb-121">Этот атрибут должен всегда использоваться с элементом [имажедата](msdn-online-vml-imagedata-element.md) и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="92beb-121">This attribute must always be used with the [ImageData](msdn-online-vml-imagedata-element.md) element and point to valid image data for a picture to be displayed.</span></span> <span data-ttu-id="92beb-122">Если этот атрибут отображается без [href](https://www.bing.com/search?q=HRef) или [Title](title-attribute--imagedata--vml.md), то это изображение связывается.</span><span class="sxs-lookup"><span data-stu-id="92beb-122">If this attribute appears without [HRef](https://www.bing.com/search?q=HRef) or [Title](title-attribute--imagedata--vml.md), then the image is linked.</span></span>

<span data-ttu-id="92beb-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="92beb-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="92beb-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="92beb-124">**Example**</span></span>

<span data-ttu-id="92beb-125">Источником изображения является файл с именем "kids.jpg".</span><span class="sxs-lookup"><span data-stu-id="92beb-125">The source of the image is a file named "kids.jpg".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 