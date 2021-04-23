---
title: Перечисление D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Стандартные параметры карт. Любое число этих флагов можно объединить с помощью побитовой операции или.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- Перечисление D3DX11_NORMALMAP_FLAG Direct3D 11
- Указатель перечисления LPD3DX11_NORMALMAP_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273964"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a><span data-ttu-id="da5a4-107">\_ \_ Перечисление флагов нормалмап D3DX11</span><span class="sxs-lookup"><span data-stu-id="da5a4-107">D3DX11\_NORMALMAP\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="da5a4-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="da5a4-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="da5a4-109">Стандартные параметры карт.</span><span class="sxs-lookup"><span data-stu-id="da5a4-109">Normal map options.</span></span> <span data-ttu-id="da5a4-110">Любое число этих флагов можно объединить с помощью побитовой операции или.</span><span class="sxs-lookup"><span data-stu-id="da5a4-110">You can combine any number of these flags by using a bitwise OR operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="da5a4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da5a4-111">Syntax</span></span>


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a><span data-ttu-id="da5a4-112">Константы</span><span class="sxs-lookup"><span data-stu-id="da5a4-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da5a4-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**\_ \_ Зеркальная копия D3DX11 нормалмап \_ U**</span><span class="sxs-lookup"><span data-stu-id="da5a4-113"><span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11\_NORMALMAP\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="da5a4-114">Указывает, что пиксели от края текстуры на оси U должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="da5a4-114">Indicates that pixels off the edge of the texture on the U-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="da5a4-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ нормалмап \_ Mirror \_ V**</span><span class="sxs-lookup"><span data-stu-id="da5a4-115"><span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11\_NORMALMAP\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="da5a4-116">Указывает, что пиксели с края текстуры на оси V должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="da5a4-116">Indicates that pixels off the edge of the texture on the V-axis should be mirrored, not wraped.</span></span>

</dd> <dt>

<span data-ttu-id="da5a4-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**\_Зеркало D3DX11 нормалмап \_**</span><span class="sxs-lookup"><span data-stu-id="da5a4-117"><span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11\_NORMALMAP\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="da5a4-118">То же, что и D3DX11 \_ нормалмап \_ Mirror \_ U \| D3DX11 \_ нормалмап \_ Mirror \_ V.</span><span class="sxs-lookup"><span data-stu-id="da5a4-118">Same as D3DX11\_NORMALMAP\_MIRROR\_U \| D3DX11\_NORMALMAP\_MIRROR\_V.</span></span>

</dd> <dt>

<span data-ttu-id="da5a4-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ нормалмап \_ инвертсигн**</span><span class="sxs-lookup"><span data-stu-id="da5a4-119"><span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11\_NORMALMAP\_INVERTSIGN**</span></span>
</dt> <dd>

<span data-ttu-id="da5a4-120">Инвертирует направление каждого нормального.</span><span class="sxs-lookup"><span data-stu-id="da5a4-120">Inverts the direction of each normal.</span></span>

</dd> <dt>

<span data-ttu-id="da5a4-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11 \_ нормалмап \_ COMPUTE \_ перекрытия**</span><span class="sxs-lookup"><span data-stu-id="da5a4-121"><span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11\_NORMALMAP\_COMPUTE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="da5a4-122">Выполняет вычисление Терма перекрытия на пиксель и кодирует его в альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="da5a4-122">Computes the per pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="da5a4-123">Значение альфа, равное 1, означает, что пиксел не закрывается каким-либо образом, а значение альфа, равное 0, означает, что пиксель полностью скрыт.</span><span class="sxs-lookup"><span data-stu-id="da5a4-123">An Alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 would mean that the pixel is completely obscured.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da5a4-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="da5a4-124">Remarks</span></span>

<span data-ttu-id="da5a4-125">Эти флаги используются [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span><span class="sxs-lookup"><span data-stu-id="da5a4-125">These flags are used by [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da5a4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="da5a4-126">Requirements</span></span>



| <span data-ttu-id="da5a4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="da5a4-127">Requirement</span></span> | <span data-ttu-id="da5a4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="da5a4-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da5a4-129">Header</span><span class="sxs-lookup"><span data-stu-id="da5a4-129">Header</span></span><br/> | <dl> <span data-ttu-id="da5a4-130"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="da5a4-130"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da5a4-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da5a4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5a4-132">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="da5a4-132">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





