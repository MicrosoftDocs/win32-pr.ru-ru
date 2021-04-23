---
description: Возвращает буфер индекса сетки.
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'Метод ID3DXPatchMesh:: Жетиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2730b90f77d33db519d2231a68ab7fdc2b520fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713935"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a><span data-ttu-id="a60e0-103">Метод ID3DXPatchMesh:: Жетиндексбуффер</span><span class="sxs-lookup"><span data-stu-id="a60e0-103">ID3DXPatchMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="a60e0-104">Возвращает буфер индекса сетки.</span><span class="sxs-lookup"><span data-stu-id="a60e0-104">Gets the mesh index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a60e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a60e0-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="a60e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a60e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a60e0-107">*ппиб* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a60e0-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a60e0-108">Тип: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="a60e0-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="a60e0-109">Указатель на индексный буфер.</span><span class="sxs-lookup"><span data-stu-id="a60e0-109">Pointer to the index buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a60e0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a60e0-110">Return value</span></span>

<span data-ttu-id="a60e0-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a60e0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a60e0-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a60e0-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a60e0-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a60e0-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a60e0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a60e0-114">Remarks</span></span>

<span data-ttu-id="a60e0-115">Буфер индексов содержит упорядочивание вершин в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="a60e0-115">The index buffer contains the vertex ordering in the vertex buffer.</span></span> <span data-ttu-id="a60e0-116">Буферы индексов используются для доступа к буферу вершин при подготовке к просмотру сетки.</span><span class="sxs-lookup"><span data-stu-id="a60e0-116">The index buffer is used to access the vertex buffer when the mesh is rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="a60e0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a60e0-117">Requirements</span></span>



| <span data-ttu-id="a60e0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a60e0-118">Requirement</span></span> | <span data-ttu-id="a60e0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a60e0-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a60e0-120">Header</span><span class="sxs-lookup"><span data-stu-id="a60e0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a60e0-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a60e0-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a60e0-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a60e0-122">Library</span></span><br/> | <dl> <span data-ttu-id="a60e0-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a60e0-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a60e0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a60e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a60e0-125">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="a60e0-125">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
