---
title: Атрибут Иранже VML
description: Атрибут Иранже VML
ms.assetid: 9386fc06-cf00-45ce-95fe-13a2ca40cb69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417e302b865f820850c937c5d83e4b60c2898861
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791815"
---
# <a name="vml-yrange-attribute"></a><span data-ttu-id="2a9ce-103">Атрибут Иранже VML</span><span class="sxs-lookup"><span data-stu-id="2a9ce-103">VML YRange Attribute</span></span>

<span data-ttu-id="2a9ce-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2a9ce-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2a9ce-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2a9ce-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2a9ce-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2a9ce-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2a9ce-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2a9ce-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2a9ce-110">Определяет диапазон y для маркера.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-110">Defines the y range of a handle.</span></span> <span data-ttu-id="2a9ce-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-111">Read/write.</span></span> <span data-ttu-id="2a9ce-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-112">**VgVector2D**.</span></span>

<span data-ttu-id="2a9ce-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="2a9ce-113">**Applies To**</span></span>

<span data-ttu-id="2a9ce-114">[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="2a9ce-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="2a9ce-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="2a9ce-115">**Tag Syntax**</span></span>

<span data-ttu-id="2a9ce-116"><v: *element* иранже = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="2a9ce-116"><v: *element* yrange=" *expression* "></span></span>

<span data-ttu-id="2a9ce-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="2a9ce-117">**Remarks**</span></span>

<span data-ttu-id="2a9ce-118">Минимальное и максимальное значения определяются для маркера в направлении y.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-118">A minimum and maximum value is defined for the handle in the y direction.</span></span> <span data-ttu-id="2a9ce-119">Каждое значение может быть константой или формулой.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-119">Each value can be a constant or a formula.</span></span> <span data-ttu-id="2a9ce-120">Если значение не определено, маркер можно переместить без ограничения в этом направлении.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-120">If a value is not defined, the handle can be moved without limit in this direction.</span></span> <span data-ttu-id="2a9ce-121">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-121">The default value is 0,0.</span></span>

<span data-ttu-id="2a9ce-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="2a9ce-122">*VML Standard Attribute*</span></span>

 

 