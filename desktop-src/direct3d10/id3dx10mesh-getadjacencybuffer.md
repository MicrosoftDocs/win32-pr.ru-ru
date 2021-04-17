---
description: Доступ к буферу соседей в сетке.
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: 'Метод ID3DX10Mesh:: Жетаджаценцибуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80dd5c6e6d9b12cb1c648c42a4758d215d3810c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703897"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a><span data-ttu-id="bf80c-103">Метод ID3DX10Mesh:: Жетаджаценцибуффер</span><span class="sxs-lookup"><span data-stu-id="bf80c-103">ID3DX10Mesh::GetAdjacencyBuffer method</span></span>

<span data-ttu-id="bf80c-104">Доступ к буферу соседей в сетке.</span><span class="sxs-lookup"><span data-stu-id="bf80c-104">Access the mesh's adjacency buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf80c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf80c-105">Syntax</span></span>


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="bf80c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf80c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf80c-107">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf80c-107">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf80c-108">Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bf80c-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="bf80c-109">Буфер соседства.</span><span class="sxs-lookup"><span data-stu-id="bf80c-109">The adjacency buffer.</span></span> <span data-ttu-id="bf80c-110">См. [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="bf80c-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf80c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf80c-111">Return value</span></span>

<span data-ttu-id="bf80c-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf80c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf80c-113">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bf80c-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf80c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bf80c-114">Requirements</span></span>



| <span data-ttu-id="bf80c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bf80c-115">Requirement</span></span> | <span data-ttu-id="bf80c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bf80c-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf80c-117">Header</span><span class="sxs-lookup"><span data-stu-id="bf80c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bf80c-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf80c-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf80c-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf80c-119">Library</span></span><br/> | <dl> <span data-ttu-id="bf80c-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf80c-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf80c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf80c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf80c-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="bf80c-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="bf80c-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="bf80c-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




