---
description: Извлекает буфер вершин, связанный с сеткой.
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
ms.openlocfilehash: 2098d97c1b7a685e9bd68cb3a6ac4feb6b949d2a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694082"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a><span data-ttu-id="7d057-103">Метод ID3DXBaseMesh:: Жетвертексбуффер</span><span class="sxs-lookup"><span data-stu-id="7d057-103">ID3DXBaseMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="7d057-104">Извлекает буфер вершин, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="7d057-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d057-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d057-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="7d057-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d057-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d057-107">*ППВБ* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7d057-107">*ppVB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7d057-108">Тип: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="7d057-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="7d057-109">Адрес указателя на интерфейс [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) , представляющий объект буфера вершин, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="7d057-109">Address of a pointer to an [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface, representing the vertex buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d057-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d057-110">Return value</span></span>

<span data-ttu-id="7d057-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d057-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d057-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7d057-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7d057-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="7d057-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d057-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7d057-114">Requirements</span></span>



| <span data-ttu-id="7d057-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7d057-115">Requirement</span></span> | <span data-ttu-id="7d057-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7d057-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d057-117">Header</span><span class="sxs-lookup"><span data-stu-id="7d057-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7d057-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d057-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7d057-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7d057-119">Library</span></span><br/> | <dl> <span data-ttu-id="7d057-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d057-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d057-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d057-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d057-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="7d057-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
