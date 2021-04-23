---
description: Извлекает буфер вершин, связанный с сеткой.
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'Метод ID3DX10Mesh:: Жетвертексбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b78db368f2467c25b4bb4218a314a22027d5d3f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703892"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a><span data-ttu-id="80856-103">Метод ID3DX10Mesh:: Жетвертексбуффер</span><span class="sxs-lookup"><span data-stu-id="80856-103">ID3DX10Mesh::GetVertexBuffer method</span></span>

<span data-ttu-id="80856-104">Извлекает буфер вершин, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="80856-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="80856-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80856-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="80856-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80856-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80856-107">*iBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80856-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80856-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80856-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80856-109">Буфер вершин для получения.</span><span class="sxs-lookup"><span data-stu-id="80856-109">The vertex buffer to get.</span></span> <span data-ttu-id="80856-110">Это значение индекса.</span><span class="sxs-lookup"><span data-stu-id="80856-110">This is an index value.</span></span>

</dd> <dt>

<span data-ttu-id="80856-111">*ппвертексбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80856-111">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80856-112">Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="80856-112">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="80856-113">Буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="80856-113">The vertex buffer.</span></span> <span data-ttu-id="80856-114">См. [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="80856-114">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80856-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80856-115">Return value</span></span>

<span data-ttu-id="80856-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80856-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80856-117">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="80856-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80856-118">Требования</span><span class="sxs-lookup"><span data-stu-id="80856-118">Requirements</span></span>



| <span data-ttu-id="80856-119">Требование</span><span class="sxs-lookup"><span data-stu-id="80856-119">Requirement</span></span> | <span data-ttu-id="80856-120">Значение</span><span class="sxs-lookup"><span data-stu-id="80856-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80856-121">Header</span><span class="sxs-lookup"><span data-stu-id="80856-121">Header</span></span><br/>  | <dl> <span data-ttu-id="80856-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="80856-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="80856-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80856-123">Library</span></span><br/> | <dl> <span data-ttu-id="80856-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80856-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80856-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80856-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80856-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="80856-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="80856-127">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="80856-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
