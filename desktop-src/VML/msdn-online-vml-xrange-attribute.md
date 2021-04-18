---
title: Атрибут Ксранже VML
description: Атрибут Ксранже VML
ms.assetid: c2881fd6-08b2-4ec8-b4fd-b271a049da09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f206afce0744ad7a83b30a7eac6de5590b3ea49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691556"
---
# <a name="vml-xrange-attribute"></a><span data-ttu-id="76b91-103">Атрибут Ксранже VML</span><span class="sxs-lookup"><span data-stu-id="76b91-103">VML XRange Attribute</span></span>

<span data-ttu-id="76b91-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="76b91-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="76b91-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="76b91-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="76b91-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="76b91-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="76b91-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76b91-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="76b91-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="76b91-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="76b91-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="76b91-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="76b91-110">Определяет сексранже маркера.</span><span class="sxs-lookup"><span data-stu-id="76b91-110">Defines thexrange of a handle.</span></span> <span data-ttu-id="76b91-111">Чтение и запись **VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="76b91-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="76b91-112">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="76b91-112">**Applies To**</span></span>

<span data-ttu-id="76b91-113">[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="76b91-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="76b91-114">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="76b91-114">**Tag Syntax**</span></span>

<span data-ttu-id="76b91-115"><v: *element* ксранже = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="76b91-115"><v: *element* xrange=" *expression* "></span></span>

<span data-ttu-id="76b91-116">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="76b91-116">**Remarks**</span></span>

<span data-ttu-id="76b91-117">Минимальное и максимальное значения определяются для маркера в направлении по оси x.</span><span class="sxs-lookup"><span data-stu-id="76b91-117">A minimum and maximum value is defined for the handle in the x direction.</span></span> <span data-ttu-id="76b91-118">Каждое значение может быть константой или формулой.</span><span class="sxs-lookup"><span data-stu-id="76b91-118">Each value can be a constant or a formula.</span></span> <span data-ttu-id="76b91-119">Если значение не определено, маркер можно переместить без ограничения в этом направлении.</span><span class="sxs-lookup"><span data-stu-id="76b91-119">If a value is not defined, the handle can be moved without limit in this direction.</span></span> <span data-ttu-id="76b91-120">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="76b91-120">The default value is 0,0.</span></span>

<span data-ttu-id="76b91-121">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="76b91-121">*VML Standard Attribute*</span></span>

 

 