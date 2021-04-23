---
title: Атрибут Clip для VML
description: Атрибут Clip для VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691578"
---
# <a name="vml-clip-attribute"></a><span data-ttu-id="06a07-103">Атрибут Clip для VML</span><span class="sxs-lookup"><span data-stu-id="06a07-103">VML Clip Attribute</span></span>

<span data-ttu-id="06a07-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="06a07-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="06a07-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="06a07-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="06a07-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="06a07-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="06a07-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="06a07-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="06a07-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="06a07-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="06a07-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="06a07-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="06a07-110">Определяет, включено ли обрезание.</span><span class="sxs-lookup"><span data-stu-id="06a07-110">Determines whether the clipping is on.</span></span> <span data-ttu-id="06a07-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="06a07-111">Read/write.</span></span> <span data-ttu-id="06a07-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="06a07-112">**VgTriState**.</span></span>

<span data-ttu-id="06a07-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="06a07-113">**Applies To**</span></span>

[<span data-ttu-id="06a07-114">вмлфраме</span><span class="sxs-lookup"><span data-stu-id="06a07-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="06a07-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="06a07-115">**Tag Syntax**</span></span>

<span data-ttu-id="06a07-116"><v: *элемент* Clip = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="06a07-116"><v: *element* clip=" *expression* "></span></span>

<span data-ttu-id="06a07-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="06a07-117">**Script Syntax**</span></span>

<span data-ttu-id="06a07-118">*element* . Clip = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="06a07-118">*element* .clip="*expression*"</span></span>

<span data-ttu-id="06a07-119">*выражение* = *элемент*. Clip</span><span class="sxs-lookup"><span data-stu-id="06a07-119">*expression*=*element*.clip</span></span>

<span data-ttu-id="06a07-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="06a07-120">**Remarks**</span></span>

<span data-ttu-id="06a07-121">Если значение **Clip** равно **false**, фигура будет масштабироваться в соответствии с размерами рамки.</span><span class="sxs-lookup"><span data-stu-id="06a07-121">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="06a07-122">Если **значение равно true**, то все части фигуры, находящиеся за пределами рамки, не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="06a07-122">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="06a07-123">Обратите внимание, что [источник](origin-attribute--vmlframe--vml.md) и [Размер](size-attribute--vmlframe.md) не будут использоваться, если только значение **Clip** не равно **true**.</span><span class="sxs-lookup"><span data-stu-id="06a07-123">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="06a07-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="06a07-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="06a07-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="06a07-125">**Example**</span></span>

<span data-ttu-id="06a07-126">Изображение, определенное во внешнем файле, будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="06a07-126">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 