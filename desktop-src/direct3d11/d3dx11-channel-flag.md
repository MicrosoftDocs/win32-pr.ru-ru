---
title: Перечисление D3DX11_CHANNEL_FLAG (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- Перечисление D3DX11_CHANNEL_FLAG Direct3D 11
- Указатель перечисления LPD3DX11_CHANNEL_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424522"
---
# <a name="d3dx11_channel_flag-enumeration"></a><span data-ttu-id="f3b06-106">\_ \_ Перечисление флагов канала D3DX11</span><span class="sxs-lookup"><span data-stu-id="f3b06-106">D3DX11\_CHANNEL\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="f3b06-107">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f3b06-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f3b06-108">Эти флаги используются функциями, которые работают с одним или несколькими каналами в текстуре.</span><span class="sxs-lookup"><span data-stu-id="f3b06-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b06-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3b06-109">Syntax</span></span>


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="f3b06-110">Константы</span><span class="sxs-lookup"><span data-stu-id="f3b06-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f3b06-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**\_Канал D3DX11 \_ красный**</span><span class="sxs-lookup"><span data-stu-id="f3b06-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="f3b06-112">Указывает, что следует использовать красный канал.</span><span class="sxs-lookup"><span data-stu-id="f3b06-112">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f3b06-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**\_Канал D3DX11 \_ синий**</span><span class="sxs-lookup"><span data-stu-id="f3b06-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="f3b06-114">Указывает, что должен использоваться синий канал.</span><span class="sxs-lookup"><span data-stu-id="f3b06-114">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f3b06-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**\_Зеленый канал \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="f3b06-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="f3b06-116">Указывает, что должен использоваться зеленый канал.</span><span class="sxs-lookup"><span data-stu-id="f3b06-116">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f3b06-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**\_Альфа-канал D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="f3b06-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="f3b06-118">Указывает, что следует использовать альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="f3b06-118">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f3b06-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**\_ \_ Освещенность канала D3DX11**</span><span class="sxs-lookup"><span data-stu-id="f3b06-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="f3b06-120">Указывает, что следует использовать луминацесие красного, зеленого и синего каналов.</span><span class="sxs-lookup"><span data-stu-id="f3b06-120">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3b06-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f3b06-121">Requirements</span></span>



| <span data-ttu-id="f3b06-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f3b06-122">Requirement</span></span> | <span data-ttu-id="f3b06-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f3b06-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b06-124">Header</span><span class="sxs-lookup"><span data-stu-id="f3b06-124">Header</span></span><br/> | <dl> <span data-ttu-id="f3b06-125"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b06-125"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b06-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3b06-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b06-127">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="f3b06-127">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





