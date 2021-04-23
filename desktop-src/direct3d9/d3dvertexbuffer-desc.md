---
description: Описывает буфер вершин.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: Структура D3DVERTEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548007"
---
# <a name="d3dvertexbuffer_desc-structure"></a><span data-ttu-id="df502-103">\_Структура D3DVERTEXBUFFER DESC</span><span class="sxs-lookup"><span data-stu-id="df502-103">D3DVERTEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="df502-104">Описывает буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="df502-104">Describes a vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="df502-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df502-105">Syntax</span></span>


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="df502-106">Члены</span><span class="sxs-lookup"><span data-stu-id="df502-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="df502-107">**Формат**</span><span class="sxs-lookup"><span data-stu-id="df502-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="df502-108">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="df502-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df502-109">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности данных буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="df502-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the vertex buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="df502-110">**Тип**</span><span class="sxs-lookup"><span data-stu-id="df502-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="df502-111">Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="df502-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df502-112">Член перечисляемого типа [**D3DRESOURCETYPE**](./d3dresourcetype.md) , определяющий этот ресурс в качестве буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="df502-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="df502-113">**Использование**</span><span class="sxs-lookup"><span data-stu-id="df502-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="df502-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df502-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df502-115">Сочетание одного или нескольких флагов [**D3DUSAGE**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="df502-115">Combination of one or more [**D3DUSAGE**](d3dusage.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="df502-116">**Пул.**</span><span class="sxs-lookup"><span data-stu-id="df502-116">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="df502-117">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="df502-117">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df502-118">Член перечисляемого типа [**D3DPOOL**](./d3dpool.md) , указывающий класс памяти, выделенной для этого буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="df502-118">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="df502-119">**Размер**</span><span class="sxs-lookup"><span data-stu-id="df502-119">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="df502-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df502-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df502-121">Размер буфера вершин в байтах.</span><span class="sxs-lookup"><span data-stu-id="df502-121">Size of the vertex buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="df502-122">**фвф**</span><span class="sxs-lookup"><span data-stu-id="df502-122">**FVF**</span></span>
</dt> <dd>

<span data-ttu-id="df502-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df502-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="df502-124">Сочетание [D3DFVF](d3dfvf.md) , описывающее формат вершины вершин в этом буфере.</span><span class="sxs-lookup"><span data-stu-id="df502-124">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format of the vertices in this buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df502-125">Требования</span><span class="sxs-lookup"><span data-stu-id="df502-125">Requirements</span></span>



| <span data-ttu-id="df502-126">Требование</span><span class="sxs-lookup"><span data-stu-id="df502-126">Requirement</span></span> | <span data-ttu-id="df502-127">Значение</span><span class="sxs-lookup"><span data-stu-id="df502-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df502-128">Header</span><span class="sxs-lookup"><span data-stu-id="df502-128">Header</span></span><br/> | <dl> <span data-ttu-id="df502-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="df502-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df502-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df502-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df502-131">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="df502-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="df502-132">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="df502-132">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="df502-133">Буферы вершин (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="df502-133">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
