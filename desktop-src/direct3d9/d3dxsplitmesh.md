---
description: Разделяет сетку на сетки меньше указанного размера.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Функция D3DXSplitMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713640"
---
# <a name="d3dxsplitmesh-function"></a><span data-ttu-id="92a40-103">Функция D3DXSplitMesh</span><span class="sxs-lookup"><span data-stu-id="92a40-103">D3DXSplitMesh function</span></span>

<span data-ttu-id="92a40-104">Разделяет сетку на сетки меньше указанного размера.</span><span class="sxs-lookup"><span data-stu-id="92a40-104">Splits a mesh into meshes smaller than the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92a40-105">Syntax</span></span>


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a><span data-ttu-id="92a40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92a40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a40-107">*пмешин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92a40-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="92a40-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="92a40-109">Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий исходную сетку.</span><span class="sxs-lookup"><span data-stu-id="92a40-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="92a40-110">*паджаценциин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92a40-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-111">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="92a40-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92a40-112">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сетке, которую необходимо упростить.</span><span class="sxs-lookup"><span data-stu-id="92a40-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="92a40-113">*MAXSIZE* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92a40-113">*MaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-114">Тип: **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92a40-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92a40-115">Максимальное количество вершин в результирующей сетке.</span><span class="sxs-lookup"><span data-stu-id="92a40-115">Maximum number of vertices in the resulting mesh.</span></span>

</dd> <dt>

<span data-ttu-id="92a40-116">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92a40-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-117">Тип: **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92a40-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="92a40-118">Флаги параметров для новых сеток.</span><span class="sxs-lookup"><span data-stu-id="92a40-118">Option flags for the new meshes.</span></span>

</dd> <dt>

<span data-ttu-id="92a40-119">*пмешесаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="92a40-119">*pMeshesOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="92a40-120">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="92a40-121">Число возвращенных сеток.</span><span class="sxs-lookup"><span data-stu-id="92a40-121">Number of meshes returned.</span></span>

</dd> <dt>

<span data-ttu-id="92a40-122">*ппмешаррайаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="92a40-122">*ppMeshArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-123">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="92a40-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="92a40-124">Буфер, содержащий массив интерфейсов [**ID3DXMesh**](id3dxmesh.md) для новых сеток.</span><span class="sxs-lookup"><span data-stu-id="92a40-124">Buffer containing an array of [**ID3DXMesh**](id3dxmesh.md) interfaces for the new meshes.</span></span> <span data-ttu-id="92a40-125">Для исходной сетки, разделенной на n сеток, *ппмешаррайаут* является массивом из n **ID3DXMesh** указателей.</span><span class="sxs-lookup"><span data-stu-id="92a40-125">For a source mesh split into n meshes, *ppMeshArrayOut* is an array of n **ID3DXMesh** pointers.</span></span>

</dd> <dt>

<span data-ttu-id="92a40-126">*ппаджаценциаррайаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="92a40-126">*ppAdjacencyArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-127">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="92a40-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="92a40-128">Буфер, содержащий массив смежных массивов (DWORD) для новых сеток.</span><span class="sxs-lookup"><span data-stu-id="92a40-128">Buffer containing an array of adjacency arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="92a40-129">См. [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="92a40-129">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="92a40-130">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="92a40-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="92a40-131">*ппфацеремапаррайаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="92a40-131">*ppFaceRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-132">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="92a40-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="92a40-133">Буфер, содержащий массив массивов для сопоставления лиц (DWORD) для новых сеток.</span><span class="sxs-lookup"><span data-stu-id="92a40-133">Buffer containing an array of face remap arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="92a40-134">См. [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="92a40-134">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="92a40-135">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="92a40-135">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="92a40-136">*ппвертремапаррайаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="92a40-136">*ppVertRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a40-137">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="92a40-137">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="92a40-138">Буфер, содержащий массив массивов сопоставления вершин для новых сеток.</span><span class="sxs-lookup"><span data-stu-id="92a40-138">Buffer containing an array of vertex remap arrays for the new meshes.</span></span> <span data-ttu-id="92a40-139">См. [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="92a40-139">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="92a40-140">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="92a40-140">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a40-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92a40-141">Return value</span></span>

<span data-ttu-id="92a40-142">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="92a40-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="92a40-143">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="92a40-143">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a40-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92a40-144">Remarks</span></span>

<span data-ttu-id="92a40-145">Обычно эта функция используется для разбиения сетки с 32-битовыми индексами (более 65535 вершин) в несколько сеток, каждая из которых имеет 16-разрядные индексы.</span><span class="sxs-lookup"><span data-stu-id="92a40-145">A common use of this function is to split a mesh with 32-bit indices (more than 65535 vertices) into more than one mesh, each of which has 16-bit indices.</span></span>

<span data-ttu-id="92a40-146">Массивы — это массивы типа DWORD, где каждый массив содержит n указателей DWORD, за которыми следуют данные типа DWORD, на которые ссылаются указатели.</span><span class="sxs-lookup"><span data-stu-id="92a40-146">The adjacency, vertex remap and face remap arrays are arrays are DWORDs where each array contains n DWORD pointers, followed by the DWORD data referenced by the pointers.</span></span> <span data-ttu-id="92a40-147">Например, чтобы получить сведения о сопоставлении лиц для грани 3 в сетке 2, можно использовать следующий код, предполагая, что данные о переназначении лица были возвращены в переменной с именем *ппфацеремапаррайаут*.</span><span class="sxs-lookup"><span data-stu-id="92a40-147">For example, to obtain the face remap information for face 3 in mesh 2, the following code could be used, assuming the face remap data was returned in a variable named *ppFaceRemapArrayOut*.</span></span>


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a><span data-ttu-id="92a40-148">Требования</span><span class="sxs-lookup"><span data-stu-id="92a40-148">Requirements</span></span>



| <span data-ttu-id="92a40-149">Требование</span><span class="sxs-lookup"><span data-stu-id="92a40-149">Requirement</span></span> | <span data-ttu-id="92a40-150">Значение</span><span class="sxs-lookup"><span data-stu-id="92a40-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92a40-151">Header</span><span class="sxs-lookup"><span data-stu-id="92a40-151">Header</span></span><br/>  | <dl> <span data-ttu-id="92a40-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="92a40-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="92a40-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92a40-153">Library</span></span><br/> | <dl> <span data-ttu-id="92a40-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92a40-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="92a40-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92a40-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a40-156">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="92a40-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
