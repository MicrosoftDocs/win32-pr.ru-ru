---
title: Атрибут аспекта VML
description: Атрибут аспекта VML
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d4fec254ff3e6af35d82cd45146c201701555b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134078"
---
# <a name="vml-facet-attribute"></a><span data-ttu-id="717f4-103">Атрибут аспекта VML</span><span class="sxs-lookup"><span data-stu-id="717f4-103">VML Facet Attribute</span></span>

<span data-ttu-id="717f4-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="717f4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="717f4-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="717f4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="717f4-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="717f4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="717f4-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="717f4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="717f4-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="717f4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="717f4-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="717f4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="717f4-110">Определяет число аспектов, используемых для описания кривых поверхностей объема.</span><span class="sxs-lookup"><span data-stu-id="717f4-110">Defines the number of facets used to describe curved surfaces of an extrusion.</span></span> <span data-ttu-id="717f4-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="717f4-111">Read/write.</span></span> <span data-ttu-id="717f4-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="717f4-112">**VgNumber**.</span></span>

<span data-ttu-id="717f4-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="717f4-113">**Applies To**</span></span>

[<span data-ttu-id="717f4-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="717f4-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="717f4-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="717f4-115">**Tag Syntax**</span></span>

<span data-ttu-id="717f4-116"><o: *element* аспект = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="717f4-116"><o: *element* facet=" *expression* "></span></span>

<span data-ttu-id="717f4-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="717f4-117">**Script Syntax**</span></span>

<span data-ttu-id="717f4-118">*element* . Facet = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="717f4-118">*element* .facet="*expression*"</span></span>

<span data-ttu-id="717f4-119">*выражение* = *element*. аспект</span><span class="sxs-lookup"><span data-stu-id="717f4-119">*expression*=*element*.facet</span></span>

<span data-ttu-id="717f4-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="717f4-120">**Remarks**</span></span>

<span data-ttu-id="717f4-121">Определяет способ, с помощью которого механизм визуализации будет приблизительным объемом.</span><span class="sxs-lookup"><span data-stu-id="717f4-121">Defines the way that a rendering engine will approximate the extrusion.</span></span> <span data-ttu-id="717f4-122">Меньшее число указывает на более низкое отклонение отрисовки для подсистемы визуализации и приведет к дополнительным аспектам.</span><span class="sxs-lookup"><span data-stu-id="717f4-122">A lower number will indicate a lower rendering tolerance to the rendering engine and will yield more facets.</span></span> <span data-ttu-id="717f4-123">Более высокие значения приводят к появлениям нескольких аспектов.</span><span class="sxs-lookup"><span data-stu-id="717f4-123">Higher numbers will make the extrusion appear more faceted.</span></span> <span data-ttu-id="717f4-124">Значение по умолчанию — 30 000.</span><span class="sxs-lookup"><span data-stu-id="717f4-124">The default value is 30,000.</span></span>

<span data-ttu-id="717f4-125">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="717f4-125">*Microsoft Office Extensions Attribute*</span></span>

 

 