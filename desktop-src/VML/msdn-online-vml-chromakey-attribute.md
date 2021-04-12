---
title: Атрибут Чромакэй VML
description: Атрибут Чромакэй VML
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338140"
---
# <a name="vml-chromakey-attribute"></a><span data-ttu-id="f6133-103">Атрибут Чромакэй VML</span><span class="sxs-lookup"><span data-stu-id="f6133-103">VML Chromakey Attribute</span></span>

<span data-ttu-id="f6133-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f6133-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f6133-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f6133-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f6133-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f6133-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f6133-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f6133-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f6133-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f6133-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f6133-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f6133-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f6133-110">Определяет значение цвета изображения, которое будет считаться прозрачным.</span><span class="sxs-lookup"><span data-stu-id="f6133-110">Defines the color value of the image that will be treated as transparent.</span></span> <span data-ttu-id="f6133-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f6133-111">Read/write.</span></span> <span data-ttu-id="f6133-112">**Вгколор**.</span><span class="sxs-lookup"><span data-stu-id="f6133-112">**VgColor**.</span></span>

<span data-ttu-id="f6133-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="f6133-113">**Applies To**</span></span>

[<span data-ttu-id="f6133-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="f6133-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="f6133-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="f6133-115">**Tag Syntax**</span></span>

<span data-ttu-id="f6133-116"><v: *element* чромакэй = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="f6133-116"><v: *element* chromakey=" *expression* "></span></span>

<span data-ttu-id="f6133-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="f6133-117">**Script Syntax**</span></span>

<span data-ttu-id="f6133-118">*element* . чромакэй = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="f6133-118">*element* .chromakey="*expression*"</span></span>

<span data-ttu-id="f6133-119">*выражение* = *element*. чромакэй</span><span class="sxs-lookup"><span data-stu-id="f6133-119">*expression*=*element*.chromakey</span></span>

<span data-ttu-id="f6133-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="f6133-120">**Remarks**</span></span>

<span data-ttu-id="f6133-121">Используйте этот атрибут, чтобы сделать части изображения прозрачными с помощью ключа прозрачности к определенному цвету.</span><span class="sxs-lookup"><span data-stu-id="f6133-121">Use this attribute to make parts of an image transparent by keying the transparency to a specific color.</span></span> <span data-ttu-id="f6133-122">Например, если сделать значение **чромакэй** **черным**, то любая часть изображения, которая является черновой, будет прозрачной, а цвет заливки будет отображаться в этой части изображения.</span><span class="sxs-lookup"><span data-stu-id="f6133-122">For example, if you make the **Chromakey** value **black**, then any portion of the image that is black will be transparent, and the fill color will "show through" that portion of the image.</span></span>

<span data-ttu-id="f6133-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="f6133-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f6133-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="f6133-124">**Example**</span></span>

<span data-ttu-id="f6133-125">Области изображения со сплошным черным цветом становятся прозрачными, что позволяет отображать зеленый цвет заливки через эти области.</span><span class="sxs-lookup"><span data-stu-id="f6133-125">The areas of the image that are solid black will become transparent, allowing the green fill color to show through those areas instead.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 