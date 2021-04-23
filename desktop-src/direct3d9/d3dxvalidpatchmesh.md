---
description: Проверяет сетку исправлений, возвращая число вырожденных вершин и исправлений.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Функция D3DXValidPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000343"
---
# <a name="d3dxvalidpatchmesh-function"></a><span data-ttu-id="93d16-103">Функция D3DXValidPatchMesh</span><span class="sxs-lookup"><span data-stu-id="93d16-103">D3DXValidPatchMesh function</span></span>

<span data-ttu-id="93d16-104">Проверяет сетку исправлений, возвращая число вырожденных вершин и исправлений.</span><span class="sxs-lookup"><span data-stu-id="93d16-104">Validates a patch mesh, returning the number of degenerate vertices and patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d16-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93d16-105">Syntax</span></span>


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="93d16-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="93d16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d16-107">*пмешин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d16-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d16-108">Тип: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="93d16-108">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span></span>

<span data-ttu-id="93d16-109">Указатель на интерфейс [**ID3DXPatchMesh**](id3dxpatchmesh.md) , представляющий проверяемую сетку исправлений.</span><span class="sxs-lookup"><span data-stu-id="93d16-109">Pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the patch mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="93d16-110">*пнумдеженератевертицес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="93d16-110">*pNumDegenerateVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93d16-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="93d16-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="93d16-112">Возвращает число вырожденных вершин в сетке исправлений.</span><span class="sxs-lookup"><span data-stu-id="93d16-112">Returns the number of degenerate vertices in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="93d16-113">*пнумдеженератепатчес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="93d16-113">*pNumDegeneratePatches* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93d16-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="93d16-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="93d16-115">Возвращает число вырожденных исправлений в сетке исправлений.</span><span class="sxs-lookup"><span data-stu-id="93d16-115">Returns the number of degenerate patches in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="93d16-116">*пперрорсандварнингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="93d16-116">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93d16-117">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="93d16-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="93d16-118">Возвращает указатель на буфер, содержащий строку ошибок и предупреждений, объясняющих проблемы, обнаруженные в сетке исправлений.</span><span class="sxs-lookup"><span data-stu-id="93d16-118">Returns a pointer to a buffer containing a string of errors and warnings that explain the problems found in the patch mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d16-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93d16-119">Return value</span></span>

<span data-ttu-id="93d16-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93d16-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93d16-121">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="93d16-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="93d16-122">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="93d16-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="93d16-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93d16-123">Remarks</span></span>

<span data-ttu-id="93d16-124">Этот метод проверяет сетку, проверяя наличие недопустимых индексов.</span><span class="sxs-lookup"><span data-stu-id="93d16-124">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="93d16-125">Сведения об ошибках доступны в выходных данных отладчика.</span><span class="sxs-lookup"><span data-stu-id="93d16-125">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="93d16-126">Требования</span><span class="sxs-lookup"><span data-stu-id="93d16-126">Requirements</span></span>



| <span data-ttu-id="93d16-127">Требование</span><span class="sxs-lookup"><span data-stu-id="93d16-127">Requirement</span></span> | <span data-ttu-id="93d16-128">Значение</span><span class="sxs-lookup"><span data-stu-id="93d16-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93d16-129">Header</span><span class="sxs-lookup"><span data-stu-id="93d16-129">Header</span></span><br/>  | <dl> <span data-ttu-id="93d16-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="93d16-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="93d16-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="93d16-131">Library</span></span><br/> | <dl> <span data-ttu-id="93d16-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93d16-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93d16-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93d16-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d16-134">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="93d16-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
