---
title: Атрибут «на объеме» (VML)
description: Атрибут «на объеме» (VML)
ms.assetid: 5400f165-1e86-4198-8be6-ebd7dd95f7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0107da91ddca0dfd17c7f940be06f1bde40275a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791713"
---
# <a name="on-attribute-extrusionvml"></a><span data-ttu-id="01663-103">Атрибут «на объеме» (VML)</span><span class="sxs-lookup"><span data-stu-id="01663-103">On Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="01663-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="01663-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="01663-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="01663-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="01663-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="01663-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="01663-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="01663-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="01663-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="01663-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="01663-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="01663-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="01663-110">Определяет, будет ли отображаться объем на объеме.</span><span class="sxs-lookup"><span data-stu-id="01663-110">Determines whether an extrusion will be displayed.</span></span> <span data-ttu-id="01663-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="01663-111">Read/write.</span></span> <span data-ttu-id="01663-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="01663-112">**VgTriState**.</span></span>

<span data-ttu-id="01663-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="01663-113">**Applies To**</span></span>

[<span data-ttu-id="01663-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="01663-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="01663-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="01663-115">**Tag Syntax**</span></span>

<span data-ttu-id="01663-116"><o: *element* on = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="01663-116"><o: *element* on=" *expression* "></span></span>

<span data-ttu-id="01663-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="01663-117">**Script Syntax**</span></span>

<span data-ttu-id="01663-118">*element* . on = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="01663-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="01663-119">*выражение* = *element*. on</span><span class="sxs-lookup"><span data-stu-id="01663-119">*expression*=*element*.on</span></span>

<span data-ttu-id="01663-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="01663-120">**Remarks**</span></span>

<span data-ttu-id="01663-121">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="01663-121">The default value is **False**.</span></span> <span data-ttu-id="01663-122">Объем не будет отображаться, если значение не равно **true**.</span><span class="sxs-lookup"><span data-stu-id="01663-122">An extrusion will not be displayed unless the value is set to **True**.</span></span>

<span data-ttu-id="01663-123">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="01663-123">*Microsoft Office Extensions Attribute*</span></span>

 

 