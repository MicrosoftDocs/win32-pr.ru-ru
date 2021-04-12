---
title: Атрибут стиля VML
description: Атрибут стиля VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487765"
---
# <a name="vml-style-attribute"></a><span data-ttu-id="d5830-103">Атрибут стиля VML</span><span class="sxs-lookup"><span data-stu-id="d5830-103">VML Style Attribute</span></span>

<span data-ttu-id="d5830-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d5830-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d5830-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="d5830-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d5830-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="d5830-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d5830-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d5830-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d5830-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d5830-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d5830-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d5830-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d5830-110">Определяет стиль рамки.</span><span class="sxs-lookup"><span data-stu-id="d5830-110">Defines the style of the frame.</span></span> <span data-ttu-id="d5830-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d5830-111">Read/write.</span></span> <span data-ttu-id="d5830-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="d5830-112">**String**.</span></span>

<span data-ttu-id="d5830-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="d5830-113">**Applies To**</span></span>

[<span data-ttu-id="d5830-114">вмлфраме</span><span class="sxs-lookup"><span data-stu-id="d5830-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="d5830-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="d5830-115">**Tag Syntax**</span></span>

<span data-ttu-id="d5830-116"><v: Style *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="d5830-116"><v: *element* style=" *expression* "></span></span>

<span data-ttu-id="d5830-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="d5830-117">**Script Syntax**</span></span>

<span data-ttu-id="d5830-118">*element* . Style = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="d5830-118">*element* .style="*expression*"</span></span>

<span data-ttu-id="d5830-119">*выражение* = *элемент*. Style</span><span class="sxs-lookup"><span data-stu-id="d5830-119">*expression*=*element*.style</span></span>

<span data-ttu-id="d5830-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="d5830-120">**Remarks**</span></span>

<span data-ttu-id="d5830-121">Этот атрибут использует обычные атрибуты стиля CSS для позиционирования.</span><span class="sxs-lookup"><span data-stu-id="d5830-121">This attribute uses the normal CSS style attributes for positioning.</span></span>

<span data-ttu-id="d5830-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="d5830-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="d5830-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="d5830-123">**Example**</span></span>

<span data-ttu-id="d5830-124">Стиль определяет фактическую точку кадра.</span><span class="sxs-lookup"><span data-stu-id="d5830-124">The style defines the actual position of the frame.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 