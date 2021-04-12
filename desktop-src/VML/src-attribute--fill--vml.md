---
title: Атрибут src (Fill) (VML)
description: Атрибут src (Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487761"
---
# <a name="src-attribute-fillvml"></a><span data-ttu-id="7e8d4-103">Атрибут src (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="7e8d4-103">Src Attribute (Fill)(VML)</span></span>

<span data-ttu-id="7e8d4-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7e8d4-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7e8d4-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7e8d4-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7e8d4-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7e8d4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7e8d4-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7e8d4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7e8d4-110">Определяет изображение, которое загружается для заполнения.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-110">Defines the image to load for a fill.</span></span> <span data-ttu-id="7e8d4-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-111">Read/write.</span></span> <span data-ttu-id="7e8d4-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-112">**String**.</span></span>

<span data-ttu-id="7e8d4-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="7e8d4-113">**Applies To**</span></span>

[<span data-ttu-id="7e8d4-114">Заполнить</span><span class="sxs-lookup"><span data-stu-id="7e8d4-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="7e8d4-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="7e8d4-115">**Tag Syntax**</span></span>

<span data-ttu-id="7e8d4-116"><v: *элемент* src = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="7e8d4-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="7e8d4-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="7e8d4-117">**Script Syntax**</span></span>

<span data-ttu-id="7e8d4-118">*element* . src = "*выражение \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="7e8d4-118">*element* .src="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="7e8d4-119">*выражение* = *элемент*. src</span><span class="sxs-lookup"><span data-stu-id="7e8d4-119">*expression*=*element*.src</span></span>

<span data-ttu-id="7e8d4-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="7e8d4-120">**Remarks**</span></span>

<span data-ttu-id="7e8d4-121">URL-адрес изображения, загружаемого для изображений и узорных заливок.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="7e8d4-122">Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="7e8d4-123">Если этот атрибут встречается отдельно (то есть отсутствует атрибут **href** или **Title** ), то изображение связывается.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-123">If this attribute appears alone (that is, no **HRef** or **Title** attribute), then the image is linked.</span></span>

<span data-ttu-id="7e8d4-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="7e8d4-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="7e8d4-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="7e8d4-125">**Example**</span></span>

<span data-ttu-id="7e8d4-126">Отображается мозаичное изображение, использующее файл myimage.gif в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="7e8d4-126">A tiled image using the file myimage.gif as a source is displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 