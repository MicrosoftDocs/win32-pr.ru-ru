---
description: Состояния образцов определяют операции выборки текстур, такие как адресация текстур и фильтрация текстур.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Перечисление D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713596"
---
# <a name="d3dsamplerstatetype-enumeration"></a><span data-ttu-id="7486b-103">Перечисление D3DSAMPLERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="7486b-103">D3DSAMPLERSTATETYPE enumeration</span></span>

<span data-ttu-id="7486b-104">Состояния образцов определяют операции выборки текстур, такие как адресация текстур и фильтрация текстур.</span><span class="sxs-lookup"><span data-stu-id="7486b-104">Sampler states define texture sampling operations such as texture addressing and texture filtering.</span></span> <span data-ttu-id="7486b-105">Некоторые состояния выборки настроили обработку вершин и некоторую обработку пикселов настройки.</span><span class="sxs-lookup"><span data-stu-id="7486b-105">Some sampler states set-up vertex processing, and some set-up pixel processing.</span></span> <span data-ttu-id="7486b-106">Состояния образцов можно сохранить и восстановить с помощью статеблоккс (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="7486b-106">Sampler states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="7486b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7486b-107">Syntax</span></span>


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="7486b-108">Константы</span><span class="sxs-lookup"><span data-stu-id="7486b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7486b-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ аддрессу**</span><span class="sxs-lookup"><span data-stu-id="7486b-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP\_ADDRESSU**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-110">Режим адресации текстуры для координаты u.</span><span class="sxs-lookup"><span data-stu-id="7486b-110">Texture-address mode for the u coordinate.</span></span> <span data-ttu-id="7486b-111">Значение по умолчанию — D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="7486b-111">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="7486b-112">Дополнительные сведения см. в разделе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="7486b-112">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="7486b-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ аддрессв**</span><span class="sxs-lookup"><span data-stu-id="7486b-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP\_ADDRESSV**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-114">Режим адресации текстуры для координаты v.</span><span class="sxs-lookup"><span data-stu-id="7486b-114">Texture-address mode for the v coordinate.</span></span> <span data-ttu-id="7486b-115">Значение по умолчанию — D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="7486b-115">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="7486b-116">Дополнительные сведения см. в разделе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="7486b-116">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="7486b-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ аддрессв**</span><span class="sxs-lookup"><span data-stu-id="7486b-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP\_ADDRESSW**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-118">Режим адресации текстуры для координаты w.</span><span class="sxs-lookup"><span data-stu-id="7486b-118">Texture-address mode for the w coordinate.</span></span> <span data-ttu-id="7486b-119">Значение по умолчанию — D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="7486b-119">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="7486b-120">Дополнительные сведения см. в разделе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="7486b-120">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="7486b-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BORDERCOLOR**</span><span class="sxs-lookup"><span data-stu-id="7486b-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP\_BORDERCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-122">Цвет границы или тип [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="7486b-122">Border color or type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="7486b-123">Цвет по умолчанию — 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="7486b-123">The default color is 0x00000000.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ магфилтер**</span><span class="sxs-lookup"><span data-stu-id="7486b-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP\_MAGFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-125">Фильтр увеличения типа [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="7486b-125">Magnification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="7486b-126">Значение по умолчанию — D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="7486b-126">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ минфилтер**</span><span class="sxs-lookup"><span data-stu-id="7486b-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP\_MINFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-128">Фильтр минификации типа [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="7486b-128">Minification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="7486b-129">Значение по умолчанию — D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="7486b-129">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ мипфилтер**</span><span class="sxs-lookup"><span data-stu-id="7486b-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP\_MIPFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-131">Фильтр mipmap для использования во время минификации.</span><span class="sxs-lookup"><span data-stu-id="7486b-131">Mipmap filter to use during minification.</span></span> <span data-ttu-id="7486b-132">См. [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="7486b-132">See [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="7486b-133">Значение по умолчанию — D3DTEXF \_ None.</span><span class="sxs-lookup"><span data-stu-id="7486b-133">The default value is D3DTEXF\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ мипмаплодбиас**</span><span class="sxs-lookup"><span data-stu-id="7486b-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP\_MIPMAPLODBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-135">Mipmap уровень детализации.</span><span class="sxs-lookup"><span data-stu-id="7486b-135">Mipmap level-of-detail bias.</span></span> <span data-ttu-id="7486b-136">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7486b-136">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ максмиплевел**</span><span class="sxs-lookup"><span data-stu-id="7486b-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP\_MAXMIPLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-138">Индекс уровня детализации для максимальной используемой схемы.</span><span class="sxs-lookup"><span data-stu-id="7486b-138">level-of-detail index of largest map to use.</span></span> <span data-ttu-id="7486b-139">Диапазон значений — от 0 до (n – 1), где 0 — это самый крупный.</span><span class="sxs-lookup"><span data-stu-id="7486b-139">Values range from 0 to (n - 1) where 0 is the largest.</span></span> <span data-ttu-id="7486b-140">Значение по умолчанию равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7486b-140">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ максанисотропи**</span><span class="sxs-lookup"><span data-stu-id="7486b-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP\_MAXANISOTROPY**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-142">Максимальная анизотропная длина DWORD.</span><span class="sxs-lookup"><span data-stu-id="7486b-142">DWORD maximum anisotropy.</span></span> <span data-ttu-id="7486b-143">Значения находятся в диапазоне от 1 до значения, указанного в элементе **максанисотропи** структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="7486b-143">Values range from 1 to the value that is specified in the **MaxAnisotropy** member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="7486b-144">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="7486b-144">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ сргбтекстуре**</span><span class="sxs-lookup"><span data-stu-id="7486b-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP\_SRGBTEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-146">Значение гамма-коррекции.</span><span class="sxs-lookup"><span data-stu-id="7486b-146">Gamma correction value.</span></span> <span data-ttu-id="7486b-147">Значение по умолчанию — 0. Это означает, что гамма-1,0 и не требуется никаких исправлений.</span><span class="sxs-lookup"><span data-stu-id="7486b-147">The default value is 0, which means gamma is 1.0 and no correction is required.</span></span> <span data-ttu-id="7486b-148">В противном случае это значение означает, что образец должен иметь гамму 2,2 на содержимом и преобразовать его в линейный (гамма-1,0) перед представлением в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="7486b-148">Otherwise, this value means that the sampler should assume gamma of 2.2 on the content and convert it to linear (gamma 1.0) before presenting it to the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ елементиндекс**</span><span class="sxs-lookup"><span data-stu-id="7486b-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP\_ELEMENTINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-150">Если для образца назначена Многоэлементная текстура, это указывает, какой индекс элемента следует использовать.</span><span class="sxs-lookup"><span data-stu-id="7486b-150">When a multielement texture is assigned to the sampler, this indicates which element index to use.</span></span> <span data-ttu-id="7486b-151">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="7486b-151">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ дмапоффсет**</span><span class="sxs-lookup"><span data-stu-id="7486b-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP\_DMAPOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-153">Смещение вершины в предвыборочной карте смещения.</span><span class="sxs-lookup"><span data-stu-id="7486b-153">Vertex offset in the presampled displacement map.</span></span> <span data-ttu-id="7486b-154">Это константа, используемая тесселяцией, ее значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="7486b-154">This is a constant used by the tessellator, its default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="7486b-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7486b-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7486b-156">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="7486b-156">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7486b-157">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="7486b-157">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7486b-158">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="7486b-158">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7486b-159">Требования</span><span class="sxs-lookup"><span data-stu-id="7486b-159">Requirements</span></span>



| <span data-ttu-id="7486b-160">Требование</span><span class="sxs-lookup"><span data-stu-id="7486b-160">Requirement</span></span> | <span data-ttu-id="7486b-161">Значение</span><span class="sxs-lookup"><span data-stu-id="7486b-161">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7486b-162">Header</span><span class="sxs-lookup"><span data-stu-id="7486b-162">Header</span></span><br/> | <dl> <span data-ttu-id="7486b-163"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7486b-163"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7486b-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7486b-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7486b-165">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="7486b-165">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
