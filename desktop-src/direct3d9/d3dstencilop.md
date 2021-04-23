---
description: Определяет операции с буфером набора элементов.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Перечисление D3DSTENCILOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674693"
---
# <a name="d3dstencilop-enumeration"></a><span data-ttu-id="1d426-103">Перечисление D3DSTENCILOP</span><span class="sxs-lookup"><span data-stu-id="1d426-103">D3DSTENCILOP enumeration</span></span>

<span data-ttu-id="1d426-104">Определяет операции с буфером набора элементов.</span><span class="sxs-lookup"><span data-stu-id="1d426-104">Defines stencil-buffer operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d426-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d426-105">Syntax</span></span>


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a><span data-ttu-id="1d426-106">Константы</span><span class="sxs-lookup"><span data-stu-id="1d426-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1d426-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_**</span><span class="sxs-lookup"><span data-stu-id="1d426-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP\_KEEP**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-108">Не обновляйте запись в буфере шаблона.</span><span class="sxs-lookup"><span data-stu-id="1d426-108">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="1d426-109">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1d426-109">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="1d426-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ 0**</span><span class="sxs-lookup"><span data-stu-id="1d426-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-111">Задайте для записи в буфере набора элементов значение 0.</span><span class="sxs-lookup"><span data-stu-id="1d426-111">Set the stencil-buffer entry to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1d426-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ заменить**</span><span class="sxs-lookup"><span data-stu-id="1d426-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP\_REPLACE**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-113">Замените запись в буфере набора элементов значением ссылки.</span><span class="sxs-lookup"><span data-stu-id="1d426-113">Replace the stencil-buffer entry with a reference value.</span></span>

</dd> <dt>

<span data-ttu-id="1d426-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ инкрсат**</span><span class="sxs-lookup"><span data-stu-id="1d426-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP\_INCRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-115">Увеличение записи буфера набора элементов с фиксацией до максимального значения.</span><span class="sxs-lookup"><span data-stu-id="1d426-115">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="1d426-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ декрсат**</span><span class="sxs-lookup"><span data-stu-id="1d426-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP\_DECRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-117">Уменьшение записи в буфере набора элементов с фиксацией в ноль.</span><span class="sxs-lookup"><span data-stu-id="1d426-117">Decrement the stencil-buffer entry, clamping to zero.</span></span>

</dd> <dt>

<span data-ttu-id="1d426-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ инверсия**</span><span class="sxs-lookup"><span data-stu-id="1d426-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP\_INVERT**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-119">Инвертировать биты в записи в буфере набора элементов.</span><span class="sxs-lookup"><span data-stu-id="1d426-119">Invert the bits in the stencil-buffer entry.</span></span>

</dd> <dt>

<span data-ttu-id="1d426-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ INCR**</span><span class="sxs-lookup"><span data-stu-id="1d426-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP\_INCR**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-121">Увеличение записи буфера набора элементов с переносом в ноль, если новое значение превышает максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="1d426-121">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="1d426-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ декр**</span><span class="sxs-lookup"><span data-stu-id="1d426-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP\_DECR**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-123">Уменьшите запись в буфере набора элементов, заключив в нее максимальное значение, если новое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="1d426-123">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span>

</dd> <dt>

<span data-ttu-id="1d426-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1d426-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1d426-125">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="1d426-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1d426-126">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="1d426-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1d426-127">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="1d426-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d426-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d426-128">Remarks</span></span>

<span data-ttu-id="1d426-129">Элементы в буфере набора элементов — это целые значения в диапазоне от 0 до 2 ⁿ-1, где n — битовая глубина буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="1d426-129">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d426-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1d426-130">Requirements</span></span>



| <span data-ttu-id="1d426-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1d426-131">Requirement</span></span> | <span data-ttu-id="1d426-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1d426-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d426-133">Header</span><span class="sxs-lookup"><span data-stu-id="1d426-133">Header</span></span><br/> | <dl> <span data-ttu-id="1d426-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d426-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d426-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d426-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d426-136">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="1d426-136">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




