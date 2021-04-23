---
description: Создайте UV Atlas для сетки.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Функция D3DXUVAtlasCreate (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f213b0195b0922270d0548d8b5fd4c48fb3e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713605"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="0bf3d-103">Функция D3DXUVAtlasCreate</span><span class="sxs-lookup"><span data-stu-id="0bf3d-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="0bf3d-104">Создайте UV Atlas для сетки.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf3d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bf3d-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="0bf3d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf3d-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0bf3d-109">Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления Atlas.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="0bf3d-110">Как минимум, сетка должна содержать данные позиции и координаты двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-111">*двмаксчартнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-113">Максимальное число диаграмм, в которых нужно секционировать сетку.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="0bf3d-114">См. раздел Примечания о режимах секционирования.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="0bf3d-115">Используйте значение 0, чтобы сообщить D3DX, что Atlas следует заменять на основе растяжения.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-116">*фмаксстретч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-118">Допустимый объем растяжения.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-118">The amount of stretching allowed.</span></span> <span data-ttu-id="0bf3d-119">0 означает, что растяжение не разрешено, 1 означает, что можно использовать любой уровень растяжения.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-120">*дввидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-122">Ширина текстуры.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-123">*двхеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-124">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-125">Высота текстуры.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-126">*фгуттер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-127">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-128">Минимальное расстояние в пикселей текстуры между двумя диаграммами в Atlas.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="0bf3d-129">Переплет всегда масштабируется по ширине; Таким образом, если для текстуры 512 x 512 используется переплет 2,5, то минимальное расстояние между двумя диаграммами — 2,5/512,0 пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-130">*двтекстуреиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-132">Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-133">*пдваджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-134">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bf3d-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bf3d-135">Указатель на массив соседических данных.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="0bf3d-136">При наличии 3 DWORD на грань, указывающих, какие треугольники являются смежными друг с другом (см. раздел [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="0bf3d-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-137">*пдвфалсиджес*</span><span class="sxs-lookup"><span data-stu-id="0bf3d-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="0bf3d-138">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bf3d-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bf3d-139">Массив с 3 DWORD на грань.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="0bf3d-140">Каждая Сторона указывает, имеет ли граница значение false.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="0bf3d-141">Неложное ребро обозначается параметром-1, а значение false — с любым другим значением.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="0bf3d-142">Это обеспечивает параметризацию сетки из четырех, в которых края, расположенные в середине каждого из четырех, не будут вырезаны.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-143">*пфимтаррай* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-144">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bf3d-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bf3d-145">Указатель на массив встроенных десятков метрик, описывающих растяжение треугольника (см. [интегратедметриктенсор](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="0bf3d-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-146">*пкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-147">Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="0bf3d-148">Указатель на функцию обратного вызова (см. [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), который полезен для мониторинга хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-149">*фкаллбаккфрекуенци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-150">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-151">Укажите, как часто D3DX будет вызывать обратный вызов. разумное значение по умолчанию — 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-152">*пусерконтент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-153">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-154">Указатель на определяемое пользователем значение, которое передается функции обратного вызова; обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-155">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-156">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bf3d-157">Укажите качество создаваемых диаграмм.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="0bf3d-158">См. [**D3DXUVATLAS**](./d3dxuvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="0bf3d-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-159">*ппмешаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-160">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bf3d-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0bf3d-161">Указатель на созданную сетку с помощью Atlas (см. [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="0bf3d-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-162">*ппфацепартитионинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-163">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bf3d-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0bf3d-164">Указатель на массив окончательных данных секционирования для граней.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="0bf3d-165">Каждый элемент содержит один DWORD для каждого лица (см. [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="0bf3d-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-166">*ппвертексремапаррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-167">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bf3d-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0bf3d-168">Указатель на массив повторно сопоставленных вершин.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="0bf3d-169">Каждый элемент массива определяет исходную вершину, из которой получена каждая конечная вершина (Если вершина была разделена во время повторного сопоставления).</span><span class="sxs-lookup"><span data-stu-id="0bf3d-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="0bf3d-170">Каждый элемент массива содержит один DWORD на вершину.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-171">*пфмаксстретчаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-172">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bf3d-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bf3d-173">Указатель на максимальное значение растяжения, созданное алгоритмом Atlas.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="0bf3d-174">Диапазон составляет от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="0bf3d-175">*пдвнумчартсаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0bf3d-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf3d-176">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bf3d-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bf3d-177">Указатель на число диаграмм, созданных алгоритмом Atlas.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="0bf3d-178">Если Двмаксчартнумбер имеет слишком малое значение, этот параметр возвратит минимальное число диаграмм, необходимых для создания Atlas.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bf3d-179">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bf3d-179">Return value</span></span>

<span data-ttu-id="0bf3d-180">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bf3d-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bf3d-181">Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bf3d-182">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bf3d-182">Remarks</span></span>

<span data-ttu-id="0bf3d-183">D3DXUVAtlasCreate может секционировать сетчатую геометрию двумя способами:</span><span class="sxs-lookup"><span data-stu-id="0bf3d-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="0bf3d-184">На основе числа диаграмм</span><span class="sxs-lookup"><span data-stu-id="0bf3d-184">Based on the number of charts</span></span>
-   <span data-ttu-id="0bf3d-185">На основе максимально допустимого растяжения.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="0bf3d-186">Если максимально допустимое растяжение равно 0, каждый треугольник скорее всего будет находиться в собственной диаграмме.</span><span class="sxs-lookup"><span data-stu-id="0bf3d-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf3d-187">Требования</span><span class="sxs-lookup"><span data-stu-id="0bf3d-187">Requirements</span></span>



| <span data-ttu-id="0bf3d-188">Требование</span><span class="sxs-lookup"><span data-stu-id="0bf3d-188">Requirement</span></span> | <span data-ttu-id="0bf3d-189">Значение</span><span class="sxs-lookup"><span data-stu-id="0bf3d-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf3d-190">Header</span><span class="sxs-lookup"><span data-stu-id="0bf3d-190">Header</span></span><br/>  | <dl> <span data-ttu-id="0bf3d-191"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bf3d-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0bf3d-192">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0bf3d-192">Library</span></span><br/> | <dl> <span data-ttu-id="0bf3d-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bf3d-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bf3d-194">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bf3d-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf3d-195">Функции Уватлас</span><span class="sxs-lookup"><span data-stu-id="0bf3d-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="0bf3d-196">[Инструмент Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="0bf3d-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
