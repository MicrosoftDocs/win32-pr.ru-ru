---
description: Разблокируйте буфер атрибута.
ms.assetid: 4077ad15-9753-4031-81e7-c04e4267a0c9
title: 'Метод ID3DXPatchMesh:: Унлоккаттрибутебуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 42ea5ffacae2a2de073f6c16a9d29a7f76633ef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105665003"
---
# <a name="id3dxpatchmeshunlockattributebuffer-method"></a><span data-ttu-id="8b821-103">Метод ID3DXPatchMesh:: Унлоккаттрибутебуффер</span><span class="sxs-lookup"><span data-stu-id="8b821-103">ID3DXPatchMesh::UnlockAttributeBuffer method</span></span>

<span data-ttu-id="8b821-104">Разблокируйте буфер атрибута.</span><span class="sxs-lookup"><span data-stu-id="8b821-104">Unlock the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b821-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b821-105">Syntax</span></span>


```C++
HRESULT UnlockAttributeBuffer();
```



## <a name="parameters"></a><span data-ttu-id="8b821-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b821-106">Parameters</span></span>

<span data-ttu-id="8b821-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8b821-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b821-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b821-108">Return value</span></span>

<span data-ttu-id="8b821-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b821-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b821-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8b821-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8b821-111">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8b821-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b821-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b821-112">Remarks</span></span>

<span data-ttu-id="8b821-113">Буфер атрибутов обычно блокируется, записывается в, а затем разблокируется для чтения.</span><span class="sxs-lookup"><span data-stu-id="8b821-113">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b821-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8b821-114">Requirements</span></span>



| <span data-ttu-id="8b821-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8b821-115">Requirement</span></span> | <span data-ttu-id="8b821-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8b821-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b821-117">Header</span><span class="sxs-lookup"><span data-stu-id="8b821-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8b821-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b821-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8b821-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b821-119">Library</span></span><br/> | <dl> <span data-ttu-id="8b821-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b821-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b821-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b821-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b821-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="8b821-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




