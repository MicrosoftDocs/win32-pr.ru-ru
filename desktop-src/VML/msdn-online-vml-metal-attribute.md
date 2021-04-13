---
title: Атрибут металла VML
description: Атрибут металла VML
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413001"
---
# <a name="vml-metal-attribute"></a><span data-ttu-id="cbf9d-103">Атрибут металла VML</span><span class="sxs-lookup"><span data-stu-id="cbf9d-103">VML Metal Attribute</span></span>

<span data-ttu-id="cbf9d-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cbf9d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cbf9d-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="cbf9d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cbf9d-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="cbf9d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cbf9d-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cbf9d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cbf9d-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cbf9d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cbf9d-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cbf9d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cbf9d-110">Определяет, будет ли поверхность вытянутой фигуры иметь вид металла.</span><span class="sxs-lookup"><span data-stu-id="cbf9d-110">Determines whether the surface of the extruded shape will resemble metal.</span></span> <span data-ttu-id="cbf9d-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="cbf9d-111">Read/write.</span></span> <span data-ttu-id="cbf9d-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="cbf9d-112">**VgTriState**.</span></span>

<span data-ttu-id="cbf9d-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="cbf9d-113">**Applies To**</span></span>

[<span data-ttu-id="cbf9d-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="cbf9d-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="cbf9d-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="cbf9d-115">**Tag Syntax**</span></span>

<span data-ttu-id="cbf9d-116"><o: *element* металла = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="cbf9d-116"><o: *element* metal=" *expression* "></span></span>

<span data-ttu-id="cbf9d-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="cbf9d-117">**Script Syntax**</span></span>

<span data-ttu-id="cbf9d-118">*element* . металла = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="cbf9d-118">*element* .metal="*expression*"</span></span>

<span data-ttu-id="cbf9d-119">*выражение* = *элемент element*. металла</span><span class="sxs-lookup"><span data-stu-id="cbf9d-119">*expression*=*element*.metal</span></span>

<span data-ttu-id="cbf9d-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="cbf9d-120">**Remarks**</span></span>

<span data-ttu-id="cbf9d-121">Если задано значение **true**, то этот атрибут приводит к тому, что отраженный свет отражается цветом материала вместо цвета источника, что делает объект более металлным. Для дальнейшего приближения к металлическим материалам требуется, чтобы зеркальное отражение было относительно высоким (около 1,2), а диффузия была относительно низкой (около 0,6).</span><span class="sxs-lookup"><span data-stu-id="cbf9d-121">If set to **True**, this attribute causes the specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.To further approximate a metallic material requires that specularity be relatively high (about 1.2) and diffusity be relatively low (about 0.6).</span></span> <span data-ttu-id="cbf9d-122">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="cbf9d-122">The default value is **False**.</span></span>

<span data-ttu-id="cbf9d-123">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="cbf9d-123">*Microsoft Office Extensions Attribute*</span></span>

 

 