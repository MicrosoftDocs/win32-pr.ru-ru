---
title: Атрибут расстояния по тексту VML V
description: Атрибут расстояния по тексту VML V
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413312"
---
# <a name="vml-v-text-spacing-attribute"></a><span data-ttu-id="3138f-103">Атрибут расстояния по тексту VML V</span><span class="sxs-lookup"><span data-stu-id="3138f-103">VML V-Text-Spacing Attribute</span></span>

<span data-ttu-id="3138f-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3138f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3138f-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="3138f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3138f-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="3138f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3138f-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3138f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3138f-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3138f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3138f-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3138f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3138f-110">Определяет величину интервала для текста.</span><span class="sxs-lookup"><span data-stu-id="3138f-110">Defines the amount of spacing for text.</span></span> <span data-ttu-id="3138f-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="3138f-111">Read/write.</span></span> <span data-ttu-id="3138f-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="3138f-112">**VgNumber**.</span></span>

<span data-ttu-id="3138f-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="3138f-113">**Applies To**</span></span>

[<span data-ttu-id="3138f-114">текстпас</span><span class="sxs-lookup"><span data-stu-id="3138f-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="3138f-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="3138f-115">**Tag Syntax**</span></span>

<span data-ttu-id="3138f-116"><v: Style *элемента* = "v-Text-просвет: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3138f-116"><v: *element* style="v-text-spacing: *expression* "></span></span>

<span data-ttu-id="3138f-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="3138f-117">**Script Syntax**</span></span>

<span data-ttu-id="3138f-118">*element* . Style. v-Text-просвет = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="3138f-118">*element* .style.v-text-spacing="*expression*"</span></span>

<span data-ttu-id="3138f-119">*выражение* = Text *. Style. v*-текстовые отступы</span><span class="sxs-lookup"><span data-stu-id="3138f-119">*expression*=*element*.style.v-text-spacing</span></span>

<span data-ttu-id="3138f-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3138f-120">**Remarks**</span></span>

<span data-ttu-id="3138f-121">Значение по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="3138f-121">The default value is 100.</span></span> <span data-ttu-id="3138f-122">Дополнительные сведения о межтекстовых шагах см. в разделе атрибут [V-text-mode](msdn-online-vml-v-text-spacing-mode-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3138f-122">See the [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) attribute for more information about text spacing.</span></span>

<span data-ttu-id="3138f-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="3138f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3138f-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="3138f-124">**Example**</span></span>

<span data-ttu-id="3138f-125">ЛеттерспаЦинг между каждой буквой заменяется на 200 единиц.</span><span class="sxs-lookup"><span data-stu-id="3138f-125">The letterspacing between each letter is tightened by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 