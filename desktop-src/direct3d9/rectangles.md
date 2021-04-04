---
description: В рамках программирования Direct3D и окон объекты на экране называются в плане ограничивающих прямоугольников.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Прямоугольники (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139275"
---
# <a name="rectangles-direct3d-9"></a><span data-ttu-id="d9585-103">Прямоугольники (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9585-103">Rectangles (Direct3D 9)</span></span>

<span data-ttu-id="d9585-104">В рамках программирования Direct3D и окон объекты на экране называются в плане ограничивающих прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="d9585-104">Throughout Direct3D and Window programming, objects on the screen are referred to in terms of bounding rectangles.</span></span> <span data-ttu-id="d9585-105">Стороны ограничивающего прямоугольника всегда параллельны сторонам экрана, поэтому такой прямоугольник можно описать двумя точками: левый верхний угол и правый нижний угол.</span><span class="sxs-lookup"><span data-stu-id="d9585-105">The sides of a bounding rectangle are always parallel to the sides of the screen, so the rectangle can be described by two points, the upper-left corner and lower-right corner.</span></span> <span data-ttu-id="d9585-106">В большинстве приложений структура [**Rect**](/previous-versions//dd162897(v=vs.85)) используется для передачи сведений об ограничивающем прямоугольнике для использования при блиттинг на экран или при обнаружении попаданий.</span><span class="sxs-lookup"><span data-stu-id="d9585-106">Most applications use the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to carry information about a bounding rectangle to use when blitting to the screen or performing hit detection.</span></span>

<span data-ttu-id="d9585-107">В C++ структура [**Rect**](/previous-versions//dd162897(v=vs.85)) имеет следующее определение.</span><span class="sxs-lookup"><span data-stu-id="d9585-107">In C++, the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure has the following definition.</span></span>


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



<span data-ttu-id="d9585-108">В предыдущем примере верхний и левый элементы — это координаты x и y верхнего левого угла ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d9585-108">In the preceding example, the left and top members are the x- and y-coordinates of a bounding rectangle's upper-left corner.</span></span> <span data-ttu-id="d9585-109">Аналогичным образом правый и нижний элементы представляют координаты правого нижнего угла.</span><span class="sxs-lookup"><span data-stu-id="d9585-109">Similarly, the right and bottom members make up the coordinates of the lower-right corner.</span></span> <span data-ttu-id="d9585-110">На следующем рисунке показано, как можно отобразить эти значения.</span><span class="sxs-lookup"><span data-stu-id="d9585-110">The following illustration shows how you can visualize these values.</span></span>

![иллюстрации прямоугольника, ограниченного значениями левой, верхней, правой и нижней сторон](images/rect.png)

<span data-ttu-id="d9585-112">Столбец пикселей справа и строка пикселей внизу не включаются в RECT.</span><span class="sxs-lookup"><span data-stu-id="d9585-112">The column of pixels at the right edge and the row of pixels at the bottom edge are not included in the RECT.</span></span> <span data-ttu-id="d9585-113">Например, блокировка RECT с использованием элементов {10, 10, 138, 138} в результате даст объект шириной и высотой 128 пикселей.</span><span class="sxs-lookup"><span data-stu-id="d9585-113">For example, locking a RECT with members {10, 10, 138, 138} results in an object 128 pixels in width and height.</span></span>

<span data-ttu-id="d9585-114">В интересах эффективности, согласованности и простоты использования все функции представления Direct3D работают с прямоугольниками.</span><span class="sxs-lookup"><span data-stu-id="d9585-114">In the interest of efficiency, consistency, and ease of use, all Direct3D presentation functions work with rectangles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9585-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d9585-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9585-116">Системы координат и геометрия</span><span class="sxs-lookup"><span data-stu-id="d9585-116">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
