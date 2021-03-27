---
description: Приложение получает размеры ограничивающего прямоугольника области путем вызова функции Жетргнбокс.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Получение ограничивающего прямоугольника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811879"
---
# <a name="retrieving-a-bounding-rectangle"></a><span data-ttu-id="a3590-103">Получение ограничивающего прямоугольника</span><span class="sxs-lookup"><span data-stu-id="a3590-103">Retrieving a Bounding Rectangle</span></span>

<span data-ttu-id="a3590-104">Приложение получает размеры ограничивающего прямоугольника области путем вызова функции [**жетргнбокс**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) .</span><span class="sxs-lookup"><span data-stu-id="a3590-104">An application retrieves the dimensions of a region's bounding rectangle by calling the [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) function.</span></span> <span data-ttu-id="a3590-105">Если область является прямоугольной, **жетргнбокс** возвращает размеры области.</span><span class="sxs-lookup"><span data-stu-id="a3590-105">If the region is rectangular, **GetRgnBox** returns the dimensions of the region.</span></span> <span data-ttu-id="a3590-106">Если регион является эллиптическим, функция возвращает размеры наименьшего прямоугольника, который может быть нарисован вокруг эллипса.</span><span class="sxs-lookup"><span data-stu-id="a3590-106">If the region is elliptical, the function returns the dimensions of the smallest rectangle that can be drawn around the ellipse.</span></span> <span data-ttu-id="a3590-107">Длинные стороны прямоугольника имеют ту же длину, что и основная ось эллипса, а короткие стороны прямоугольника имеют ту же длину, что и Вспомогательная ось эллипса.</span><span class="sxs-lookup"><span data-stu-id="a3590-107">The long sides of the rectangle are the same length as the ellipse's major axis, and the short sides of the rectangle are the same length as the ellipse's minor axis.</span></span> <span data-ttu-id="a3590-108">Если регион является многоугольным, **жетргнбокс** возвращает размеры наименьшего прямоугольника, который может быть нарисован вокруг всего многоугольника.</span><span class="sxs-lookup"><span data-stu-id="a3590-108">If the region is polygonal, **GetRgnBox** returns the dimensions of the smallest rectangle that can be drawn around the entire polygon.</span></span>

 

 



