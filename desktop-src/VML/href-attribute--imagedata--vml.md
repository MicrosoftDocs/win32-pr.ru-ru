---
title: Атрибут HRef (Имажедата) (VML)
description: Атрибут HRef (Имажедата) (VML)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791724"
---
# <a name="href-attribute-imagedatavml"></a><span data-ttu-id="f44e6-103">Атрибут HRef (Имажедата) (VML)</span><span class="sxs-lookup"><span data-stu-id="f44e6-103">HRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="f44e6-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f44e6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f44e6-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f44e6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f44e6-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f44e6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f44e6-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f44e6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f44e6-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f44e6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f44e6-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f44e6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f44e6-110">Определяет URL-адрес изображения.</span><span class="sxs-lookup"><span data-stu-id="f44e6-110">Defines a URL for an image.</span></span> <span data-ttu-id="f44e6-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f44e6-111">Read/write.</span></span> <span data-ttu-id="f44e6-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="f44e6-112">**String**.</span></span>

<span data-ttu-id="f44e6-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="f44e6-113">**Applies To**</span></span>

[<span data-ttu-id="f44e6-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="f44e6-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="f44e6-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="f44e6-115">**Tag Syntax**</span></span>

<span data-ttu-id="f44e6-116"><v: *element* о:хреф = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="f44e6-116"><v: *element* o:href=" *expression* "></span></span>

<span data-ttu-id="f44e6-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="f44e6-117">**Script Syntax**</span></span>

<span data-ttu-id="f44e6-118">*element* . href = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="f44e6-118">*element* .href="*expression*"</span></span>

<span data-ttu-id="f44e6-119">*выражение* = *element*. href</span><span class="sxs-lookup"><span data-stu-id="f44e6-119">*expression*=*element*.href</span></span>

<span data-ttu-id="f44e6-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="f44e6-120">**Remarks**</span></span>

<span data-ttu-id="f44e6-121">Когда вы щелкните фигуру, браузер загрузит URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f44e6-121">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="f44e6-122">Атрибут **href** аналогичен стандартному атрибуту HTML **href** привязок.</span><span class="sxs-lookup"><span data-stu-id="f44e6-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="f44e6-123">Использование этого атрибута упрощает создание буттонсвис изображений на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="f44e6-123">Using this attribute makes it easy to create buttonswith images on a Web page.</span></span>

<span data-ttu-id="f44e6-124">Этот атрибут используется Microsoft Office только в том случае, если рисунок связан и внедрен. Microsoft Word имеет пользовательский интерфейс для вставки рисунков таким образом.</span><span class="sxs-lookup"><span data-stu-id="f44e6-124">This attribute is used by Microsoft Office only if a picture has been linked and embedded.Microsoft Word has a user interface for inserting pictures this way.</span></span>

<span data-ttu-id="f44e6-125">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="f44e6-125">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="f44e6-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="f44e6-126">**Example**</span></span>

<span data-ttu-id="f44e6-127">Когда вы щелкните изображение, браузер загрузит домашнюю страницу корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f44e6-127">When the image is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 