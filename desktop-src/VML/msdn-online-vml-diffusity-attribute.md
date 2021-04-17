---
title: Атрибут диффузии VML
description: Атрибут диффузии VML
ms.assetid: 1d131540-9166-47fc-bb0d-fada38f6a3de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a8e51750bcd71421609221812eb38bbf709657
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691521"
---
# <a name="vml-diffusity-attribute"></a><span data-ttu-id="21d6e-103">Атрибут диффузии VML</span><span class="sxs-lookup"><span data-stu-id="21d6e-103">VML Diffusity Attribute</span></span>

<span data-ttu-id="21d6e-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="21d6e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21d6e-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="21d6e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21d6e-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="21d6e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21d6e-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21d6e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21d6e-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21d6e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21d6e-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21d6e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21d6e-110">Определяет степень рассеяния отраженного света от вытянутой фигуры.</span><span class="sxs-lookup"><span data-stu-id="21d6e-110">Defines the amount of diffusion of reflected light from an extruded shape.</span></span> <span data-ttu-id="21d6e-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="21d6e-111">Read/write.</span></span> <span data-ttu-id="21d6e-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="21d6e-112">**VgNumber**.</span></span>

<span data-ttu-id="21d6e-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="21d6e-113">**Applies To**</span></span>

[<span data-ttu-id="21d6e-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="21d6e-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="21d6e-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="21d6e-115">**Tag Syntax**</span></span>

<span data-ttu-id="21d6e-116"><o: рассеянность *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="21d6e-116"><o: *element* diffusity=" *expression* "></span></span>

<span data-ttu-id="21d6e-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="21d6e-117">**Script Syntax**</span></span>

<span data-ttu-id="21d6e-118">*element* . диффузия = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="21d6e-118">*element* .diffusity="*expression*"</span></span>

<span data-ttu-id="21d6e-119">*выражение* = *элемент*. рассеянность</span><span class="sxs-lookup"><span data-stu-id="21d6e-119">*expression*=*element*.diffusity</span></span>

<span data-ttu-id="21d6e-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="21d6e-120">**Remarks**</span></span>

<span data-ttu-id="21d6e-121">Это значение определяет отношение света инцидента к рассеянному свету.</span><span class="sxs-lookup"><span data-stu-id="21d6e-121">This value defines the ratio of incident light to diffused reflected light.</span></span> <span data-ttu-id="21d6e-122">Обычные значения находятся в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="21d6e-122">Normal values range from 0 to 1.</span></span> <span data-ttu-id="21d6e-123">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="21d6e-123">The default value is 0.</span></span>

<span data-ttu-id="21d6e-124">Если заданы значения больше 1, может произойти необычное воздействие.</span><span class="sxs-lookup"><span data-stu-id="21d6e-124">If values greater than 1 are specified, unusual effects can result.</span></span>

<span data-ttu-id="21d6e-125">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="21d6e-125">*Microsoft Office Extensions Attribute*</span></span>

 

 