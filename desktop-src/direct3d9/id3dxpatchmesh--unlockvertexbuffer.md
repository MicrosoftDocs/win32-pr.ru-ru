---
description: Разблокируйте буфер вершин.
ms.assetid: 98b82fd1-56e8-45f3-bf26-a1e3b54c2979
title: 'Метод ID3DXPatchMesh:: Унлокквертексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6d4b6a55281048b303733e1addf2ab4636f74ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694341"
---
# <a name="id3dxpatchmeshunlockvertexbuffer-method"></a><span data-ttu-id="d5cd7-103">Метод ID3DXPatchMesh:: Унлокквертексбуффер</span><span class="sxs-lookup"><span data-stu-id="d5cd7-103">ID3DXPatchMesh::UnlockVertexBuffer method</span></span>

<span data-ttu-id="d5cd7-104">Разблокируйте буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-104">Unlock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5cd7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5cd7-105">Syntax</span></span>


```C++
HRESULT UnlockVertexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="d5cd7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5cd7-106">Parameters</span></span>

<span data-ttu-id="d5cd7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5cd7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5cd7-108">Return value</span></span>

<span data-ttu-id="d5cd7-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5cd7-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5cd7-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5cd7-111">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5cd7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5cd7-112">Remarks</span></span>

<span data-ttu-id="d5cd7-113">Буфер вершин обычно блокируется, записывается в, а затем разблокируется для чтения.</span><span class="sxs-lookup"><span data-stu-id="d5cd7-113">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5cd7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d5cd7-114">Requirements</span></span>



| <span data-ttu-id="d5cd7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d5cd7-115">Requirement</span></span> | <span data-ttu-id="d5cd7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d5cd7-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5cd7-117">Header</span><span class="sxs-lookup"><span data-stu-id="d5cd7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d5cd7-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd7-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d5cd7-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5cd7-119">Library</span></span><br/> | <dl> <span data-ttu-id="d5cd7-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd7-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d5cd7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5cd7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5cd7-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="d5cd7-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




