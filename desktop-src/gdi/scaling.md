---
description: Большинство приложений САПР и рисования предоставляют возможности масштабирования выходных данных, созданных пользователем.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Масштабирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985812"
---
# <a name="scaling"></a><span data-ttu-id="afc7f-103">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="afc7f-103">Scaling</span></span>

<span data-ttu-id="afc7f-104">Большинство приложений САПР и рисования предоставляют возможности масштабирования выходных данных, созданных пользователем.</span><span class="sxs-lookup"><span data-stu-id="afc7f-104">Most CAD and drawing applications provide features that scale output created by the user.</span></span> <span data-ttu-id="afc7f-105">Приложения, которые включают возможности масштабирования (или масштабирования), вызывают функцию [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , чтобы задать соответствующее пространство для преобразования страничного пространства.</span><span class="sxs-lookup"><span data-stu-id="afc7f-105">Applications that include scaling (or zoom) capabilities call the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="afc7f-106">Эта функция получает указатель на структуру [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) , содержащую соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="afc7f-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="afc7f-107">Члены eM11 и eM22 XFORM указывают компоненты горизонтального и вертикального масштабирования соответственно.</span><span class="sxs-lookup"><span data-stu-id="afc7f-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical scaling components, respectively.</span></span>

<span data-ttu-id="afc7f-108">При *масштабировании* вертикальные и горизонтальные линии (или векторы), составляющие объект, растягиваются или сжимаются относительно оси x или y.</span><span class="sxs-lookup"><span data-stu-id="afc7f-108">When *scaling* occurs, the vertical and horizontal lines (or vectors), that constitute an object, are stretched or compressed with respect to the x- or y-axis.</span></span> <span data-ttu-id="afc7f-109">На следующем рисунке показан прямоугольник с 20 по 20, масштабируемый по вертикали, в два раза больше первоначальной высоты при копировании из универсального пространства в пространство координат страницы.</span><span class="sxs-lookup"><span data-stu-id="afc7f-109">The following illustration shows a 20-by-20-unit rectangle scaled vertically to twice its original height when copied from world-coordinate space to page-coordinate space.</span></span>

![Иллюстрация с небольшим прямоугольником в мировом пространстве и более высокой единицей в пространстве страницы](images/cstrn-10.png)

<span data-ttu-id="afc7f-111">На предыдущем рисунке вертикальные линии, определяющие сторону исходного прямоугольника, измеряют 20 единиц, а вертикальные линии, определяющие стороны масштабированного прямоугольника, измеряют единицы измерения 40.</span><span class="sxs-lookup"><span data-stu-id="afc7f-111">In the preceding illustration, the vertical lines that define the original rectangle's side measure 20 units, while the vertical lines that define the scaled rectangle's sides measure 40 units.</span></span>

<span data-ttu-id="afc7f-112">Вертикальное масштабирование может быть представлено следующим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="afc7f-112">Vertical scaling can be represented by the following algorithm.</span></span>

``` syntax
y' = y * Dy 
```

<span data-ttu-id="afc7f-113">Где y — это новая длина, y — Исходная длина, а DY — Вертикальный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="afc7f-113">Where y' is the new length, y is the original length, and Dy is the vertical scaling factor.</span></span>

<span data-ttu-id="afc7f-114">Горизонтальное масштабирование может быть представлено следующим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="afc7f-114">Horizontal scaling can be represented by the following algorithm.</span></span>

``` syntax
x' = x * Dx 
```

<span data-ttu-id="afc7f-115">Где x — это новая длина, x — Исходная длина, а DX — Горизонтальный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="afc7f-115">Where x' is the new length, x is the original length, and Dx is the horizontal scaling factor.</span></span>

<span data-ttu-id="afc7f-116">Преобразование вертикального и горизонтального масштабирования можно объединить в одну операцию с помощью матрицы 2 на 2.</span><span class="sxs-lookup"><span data-stu-id="afc7f-116">The vertical and horizontal scaling transformations can be combined into a single operation by using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

<span data-ttu-id="afc7f-117">Матрица 2 на 2, которая создала преобразование масштабирования, содержит следующие значения.</span><span class="sxs-lookup"><span data-stu-id="afc7f-117">The 2-by-2 matrix that produced the scaling transformation contains the following values.</span></span>

``` syntax
|1    0| 
|0    2| 
```

 

 



