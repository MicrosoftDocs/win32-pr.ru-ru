---
description: Определяет параметры, используемые для вычислений с использованием сетки касательно.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Перечисление D3DXTANGENT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713637"
---
# <a name="d3dxtangent-enumeration"></a><span data-ttu-id="ce44f-103">Перечисление D3DXTANGENT</span><span class="sxs-lookup"><span data-stu-id="ce44f-103">D3DXTANGENT enumeration</span></span>

<span data-ttu-id="ce44f-104">Определяет параметры, используемые для вычислений с использованием сетки касательно.</span><span class="sxs-lookup"><span data-stu-id="ce44f-104">Defines settings used for mesh tangent frame computations.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce44f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce44f-105">Syntax</span></span>


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a><span data-ttu-id="ce44f-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ce44f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ce44f-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT в \_ оболочке \_ U**</span><span class="sxs-lookup"><span data-stu-id="ce44f-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-108">Значения координат текстуры в направлении u находятся в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="ce44f-108">Texture coordinate values in the u direction are between 0 and 1.</span></span> <span data-ttu-id="ce44f-109">В этом случае будет выбран набор координат текстуры, который свертывает периметр треугольника.</span><span class="sxs-lookup"><span data-stu-id="ce44f-109">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="ce44f-110">См. раздел [Перенос текстур (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="ce44f-110">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ переносить \_ V**</span><span class="sxs-lookup"><span data-stu-id="ce44f-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-112">Значения координат текстуры в направлении v находятся в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="ce44f-112">Texture coordinate values in the v direction are between 0 and 1.</span></span> <span data-ttu-id="ce44f-113">В этом случае будет выбран набор координат текстуры, который свертывает периметр треугольника.</span><span class="sxs-lookup"><span data-stu-id="ce44f-113">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="ce44f-114">См. раздел [Перенос текстур (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="ce44f-114">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ переносить \_ UV**</span><span class="sxs-lookup"><span data-stu-id="ce44f-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-116">Значения координат текстуры в обоих направлениях находятся в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="ce44f-116">Texture coordinate values in both u and v directions are between 0 and 1.</span></span> <span data-ttu-id="ce44f-117">В этом случае будет выбран набор координат текстуры, который свертывает периметр треугольника.</span><span class="sxs-lookup"><span data-stu-id="ce44f-117">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="ce44f-118">См. раздел [Перенос текстур (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="ce44f-118">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ не \_ нормализация \_ частичных частей**</span><span class="sxs-lookup"><span data-stu-id="ce44f-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-120">Не следует нормализовать частичные производные от относительно координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="ce44f-120">Do not normalize partial derivatives with respect to texture coordinates.</span></span> <span data-ttu-id="ce44f-121">Если не нормализовано, масштаб частичных производных объектов пропорционален масштабу трехмерной модели, деленной на масштабе треугольника в (u, v) пространстве.</span><span class="sxs-lookup"><span data-stu-id="ce44f-121">If not normalized, the scale of the partial derivatives is proportional to the scale of the 3D model divided by the scale of the triangle in (u, v) space.</span></span> <span data-ttu-id="ce44f-122">Это значение шкалы позволяет определить степень растяжения текстуры в заданном направлении.</span><span class="sxs-lookup"><span data-stu-id="ce44f-122">This scale value provides a measure of how much the texture is stretched in a given direction.</span></span> <span data-ttu-id="ce44f-123">Результирующая Длина вектора является взвешенной суммой длин частичных производных.</span><span class="sxs-lookup"><span data-stu-id="ce44f-123">The resulting vector length is a weighted sum of the lengths of the partial derivatives.</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ не \_ орсогонализе**</span><span class="sxs-lookup"><span data-stu-id="ce44f-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT\_DONT\_ORTHOGONALIZE**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-125">Не преобразуйте координаты текстуры в деортогональные координаты Декарт.</span><span class="sxs-lookup"><span data-stu-id="ce44f-125">Do not transform texture coordinates to orthogonal Cartesian coordinates.</span></span> <span data-ttu-id="ce44f-126">Взаимоисключающий с D3DXTANGENT \_ орсогонализе \_ из \_ вас и D3DXTANGENT \_ орсогонализе \_ из \_ V.</span><span class="sxs-lookup"><span data-stu-id="ce44f-126">Mutually exclusive with D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ орсогонализе \_ из \_ V**</span><span class="sxs-lookup"><span data-stu-id="ce44f-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-128">Вычислите частичные производные с учетом координаты текстуры v независимо для каждой вершины, а затем вычислите частичный производный результат по отношению к вам как перекрестное произведение частичного производного типа относительно v и обычного вектора.</span><span class="sxs-lookup"><span data-stu-id="ce44f-128">Compute the partial derivative with respect to texture coordinate v independently for each vertex, and then compute the partial derivative with respect to u as the cross product of the partial derivative with respect to v and the normal vector.</span></span> <span data-ttu-id="ce44f-129">Взаимоисключающий с D3DXTANGENT \_ не \_ ОРСОГОНАЛИЗЕ и D3DXTANGENT \_ орсогонализе \_ от \_ U.</span><span class="sxs-lookup"><span data-stu-id="ce44f-129">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U.</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ орсогонализе \_ от \_ U**</span><span class="sxs-lookup"><span data-stu-id="ce44f-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-131">Вычислите частичные производные с учетом координаты текстуры u независимо для каждой вершины, а затем вычислите частичную производную по отношению к v как перекрестное произведение обычного вектора и частичного производного класса.</span><span class="sxs-lookup"><span data-stu-id="ce44f-131">Compute the partial derivative with respect to texture coordinate u independently for each vertex, and then compute the partial derivative with respect to v as the cross product of the normal vector and the partial derivative with respect to u.</span></span> <span data-ttu-id="ce44f-132">Взаимоисключающий с D3DXTANGENT \_ не \_ ОРСОГОНАЛИЗЕ и D3DXTANGENT \_ орсогонализе \_ из \_ V.</span><span class="sxs-lookup"><span data-stu-id="ce44f-132">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**\_Вес D3DXTANGENT \_ по \_ областям**</span><span class="sxs-lookup"><span data-stu-id="ce44f-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT\_WEIGHT\_BY\_AREA**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-134">Толщина направления для вычисленного среднего или частичного производного вектора на вершину в соответствии с областями треугольников, присоединенных к этой вершине.</span><span class="sxs-lookup"><span data-stu-id="ce44f-134">Weight the direction of the computed per-vertex normal or partial derivative vector according to the areas of triangles attached to that vertex.</span></span> <span data-ttu-id="ce44f-135">Взаимоисключающий с D3DXTANGENTным \_ весом \_ равно.</span><span class="sxs-lookup"><span data-stu-id="ce44f-135">Mutually exclusive with D3DXTANGENT\_WEIGHT\_EQUAL.</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ вес \_ равен**</span><span class="sxs-lookup"><span data-stu-id="ce44f-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT\_WEIGHT\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-137">Вычислите для каждого треугольника входной сетки Стандартный вектор длины блока.</span><span class="sxs-lookup"><span data-stu-id="ce44f-137">Compute a unit-length normal vector for each triangle of the input mesh.</span></span> <span data-ttu-id="ce44f-138">Взаимоисключающий с D3DXTANGENT \_ весом \_ по \_ областям.</span><span class="sxs-lookup"><span data-stu-id="ce44f-138">Mutually exclusive with D3DXTANGENT\_WEIGHT\_BY\_AREA.</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ обмотка \_ во вт.**</span><span class="sxs-lookup"><span data-stu-id="ce44f-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT\_WIND\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-140">Вершины упорядочиваются по часовой стрелке вокруг каждого треугольника.</span><span class="sxs-lookup"><span data-stu-id="ce44f-140">Vertices are ordered in a clockwise direction around each triangle.</span></span> <span data-ttu-id="ce44f-141">Следовательно, вычисленное нормальное векторное направление передается на обратный 180 градусов от направления, вычисленного с помощью порядка вершин против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="ce44f-141">The computed normal vector direction is therefore inverted 180 degrees from the direction computed using counterclockwise vertex ordering.</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ Вычисление \_ нормальных вычислений**</span><span class="sxs-lookup"><span data-stu-id="ce44f-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT\_CALCULATE\_NORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-143">Вычислите вектор нормали для каждого вершины для каждого треугольника входной сетки и проигнорируйте все обычные векторы, которые уже находятся во входной сетке.</span><span class="sxs-lookup"><span data-stu-id="ce44f-143">Compute the per-vertex normal vector for each triangle of the input mesh, and ignore any normal vectors already in the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ce44f-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ создать \_ на \_ месте**</span><span class="sxs-lookup"><span data-stu-id="ce44f-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT\_GENERATE\_IN\_PLACE**</span></span>
</dt> <dd>

<span data-ttu-id="ce44f-145">Результаты хранятся в исходной входной сетке, а Выходная сетка не используется.</span><span class="sxs-lookup"><span data-stu-id="ce44f-145">The results are stored in the original input mesh, and the output mesh is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce44f-146">Требования</span><span class="sxs-lookup"><span data-stu-id="ce44f-146">Requirements</span></span>



| <span data-ttu-id="ce44f-147">Требование</span><span class="sxs-lookup"><span data-stu-id="ce44f-147">Requirement</span></span> | <span data-ttu-id="ce44f-148">Значение</span><span class="sxs-lookup"><span data-stu-id="ce44f-148">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce44f-149">Header</span><span class="sxs-lookup"><span data-stu-id="ce44f-149">Header</span></span><br/> | <dl> <span data-ttu-id="ce44f-150"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce44f-150"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce44f-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce44f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce44f-152">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="ce44f-152">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="ce44f-153">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="ce44f-153">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




