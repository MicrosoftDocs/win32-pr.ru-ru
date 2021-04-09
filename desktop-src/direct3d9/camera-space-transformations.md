---
description: Вершины в пространстве камеры вычисляются путем преобразования вершин объекта с помощью матрицы представления реального мира.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Преобразования пространства камеры (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141602"
---
# <a name="camera-space-transformations-direct3d-9"></a><span data-ttu-id="09c5b-103">Преобразования пространства камеры (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="09c5b-103">Camera Space Transformations (Direct3D 9)</span></span>

<span data-ttu-id="09c5b-104">Вершины в пространстве камеры вычисляются путем преобразования вершин объекта с помощью матрицы представления реального мира.</span><span class="sxs-lookup"><span data-stu-id="09c5b-104">Vertices in the camera space are computed by transforming the object vertices with the world view matrix.</span></span>

<span data-ttu-id="09c5b-105">V = V \* ввматрикс</span><span class="sxs-lookup"><span data-stu-id="09c5b-105">V = V \* wvMatrix</span></span>

<span data-ttu-id="09c5b-106">Нормали вершин в пространстве камеры вычисляются путем преобразования нормалей объекта с обратной перестановкой матрицы представления реального мира.</span><span class="sxs-lookup"><span data-stu-id="09c5b-106">Vertex normals, in camera space, are computed by transforming the object normals with the inverse transpose of the world view matrix.</span></span> <span data-ttu-id="09c5b-107">Матрица представления реального мира может быть ортогональной, однако это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="09c5b-107">The world view matrix may or may not be orthogonal.</span></span>

<span data-ttu-id="09c5b-108">N = N \* (ввматрикс ⁻ ¹)<sup>T</sup></span><span class="sxs-lookup"><span data-stu-id="09c5b-108">N = N \* (wvMatrix⁻¹)<sup>T</sup></span></span>

<span data-ttu-id="09c5b-109">Инверсия и перестановка матрицы выполняются в матрице 4x4.</span><span class="sxs-lookup"><span data-stu-id="09c5b-109">The matrix inversion and matrix transpose operate on a 4x4 matrix.</span></span> <span data-ttu-id="09c5b-110">При умножении нормаль объединяется с частью 3x3 получившейся матрицы 4x4.</span><span class="sxs-lookup"><span data-stu-id="09c5b-110">The multiply combines the normal with the 3x3 portion of the resulting 4x4 matrix.</span></span>

<span data-ttu-id="09c5b-111">Если для состояния визуализации D3DRENDERSTATE \_ нормализенормалс имеет значение **true**, векторы нормали вершин нормализованы после преобразования в пространство камеры следующим образом:</span><span class="sxs-lookup"><span data-stu-id="09c5b-111">If the render state, D3DRENDERSTATE\_NORMALIZENORMALS is set to **TRUE**, vertex normal vectors are normalized after transformation to camera space as follows:</span></span>

<span data-ttu-id="09c5b-112">N = norm(N)</span><span class="sxs-lookup"><span data-stu-id="09c5b-112">N = norm(N)</span></span>

<span data-ttu-id="09c5b-113">Положение источника света в пространстве камеры вычисляется путем преобразования положения источника света с матрицей представления.</span><span class="sxs-lookup"><span data-stu-id="09c5b-113">Light position in camera space is computed by transforming the light source position with the view matrix.</span></span>

<span data-ttu-id="09c5b-114">LP = LP \* вматрикс</span><span class="sxs-lookup"><span data-stu-id="09c5b-114">Lₚ = Lₚ \* vMatrix</span></span>

<span data-ttu-id="09c5b-115">Направление к свету в пространстве камеры (для направленного света) вычисляется путем умножения направления источника света и матрицы представления. В результате происходит нормализация и инверсия результата.</span><span class="sxs-lookup"><span data-stu-id="09c5b-115">The direction to the light in camera space for a directional light is computed by multiplying the light source direction by the view matrix, normalizing, and negating the result.</span></span>

<span data-ttu-id="09c5b-116">L<sub>dir</sub> =-норма (l<sub>dir</sub> \* ввматрикс)</span><span class="sxs-lookup"><span data-stu-id="09c5b-116">L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)</span></span>

<span data-ttu-id="09c5b-117">Для точки D3DLIGHT \_ и D3DLIGHT \_ направление освещения будет вычислено следующим образом:</span><span class="sxs-lookup"><span data-stu-id="09c5b-117">For the D3DLIGHT\_POINT and D3DLIGHT\_SPOT the direction to light is computed as follows:</span></span>

<span data-ttu-id="09c5b-118">L<sub>dir</sub> = норма (V \* LP), где параметры определены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="09c5b-118">L<sub>dir</sub> = norm(V \* Lₚ), where the parameters are defined in the following table.</span></span>



| <span data-ttu-id="09c5b-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="09c5b-119">Parameter</span></span>       | <span data-ttu-id="09c5b-120">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="09c5b-120">Default value</span></span> | <span data-ttu-id="09c5b-121">Тип</span><span class="sxs-lookup"><span data-stu-id="09c5b-121">Type</span></span>      | <span data-ttu-id="09c5b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="09c5b-122">Description</span></span>                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <span data-ttu-id="09c5b-123">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="09c5b-123">L<sub>dir</sub></span></span> | <span data-ttu-id="09c5b-124">Н/Д</span><span class="sxs-lookup"><span data-stu-id="09c5b-124">N/A</span></span>           | <span data-ttu-id="09c5b-125">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="09c5b-125">D3DVECTOR</span></span> | <span data-ttu-id="09c5b-126">Вектор направления от вершины объекта до света</span><span class="sxs-lookup"><span data-stu-id="09c5b-126">Direction vector from object vertex to the light</span></span>          |
| <span data-ttu-id="09c5b-127">V</span><span class="sxs-lookup"><span data-stu-id="09c5b-127">V</span></span>               | <span data-ttu-id="09c5b-128">Н/Д</span><span class="sxs-lookup"><span data-stu-id="09c5b-128">N/A</span></span>           | <span data-ttu-id="09c5b-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="09c5b-129">D3DVECTOR</span></span> | <span data-ttu-id="09c5b-130">Положение вершины в пространстве камеры</span><span class="sxs-lookup"><span data-stu-id="09c5b-130">Vertex position in camera space</span></span>                           |
| <span data-ttu-id="09c5b-131">wvMatrix</span><span class="sxs-lookup"><span data-stu-id="09c5b-131">wvMatrix</span></span>        | <span data-ttu-id="09c5b-132">Идентификация</span><span class="sxs-lookup"><span data-stu-id="09c5b-132">Identity</span></span>      | <span data-ttu-id="09c5b-133">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="09c5b-133">D3DMATRIX</span></span> | <span data-ttu-id="09c5b-134">Составная матрица, содержащая преобразования реального мира и представления</span><span class="sxs-lookup"><span data-stu-id="09c5b-134">Composite matrix containing the world and view transforms</span></span> |
| <span data-ttu-id="09c5b-135">Нет</span><span class="sxs-lookup"><span data-stu-id="09c5b-135">N</span></span>               | <span data-ttu-id="09c5b-136">Н/Д</span><span class="sxs-lookup"><span data-stu-id="09c5b-136">N/A</span></span>           | <span data-ttu-id="09c5b-137">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="09c5b-137">D3DVECTOR</span></span> | <span data-ttu-id="09c5b-138">Нормаль вершины</span><span class="sxs-lookup"><span data-stu-id="09c5b-138">Vertex normal</span></span>                                             |
| <span data-ttu-id="09c5b-139">Lₚ</span><span class="sxs-lookup"><span data-stu-id="09c5b-139">Lₚ</span></span>              | <span data-ttu-id="09c5b-140">Н/Д</span><span class="sxs-lookup"><span data-stu-id="09c5b-140">N/A</span></span>           | <span data-ttu-id="09c5b-141">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="09c5b-141">D3DVECTOR</span></span> | <span data-ttu-id="09c5b-142">Положение света в пространстве камеры</span><span class="sxs-lookup"><span data-stu-id="09c5b-142">Light position in camera space</span></span>                            |
| <span data-ttu-id="09c5b-143">vMatrix</span><span class="sxs-lookup"><span data-stu-id="09c5b-143">vMatrix</span></span>         | <span data-ttu-id="09c5b-144">Идентификация</span><span class="sxs-lookup"><span data-stu-id="09c5b-144">Identity</span></span>      | <span data-ttu-id="09c5b-145">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="09c5b-145">D3DMATRIX</span></span> | <span data-ttu-id="09c5b-146">Матрица, содержащая преобразование представления</span><span class="sxs-lookup"><span data-stu-id="09c5b-146">Matrix containing the view transform</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="09c5b-147">См. также</span><span class="sxs-lookup"><span data-stu-id="09c5b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09c5b-148">Математика освещения</span><span class="sxs-lookup"><span data-stu-id="09c5b-148">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



