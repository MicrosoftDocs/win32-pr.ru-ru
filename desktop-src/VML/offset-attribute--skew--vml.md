---
title: Атрибут Offset (асимметрия) (VML)
description: Атрибут Offset (асимметрия) (VML)
ms.assetid: 3d4b08c5-e29b-4ace-9c3e-75598068ff18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6dbabad6429ad82d4a5aa5cb9187fb1326d4900
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413023"
---
# <a name="offset-attribute-skewvml"></a><span data-ttu-id="770a0-103">Атрибут Offset (асимметрия) (VML)</span><span class="sxs-lookup"><span data-stu-id="770a0-103">Offset Attribute (Skew)(VML)</span></span>

<span data-ttu-id="770a0-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="770a0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="770a0-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="770a0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="770a0-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="770a0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="770a0-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="770a0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="770a0-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="770a0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="770a0-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="770a0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="770a0-110">Определяет смещение наклона.</span><span class="sxs-lookup"><span data-stu-id="770a0-110">Defines the offset of the skew.</span></span> <span data-ttu-id="770a0-111">Чтение и запись **VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="770a0-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="770a0-112">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="770a0-112">**Applies To**</span></span>

[<span data-ttu-id="770a0-113">Отклонение</span><span class="sxs-lookup"><span data-stu-id="770a0-113">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="770a0-114">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="770a0-114">**Tag Syntax**</span></span>

<span data-ttu-id="770a0-115"><o: offset *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="770a0-115"><o: *element* offset=" *expression* "></span></span>

<span data-ttu-id="770a0-116">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="770a0-116">**Script Syntax**</span></span>

<span data-ttu-id="770a0-117">*element* . offset = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="770a0-117">*element* .offset="*expression*"</span></span>

<span data-ttu-id="770a0-118">*выражение* = *элемент*. offset</span><span class="sxs-lookup"><span data-stu-id="770a0-118">*expression*=*element*.offset</span></span>

<span data-ttu-id="770a0-119">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="770a0-119">**Remarks**</span></span>

<span data-ttu-id="770a0-120">Определяет величину смещения x и y от исходного расположения фигуры.</span><span class="sxs-lookup"><span data-stu-id="770a0-120">Determines the amount of x and y offset from the shape's original location.</span></span> <span data-ttu-id="770a0-121">Значения определяются в абсолютном измерении или дробных значениях фигуры (от-0,5 до + 0,5).</span><span class="sxs-lookup"><span data-stu-id="770a0-121">Values are defined in absolute measurement or fractional values of a shape (ranging from -0.5 to +0.5).</span></span> <span data-ttu-id="770a0-122">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="770a0-122">Default is 0,0.</span></span>

<span data-ttu-id="770a0-123">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="770a0-123">*Microsoft Office Extensions Attribute*</span></span>

 

 