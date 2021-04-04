---
title: Атрибут Origin (Вмлфраме) (VML)
description: Атрибут Origin (Вмлфраме) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793644"
---
# <a name="origin-attribute-vmlframevml"></a><span data-ttu-id="4a877-103">Атрибут Origin (Вмлфраме) (VML)</span><span class="sxs-lookup"><span data-stu-id="4a877-103">Origin Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="4a877-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4a877-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4a877-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="4a877-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4a877-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="4a877-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4a877-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4a877-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4a877-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4a877-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4a877-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4a877-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4a877-110">Определяет источник области обрезки кадра.</span><span class="sxs-lookup"><span data-stu-id="4a877-110">Defines the origin of the clipping region of the frame.</span></span> <span data-ttu-id="4a877-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="4a877-111">Read/write.</span></span> <span data-ttu-id="4a877-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="4a877-112">**VgVector2D**.</span></span>

<span data-ttu-id="4a877-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="4a877-113">**Applies To**</span></span>

[<span data-ttu-id="4a877-114">вмлфраме</span><span class="sxs-lookup"><span data-stu-id="4a877-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="4a877-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="4a877-115">**Tag Syntax**</span></span>

<span data-ttu-id="4a877-116"><v: *элемент* Origin = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="4a877-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="4a877-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="4a877-117">**Script Syntax**</span></span>

<span data-ttu-id="4a877-118">*element* . Origin = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="4a877-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="4a877-119">*выражение* = *элемент*. Origin</span><span class="sxs-lookup"><span data-stu-id="4a877-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="4a877-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="4a877-120">**Remarks**</span></span>

<span data-ttu-id="4a877-121">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="4a877-121">The default value is 0,0.</span></span> <span data-ttu-id="4a877-122">Обратите внимание, что **источник** работает, только если функция [Clip](msdn-online-vml-clip-attribute.md) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="4a877-122">Note that **Origin** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="4a877-123">В этом атрибуте источник определяется как левый верхний угол рамки.</span><span class="sxs-lookup"><span data-stu-id="4a877-123">In this attribute, the origin is defined as the upper left corner of the frame.</span></span>

<span data-ttu-id="4a877-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="4a877-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="4a877-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="4a877-125">**Example**</span></span>

<span data-ttu-id="4a877-126">Источником вырезанной области является 100pt, 100pt.</span><span class="sxs-lookup"><span data-stu-id="4a877-126">The origin of the clipping region is 100pt,100pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 