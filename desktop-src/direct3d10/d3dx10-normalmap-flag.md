---
description: Эти флаги используются для управления тем, как D3DX10ComputeNormalMap создает нормальные карты. Любое число этих флагов может быть или в любом сочетании.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Перечисление D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720918"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a><span data-ttu-id="1e345-104">\_ \_ Перечисление флагов нормалмап D3DX10</span><span class="sxs-lookup"><span data-stu-id="1e345-104">D3DX10\_NORMALMAP\_FLAG enumeration</span></span>

<span data-ttu-id="1e345-105">Эти флаги используются для управления тем, как [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) создает нормальные карты.</span><span class="sxs-lookup"><span data-stu-id="1e345-105">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="1e345-106">Любое число этих флагов может быть или в любом сочетании.</span><span class="sxs-lookup"><span data-stu-id="1e345-106">Any number of these flags may be OR'd together in any combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e345-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e345-107">Syntax</span></span>


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="1e345-108">Константы</span><span class="sxs-lookup"><span data-stu-id="1e345-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e345-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**\_ \_ Зеркальная копия D3DX10 нормалмап \_ U**</span><span class="sxs-lookup"><span data-stu-id="1e345-109"><span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="1e345-110">Указывает, что пиксели от края текстуры на оси U должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="1e345-110">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="1e345-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ нормалмап \_ Mirror \_ V**</span><span class="sxs-lookup"><span data-stu-id="1e345-111"><span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="1e345-112">Указывает, что пиксели с края текстуры на оси V должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="1e345-112">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="1e345-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**\_Зеркало D3DX10 нормалмап \_**</span><span class="sxs-lookup"><span data-stu-id="1e345-113"><span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="1e345-114">То же, что и D3DX10 \_ нормалмап \_ Mirror \_ U \| D3DX10 \_ нормалмап \_ Mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="1e345-114">Same as D3DX10\_NORMALMAP\_MIRROR\_U \| D3DX10\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="1e345-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ нормалмап \_ инвертсигн**</span><span class="sxs-lookup"><span data-stu-id="1e345-115"><span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="1e345-116">Инвертирует направление каждого нормального.</span><span class="sxs-lookup"><span data-stu-id="1e345-116">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="1e345-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10 \_ нормалмап \_ COMPUTE \_ перекрытия**</span><span class="sxs-lookup"><span data-stu-id="1e345-117"><span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="1e345-118">Выполняет вычисление Терма перекрытия на пиксель и кодирует его в альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="1e345-118">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="1e345-119">Значение альфа, равное 1, означает, что пиксел не закрывается каким-либо образом, а значение альфа, равное 0, означает, что пиксель полностью скрыт.</span><span class="sxs-lookup"><span data-stu-id="1e345-119">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e345-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1e345-120">Requirements</span></span>



| <span data-ttu-id="1e345-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1e345-121">Requirement</span></span> | <span data-ttu-id="1e345-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1e345-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e345-123">Header</span><span class="sxs-lookup"><span data-stu-id="1e345-123">Header</span></span><br/> | <dl> <span data-ttu-id="1e345-124"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e345-124"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e345-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e345-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e345-126">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="1e345-126">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




