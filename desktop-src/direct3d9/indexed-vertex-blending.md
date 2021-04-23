---
description: Индексированное смешение вершин расширяет поддержку смешения вершин в Direct3D, позволяя использовать матрицы для смешения.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Индексированное смешение вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494289"
---
# <a name="indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="41546-103">Индексированное смешение вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="41546-103">Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="41546-104">Индексированное смешение вершин расширяет поддержку смешения вершин в Direct3D, позволяя использовать матрицы для смешения.</span><span class="sxs-lookup"><span data-stu-id="41546-104">Indexed vertex blending extends the vertex blending support in Direct3D to allow matrices to be used for blending.</span></span> <span data-ttu-id="41546-105">Ссылки на эти матрицы можно получить с помощью индекса матрицы.</span><span class="sxs-lookup"><span data-stu-id="41546-105">These matrices are referred to by using a matrix index.</span></span> <span data-ttu-id="41546-106">Эти индексы предоставляются для каждой вершины и ссылаются на палитру размером до 256 матриц.</span><span class="sxs-lookup"><span data-stu-id="41546-106">These indices are supplied on a per-vertex basis and refer to a palette of up to 256 matrices.</span></span> <span data-ttu-id="41546-107">Каждый индекс имеет 8 бит, и каждая вершина может содержать до четырех индексов, что позволяет смешивать четыре матрицы на вершину.</span><span class="sxs-lookup"><span data-stu-id="41546-107">Each index is 8 bits and each vertex can have up to four indices, which allows four matrices to be blended per vertex.</span></span> <span data-ttu-id="41546-108">Индексы упаковываются в DWORD.</span><span class="sxs-lookup"><span data-stu-id="41546-108">The indices are packed into a DWORD.</span></span> <span data-ttu-id="41546-109">Поскольку индексы указываются для каждой вершины, на один треугольник может влиять до 12 матриц, а любая матрица в палитре может повлиять на вершины одного вызова Draw.</span><span class="sxs-lookup"><span data-stu-id="41546-109">Because indices are specified on a per-vertex basis, up to 12 matrices can affect a single triangle, and any matrix in the palette can affect the vertices of one draw call.</span></span> <span data-ttu-id="41546-110">Этот подход имеет следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="41546-110">This approach has the following advantages.</span></span>

-   <span data-ttu-id="41546-111">Он позволяет больше матриц повлиять на один треугольник.</span><span class="sxs-lookup"><span data-stu-id="41546-111">It enables more matrices to affect a single triangle.</span></span>
-   <span data-ttu-id="41546-112">Он позволяет передавать более плавные треугольники в одном вызове Draw.</span><span class="sxs-lookup"><span data-stu-id="41546-112">It enables more blended triangles to be passed in the same draw call.</span></span>
-   <span data-ttu-id="41546-113">Он делает смешение вершин независимым от индексов треугольника.</span><span class="sxs-lookup"><span data-stu-id="41546-113">It makes vertex blending independent of triangle indices.</span></span> <span data-ttu-id="41546-114">Это позволяет прогрессивным сеткам работать в сочетании с смешением вершин.</span><span class="sxs-lookup"><span data-stu-id="41546-114">This enables progressive meshes to work in conjunction with vertex blending.</span></span>

<span data-ttu-id="41546-115">Одним из недостатков этого подхода является то, что он не работает с примитивами с изогнутыми поверхностими, когда тесселяция происходит перед обработкой вершин.</span><span class="sxs-lookup"><span data-stu-id="41546-115">One disadvantage of this approach is that it does not work with curved-surface primitives when tessellation occurs before vertex processing.</span></span>

<span data-ttu-id="41546-116">На следующей схеме показано, как четыре матрицы могут повлиять на вершину.</span><span class="sxs-lookup"><span data-stu-id="41546-116">The following diagram demonstrates how four matrices can affect a vertex.</span></span> <span data-ttu-id="41546-117">Каждая вершина имеет до четырех индексов, поэтому для каждой вершины можно смешивать четыре матрицы.</span><span class="sxs-lookup"><span data-stu-id="41546-117">Each vertex has up to four indices, so four matrices can be blended per vertex.</span></span> <span data-ttu-id="41546-118">Схема использует матрицы, индексированные по 0, 2, 5 и 6.</span><span class="sxs-lookup"><span data-stu-id="41546-118">The diagram uses the matrices indexed at 0, 2, 5, and 6.</span></span>

![схема индексированного смешения вершин с использованием 4 из 256 доступных матриц](images/dword1.png)

<span data-ttu-id="41546-120">На следующей схеме показано, как до 12 матриц может повлиять на треугольник.</span><span class="sxs-lookup"><span data-stu-id="41546-120">The following diagram demonstrates how up to 12 matrices can affect a triangle.</span></span> <span data-ttu-id="41546-121">Использование индексов, заданных для каждой вершины, может повлиять на треугольник до 12 матриц.</span><span class="sxs-lookup"><span data-stu-id="41546-121">Using indices specified on a per-vertex basis, up to 12 matrices can affect the triangle.</span></span>

![Схема индексированной вершинного смешения для треугольника с использованием 12 из 256 доступных матриц](images/dword2.png)

<span data-ttu-id="41546-123">Следующее уравнение определяет общий случай того, как матрицы влияют на вершину.</span><span class="sxs-lookup"><span data-stu-id="41546-123">The following equation determines the general case for how matrices effect a vertex.</span></span>

![уравнение индексированного смешения вершин](images/indexedvblend.png)

<span data-ttu-id="41546-125">V <sub>модель</sub> — это расположение вершины входной модели.</span><span class="sxs-lookup"><span data-stu-id="41546-125">V <sub>model</sub> is the input model space vertex position.</span></span> <span data-ttu-id="41546-126">Index0.. Index3 — это индексы матрицы для каждого вершины, Упакованные в DWORD.</span><span class="sxs-lookup"><span data-stu-id="41546-126">Index0..Index3 are the per-vertex matrix indices packed into a DWORD.</span></span> <span data-ttu-id="41546-127">M \[ \] — это массив мировых матриц, которые индексируются в.</span><span class="sxs-lookup"><span data-stu-id="41546-127">M\[\] is the array of world matrices that get indexed into.</span></span> <span data-ttu-id="41546-128">б ₀... b ₂ являются весовыми коэффициентами смешения.</span><span class="sxs-lookup"><span data-stu-id="41546-128">b₀..b₂ are the blend weights.</span></span> <span data-ttu-id="41546-129">V<sub>World</sub> — это расположение вершины выходного пространства.</span><span class="sxs-lookup"><span data-stu-id="41546-129">V<sub>world</sub> is the output world space vertex position.</span></span>

<span data-ttu-id="41546-130">Дополнительные сведения об индексированном смешении вершин см. [в разделе использование индексированного смешения вершин (Direct3D 9)](using-indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="41546-130">For more information about indexed vertex blending, see [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41546-131">См. также</span><span class="sxs-lookup"><span data-stu-id="41546-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41546-132">Смешение геометрических объектов</span><span class="sxs-lookup"><span data-stu-id="41546-132">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



