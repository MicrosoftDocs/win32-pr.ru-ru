---
description: Сплайновые записи представляют собой квадратичные кривые (то есть, квадратичные b-сплайны), используемые в TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Записи сплайна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813030"
---
# <a name="spline-records"></a><span data-ttu-id="eaa4a-103">Записи сплайна</span><span class="sxs-lookup"><span data-stu-id="eaa4a-103">Spline Records</span></span>

<span data-ttu-id="eaa4a-104">Сплайновые записи представляют собой квадратичные кривые (то есть, квадратичные b-сплайны), используемые в TrueType.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-104">Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.</span></span> <span data-ttu-id="eaa4a-105">Запись сплайна начинается с последней точки предыдущей записи (или для первой записи в контуре с начальной точкой).</span><span class="sxs-lookup"><span data-stu-id="eaa4a-105">A spline record begins with the last point in the previous record (or for the first record in the contour, with the starting point).</span></span> <span data-ttu-id="eaa4a-106">Для первой записи сплайна начальная точка и последняя точка в записи находятся в структуре глифа.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-106">For the first spline record, the starting point and the last point in the record are on the glyph outline.</span></span> <span data-ttu-id="eaa4a-107">Для всех остальных записей сплайна только последняя точка находится в структуре глифа.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-107">For all other spline records, only the last point is on the glyph outline.</span></span> <span data-ttu-id="eaa4a-108">Все остальные точки в записях сплайна выходят за пределы структуры глифов и должны подготавливаться к просмотру как контрольные точки b-сплайнов.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-108">All other points in the spline records are off the glyph outline and must be rendered as the control points of b-splines.</span></span>

<span data-ttu-id="eaa4a-109">Последняя запись сплайна или ломаной линии в контуре всегда заканчивается начальной точкой контура.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-109">The last spline or polyline record in a contour always ends with the contour's starting point.</span></span> <span data-ttu-id="eaa4a-110">Это обеспечивает закрытие каждого профиля.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-110">This arrangement ensures that every contour is closed.</span></span>

<span data-ttu-id="eaa4a-111">Так как для линий b-сплайнов требуется три точки (один из которых находится между двумя точками, расположенными в контуре), необходимо выполнить некоторые вычисления, если в записи сплайна содержится более одной точки кривой.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-111">Because b-splines require three points (one point off the glyph outline between two points that are on the outline), you must perform some calculations when a spline record contains more than one off-curve point.</span></span>

<span data-ttu-id="eaa4a-112">Например, если запись сплайна содержит три точки (A, B и C), а не первая запись, точки A и B выходят за пределы структуры глифов.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-112">For example, if a spline record contains three points (A, B, and C) and it is not the first record, points A and B are off the glyph outline.</span></span> <span data-ttu-id="eaa4a-113">Чтобы интерпретировать точку A, используйте текущую позицию (которая всегда находится на контуре глифа) и точку на контуре глифа между точками A и B. Чтобы найти среднюю точку (M) между A и B, можно выполнить следующие вычисления.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-113">To interpret point A, use the current position (which is always on the glyph outline) and the point on the glyph outline between points A and B. To find the midpoint (M) between A and B, you can perform the following calculation.</span></span>

<span data-ttu-id="eaa4a-114">M = A + (Б A)/2</span><span class="sxs-lookup"><span data-stu-id="eaa4a-114">M = A + (B A)/2</span></span>

<span data-ttu-id="eaa4a-115">Середина между последовательными точками структуры в записи сплайна — это точка на контуре глифа в соответствии с определением формата сплайна, используемого в шрифтах TrueType.</span><span class="sxs-lookup"><span data-stu-id="eaa4a-115">The midpoint between consecutive off-outline points in a spline record is a point on the glyph outline, according to the definition of the spline format used in TrueType fonts.</span></span>

<span data-ttu-id="eaa4a-116">Если текущая позицией обозначена P, двумя квадратными сплайнами, определяемыми этой записью, являются (P, A, M) и (M, B, C).</span><span class="sxs-lookup"><span data-stu-id="eaa4a-116">If the current position is designated by P, the two quadratic splines defined by this spline record are (P, A, M) and (M, B, C).</span></span>

 

 



