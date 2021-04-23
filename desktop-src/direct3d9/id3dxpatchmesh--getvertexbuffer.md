---
description: Возвращает буфер вершин сетки.
ms.assetid: 4ea4e99b-5c2c-467b-8b5d-8174c446680a
title: 'Метод ID3DXPatchMesh:: Жетвертексбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8c3bb79d4c04db072adef857de195df7a0f0fff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714035"
---
# <a name="id3dxpatchmeshgetvertexbuffer-method"></a><span data-ttu-id="c351f-103">Метод ID3DXPatchMesh:: Жетвертексбуффер</span><span class="sxs-lookup"><span data-stu-id="c351f-103">ID3DXPatchMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="c351f-104">Возвращает буфер вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="c351f-104">Gets the mesh vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c351f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c351f-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="c351f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c351f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c351f-107">*ППВБ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c351f-107">*ppVB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c351f-108">Тип: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="c351f-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="c351f-109">Указатель на буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="c351f-109">Pointer to the vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c351f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c351f-110">Return value</span></span>

<span data-ttu-id="c351f-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c351f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c351f-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c351f-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c351f-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c351f-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c351f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c351f-114">Remarks</span></span>

<span data-ttu-id="c351f-115">Этот метод предполагает однородную тесселяцию.</span><span class="sxs-lookup"><span data-stu-id="c351f-115">This method assumes uniform tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c351f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c351f-116">Requirements</span></span>



| <span data-ttu-id="c351f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c351f-117">Requirement</span></span> | <span data-ttu-id="c351f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c351f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c351f-119">Header</span><span class="sxs-lookup"><span data-stu-id="c351f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c351f-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c351f-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c351f-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c351f-121">Library</span></span><br/> | <dl> <span data-ttu-id="c351f-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c351f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c351f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c351f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c351f-124">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="c351f-124">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
