---
description: Создает сетку N-Patch из сетки треугольников.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: Функция D3DXCreateNPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ab73d1254700808bbd56b7b46f7781b27b188b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694308"
---
# <a name="d3dxcreatenpatchmesh-function"></a><span data-ttu-id="f7caf-103">Функция D3DXCreateNPatchMesh</span><span class="sxs-lookup"><span data-stu-id="f7caf-103">D3DXCreateNPatchMesh function</span></span>

<span data-ttu-id="f7caf-104">Создает сетку N-Patch из сетки треугольников.</span><span class="sxs-lookup"><span data-stu-id="f7caf-104">Creates an N-patch mesh from a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7caf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7caf-105">Syntax</span></span>


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="f7caf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7caf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7caf-107">*пмешсисмем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7caf-107">*pMeshSysMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7caf-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f7caf-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f7caf-109">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий объект сетки треугольника.</span><span class="sxs-lookup"><span data-stu-id="f7caf-109">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represents the triangle mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="f7caf-110">*ппатчмеш* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f7caf-110">*pPatchMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7caf-111">Тип: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7caf-111">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="f7caf-112">Адрес указателя на интерфейс [**ID3DXPatchMesh**](id3dxpatchmesh.md) , представляющий созданный объект сетки исправлений.</span><span class="sxs-lookup"><span data-stu-id="f7caf-112">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the created patch mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7caf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7caf-113">Return value</span></span>

<span data-ttu-id="f7caf-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7caf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7caf-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f7caf-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f7caf-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f7caf-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7caf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f7caf-117">Requirements</span></span>



| <span data-ttu-id="f7caf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f7caf-118">Requirement</span></span> | <span data-ttu-id="f7caf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f7caf-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7caf-120">Header</span><span class="sxs-lookup"><span data-stu-id="f7caf-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f7caf-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7caf-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f7caf-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f7caf-122">Library</span></span><br/> | <dl> <span data-ttu-id="f7caf-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7caf-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7caf-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7caf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7caf-125">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="f7caf-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




