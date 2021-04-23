---
description: Преобразует заданный поднабор сетки в одну ленту треугольника.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: Функция D3DXConvertMeshSubsetToSingleStrip (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664959"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a><span data-ttu-id="1801f-103">Функция D3DXConvertMeshSubsetToSingleStrip</span><span class="sxs-lookup"><span data-stu-id="1801f-103">D3DXConvertMeshSubsetToSingleStrip function</span></span>

<span data-ttu-id="1801f-104">Преобразует заданный поднабор сетки в одну ленту треугольника.</span><span class="sxs-lookup"><span data-stu-id="1801f-104">Converts the specified mesh subset into a single triangle strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="1801f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1801f-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="1801f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1801f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1801f-107">*Сетка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1801f-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-108">Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1801f-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="1801f-109">Указатель на интерфейс [**ID3DXBaseMesh**](id3dxbasemesh.md) , представляющий сетку для преобразования в ленту.</span><span class="sxs-lookup"><span data-stu-id="1801f-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="1801f-110">*Аттрибид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1801f-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1801f-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1801f-112">Идентификатор атрибута подмножества сетки для преобразования в ленты.</span><span class="sxs-lookup"><span data-stu-id="1801f-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="1801f-113">*Ибоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1801f-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1801f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1801f-115">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) с указанием параметров для создания буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="1801f-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="1801f-116">Не может быть D3DXMESH \_ 32-разрядным.</span><span class="sxs-lookup"><span data-stu-id="1801f-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="1801f-117">Буфер индекса будет создан с 32-разрядными или 16-битовыми индексами в зависимости от формата буфера индекса сетки, указанной параметром *сетки* .</span><span class="sxs-lookup"><span data-stu-id="1801f-117">The index buffer will be created with 32-bit or 16-bit indices, depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1801f-118">*ппиндексбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1801f-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-119">Тип: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="1801f-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="1801f-120">Указатель на интерфейс [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , представляющий буфер индекса, содержащий полосу.</span><span class="sxs-lookup"><span data-stu-id="1801f-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="1801f-121">*пнуминдицес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1801f-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1801f-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1801f-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1801f-123">Количество индексов в буфере, возвращенном в параметре *ппиндексбуффер* .</span><span class="sxs-lookup"><span data-stu-id="1801f-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1801f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1801f-124">Return value</span></span>

<span data-ttu-id="1801f-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1801f-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1801f-126">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1801f-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1801f-127">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1801f-127">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1801f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1801f-128">Remarks</span></span>

<span data-ttu-id="1801f-129">Перед выполнением этой функции вызовите [**optimize**](id3dxmesh--optimize.md) или [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)с \_ установленным флагом D3DXMESHOPT аттрсорт.</span><span class="sxs-lookup"><span data-stu-id="1801f-129">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1801f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1801f-130">Requirements</span></span>



| <span data-ttu-id="1801f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1801f-131">Requirement</span></span> | <span data-ttu-id="1801f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1801f-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1801f-133">Header</span><span class="sxs-lookup"><span data-stu-id="1801f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1801f-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1801f-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1801f-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1801f-135">Library</span></span><br/> | <dl> <span data-ttu-id="1801f-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1801f-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1801f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1801f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1801f-138">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="1801f-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
