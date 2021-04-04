---
title: Атрибут плоскости VML
description: Атрибут плоскости VML
ms.assetid: e1de630b-8e25-4052-b316-251046f73e98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f279f008adf8f12f78d6edd790cc533678adc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987610"
---
# <a name="vml-plane-attribute"></a><span data-ttu-id="cd973-103">Атрибут плоскости VML</span><span class="sxs-lookup"><span data-stu-id="cd973-103">VML Plane Attribute</span></span>

<span data-ttu-id="cd973-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cd973-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cd973-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="cd973-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cd973-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="cd973-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cd973-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd973-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cd973-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cd973-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cd973-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cd973-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cd973-110">Указывает плоскость, находящуюся справа от объема.</span><span class="sxs-lookup"><span data-stu-id="cd973-110">Specifies the plane that is at right angles to the extrusion.</span></span> <span data-ttu-id="cd973-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="cd973-111">Read/write.</span></span> <span data-ttu-id="cd973-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="cd973-112">**String**.</span></span>

<span data-ttu-id="cd973-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="cd973-113">**Applies To**</span></span>

[<span data-ttu-id="cd973-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="cd973-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="cd973-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="cd973-115">**Tag Syntax**</span></span>

<span data-ttu-id="cd973-116"><o: *element* плоскость = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="cd973-116"><o: *element* plane=" *expression* "></span></span>

<span data-ttu-id="cd973-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="cd973-117">**Script Syntax**</span></span>

<span data-ttu-id="cd973-118">*element* . плоскость = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="cd973-118">*element* .plane="*expression*"</span></span>

<span data-ttu-id="cd973-119">*выражение* = *элемент*. плоскость</span><span class="sxs-lookup"><span data-stu-id="cd973-119">*expression*=*element*.plane</span></span>

<span data-ttu-id="cd973-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="cd973-120">**Remarks**</span></span>

<span data-ttu-id="cd973-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="cd973-121">Values include:</span></span>



| <span data-ttu-id="cd973-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cd973-122">Value</span></span> | <span data-ttu-id="cd973-123">Описание</span><span class="sxs-lookup"><span data-stu-id="cd973-123">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="cd973-124">xy</span><span class="sxs-lookup"><span data-stu-id="cd973-124">xy</span></span>    | <span data-ttu-id="cd973-125">Объем на уровне справа расположен на плоскости XY.</span><span class="sxs-lookup"><span data-stu-id="cd973-125">Extrusion is at right angles to the xy -plane.</span></span> <span data-ttu-id="cd973-126">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cd973-126">Default</span></span> |
| <span data-ttu-id="cd973-127">зкс</span><span class="sxs-lookup"><span data-stu-id="cd973-127">zx</span></span>    | <span data-ttu-id="cd973-128">Объем на уровне справа ЗКС плоскости.</span><span class="sxs-lookup"><span data-stu-id="cd973-128">Extrusion is at right angles to the zx -plane.</span></span>         |
| <span data-ttu-id="cd973-129">из</span><span class="sxs-lookup"><span data-stu-id="cd973-129">yz</span></span>    | <span data-ttu-id="cd973-130">Объем на уровне справа из плоскости.</span><span class="sxs-lookup"><span data-stu-id="cd973-130">Extrusion is at right angles to the yz -plane.</span></span>         |



 

<span data-ttu-id="cd973-131">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="cd973-131">*Microsoft Office Extensions Attribute*</span></span>

 

 