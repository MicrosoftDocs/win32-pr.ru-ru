---
description: Определяет тип данных объявления вершины.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Перечисление D3DDECLTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354380"
---
# <a name="d3ddecltype-enumeration"></a><span data-ttu-id="53af3-103">Перечисление D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="53af3-103">D3DDECLTYPE enumeration</span></span>

<span data-ttu-id="53af3-104">Определяет тип данных объявления вершины.</span><span class="sxs-lookup"><span data-stu-id="53af3-104">Defines a vertex declaration data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="53af3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53af3-105">Syntax</span></span>


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a><span data-ttu-id="53af3-106">Константы</span><span class="sxs-lookup"><span data-stu-id="53af3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53af3-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**</span><span class="sxs-lookup"><span data-stu-id="53af3-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE\_FLOAT1**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-108">Плавающее число одного компонента развернуто до (float, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-108">One-component float expanded to (float, 0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="53af3-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE\_FLOAT2**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-110">Развернутое число с плавающей запятой двух компонентов (float, float, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-110">Two-component float expanded to (float, float, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="53af3-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE\_FLOAT3**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-112">Три компонента с плавающей запятой, развернутые до (float, float, float, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-112">Three-component float expanded to (float, float, float, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="53af3-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-114">Четыре компонента с плавающей запятой, развернутые до (float, float, float, float).</span><span class="sxs-lookup"><span data-stu-id="53af3-114">Four-component float expanded to (float, float, float, float).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="53af3-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE\_D3DCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-116">Четыре компонента Упакованные, неподписанные байты сопоставлены с 0 и 1 диапазоном.</span><span class="sxs-lookup"><span data-stu-id="53af3-116">Four-component, packed, unsigned bytes mapped to 0 to 1 range.</span></span> <span data-ttu-id="53af3-117">Входные данные — это [**D3DCOLOR**](d3dcolor.md) , который расширяется до порядка RGBA.</span><span class="sxs-lookup"><span data-stu-id="53af3-117">Input is a [**D3DCOLOR**](d3dcolor.md) and is expanded to RGBA order.</span></span>

</dd> <dt>

<span data-ttu-id="53af3-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**</span><span class="sxs-lookup"><span data-stu-id="53af3-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE\_UBYTE4**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-119">4-компонентный байт без знака.</span><span class="sxs-lookup"><span data-stu-id="53af3-119">Four-component, unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="53af3-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**</span><span class="sxs-lookup"><span data-stu-id="53af3-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE\_SHORT2**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-121">Два компонента, сокращенное число со знаком, расширенное до (значение, значение, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-121">Two-component, signed short expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**</span><span class="sxs-lookup"><span data-stu-id="53af3-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE\_SHORT4**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-123">Четыре компонента, сокращенное число со знаком, расширенное до (значение, значение, значение, значение).</span><span class="sxs-lookup"><span data-stu-id="53af3-123">Four-component, signed short expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**</span><span class="sxs-lookup"><span data-stu-id="53af3-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE\_UBYTE4N**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-125">4-компонентный байт с каждым байтом, нормализованным путем деления на 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="53af3-125">Four-component byte with each byte normalized by dividing with 255.0f.</span></span>

</dd> <dt>

<span data-ttu-id="53af3-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**</span><span class="sxs-lookup"><span data-stu-id="53af3-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE\_SHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-127">Нормализованное, с двумя компонентами, со знаком, с короткой длиной, расширено до (первые короткие/32767.0, секунды Short/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-127">Normalized, two-component, signed short, expanded to (first short/32767.0, second short/32767.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**</span><span class="sxs-lookup"><span data-stu-id="53af3-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE\_SHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-129">Нормализованный, четыре компонента со знаком, короткий, расширенный (первый короткий/32767.0, второй короткий/32767.0, третий короткий/32767.0, четвертый короткий/32767.0).</span><span class="sxs-lookup"><span data-stu-id="53af3-129">Normalized, four-component, signed short, expanded to (first short/32767.0, second short/32767.0, third short/32767.0, fourth short/32767.0).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**</span><span class="sxs-lookup"><span data-stu-id="53af3-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE\_USHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-131">Нормализованное, с двумя компонентами, без знака, с расширенными значениями (первые короткие/65535.0, короткие короткие и 65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-131">Normalized, two-component, unsigned short, expanded to (first short/65535.0, short short/65535.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**</span><span class="sxs-lookup"><span data-stu-id="53af3-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE\_USHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-133">Нормализованное, 4-компонентное, неподписанное короткое, расширенное до (первые короткие/65535.0, Second Short/65535.0, третья короткая/65535.0, четвертая короткая/65535.0).</span><span class="sxs-lookup"><span data-stu-id="53af3-133">Normalized, four-component, unsigned short, expanded to (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**</span><span class="sxs-lookup"><span data-stu-id="53af3-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE\_UDEC3**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-135">Развернутый формат с тремя компонентами, без знака, 10 10 10 (значение, значение, значение, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-135">Three-component, unsigned, 10 10 10 format expanded to (value, value, value, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**</span><span class="sxs-lookup"><span data-stu-id="53af3-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE\_DEC3N**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-137">Формат трех компонентов, подписанный, 10 10 10, нормализован и расширен до (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-137">Three-component, signed, 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="53af3-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE\_FLOAT16\_2**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-139">Два компонента, 16-разрядная, с плавающей точкой, развернутая до (значение, значение, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="53af3-139">Two-component, 16-bit, floating point expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="53af3-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE\_FLOAT16\_4**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-141">Четыре компонента, 16-разрядная, с плавающей точкой, развернутая до (значение, значение, значение, значение).</span><span class="sxs-lookup"><span data-stu-id="53af3-141">Four-component, 16-bit, floating point expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="53af3-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE не \_ используется**</span><span class="sxs-lookup"><span data-stu-id="53af3-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="53af3-143">Поле типа в объявлении не используется.</span><span class="sxs-lookup"><span data-stu-id="53af3-143">Type field in the declaration is unused.</span></span> <span data-ttu-id="53af3-144">Он предназначен для использования с D3DDECLMETHOD \_ UV и D3DDECLMETHOD \_ лукуппресамплед.</span><span class="sxs-lookup"><span data-stu-id="53af3-144">This is designed for use with D3DDECLMETHOD\_UV and D3DDECLMETHOD\_LOOKUPPRESAMPLED.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53af3-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53af3-145">Remarks</span></span>

<span data-ttu-id="53af3-146">Данные вершин объявляются с помощью массива структур [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="53af3-146">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="53af3-147">Каждый элемент массива содержит тип данных объявления вершины.</span><span class="sxs-lookup"><span data-stu-id="53af3-147">Each element in the array contains a vertex declaration data type.</span></span>

<span data-ttu-id="53af3-148">Используйте средство просмотра DirectX Caps Viewer (DXCapsViewer.exe), чтобы узнать, какие типы поддерживаются на вашем устройстве.</span><span class="sxs-lookup"><span data-stu-id="53af3-148">Use the DirectX Caps Viewer Tool (DXCapsViewer.exe) to see which types are supported on your device.</span></span> <span data-ttu-id="53af3-149">Это средство можно получить и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="53af3-149">You can get this tool and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="53af3-150">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="53af3-150">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53af3-151">Требования</span><span class="sxs-lookup"><span data-stu-id="53af3-151">Requirements</span></span>



| <span data-ttu-id="53af3-152">Требование</span><span class="sxs-lookup"><span data-stu-id="53af3-152">Requirement</span></span> | <span data-ttu-id="53af3-153">Значение</span><span class="sxs-lookup"><span data-stu-id="53af3-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53af3-154">Header</span><span class="sxs-lookup"><span data-stu-id="53af3-154">Header</span></span><br/> | <dl> <span data-ttu-id="53af3-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="53af3-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53af3-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53af3-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53af3-157">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="53af3-157">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="53af3-158">**D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="53af3-158">**D3DDECLMETHOD**</span></span>](./d3ddeclmethod.md)
</dt> </dl>

 

 
