---
title: Атрибут отражения VML
description: Атрибут отражения VML
ms.assetid: df04c15c-cfad-4172-81fa-a28e13f205fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b4e8814a9bd0cd897ae018cf8b37aa67d732aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890813"
---
# <a name="vml-specularity-attribute"></a><span data-ttu-id="a2598-103">Атрибут отражения VML</span><span class="sxs-lookup"><span data-stu-id="a2598-103">VML Specularity Attribute</span></span>

<span data-ttu-id="a2598-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a2598-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a2598-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="a2598-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a2598-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="a2598-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a2598-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a2598-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a2598-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a2598-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a2598-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a2598-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a2598-110">Определяет зеркальное отражение вытянутой фигуры.</span><span class="sxs-lookup"><span data-stu-id="a2598-110">Defines the specularity of an extruded shape.</span></span> <span data-ttu-id="a2598-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="a2598-111">Read/write.</span></span> <span data-ttu-id="a2598-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="a2598-112">**VgNumber**.</span></span>

<span data-ttu-id="a2598-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="a2598-113">**Applies To**</span></span>

[<span data-ttu-id="a2598-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="a2598-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="a2598-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="a2598-115">**Tag Syntax**</span></span>

<span data-ttu-id="a2598-116"><o: отражение *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="a2598-116"><o: *element* specularity=" *expression* "></span></span>

<span data-ttu-id="a2598-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="a2598-117">**Script Syntax**</span></span>

<span data-ttu-id="a2598-118">*element* . бликность = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="a2598-118">*element* .specularity="*expression*"</span></span>

<span data-ttu-id="a2598-119">*выражение* = *элемент*. отражающий</span><span class="sxs-lookup"><span data-stu-id="a2598-119">*expression*=*element*.specularity</span></span>

<span data-ttu-id="a2598-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="a2598-120">**Remarks**</span></span>

<span data-ttu-id="a2598-121">Это значение определяет отношение освещения инцидента к отраженно отраженному свету.</span><span class="sxs-lookup"><span data-stu-id="a2598-121">This value defines the ratio of incident light to specularly reflected light.</span></span> <span data-ttu-id="a2598-122">Обычные значения находятся в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="a2598-122">Normal values range from 0 to 1.</span></span> <span data-ttu-id="a2598-123">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="a2598-123">The default value is 0.</span></span>

<span data-ttu-id="a2598-124">Если заданы значения больше 1, может произойти необычное воздействие.</span><span class="sxs-lookup"><span data-stu-id="a2598-124">If values greater than 1 are specified, unusual effects can result.</span></span>

<span data-ttu-id="a2598-125">Атрибут расширений Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="a2598-125">Microsoft Office Extensions Attribute</span></span>

 

 