---
description: Проверяет сетку.
ms.assetid: e5bec2f3-e914-4677-8114-77c71b8a586e
title: Функция D3DXValidMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 469b9b32072107885417266266f804a955301668
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354610"
---
# <a name="d3dxvalidmesh-function"></a><span data-ttu-id="0faf8-103">Функция D3DXValidMesh</span><span class="sxs-lookup"><span data-stu-id="0faf8-103">D3DXValidMesh function</span></span>

<span data-ttu-id="0faf8-104">Проверяет сетку.</span><span class="sxs-lookup"><span data-stu-id="0faf8-104">Validates a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0faf8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0faf8-105">Syntax</span></span>


```C++
HRESULT D3DXValidMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacency,
  _Out_       LPD3DXBUFFER *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="0faf8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0faf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0faf8-107">*пмешин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0faf8-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0faf8-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0faf8-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0faf8-109">Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий проверяемую сеть.</span><span class="sxs-lookup"><span data-stu-id="0faf8-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="0faf8-110">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0faf8-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0faf8-111">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0faf8-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0faf8-112">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждого лица в проверяемой сети.</span><span class="sxs-lookup"><span data-stu-id="0faf8-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="0faf8-113">*пперрорсандварнингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0faf8-113">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0faf8-114">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0faf8-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0faf8-115">Возвращает буфер, содержащий строку ошибок и предупреждений, в которых объясняются проблемы, обнаруженные в сетке.</span><span class="sxs-lookup"><span data-stu-id="0faf8-115">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0faf8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0faf8-116">Return value</span></span>

<span data-ttu-id="0faf8-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0faf8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0faf8-118">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0faf8-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0faf8-119">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DXERR \_ инвалидмеш, D3DERR \_ Инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0faf8-119">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0faf8-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0faf8-120">Remarks</span></span>

<span data-ttu-id="0faf8-121">Этот метод проверяет сетку, проверяя наличие недопустимых индексов.</span><span class="sxs-lookup"><span data-stu-id="0faf8-121">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="0faf8-122">Сведения об ошибках доступны в выходных данных отладчика.</span><span class="sxs-lookup"><span data-stu-id="0faf8-122">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="0faf8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0faf8-123">Requirements</span></span>



| <span data-ttu-id="0faf8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0faf8-124">Requirement</span></span> | <span data-ttu-id="0faf8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0faf8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0faf8-126">Header</span><span class="sxs-lookup"><span data-stu-id="0faf8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0faf8-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0faf8-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0faf8-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0faf8-128">Library</span></span><br/> | <dl> <span data-ttu-id="0faf8-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0faf8-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0faf8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0faf8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0faf8-131">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="0faf8-131">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
