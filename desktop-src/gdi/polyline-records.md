---
description: Записи ломаной линии — это ряд точек; линии, нарисованные между точками, описывают контур символа.
ms.assetid: 6f0de0bb-ad23-471f-9771-8f28614ee28d
title: Записи ломаной линии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e9a9e87a730d06d15eae219f6f626f1d6d3848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263657"
---
# <a name="polyline-records"></a><span data-ttu-id="d374b-103">Записи ломаной линии</span><span class="sxs-lookup"><span data-stu-id="d374b-103">Polyline Records</span></span>

<span data-ttu-id="d374b-104">Записи [ломаной линии](/windows/desktop/api/Wingdi/nf-wingdi-polyline) — это ряд точек; линии, нарисованные между точками, описывают контур символа.</span><span class="sxs-lookup"><span data-stu-id="d374b-104">[Polyline](/windows/desktop/api/Wingdi/nf-wingdi-polyline) records are a series of points; lines drawn between the points describe the outline of the character.</span></span> <span data-ttu-id="d374b-105">Запись ломаной линии начинается с последней точки предыдущей записи (или для первой записи в контуре, начальной точки).</span><span class="sxs-lookup"><span data-stu-id="d374b-105">A polyline record begins with the last point in the previous record (or, for the first record in the contour, the starting point).</span></span> <span data-ttu-id="d374b-106">Каждая точка в записи находится в структуре глифа и может быть подключена просто с помощью прямых линий.</span><span class="sxs-lookup"><span data-stu-id="d374b-106">Each point in the record is on the glyph outline and can be connected simply by using straight lines.</span></span>

 

 



