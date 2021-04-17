---
description: Выполняет однородную тесселяцию на основе уровня тесселяции.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'Метод ID3DXPatchMesh:: тесселяции (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105665004"
---
# <a name="id3dxpatchmeshtessellate-method"></a><span data-ttu-id="1c2a3-103">Метод ID3DXPatchMesh:: тесселяции</span><span class="sxs-lookup"><span data-stu-id="1c2a3-103">ID3DXPatchMesh::Tessellate method</span></span>

<span data-ttu-id="1c2a3-104">Выполняет однородную тесселяцию на основе уровня тесселяции.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-104">Performs uniform tessellation based on the tessellation level.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c2a3-105">Syntax</span></span>


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="1c2a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c2a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c2a3-107">*фтесслевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c2a3-107">*fTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2a3-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2a3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c2a3-109">Уровень тесселяции.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-109">Tessellation level.</span></span> <span data-ttu-id="1c2a3-110">Это число вершин, появившихся между существующими вершинами.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-110">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="1c2a3-111">Диапазон этого параметра с плавающей запятой равен 0 < Фтесслевел <= 32.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-111">The range of this float parameter is 0 < fTessLevel <= 32.</span></span>

</dd> <dt>

<span data-ttu-id="1c2a3-112">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c2a3-112">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2a3-113">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2a3-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="1c2a3-114">Результирующая Тесселяция сетки.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-114">Resulting tessellated mesh.</span></span> <span data-ttu-id="1c2a3-115">См. [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="1c2a3-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c2a3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c2a3-116">Return value</span></span>

<span data-ttu-id="1c2a3-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c2a3-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c2a3-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1c2a3-119">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c2a3-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c2a3-120">Remarks</span></span>

<span data-ttu-id="1c2a3-121">Эта функция будет работать более эффективно, если сетка исправлений оптимизирована с помощью [**ID3DXPatchMesh:: optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="1c2a3-121">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c2a3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1c2a3-122">Requirements</span></span>



| <span data-ttu-id="1c2a3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1c2a3-123">Requirement</span></span> | <span data-ttu-id="1c2a3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1c2a3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2a3-125">Header</span><span class="sxs-lookup"><span data-stu-id="1c2a3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1c2a3-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1c2a3-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c2a3-127">Library</span></span><br/> | <dl> <span data-ttu-id="1c2a3-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c2a3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c2a3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2a3-130">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="1c2a3-130">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
