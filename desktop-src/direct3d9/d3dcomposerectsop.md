---
description: Задает способ объединения данных глифов из исходных и целевых поверхностей в вызове Компосеректс.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: Перечисление D3DCOMPOSERECTSOP (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cd47cb14ab129bf27a4b59ba07e0be12d144fb8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713569"
---
# <a name="d3dcomposerectsop-enumeration"></a><span data-ttu-id="f2592-103">Перечисление D3DCOMPOSERECTSOP</span><span class="sxs-lookup"><span data-stu-id="f2592-103">D3DCOMPOSERECTSOP enumeration</span></span>

<span data-ttu-id="f2592-104">Задает способ объединения данных глифов из исходных и целевых поверхностей в вызове [**компосеректс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span><span class="sxs-lookup"><span data-stu-id="f2592-104">Specifies how to combine the glyph data from the source and destination surfaces in a call to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2592-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2592-105">Syntax</span></span>


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a><span data-ttu-id="f2592-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f2592-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f2592-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**\_Копирование D3DCOMPOSERECTS**</span><span class="sxs-lookup"><span data-stu-id="f2592-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="f2592-108">Скопируйте источник в место назначения.</span><span class="sxs-lookup"><span data-stu-id="f2592-108">Copy the source to the destination.</span></span>

</dd> <dt>

<span data-ttu-id="f2592-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ или**</span><span class="sxs-lookup"><span data-stu-id="f2592-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS\_OR**</span></span>
</dt> <dd>

<span data-ttu-id="f2592-110">Побитовое или исходное и конечное.</span><span class="sxs-lookup"><span data-stu-id="f2592-110">Bitwise OR the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="f2592-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ и**</span><span class="sxs-lookup"><span data-stu-id="f2592-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS\_AND**</span></span>
</dt> <dd>

<span data-ttu-id="f2592-112">Побитовое и исходное и конечное.</span><span class="sxs-lookup"><span data-stu-id="f2592-112">Bitwise AND the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="f2592-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_**</span><span class="sxs-lookup"><span data-stu-id="f2592-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS\_NEG**</span></span>
</dt> <dd>

<span data-ttu-id="f2592-114">Скопируйте источник с отрицанием в место назначения (DST & ~ src).</span><span class="sxs-lookup"><span data-stu-id="f2592-114">Copy the negated source to the destination (Dst & ~Src).</span></span>

</dd> <dt>

<span data-ttu-id="f2592-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f2592-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f2592-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f2592-116">Reserved.</span></span> <span data-ttu-id="f2592-117">Используется для принудительного перечисления в 32-разрядный размер.</span><span class="sxs-lookup"><span data-stu-id="f2592-117">Used to force enumeration to 32-bits in size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2592-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f2592-118">Requirements</span></span>



| <span data-ttu-id="f2592-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f2592-119">Requirement</span></span> | <span data-ttu-id="f2592-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f2592-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2592-121">Header</span><span class="sxs-lookup"><span data-stu-id="f2592-121">Header</span></span><br/> | <dl> <span data-ttu-id="f2592-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2592-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2592-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2592-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2592-124">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="f2592-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




