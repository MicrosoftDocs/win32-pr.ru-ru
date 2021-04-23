---
description: Описывает поверхность рендеринга.
ms.assetid: cffa1555-1fa2-427d-8bcb-da0e61d82152
title: Структура D3DXRTS_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 3a0b52f258956f7b62734ca97cc5d1bf5ed00ac3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000353"
---
# <a name="d3dxrts_desc-structure"></a><span data-ttu-id="dd2bb-103">\_Структура D3DXRTS DESC</span><span class="sxs-lookup"><span data-stu-id="dd2bb-103">D3DXRTS\_DESC structure</span></span>

<span data-ttu-id="dd2bb-104">Описывает поверхность рендеринга.</span><span class="sxs-lookup"><span data-stu-id="dd2bb-104">Describes a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd2bb-105">Syntax</span></span>


```C++
typedef struct D3DXRTS_DESC {
  UINT      Width;
  UINT      Height;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTS_DESC, *LPD3DXRTS_DESC;
```



## <a name="members"></a><span data-ttu-id="dd2bb-106">Члены</span><span class="sxs-lookup"><span data-stu-id="dd2bb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd2bb-107">**Width**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-107">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="dd2bb-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd2bb-109">Ширина поверхности рендеринга в пикселях.</span><span class="sxs-lookup"><span data-stu-id="dd2bb-109">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dd2bb-110">**Height**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-110">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="dd2bb-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd2bb-112">Высота поверхности рендеринга (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="dd2bb-112">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="dd2bb-113">**Формат**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="dd2bb-114">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd2bb-115">Элемент перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат пикселей поверхности рендеринга.</span><span class="sxs-lookup"><span data-stu-id="dd2bb-115">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="dd2bb-116">**депсстенЦил**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="dd2bb-117">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd2bb-118">Если **значение — true**, поверхность рендеринга поддерживает поверхность набора элементов глубины; в противном случае этому члену присваивается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="dd2bb-118">If **TRUE**, the render surface supports a depth-stencil surface; otherwise this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="dd2bb-119">**депсстенЦилформат**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="dd2bb-120">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd2bb-121">Если ДепсстенЦил имеет значение **true**, этот параметр является членом перечислимого типа [D3DFORMAT](d3dformat.md) , описывающим формат трафарета глубины области рендеринга.</span><span class="sxs-lookup"><span data-stu-id="dd2bb-121">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd2bb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dd2bb-122">Requirements</span></span>



| <span data-ttu-id="dd2bb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dd2bb-123">Requirement</span></span> | <span data-ttu-id="dd2bb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dd2bb-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2bb-125">Header</span><span class="sxs-lookup"><span data-stu-id="dd2bb-125">Header</span></span><br/> | <dl> <span data-ttu-id="dd2bb-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd2bb-126"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2bb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd2bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2bb-128">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="dd2bb-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="dd2bb-129">**ID3DXRenderToSurface:: DESC**</span><span class="sxs-lookup"><span data-stu-id="dd2bb-129">**ID3DXRenderToSurface::GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)
</dt> </dl>

 

 
