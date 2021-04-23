---
description: Создайте UV Atlas для сетки.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Функция D3DXUVAtlasPartition (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707a503832a4fd66ab2e8d9346587d11544a885c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703768"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="24cd2-103">Функция D3DXUVAtlasPartition</span><span class="sxs-lookup"><span data-stu-id="24cd2-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="24cd2-104">Создайте UV Atlas для сетки.</span><span class="sxs-lookup"><span data-stu-id="24cd2-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="24cd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24cd2-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="24cd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24cd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24cd2-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="24cd2-109">Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), содержащую объект Geometry для вычисления Atlas.</span><span class="sxs-lookup"><span data-stu-id="24cd2-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="24cd2-110">Как минимум, сетка должна содержать данные позиции и координаты двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="24cd2-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-111">*двмаксчартнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24cd2-113">Максимальное число диаграмм, в которых нужно секционировать сетку.</span><span class="sxs-lookup"><span data-stu-id="24cd2-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="24cd2-114">См. раздел Примечания о режимах секционирования.</span><span class="sxs-lookup"><span data-stu-id="24cd2-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="24cd2-115">Используйте значение 0, чтобы сообщить D3DX, что Atlas следует заменять на основе растяжения.</span><span class="sxs-lookup"><span data-stu-id="24cd2-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-116">*фмаксстретч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24cd2-118">Допустимый объем растяжения.</span><span class="sxs-lookup"><span data-stu-id="24cd2-118">The amount of stretching allowed.</span></span> <span data-ttu-id="24cd2-119">0 означает, что растяжение не разрешено, 1 означает, что можно использовать любой уровень растяжения.</span><span class="sxs-lookup"><span data-stu-id="24cd2-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-120">*двтекстуреиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-121">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24cd2-122">Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.</span><span class="sxs-lookup"><span data-stu-id="24cd2-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-123">*пдваджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-124">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="24cd2-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="24cd2-125">Указатель на массив из соседей данных с 3 DWORD на грань, указывающий, какие треугольники являются смежными друг с другом (см. [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="24cd2-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-126">*пдвфалсиджес*</span><span class="sxs-lookup"><span data-stu-id="24cd2-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="24cd2-127">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="24cd2-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="24cd2-128">Массив с 3 DWORD на грань.</span><span class="sxs-lookup"><span data-stu-id="24cd2-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="24cd2-129">Каждая Сторона указывает, имеет ли граница значение false.</span><span class="sxs-lookup"><span data-stu-id="24cd2-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="24cd2-130">Неложное ребро обозначается параметром-1, а значение false — с любым другим значением.</span><span class="sxs-lookup"><span data-stu-id="24cd2-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="24cd2-131">Это обеспечивает параметризацию сетки из четырех, в которых края, расположенные в середине каждого из четырех, не будут вырезаны.</span><span class="sxs-lookup"><span data-stu-id="24cd2-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-132">*пфимтаррай* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-133">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="24cd2-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="24cd2-134">Указатель на массив встроенных десятков метрик, описывающих растяжение треугольника (см. [интегратедметриктенсор](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="24cd2-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-135">*пкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-136">Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="24cd2-137">Указатель на функцию обратного вызова (см. [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), который полезен для мониторинга хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="24cd2-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-138">*фкаллбаккфрекуенци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-139">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24cd2-140">Укажите, как часто D3DX будет вызывать обратный вызов. разумное значение по умолчанию — 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="24cd2-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-141">*пусерконтент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-142">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24cd2-143">Указатель на определяемое пользователем значение, которое передается функции обратного вызова; обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="24cd2-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-144">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-145">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24cd2-146">Укажите качество диаграмм, созданных путем объединения одного или нескольких флагов [**D3DXUVATLAS**](./d3dxuvatlas.md) .</span><span class="sxs-lookup"><span data-stu-id="24cd2-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-147">*ппмешаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-148">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="24cd2-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="24cd2-149">Указатель на созданную сетку с помощью Atlas (см. [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="24cd2-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-150">*пфацепартитионинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-151">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="24cd2-152">Указатель на массив окончательных данных секционирования для граней.</span><span class="sxs-lookup"><span data-stu-id="24cd2-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="24cd2-153">Каждый элемент содержит один DWORD для каждого лица (см. [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="24cd2-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-154">*ппвертексремапаррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-155">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="24cd2-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="24cd2-156">Указатель на массив повторно сопоставленных вершин.</span><span class="sxs-lookup"><span data-stu-id="24cd2-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="24cd2-157">Каждый элемент массива определяет исходную вершину каждой конечной вершины (Если вершина была разделена во время повторного сопоставления).</span><span class="sxs-lookup"><span data-stu-id="24cd2-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="24cd2-158">Каждый элемент массива содержит один DWORD на вершину.</span><span class="sxs-lookup"><span data-stu-id="24cd2-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-159">*пппартитионресултаджаценци*</span><span class="sxs-lookup"><span data-stu-id="24cd2-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="24cd2-160">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="24cd2-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="24cd2-161">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="24cd2-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="24cd2-162">Этот буфер будет содержать массив из трех DWORD на лицо, задающих три соседи для каждой грани в выходной сетке.</span><span class="sxs-lookup"><span data-stu-id="24cd2-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="24cd2-163">Этот параметр не должен иметь **значение NULL**, поскольку он требуется для последующего вызова D3DXUVAtlasPack ().</span><span class="sxs-lookup"><span data-stu-id="24cd2-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-164">*пфмаксстретчаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-165">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="24cd2-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="24cd2-166">Указатель на максимальное значение растяжения, созданное алгоритмом Atlas.</span><span class="sxs-lookup"><span data-stu-id="24cd2-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="24cd2-167">Диапазон составляет от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="24cd2-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="24cd2-168">*пдвнумчартсаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="24cd2-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24cd2-169">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="24cd2-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="24cd2-170">Указатель на число диаграмм, созданных алгоритмом Atlas.</span><span class="sxs-lookup"><span data-stu-id="24cd2-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="24cd2-171">Если Двмаксчартнумбер имеет слишком малое значение, этот параметр возвратит минимальное число диаграмм, необходимых для создания Atlas.</span><span class="sxs-lookup"><span data-stu-id="24cd2-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24cd2-172">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24cd2-172">Return value</span></span>

<span data-ttu-id="24cd2-173">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24cd2-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24cd2-174">Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="24cd2-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="24cd2-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24cd2-175">Remarks</span></span>

<span data-ttu-id="24cd2-176">D3DXUVAtlasPartition похож на [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), за исключением того, что D3DXUVAtlasPartition не выполняет окончательный шаг упаковки.</span><span class="sxs-lookup"><span data-stu-id="24cd2-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="24cd2-177">Требования</span><span class="sxs-lookup"><span data-stu-id="24cd2-177">Requirements</span></span>



| <span data-ttu-id="24cd2-178">Требование</span><span class="sxs-lookup"><span data-stu-id="24cd2-178">Requirement</span></span> | <span data-ttu-id="24cd2-179">Значение</span><span class="sxs-lookup"><span data-stu-id="24cd2-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24cd2-180">Header</span><span class="sxs-lookup"><span data-stu-id="24cd2-180">Header</span></span><br/>  | <dl> <span data-ttu-id="24cd2-181"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="24cd2-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="24cd2-182">Библиотека</span><span class="sxs-lookup"><span data-stu-id="24cd2-182">Library</span></span><br/> | <dl> <span data-ttu-id="24cd2-183"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24cd2-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="24cd2-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24cd2-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24cd2-185">Функции Уватлас</span><span class="sxs-lookup"><span data-stu-id="24cd2-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="24cd2-186">[Инструмент Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="24cd2-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
