---
description: Преобразование указанного подмножества сетки в ряд полос.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: Функция D3DXConvertMeshSubsetToStrips (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703951"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a><span data-ttu-id="325c0-103">Функция D3DXConvertMeshSubsetToStrips</span><span class="sxs-lookup"><span data-stu-id="325c0-103">D3DXConvertMeshSubsetToStrips function</span></span>

<span data-ttu-id="325c0-104">Преобразование указанного подмножества сетки в ряд полос.</span><span class="sxs-lookup"><span data-stu-id="325c0-104">Convert the specified mesh subset into a series of strips.</span></span>

## <a name="syntax"></a><span data-ttu-id="325c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="325c0-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a><span data-ttu-id="325c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="325c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="325c0-107">*Сетка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="325c0-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="325c0-108">Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="325c0-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="325c0-109">Указатель на интерфейс [**ID3DXBaseMesh**](id3dxbasemesh.md) , представляющий сетку для преобразования в ленту.</span><span class="sxs-lookup"><span data-stu-id="325c0-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="325c0-110">*Аттрибид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="325c0-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="325c0-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="325c0-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="325c0-112">Идентификатор атрибута подмножества сетки для преобразования в ленты.</span><span class="sxs-lookup"><span data-stu-id="325c0-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="325c0-113">*Ибоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="325c0-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="325c0-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="325c0-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="325c0-115">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) с указанием параметров для создания буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="325c0-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="325c0-116">Не может быть D3DXMESH \_ 32-разрядным.</span><span class="sxs-lookup"><span data-stu-id="325c0-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="325c0-117">Буфер индексов будет создан с 32-разрядными или 16-битовыми индексами в зависимости от формата буфера индекса сетки, указанной параметром *сетки* .</span><span class="sxs-lookup"><span data-stu-id="325c0-117">The index buffer will be created with 32-bit or 16-bit indices depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="325c0-118">*ппиндексбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="325c0-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="325c0-119">Тип: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="325c0-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="325c0-120">Указатель на интерфейс [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , представляющий буфер индекса, содержащий полосу.</span><span class="sxs-lookup"><span data-stu-id="325c0-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="325c0-121">*пнуминдицес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="325c0-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="325c0-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="325c0-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="325c0-123">Количество индексов в буфере, возвращенном в параметре *ппиндексбуффер* .</span><span class="sxs-lookup"><span data-stu-id="325c0-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="325c0-124">*ппстрипленгсс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="325c0-124">*ppStripLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="325c0-125">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="325c0-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="325c0-126">Буфер, содержащий массив из одного DWORD на ленту, который указывает количество треугольников в этой полосе.</span><span class="sxs-lookup"><span data-stu-id="325c0-126">Buffer containing an array of one DWORD per strip, which specifies the number of triangles in the that strip.</span></span>

</dd> <dt>

<span data-ttu-id="325c0-127">*пнумстрипс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="325c0-127">*pNumStrips* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="325c0-128">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="325c0-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="325c0-129">Число отдельных лент в буфере индекса и соответствующий массив длины полосы.</span><span class="sxs-lookup"><span data-stu-id="325c0-129">Number of individual strips in the index buffer and corresponding strip length array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="325c0-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="325c0-130">Return value</span></span>

<span data-ttu-id="325c0-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="325c0-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="325c0-132">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="325c0-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="325c0-133">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="325c0-133">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="325c0-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="325c0-134">Remarks</span></span>

<span data-ttu-id="325c0-135">Перед выполнением этой функции вызовите [**optimize**](id3dxmesh--optimize.md) или [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)с \_ установленным флагом D3DXMESHOPT аттрсорт.</span><span class="sxs-lookup"><span data-stu-id="325c0-135">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="325c0-136">Требования</span><span class="sxs-lookup"><span data-stu-id="325c0-136">Requirements</span></span>



| <span data-ttu-id="325c0-137">Требование</span><span class="sxs-lookup"><span data-stu-id="325c0-137">Requirement</span></span> | <span data-ttu-id="325c0-138">Значение</span><span class="sxs-lookup"><span data-stu-id="325c0-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="325c0-139">Header</span><span class="sxs-lookup"><span data-stu-id="325c0-139">Header</span></span><br/>  | <dl> <span data-ttu-id="325c0-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="325c0-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="325c0-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="325c0-141">Library</span></span><br/> | <dl> <span data-ttu-id="325c0-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="325c0-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="325c0-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="325c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325c0-144">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="325c0-144">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
