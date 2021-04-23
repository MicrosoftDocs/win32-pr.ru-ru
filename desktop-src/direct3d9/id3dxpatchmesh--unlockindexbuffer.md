---
description: Разблокируйте буфер индексов.
ms.assetid: de3d0893-1596-42df-b049-6574c58ffa8d
title: 'Метод ID3DXPatchMesh:: Унлоккиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9bae54c6c4477682422328410558f1b405eb2677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694223"
---
# <a name="id3dxpatchmeshunlockindexbuffer-method"></a><span data-ttu-id="2bdb3-103">Метод ID3DXPatchMesh:: Унлоккиндексбуффер</span><span class="sxs-lookup"><span data-stu-id="2bdb3-103">ID3DXPatchMesh::UnlockIndexBuffer method</span></span>

<span data-ttu-id="2bdb3-104">Разблокируйте буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-104">Unlock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bdb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bdb3-105">Syntax</span></span>


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="2bdb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bdb3-106">Parameters</span></span>

<span data-ttu-id="2bdb3-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bdb3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bdb3-108">Return value</span></span>

<span data-ttu-id="2bdb3-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2bdb3-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2bdb3-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2bdb3-111">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bdb3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bdb3-112">Remarks</span></span>

<span data-ttu-id="2bdb3-113">Буфер индексов обычно блокируется, записывается в, а затем разблокируется для чтения.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-113">The index buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bdb3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2bdb3-114">Requirements</span></span>



| <span data-ttu-id="2bdb3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="2bdb3-115">Requirement</span></span> | <span data-ttu-id="2bdb3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2bdb3-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bdb3-117">Header</span><span class="sxs-lookup"><span data-stu-id="2bdb3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2bdb3-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bdb3-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2bdb3-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2bdb3-119">Library</span></span><br/> | <dl> <span data-ttu-id="2bdb3-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bdb3-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2bdb3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bdb3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdb3-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="2bdb3-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




