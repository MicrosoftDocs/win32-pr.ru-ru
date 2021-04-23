---
title: Атрибут Ротатионангле VML
description: Атрибут Ротатионангле VML
ms.assetid: d5432512-1ac2-497b-a415-cec3c1217120
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8af10704c74138192453894427f74003543510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691570"
---
# <a name="vml-rotationangle-attribute"></a><span data-ttu-id="fed81-103">Атрибут Ротатионангле VML</span><span class="sxs-lookup"><span data-stu-id="fed81-103">VML RotationAngle Attribute</span></span>

<span data-ttu-id="fed81-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fed81-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fed81-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="fed81-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fed81-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="fed81-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fed81-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fed81-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fed81-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fed81-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fed81-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fed81-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fed81-110">Задает поворот объекта относительно осей x и y.</span><span class="sxs-lookup"><span data-stu-id="fed81-110">Specifies the rotation of the object about the x and y -axes.</span></span> <span data-ttu-id="fed81-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="fed81-111">Read/write.</span></span> <span data-ttu-id="fed81-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="fed81-112">**VgVector2D**.</span></span>

<span data-ttu-id="fed81-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="fed81-113">**Applies To**</span></span>

[<span data-ttu-id="fed81-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="fed81-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="fed81-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="fed81-115">**Tag Syntax**</span></span>

<span data-ttu-id="fed81-116"><o: *element* ротатионангле = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="fed81-116"><o: *element* rotationangle=" *expression* "></span></span>

<span data-ttu-id="fed81-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="fed81-117">**Script Syntax**</span></span>

<span data-ttu-id="fed81-118">*element* . ротатионангле = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="fed81-118">*element* .rotationangle="*expression*"</span></span>

<span data-ttu-id="fed81-119">*выражение* = *element*. ротатионангле</span><span class="sxs-lookup"><span data-stu-id="fed81-119">*expression*=*element*.rotationangle</span></span>

<span data-ttu-id="fed81-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="fed81-120">**Remarks**</span></span>

<span data-ttu-id="fed81-121">Поворот объекта определяется углом вращения относительно оси y, за которым следует угол вращения по оси x. Угол оси z определяется значением стандартного атрибута **поворота** стиля HTML фигуры.</span><span class="sxs-lookup"><span data-stu-id="fed81-121">The rotation of the object is defined by a rotation angle about the y-axis followed by the rotation angle about the x-axis.The z-axis angle is controlled by the value of the shape's standard HTML Style **Rotation** attribute.</span></span> <span data-ttu-id="fed81-122">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="fed81-122">The default value is 0,0.</span></span>

<span data-ttu-id="fed81-123">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="fed81-123">*Microsoft Office Extensions Attribute*</span></span>

 

 