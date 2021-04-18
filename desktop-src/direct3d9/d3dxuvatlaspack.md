---
description: Упаковка данных секционирования сетки в Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Функция D3DXUVAtlasPack (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713631"
---
# <a name="d3dxuvatlaspack-function"></a><span data-ttu-id="025f7-103">Функция D3DXUVAtlasPack</span><span class="sxs-lookup"><span data-stu-id="025f7-103">D3DXUVAtlasPack function</span></span>

<span data-ttu-id="025f7-104">Упаковка данных секционирования сетки в Atlas.</span><span class="sxs-lookup"><span data-stu-id="025f7-104">Pack mesh partitioning data into an atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="025f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="025f7-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a><span data-ttu-id="025f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="025f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="025f7-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="025f7-109">Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления Atlas.</span><span class="sxs-lookup"><span data-stu-id="025f7-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="025f7-110">Как минимум, сетка должна содержать данные позиции и координаты двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="025f7-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-111">*дввидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-111">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="025f7-113">Ширина текстуры.</span><span class="sxs-lookup"><span data-stu-id="025f7-113">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-114">*двхеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-114">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="025f7-116">Высота текстуры.</span><span class="sxs-lookup"><span data-stu-id="025f7-116">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-117">*фгуттер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-117">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-118">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="025f7-119">Минимальное расстояние в пикселей текстуры между двумя диаграммами в Atlas.</span><span class="sxs-lookup"><span data-stu-id="025f7-119">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="025f7-120">Переплет всегда масштабируется по ширине; Таким образом, если для текстуры 512 x 512 используется переплет 2,5, то минимальное расстояние между двумя диаграммами — 2,5/512,0 пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="025f7-120">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-121">*двтекстуреиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-121">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="025f7-123">Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.</span><span class="sxs-lookup"><span data-stu-id="025f7-123">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-124">*пдвпартитионресултаджаценци*</span><span class="sxs-lookup"><span data-stu-id="025f7-124">*pdwPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="025f7-125">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="025f7-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="025f7-126">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="025f7-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="025f7-127">Он должен быть производным от Пппартитионресултаджаценци, возвращенного из [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span><span class="sxs-lookup"><span data-stu-id="025f7-127">It should be derived from the ppPartitionResultAdjacency returned from [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span></span> <span data-ttu-id="025f7-128">Это значение не может быть **равно NULL**, поскольку пакету необходимо узнать, где были вырезаны диаграммы на шаге секционирования, чтобы найти края каждой диаграммы.</span><span class="sxs-lookup"><span data-stu-id="025f7-128">This value cannot be **NULL**, because Pack needs to know where charts were cut in the partition step in order to find the edges of each chart.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-129">*пкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-129">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-130">Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-130">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="025f7-131">Указатель на функцию обратного вызова (см. [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), который полезен для мониторинга хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="025f7-131">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-132">*фкаллбаккфрекуенци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-132">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-133">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="025f7-134">Укажите, как часто D3DX будет вызывать обратный вызов. разумное значение по умолчанию — 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="025f7-134">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-135">*пусерконтент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-135">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-136">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-136">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="025f7-137">Указатель типа void, который должен быть передан обратно функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="025f7-137">A void pointer to be passed back to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-138">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-138">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-139">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="025f7-140">Этот параметр параметров в настоящее время зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="025f7-140">This options parameter is currently reserved.</span></span>

</dd> <dt>

<span data-ttu-id="025f7-141">*пфацепартитионинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="025f7-141">*pFacePartitioning* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="025f7-142">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="025f7-142">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="025f7-143">Указатель на объект [**ID3DXBuffer**](id3dxbuffer.md) , содержащий массив конечного секционирования.</span><span class="sxs-lookup"><span data-stu-id="025f7-143">A pointer to an [**ID3DXBuffer**](id3dxbuffer.md) containing the array of the final face-partitioning.</span></span> <span data-ttu-id="025f7-144">Каждый элемент содержит один DWORD для каждого лица.</span><span class="sxs-lookup"><span data-stu-id="025f7-144">Each element contains one DWORD per face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="025f7-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="025f7-145">Return value</span></span>

<span data-ttu-id="025f7-146">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="025f7-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="025f7-147">Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="025f7-147">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="025f7-148">Требования</span><span class="sxs-lookup"><span data-stu-id="025f7-148">Requirements</span></span>



| <span data-ttu-id="025f7-149">Требование</span><span class="sxs-lookup"><span data-stu-id="025f7-149">Requirement</span></span> | <span data-ttu-id="025f7-150">Значение</span><span class="sxs-lookup"><span data-stu-id="025f7-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="025f7-151">Header</span><span class="sxs-lookup"><span data-stu-id="025f7-151">Header</span></span><br/>  | <dl> <span data-ttu-id="025f7-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="025f7-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="025f7-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="025f7-153">Library</span></span><br/> | <dl> <span data-ttu-id="025f7-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="025f7-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="025f7-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="025f7-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="025f7-156">Функции Уватлас</span><span class="sxs-lookup"><span data-stu-id="025f7-156">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
