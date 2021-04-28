---
description: 'Метод ID3DXBaseMesh:: Жетиндексбуффер — получает данные в буфере индекса.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: 'Метод ID3DXBaseMesh:: Жетиндексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40e57193a2bf9a47ed0c57e6d13644441fbc42ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115432"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="d2d65-103">Метод ID3DXBaseMesh:: Жетиндексбуффер</span><span class="sxs-lookup"><span data-stu-id="d2d65-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="d2d65-104">Получает данные в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="d2d65-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2d65-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="d2d65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2d65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d65-107">*ппиб* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d2d65-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d65-108">Тип: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="d2d65-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="d2d65-109">Адрес указателя на интерфейс [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , представляющий объект буфера индекса, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="d2d65-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d65-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2d65-110">Return value</span></span>

<span data-ttu-id="d2d65-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2d65-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2d65-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d2d65-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d2d65-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="d2d65-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d65-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d2d65-114">Requirements</span></span>



| <span data-ttu-id="d2d65-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d2d65-115">Requirement</span></span> | <span data-ttu-id="d2d65-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d2d65-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d65-117">Header</span><span class="sxs-lookup"><span data-stu-id="d2d65-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d2d65-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d65-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d2d65-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2d65-119">Library</span></span><br/> | <dl> <span data-ttu-id="d2d65-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2d65-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2d65-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d2d65-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d65-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d2d65-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
