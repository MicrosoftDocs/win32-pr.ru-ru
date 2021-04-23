---
title: Атрибут ориентации VML
description: Атрибут ориентации VML
ms.assetid: 62298908-6e88-470d-bca2-0cfc1a38c2eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa19d8826638ef44ed99f9560e0db5dcb7ae455e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672405"
---
# <a name="vml-orientation-attribute"></a><span data-ttu-id="fbb1b-103">Атрибут ориентации VML</span><span class="sxs-lookup"><span data-stu-id="fbb1b-103">VML Orientation Attribute</span></span>

<span data-ttu-id="fbb1b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fbb1b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fbb1b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fbb1b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fbb1b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fbb1b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fbb1b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fbb1b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fbb1b-110">Задает вектор, вокруг которого можно поворачивать фигуру.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-110">Specifies the vector around which a shape can be rotated.</span></span> <span data-ttu-id="fbb1b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-111">Read/write.</span></span> <span data-ttu-id="fbb1b-112">**VgVector3D**.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-112">**VgVector3D**.</span></span>

<span data-ttu-id="fbb1b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="fbb1b-113">**Applies To**</span></span>

[<span data-ttu-id="fbb1b-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="fbb1b-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="fbb1b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="fbb1b-115">**Tag Syntax**</span></span>

<span data-ttu-id="fbb1b-116"><o: Orientation *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="fbb1b-116"><o: *element* orientation=" *expression* "></span></span>

<span data-ttu-id="fbb1b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="fbb1b-117">**Script Syntax**</span></span>

<span data-ttu-id="fbb1b-118">*element* . Orientation = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="fbb1b-118">*element* .orientation="*expression*"</span></span>

<span data-ttu-id="fbb1b-119">*выражение* = *элемент*. Orientation</span><span class="sxs-lookup"><span data-stu-id="fbb1b-119">*expression*=*element*.orientation</span></span>

<span data-ttu-id="fbb1b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="fbb1b-120">**Remarks**</span></span>

<span data-ttu-id="fbb1b-121">Используйте атрибут [ориентатионангле](msdn-online-vml-orientationangle-attribute.md) , чтобы указать величину поворота вокруг этого вектора.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-121">Use the [OrientationAngle](msdn-online-vml-orientationangle-attribute.md) attribute to specify the amount of rotation around this vector.</span></span> <span data-ttu-id="fbb1b-122">Значение по умолчанию — 100, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="fbb1b-122">Default value is 100,0,0.</span></span>

<span data-ttu-id="fbb1b-123">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="fbb1b-123">*Microsoft Office Extensions Attribute*</span></span>

 

 