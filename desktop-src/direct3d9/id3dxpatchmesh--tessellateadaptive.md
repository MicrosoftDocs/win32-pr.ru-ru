---
description: Выполняет адаптивную тесселяцию на основе z-критерия адаптивной тесселяции.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'Метод ID3DXPatchMesh:: Тесселлатеадаптиве (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664985"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a><span data-ttu-id="85302-103">Метод ID3DXPatchMesh:: Тесселлатеадаптиве</span><span class="sxs-lookup"><span data-stu-id="85302-103">ID3DXPatchMesh::TessellateAdaptive method</span></span>

<span data-ttu-id="85302-104">Выполняет адаптивную тесселяцию на основе z-критерия адаптивной тесселяции.</span><span class="sxs-lookup"><span data-stu-id="85302-104">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span>

## <a name="syntax"></a><span data-ttu-id="85302-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85302-105">Syntax</span></span>


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="85302-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85302-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85302-107">*птранс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85302-107">*pTrans* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85302-108">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="85302-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="85302-109">Задает вектор 4D, который имеет пунктирные вершины для получения суммы адаптивной тесселяции для каждого вершины.</span><span class="sxs-lookup"><span data-stu-id="85302-109">Specifies a 4D vector that is dotted with the vertices to get the per-vertex adaptive tessellation amount.</span></span> <span data-ttu-id="85302-110">Каждый ребр размещается в среднем значении уровней тесселяции для двух вершин, к которым он подключается.</span><span class="sxs-lookup"><span data-stu-id="85302-110">Each edge is tessellated to the average value of the tessellation levels for the two vertices it connects.</span></span>

</dd> <dt>

<span data-ttu-id="85302-111">*двмакстесслевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85302-111">*dwMaxTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85302-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85302-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85302-113">Максимальный предел адаптивной тесселяции.</span><span class="sxs-lookup"><span data-stu-id="85302-113">Maximum limit for adaptive tessellation.</span></span> <span data-ttu-id="85302-114">Это число вершин, появившихся между существующими вершинами.</span><span class="sxs-lookup"><span data-stu-id="85302-114">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="85302-115">Это целое значение может находиться в диапазоне от 1 до 32 включительно.</span><span class="sxs-lookup"><span data-stu-id="85302-115">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="85302-116">*двминтесслевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85302-116">*dwMinTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85302-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85302-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85302-118">Минимальный предел для адаптивной тесселяции.</span><span class="sxs-lookup"><span data-stu-id="85302-118">Minimum limit for adaptive tessellation.</span></span> <span data-ttu-id="85302-119">Это число вершин, появившихся между существующими вершинами.</span><span class="sxs-lookup"><span data-stu-id="85302-119">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="85302-120">Это целое значение может находиться в диапазоне от 1 до 32 включительно.</span><span class="sxs-lookup"><span data-stu-id="85302-120">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="85302-121">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85302-121">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85302-122">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="85302-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="85302-123">Результирующая Тесселяция сетки.</span><span class="sxs-lookup"><span data-stu-id="85302-123">Resulting tessellated mesh.</span></span> <span data-ttu-id="85302-124">См. [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="85302-124">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85302-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85302-125">Return value</span></span>

<span data-ttu-id="85302-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85302-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85302-127">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="85302-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="85302-128">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="85302-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="85302-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85302-129">Remarks</span></span>

<span data-ttu-id="85302-130">Эта функция будет работать более эффективно, если сетка исправлений оптимизирована с помощью [**ID3DXPatchMesh:: optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="85302-130">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85302-131">Требования</span><span class="sxs-lookup"><span data-stu-id="85302-131">Requirements</span></span>



| <span data-ttu-id="85302-132">Требование</span><span class="sxs-lookup"><span data-stu-id="85302-132">Requirement</span></span> | <span data-ttu-id="85302-133">Значение</span><span class="sxs-lookup"><span data-stu-id="85302-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85302-134">Header</span><span class="sxs-lookup"><span data-stu-id="85302-134">Header</span></span><br/>  | <dl> <span data-ttu-id="85302-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="85302-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85302-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85302-136">Library</span></span><br/> | <dl> <span data-ttu-id="85302-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85302-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85302-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85302-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85302-139">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="85302-139">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
