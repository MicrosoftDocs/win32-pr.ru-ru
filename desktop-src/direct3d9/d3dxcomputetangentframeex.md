---
description: Выполняет вычисления касательных кадров в сетке. Генерируются тангенс, бинормал и (при необходимости) обычные векторы. Единственные числа обрабатываются по мере необходимости путем группирования краев и разделения вершин.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Функция D3DXComputeTangentFrameEx (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713545"
---
# <a name="d3dxcomputetangentframeex-function"></a><span data-ttu-id="5760c-105">Функция D3DXComputeTangentFrameEx</span><span class="sxs-lookup"><span data-stu-id="5760c-105">D3DXComputeTangentFrameEx function</span></span>

<span data-ttu-id="5760c-106">Выполняет вычисления касательных кадров в сетке.</span><span class="sxs-lookup"><span data-stu-id="5760c-106">Performs tangent frame computations on a mesh.</span></span> <span data-ttu-id="5760c-107">Генерируются тангенс, бинормал и (при необходимости) обычные векторы.</span><span class="sxs-lookup"><span data-stu-id="5760c-107">Tangent, binormal, and optionally normal vectors are generated.</span></span> <span data-ttu-id="5760c-108">Единственные числа обрабатываются по мере необходимости путем группирования краев и разделения вершин.</span><span class="sxs-lookup"><span data-stu-id="5760c-108">Singularities are handled as required by grouping edges and splitting vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5760c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5760c-109">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a><span data-ttu-id="5760c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5760c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5760c-111">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-111">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-112">Тип: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="5760c-112">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="5760c-113">Указатель на входной объект сетки [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="5760c-113">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-114">*двтекстуреинсемантик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-114">*dwTextureInSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-115">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-116">Задает семантическую семантику ввода координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="5760c-116">Specifies the texture coordinate input semantic.</span></span> <span data-ttu-id="5760c-117">Если D3DX \_ по умолчанию, функция предполагает, что нет координат текстуры, и функция завершится ошибкой, если не задано нормальное вычисление вектора.</span><span class="sxs-lookup"><span data-stu-id="5760c-117">If D3DX\_DEFAULT, the function assumes that there are no texture coordinates, and the function will fail unless normal vector calculation is specified.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-118">*двтекстуреининдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-118">*dwTextureInIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-119">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-120">Если в сетке есть несколько координат текстуры, задает координату текстуры, используемую для вычислений касательных кадров.</span><span class="sxs-lookup"><span data-stu-id="5760c-120">If a mesh has multiple texture coordinates, specifies the texture coordinate to use for the tangent frame computations.</span></span> <span data-ttu-id="5760c-121">Если значение равно нулю, то сетка имеет только одну координату текстуры.</span><span class="sxs-lookup"><span data-stu-id="5760c-121">If zero, the mesh has only a single texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-122">*двупартиалаутсемантик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-122">*dwUPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-124">Задает выходную семантику для типа, обычно D3DDECLUSAGE \_ тангенс, который описывает, где будет храниться частичный производный объект относительно координаты текстуры U.</span><span class="sxs-lookup"><span data-stu-id="5760c-124">Specifies the output semantic for the type, typically D3DDECLUSAGE\_TANGENT, that describes where the partial derivative with respect to the U texture coordinate will be stored.</span></span> <span data-ttu-id="5760c-125">Если D3DX \_ по умолчанию, то этот частичный производный не будет сохранен.</span><span class="sxs-lookup"><span data-stu-id="5760c-125">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-126">*двупартиалаутиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-126">*dwUPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-127">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-128">Задает семантический индекс, по которому будет храниться частичный производный объект относительно координаты текстуры U.</span><span class="sxs-lookup"><span data-stu-id="5760c-128">Specifies the semantic index at which to store the partial derivative with respect to the U texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-129">*дввпартиалаутсемантик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-129">*dwVPartialOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-130">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-131">Указывает тип [**D3DDECLUSAGE**](./d3ddeclusage.md) , обычно D3DDECLUSAGE \_ бинормал, который описывает, где будет храниться частичный производный относительно координаты текстуры V.</span><span class="sxs-lookup"><span data-stu-id="5760c-131">Specifies the [**D3DDECLUSAGE**](./d3ddeclusage.md) type, typically D3DDECLUSAGE\_BINORMAL, that describes where the partial derivative with respect to the V texture coordinate will be stored.</span></span> <span data-ttu-id="5760c-132">Если D3DX \_ по умолчанию, то этот частичный производный не будет сохранен.</span><span class="sxs-lookup"><span data-stu-id="5760c-132">If D3DX\_DEFAULT, then this partial derivative will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-133">*дввпартиалаутиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-133">*dwVPartialOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-134">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-135">Задает семантический индекс для хранения частичного производного, относительно координаты текстуры V.</span><span class="sxs-lookup"><span data-stu-id="5760c-135">Specifies the semantic index at which to store the partial derivative with respect to the V texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-136">*двнормалаутсемантик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-136">*dwNormalOutSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-137">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-137">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-138">Задает выходную семантическую семантику, обычно D3DDECLUSAGE \_ нормальную, которая описывает, где будет храниться стандартный вектор в каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="5760c-138">Specifies the output normal semantic, typically D3DDECLUSAGE\_NORMAL, that describes where the normal vector at each vertex will be stored.</span></span> <span data-ttu-id="5760c-139">Если D3DX \_ по умолчанию, то этот стандартный вектор не будет сохранен.</span><span class="sxs-lookup"><span data-stu-id="5760c-139">If D3DX\_DEFAULT, then this normal vector will not be stored.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-140">*двнормалаутиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-140">*dwNormalOutIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-141">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-142">Задает семантический индекс для хранения обычного вектора в каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="5760c-142">Specifies the semantic index at which to store the normal vector at each vertex.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-143">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-143">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-144">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-145">Сочетание одного или нескольких флагов [**D3DXTANGENT**](./d3dxtangent.md) , задающих параметры вычисления касательных кадров.</span><span class="sxs-lookup"><span data-stu-id="5760c-145">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags that specify tangent frame computation options.</span></span> <span data-ttu-id="5760c-146">Если **значение равно NULL**, будут указаны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5760c-146">If **NULL**, the following options will be specified:</span></span>



| <span data-ttu-id="5760c-147">Описание</span><span class="sxs-lookup"><span data-stu-id="5760c-147">Description</span></span>                                                                                              | <span data-ttu-id="5760c-148">[**D3DXTANGENT**](./d3dxtangent.md) Значение флага</span><span class="sxs-lookup"><span data-stu-id="5760c-148">[**D3DXTANGENT**](./d3dxtangent.md) Flag Value</span></span>                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5760c-149">Установите вес обычной векторной длины на угол в радианах, который выдается двумя краями, оставляемыми вершиной.</span><span class="sxs-lookup"><span data-stu-id="5760c-149">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span> | <span data-ttu-id="5760c-150">&! (D3DXTANGENT \_ Вес \_ по \_ области \| D3DXTANGENT \_ вес \_ равен)</span><span class="sxs-lookup"><span data-stu-id="5760c-150">& !( D3DXTANGENT\_WEIGHT\_BY\_AREA \| D3DXTANGENT\_WEIGHT\_EQUAL )</span></span>                |
| <span data-ttu-id="5760c-151">Вычисление ортогональной декартовой координаты из координат текстуры (u, v).</span><span class="sxs-lookup"><span data-stu-id="5760c-151">Compute orthogonal Cartesian coordinates from texture coordinates (u, v).</span></span> <span data-ttu-id="5760c-152">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="5760c-152">See Remarks.</span></span>                   | <span data-ttu-id="5760c-153">&! (D3DXTANGENT \_ ОРСОГОНАЛИЗЕ \_ от \_ U \| D3DXTANGENT \_ орсогонализе \_ от \_ V)</span><span class="sxs-lookup"><span data-stu-id="5760c-153">& !( D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U \| D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V )</span></span> |
| <span data-ttu-id="5760c-154">Текстуры не упаковываются в направлениях u или v</span><span class="sxs-lookup"><span data-stu-id="5760c-154">Textures are not wrapped in either u or v directions</span></span>                                                     | <span data-ttu-id="5760c-155">&! (D3DXTANGENT \_ переносить \_ UV)</span><span class="sxs-lookup"><span data-stu-id="5760c-155">& !( D3DXTANGENT\_WRAP\_UV )</span></span>                                                      |
| <span data-ttu-id="5760c-156">Частичные производные от относительно координат текстуры нормализованы.</span><span class="sxs-lookup"><span data-stu-id="5760c-156">Partial derivatives with respect to texture coordinates are normalized.</span></span>                                  | <span data-ttu-id="5760c-157">&! (D3DXTANGENT \_ НЕ \_ нормализовать \_ частичные части)</span><span class="sxs-lookup"><span data-stu-id="5760c-157">& !( D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS )</span></span>                                     |
| <span data-ttu-id="5760c-158">Вершины упорядочиваются в направлении против часовой стрелки вокруг каждого треугольника.</span><span class="sxs-lookup"><span data-stu-id="5760c-158">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>                               | <span data-ttu-id="5760c-159">&! (D3DXTANGENT \_ ОБМОТКа \_ во вт.)</span><span class="sxs-lookup"><span data-stu-id="5760c-159">& !( D3DXTANGENT\_WIND\_CW )</span></span>                                                      |
| <span data-ttu-id="5760c-160">Используйте одновершинные векторы, уже имеющиеся во входной сетке.</span><span class="sxs-lookup"><span data-stu-id="5760c-160">Use per-vertex normal vectors already present in the input mesh.</span></span>                                         | <span data-ttu-id="5760c-161">&! (D3DXTANGENT \_ ВЫЧИСЛЕНие \_ нормалй)</span><span class="sxs-lookup"><span data-stu-id="5760c-161">& !( D3DXTANGENT\_CALCULATE\_NORMALS )</span></span>                                            |



 

<span data-ttu-id="5760c-162">Если D3DXTANGENT \_ \_ \_ не задан, то будет клонирована входная сеть.</span><span class="sxs-lookup"><span data-stu-id="5760c-162">If D3DXTANGENT\_GENERATE\_IN\_PLACE is not set, the input mesh is cloned.</span></span> <span data-ttu-id="5760c-163">Таким образом, Исходная сетка должна иметь достаточно места для хранения вычисленных обычных векторов и частично производных данных.</span><span class="sxs-lookup"><span data-stu-id="5760c-163">The original mesh must therefore have sufficient space to store the computed normal vector and partial derivative data.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-164">*пдваджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-164">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-165">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5760c-165">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5760c-166">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="5760c-166">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="5760c-167">Число байтов в этом массиве должно быть не менее 3 \* [**жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="5760c-167">The number of bytes in this array must be at least 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="5760c-168">*фпартиаледжесрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-168">*fPartialEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-169">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-169">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-170">Указывает максимальный косинус угла, в котором два частичных производных класса считаются несовместимыми друг с другом.</span><span class="sxs-lookup"><span data-stu-id="5760c-170">Specifies the maximum cosine of the angle at which two partial derivatives are deemed to be incompatible with each other.</span></span> <span data-ttu-id="5760c-171">Если скалярное произведение направления двух частичных производных элементов в смежных треугольниках меньше или равно этому пороговому значению, вершины, совместно используемые этими треугольниками, будут разделены.</span><span class="sxs-lookup"><span data-stu-id="5760c-171">If the dot product of the direction of the two partial derivatives in adjacent triangles is less than or equal to this threshold, then the vertices shared between these triangles will be split.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-172">*фсингуларпоинтсрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-172">*fSingularPointThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-173">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-173">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-174">Указывает максимальную величину частичного производного класса, при котором вершина будет считаться единственным.</span><span class="sxs-lookup"><span data-stu-id="5760c-174">Specifies the maximum magnitude of a partial derivative at which a vertex will be deemed singular.</span></span> <span data-ttu-id="5760c-175">Так как несколько треугольников являются инцидентами в точке, у которой есть ближайшие касательные кадры, но они полностью отменяют друг друга (например, в верхней части сферы), величина частичного производного класса будет уменьшена.</span><span class="sxs-lookup"><span data-stu-id="5760c-175">As multiple triangles are incident on a point that have nearby tangent frames, but altogether cancel each other out (such as at the top of a sphere), the magnitude of the partial derivative will decrease.</span></span> <span data-ttu-id="5760c-176">Если величина меньше или равна этому пороговому значению, то вершина будет разделяться для каждого треугольника, содержащего этот порог.</span><span class="sxs-lookup"><span data-stu-id="5760c-176">If the magnitude is less than or equal to this threshold, then the vertex will be split for every triangle that contains it.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-177">*фнормаледжесрешолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5760c-177">*fNormalEdgeThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-178">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5760c-178">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5760c-179">Как и в случае с Фпартиаледжесрешолд, задает максимальный косинус угла между двумя нормальными значениями, которые выходят за пределы вершин, которые совместно используются треугольниками.</span><span class="sxs-lookup"><span data-stu-id="5760c-179">Similar to fPartialEdgeThreshold, specifies the maximum cosine of the angle between two normals that is a threshold beyond which vertices shared between triangles will be split.</span></span> <span data-ttu-id="5760c-180">Если скалярное произведение двух нормалей меньше порогового значения, то общие вершины будут разбиты, формируя жесткую границу между соседними треугольниками.</span><span class="sxs-lookup"><span data-stu-id="5760c-180">If the dot product of the two normals is less than the threshold, the shared vertices will be split, forming a hard edge between neighboring triangles.</span></span> <span data-ttu-id="5760c-181">Если значение произведения точки больше, чем пороговое, соседние треугольники будут интерполируются.</span><span class="sxs-lookup"><span data-stu-id="5760c-181">If the dot product is more than the threshold, neighboring triangles will have their normals interpolated.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-182">*ппмешаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5760c-182">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-183">Тип: **[ **ID3DXMesh**](id3dxmesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5760c-183">Type: **[**ID3DXMesh**](id3dxmesh.md)\*\***</span></span>

<span data-ttu-id="5760c-184">Адрес указателя на выходной объект сетки [**ID3DXMesh**](id3dxmesh.md) , который получает вычисленные данные о тангенсе, бинормал и обычных векторных данных.</span><span class="sxs-lookup"><span data-stu-id="5760c-184">Address of a pointer to an output [**ID3DXMesh**](id3dxmesh.md) mesh object that receives the computed tangent, binormal, and normal vector data.</span></span>

</dd> <dt>

<span data-ttu-id="5760c-185">*ппвертексмаппинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5760c-185">*ppVertexMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5760c-186">Тип: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5760c-186">Type: **[**ID3DXBuffer**](id3dxbuffer.md)\*\***</span></span>

<span data-ttu-id="5760c-187">Адрес указателя на выходной объект буфера [**ID3DXBuffer**](id3dxbuffer.md) , который получает сопоставление новых вершин, вычисленных этим методом, с исходными вершинами.</span><span class="sxs-lookup"><span data-stu-id="5760c-187">Address of a pointer to an output [**ID3DXBuffer**](id3dxbuffer.md) buffer object that receives a mapping of new vertices computed by this method to the original vertices.</span></span> <span data-ttu-id="5760c-188">Буфер представляет собой массив DWORD, размер массива которого определяется как количество вершин в Ппмешаут.</span><span class="sxs-lookup"><span data-stu-id="5760c-188">The buffer is an array of DWORDs, with the array size defined as the number of vertices in ppMeshOut.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5760c-189">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5760c-189">Return value</span></span>

<span data-ttu-id="5760c-190">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5760c-190">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5760c-191">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5760c-191">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5760c-192">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5760c-192">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5760c-193">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5760c-193">Remarks</span></span>

<span data-ttu-id="5760c-194">Упрощенная версия этой функции доступна в виде [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span><span class="sxs-lookup"><span data-stu-id="5760c-194">A simplified version of this function is available as [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).</span></span>

<span data-ttu-id="5760c-195">Вычисленный Стандартный вектор в каждой вершине всегда нормализуется с длиной единицы.</span><span class="sxs-lookup"><span data-stu-id="5760c-195">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="5760c-196">Самым надежным решением для вычисления ортогональных декартных координат является не устанавливать флаги D3DXTANGENT \_ орсогонализе \_ от \_ вас и D3DXTANGENT \_ орсогонализе \_ из \_ V, чтобы ортогональные координаты вычисляться как в координатах текстуры, так и в v.</span><span class="sxs-lookup"><span data-stu-id="5760c-196">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both texture coordinates u and v.</span></span> <span data-ttu-id="5760c-197">Однако в этом случае, если значение u или v равно нулю, функция будет рассчитывать ортогональные координаты с помощью D3DXTANGENT \_ орсогонализе \_ из \_ v или D3DXTANGENT \_ орсогонализе \_ от \_ u соответственно.</span><span class="sxs-lookup"><span data-stu-id="5760c-197">However, in this case, if either u or v is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="5760c-198">Требования</span><span class="sxs-lookup"><span data-stu-id="5760c-198">Requirements</span></span>



| <span data-ttu-id="5760c-199">Требование</span><span class="sxs-lookup"><span data-stu-id="5760c-199">Requirement</span></span> | <span data-ttu-id="5760c-200">Значение</span><span class="sxs-lookup"><span data-stu-id="5760c-200">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5760c-201">Header</span><span class="sxs-lookup"><span data-stu-id="5760c-201">Header</span></span><br/>  | <dl> <span data-ttu-id="5760c-202"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5760c-202"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5760c-203">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5760c-203">Library</span></span><br/> | <dl> <span data-ttu-id="5760c-204"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5760c-204"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5760c-205">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5760c-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5760c-206">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="5760c-206">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="5760c-207">**D3DXComputeTangentFrame**</span><span class="sxs-lookup"><span data-stu-id="5760c-207">**D3DXComputeTangentFrame**</span></span>](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
