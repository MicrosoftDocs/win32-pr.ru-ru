---
description: Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Перечисление D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355633"
---
# <a name="d3dx10_channel_flag-enumeration"></a><span data-ttu-id="e43c1-103">\_ \_ Перечисление флагов канала D3DX10</span><span class="sxs-lookup"><span data-stu-id="e43c1-103">D3DX10\_CHANNEL\_FLAG enumeration</span></span>

<span data-ttu-id="e43c1-104">Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.</span><span class="sxs-lookup"><span data-stu-id="e43c1-104">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e43c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e43c1-105">Syntax</span></span>


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="e43c1-106">Константы</span><span class="sxs-lookup"><span data-stu-id="e43c1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e43c1-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**\_Канал D3DX10 \_ красный**</span><span class="sxs-lookup"><span data-stu-id="e43c1-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="e43c1-108">Указывает, что следует использовать красный канал.</span><span class="sxs-lookup"><span data-stu-id="e43c1-108">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="e43c1-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**\_Канал D3DX10 \_ синий**</span><span class="sxs-lookup"><span data-stu-id="e43c1-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="e43c1-110">Указывает, что должен использоваться синий канал.</span><span class="sxs-lookup"><span data-stu-id="e43c1-110">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="e43c1-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**\_Зеленый канал \_ D3DX10**</span><span class="sxs-lookup"><span data-stu-id="e43c1-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="e43c1-112">Указывает, что должен использоваться зеленый канал.</span><span class="sxs-lookup"><span data-stu-id="e43c1-112">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="e43c1-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**\_Альфа-канал D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="e43c1-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="e43c1-114">Указывает, что следует использовать альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="e43c1-114">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="e43c1-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_ \_ Освещенность канала D3DX10**</span><span class="sxs-lookup"><span data-stu-id="e43c1-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="e43c1-116">Указывает, что следует использовать луминацесие красного, зеленого и синего каналов.</span><span class="sxs-lookup"><span data-stu-id="e43c1-116">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e43c1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e43c1-117">Requirements</span></span>



| <span data-ttu-id="e43c1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e43c1-118">Requirement</span></span> | <span data-ttu-id="e43c1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e43c1-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e43c1-120">Header</span><span class="sxs-lookup"><span data-stu-id="e43c1-120">Header</span></span><br/> | <dl> <span data-ttu-id="e43c1-121"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e43c1-121"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e43c1-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e43c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43c1-123">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="e43c1-123">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




