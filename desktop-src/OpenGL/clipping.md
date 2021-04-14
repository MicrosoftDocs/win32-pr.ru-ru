---
title: Обрезка (OpenGL)
description: Обрезка происходит в два этапа
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Конвейер обработки OpenGL, обрезка
- Обрезка OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414548"
---
# <a name="clipping-opengl"></a><span data-ttu-id="0215c-105">Обрезка (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="0215c-105">Clipping (OpenGL)</span></span>

<span data-ttu-id="0215c-106">Обрезка происходит в два этапа:</span><span class="sxs-lookup"><span data-stu-id="0215c-106">Clipping occurs in two steps:</span></span>

1.  <span data-ttu-id="0215c-107">**Просмотр отсечения для тома Клиппингаппликатион.**</span><span class="sxs-lookup"><span data-stu-id="0215c-107">**View volume clippingApplication-specific clipping.**</span></span> <span data-ttu-id="0215c-108">Сразу после сборки примитивов они обрезаются в координатах глаза по мере необходимости для всех обтравочных плоскостей, определенных с помощью [**глклипплане**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="0215c-108">Immediately after primitives are assembled, they're clipped in eye coordinates as necessary for any clipping planes you've defined with [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="0215c-109">(Для OpenGL требуется поддержка по крайней мере шести плоскостей отсечения для конкретных приложений.)</span><span class="sxs-lookup"><span data-stu-id="0215c-109">(OpenGL requires support for at least six such application-specific clipping planes.)</span></span>
2.  <span data-ttu-id="0215c-110">Примитивы преобразуются матрицей проекции в координаты клипа и обрезаются соответствующим объемом представления.</span><span class="sxs-lookup"><span data-stu-id="0215c-110">Primitives are transformed by the projection matrix into clip coordinates and clipped by the corresponding view volume.</span></span> <span data-ttu-id="0215c-111">Эту матрицу можно контролировать с помощью функций преобразования матрицы (см. раздел Преобразование [матрицы](matrix-transformations.md)), но обычно это задается с помощью [**глфрустум**](glfrustum.md) или [**глорсо**](glortho.md).</span><span class="sxs-lookup"><span data-stu-id="0215c-111">This matrix can be controlled by the matrix transformation functions (see [Matrix Transformations](matrix-transformations.md)) but is typically specified by [**glFrustum**](glfrustum.md) or [**glOrtho**](glortho.md).</span></span>

<span data-ttu-id="0215c-112">Точки, сегменты линии и многоугольники обрабатываются по-разному во время обрезки:</span><span class="sxs-lookup"><span data-stu-id="0215c-112">Points, line segments, and polygons are handled differently during clipping:</span></span>

-   <span data-ttu-id="0215c-113">Точки либо сохраняются в исходном состоянии (если они находятся внутри тома обрезки), либо отменяются (если они находятся за пределами громкости).</span><span class="sxs-lookup"><span data-stu-id="0215c-113">Points are either retained in their original state (if they're inside the clip volume) or discarded (if they're outside the clip volume).</span></span>
-   <span data-ttu-id="0215c-114">Если части сегментов линий или многоугольников находятся за пределами громкости клипа, в точках обрезки создаются новые вершины.</span><span class="sxs-lookup"><span data-stu-id="0215c-114">If portions of line segments or polygons are outside the clip volume, new vertices are generated at the clip points.</span></span>
-   <span data-ttu-id="0215c-115">Для многоугольников все границы могут быть построены между новыми вершинами, созданными в точках обрезки.</span><span class="sxs-lookup"><span data-stu-id="0215c-115">For polygons, an entire edge may need to be constructed between new vertices generated at the clip points.</span></span>
-   <span data-ttu-id="0215c-116">Для сегментов линий и многоугольников, которые обрезаются, для всех новых вершин назначается флаг границы, цвет и сведения о текстуре.</span><span class="sxs-lookup"><span data-stu-id="0215c-116">For line segments and polygons that are clipped, the edge flag, color, and texture information is assigned to all new vertices.</span></span>

 

 




