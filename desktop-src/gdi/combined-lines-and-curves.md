---
description: В дополнение к рисованию линий или кривых, приложения могут нарисовать сочетания линии и кривой, вызывая одну функцию. Например, приложение может нарисовать контур круговой диаграммы, вызвав функцию Англеарк.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Объединенные линии и кривые
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985028"
---
# <a name="combined-lines-and-curves"></a><span data-ttu-id="bca77-104">Объединенные линии и кривые</span><span class="sxs-lookup"><span data-stu-id="bca77-104">Combined Lines and Curves</span></span>

<span data-ttu-id="bca77-105">В дополнение к рисованию линий или кривых, приложения могут нарисовать сочетания линии и кривой, вызывая одну функцию.</span><span class="sxs-lookup"><span data-stu-id="bca77-105">In addition to drawing lines or curves, applications can draw combinations of line and curve output by calling a single function.</span></span> <span data-ttu-id="bca77-106">Например, приложение может нарисовать контур круговой диаграммы, вызвав функцию [**англеарк**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .</span><span class="sxs-lookup"><span data-stu-id="bca77-106">For example, an application can draw the outline of a pie chart by calling the [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function.</span></span>

<span data-ttu-id="bca77-107">Функция [**англеарк**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) Рисует дугу вдоль периметра круга и рисует линию, соединяющую начальную точку дуги с центром окружности.</span><span class="sxs-lookup"><span data-stu-id="bca77-107">The [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) function draws an arc along a circle's perimeter and draws a line connecting the starting point of the arc to the circle's center.</span></span> <span data-ttu-id="bca77-108">В дополнение к использованию функции **англеарк** приложение также может объединять линии и нестандартные выходные данные кривой с помощью функции [**рисования**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .</span><span class="sxs-lookup"><span data-stu-id="bca77-108">In addition to using the **AngleArc** function, an application can also combine line and irregular curve output by using the [**PolyDraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) function.</span></span>

 

 



