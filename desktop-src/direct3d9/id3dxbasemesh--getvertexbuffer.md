---
description: 'Метод ID3DXBaseMesh:: Жетвертексбуффер — получает буфер вершин, связанный с сеткой.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: 'Метод ID3DXBaseMesh:: Жетвертексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115372"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="0f852-103">Метод ID3DXBaseMesh:: Жетвертексбуффер</span><span class="sxs-lookup"><span data-stu-id="0f852-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="0f852-104">Извлекает буфер вершин, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="0f852-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f852-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f852-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="0f852-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f852-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f852-107">*ППВБ* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0f852-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0f852-108">Тип: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="0f852-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="0f852-109">Адрес указателя на интерфейс [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) , представляющий объект буфера вершин, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="0f852-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f852-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f852-110">Return value</span></span>

<span data-ttu-id="0f852-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f852-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f852-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0f852-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0f852-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0f852-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f852-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0f852-114">Requirements</span></span>



| <span data-ttu-id="0f852-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0f852-115">Requirement</span></span> | <span data-ttu-id="0f852-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0f852-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f852-117">Header</span><span class="sxs-lookup"><span data-stu-id="0f852-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0f852-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f852-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0f852-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f852-119">Library</span></span><br/> | <dl> <span data-ttu-id="0f852-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f852-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0f852-121">См. также</span><span class="sxs-lookup"><span data-stu-id="0f852-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f852-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="0f852-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
