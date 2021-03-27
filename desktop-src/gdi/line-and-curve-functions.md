---
description: Для линий и кривых используются следующие функции.
ms.assetid: 90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b
title: Линейные и кривые функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bf04160e8b9cc0a5c2fb28378bce82a1c7650a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997339"
---
# <a name="line-and-curve-functions"></a><span data-ttu-id="9262f-103">Линейные и кривые функции</span><span class="sxs-lookup"><span data-stu-id="9262f-103">Line and Curve Functions</span></span>

<span data-ttu-id="9262f-104">Для линий и кривых используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="9262f-104">The following functions are used with lines and curves.</span></span>



| <span data-ttu-id="9262f-105">Функция</span><span class="sxs-lookup"><span data-stu-id="9262f-105">Function</span></span>                                   | <span data-ttu-id="9262f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9262f-106">Description</span></span>                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9262f-107">**англеарк**</span><span class="sxs-lookup"><span data-stu-id="9262f-107">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)               | <span data-ttu-id="9262f-108">Рисует сегмент линии и дугу.</span><span class="sxs-lookup"><span data-stu-id="9262f-108">Draws a line segment and an arc.</span></span>                                                                              |
| [<span data-ttu-id="9262f-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="9262f-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)                         | <span data-ttu-id="9262f-110">Рисование эллиптической дуги.</span><span class="sxs-lookup"><span data-stu-id="9262f-110">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="9262f-111">**аркто**</span><span class="sxs-lookup"><span data-stu-id="9262f-111">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)                     | <span data-ttu-id="9262f-112">Рисование эллиптической дуги.</span><span class="sxs-lookup"><span data-stu-id="9262f-112">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="9262f-113">**жетаркдиректион**</span><span class="sxs-lookup"><span data-stu-id="9262f-113">**GetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) | <span data-ttu-id="9262f-114">Извлекает текущее направление дуги для указанного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="9262f-114">Retrieves the current arc direction for the specified device context.</span></span>                                         |
| [<span data-ttu-id="9262f-115">**линедда**</span><span class="sxs-lookup"><span data-stu-id="9262f-115">**LineDDA**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-linedda)                 | <span data-ttu-id="9262f-116">Определяет, какие пикселы должны выделяться для линии, определяемой заданной начальной и конечной точками.</span><span class="sxs-lookup"><span data-stu-id="9262f-116">Determines which pixels should be highlighted for a line defined by the specified starting and ending points.</span></span> |
| [<span data-ttu-id="9262f-117">**линеддапрок**</span><span class="sxs-lookup"><span data-stu-id="9262f-117">**LineDDAProc**</span></span>](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)         | <span data-ttu-id="9262f-118">Определяемая приложением функция обратного вызова, используемая с функцией Линедда.</span><span class="sxs-lookup"><span data-stu-id="9262f-118">An application-defined callback function used with the LineDDA function.</span></span>                                      |
| [<span data-ttu-id="9262f-119">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="9262f-119">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)                   | <span data-ttu-id="9262f-120">Рисует линию из текущей позиции вплоть до указанной точки, но не включая.</span><span class="sxs-lookup"><span data-stu-id="9262f-120">Draws a line from the current position up to, but not including, the specified point.</span></span>                         |
| [<span data-ttu-id="9262f-121">**моветоекс**</span><span class="sxs-lookup"><span data-stu-id="9262f-121">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)               | <span data-ttu-id="9262f-122">Обновляет текущую позицию до указанной точки и при необходимости Возвращает предыдущую позицию.</span><span class="sxs-lookup"><span data-stu-id="9262f-122">Updates the current position to the specified point and optionally returns the previous position.</span></span>             |
| [<span data-ttu-id="9262f-123">**PolyBezierSegment**</span><span class="sxs-lookup"><span data-stu-id="9262f-123">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)           | <span data-ttu-id="9262f-124">Рисует одну или несколько кривых Безье.</span><span class="sxs-lookup"><span data-stu-id="9262f-124">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="9262f-125">**полибезиерто**</span><span class="sxs-lookup"><span data-stu-id="9262f-125">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)       | <span data-ttu-id="9262f-126">Рисует одну или несколько кривых Безье.</span><span class="sxs-lookup"><span data-stu-id="9262f-126">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="9262f-127">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="9262f-127">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)               | <span data-ttu-id="9262f-128">Рисует набор сегментов линий и кривых Безье.</span><span class="sxs-lookup"><span data-stu-id="9262f-128">Draws a set of line segments and Bézier curves.</span></span>                                                               |
| [<span data-ttu-id="9262f-129">**Линию**</span><span class="sxs-lookup"><span data-stu-id="9262f-129">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)               | <span data-ttu-id="9262f-130">Рисует ряд линейных сегментов, подключаясь к точкам в указанном массиве.</span><span class="sxs-lookup"><span data-stu-id="9262f-130">Draws a series of line segments by connecting the points in the specified array.</span></span>                              |
| [<span data-ttu-id="9262f-131">**Для в. lineTo**</span><span class="sxs-lookup"><span data-stu-id="9262f-131">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)           | <span data-ttu-id="9262f-132">Рисует одну или несколько прямых линий.</span><span class="sxs-lookup"><span data-stu-id="9262f-132">Draws one or more straight lines.</span></span>                                                                             |
| [<span data-ttu-id="9262f-133">**Ломаная линия**</span><span class="sxs-lookup"><span data-stu-id="9262f-133">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)       | <span data-ttu-id="9262f-134">Рисует несколько рядов Соединенных линейных сегментов.</span><span class="sxs-lookup"><span data-stu-id="9262f-134">Draws multiple series of connected line segments.</span></span>                                                             |
| [<span data-ttu-id="9262f-135">**сетаркдиректион**</span><span class="sxs-lookup"><span data-stu-id="9262f-135">**SetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) | <span data-ttu-id="9262f-136">Задает направление рисования, которое будет использоваться для функций дуги и Rectangle.</span><span class="sxs-lookup"><span data-stu-id="9262f-136">Sets the drawing direction to be used for arc and rectangle functions.</span></span>                                        |



 

 

 



