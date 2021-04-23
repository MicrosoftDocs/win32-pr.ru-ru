---
description: Определяет поддерживаемый режим смешения.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Перечисление D3DBLEND (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d8d779ad714e396f9c9a82bbbc42ddd09b76e2ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000328"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="c51ce-103">Перечисление D3DBLEND</span><span class="sxs-lookup"><span data-stu-id="c51ce-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="c51ce-104">Определяет поддерживаемый режим смешения.</span><span class="sxs-lookup"><span data-stu-id="c51ce-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="c51ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c51ce-105">Syntax</span></span>


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a><span data-ttu-id="c51ce-106">Константы</span><span class="sxs-lookup"><span data-stu-id="c51ce-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c51ce-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c51ce-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-108">Коэффициент смешения равен (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="c51ce-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ один**</span><span class="sxs-lookup"><span data-stu-id="c51ce-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-110">Коэффициент смешения равен (1, 1, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="c51ce-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ сркколор**</span><span class="sxs-lookup"><span data-stu-id="c51ce-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-112">Коэффициент смешения — (RS, GS, BS, AS).</span><span class="sxs-lookup"><span data-stu-id="c51ce-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ инвсркколор**</span><span class="sxs-lookup"><span data-stu-id="c51ce-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-114">Коэффициент смешения — (1-RS, 1-GS, 1-BS, 1 — как).</span><span class="sxs-lookup"><span data-stu-id="c51ce-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ сркалфа**</span><span class="sxs-lookup"><span data-stu-id="c51ce-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-116">Коэффициент смешения равен (как, как, как).</span><span class="sxs-lookup"><span data-stu-id="c51ce-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ инвсркалфа**</span><span class="sxs-lookup"><span data-stu-id="c51ce-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-118">Коэффициент смешения равен (1-как, 1-как, 1-как, 1 — как).</span><span class="sxs-lookup"><span data-stu-id="c51ce-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ десталфа**</span><span class="sxs-lookup"><span data-stu-id="c51ce-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-120">Коэффициент смешения — (<sub>a d a</sub> d<sub></sub> a d<sub>).</sub><sub></sub></span><span class="sxs-lookup"><span data-stu-id="c51ce-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ инвдесталфа**</span><span class="sxs-lookup"><span data-stu-id="c51ce-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-122">Коэффициент смешения — (1-A<sub>d</sub> 1 —<sub>a d 1</sub> -<sub>a d</sub> <sub>).</sub></span><span class="sxs-lookup"><span data-stu-id="c51ce-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ дестколор**</span><span class="sxs-lookup"><span data-stu-id="c51ce-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-124">Коэффициент смешения — (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="c51ce-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ инвдестколор**</span><span class="sxs-lookup"><span data-stu-id="c51ce-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-126">Коэффициент смешения равен (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="c51ce-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ сркалфасат**</span><span class="sxs-lookup"><span data-stu-id="c51ce-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-128">Коэффициент смешения — (f, f, f, 1); где f = min (как, 1-A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="c51ce-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ боссркалфа**</span><span class="sxs-lookup"><span data-stu-id="c51ce-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-130">**Устарел**.</span><span class="sxs-lookup"><span data-stu-id="c51ce-130">**Obsolete**.</span></span> <span data-ttu-id="c51ce-131">Начиная с версии DirectX 6, можно добиться того же результата, установив для исходных и целевых коэффициентов смешения D3DBLEND \_ сркалфа и D3DBLEND \_ инвсркалфа в отдельных вызовах.</span><span class="sxs-lookup"><span data-stu-id="c51ce-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ босинвсркалфа**</span><span class="sxs-lookup"><span data-stu-id="c51ce-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-133">**Устарел**.</span><span class="sxs-lookup"><span data-stu-id="c51ce-133">**Obsolete**.</span></span> <span data-ttu-id="c51ce-134">Коэффициент смешения исходного кода равен (1-как, 1-как, 1-как, 1 — как), а целевой коэффициент смешения — (AS, AS, AS); Выбор назначения Blend переопределяется.</span><span class="sxs-lookup"><span data-stu-id="c51ce-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="c51ce-135">Этот режим наложения поддерживается только для \_ состояния отрисовки D3DRS сркбленд.</span><span class="sxs-lookup"><span data-stu-id="c51ce-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ блендфактор**</span><span class="sxs-lookup"><span data-stu-id="c51ce-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-137">Постоянный коэффициент смешения цветов, используемый средством смешения буферов кадров.</span><span class="sxs-lookup"><span data-stu-id="c51ce-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="c51ce-138">Этот режим наложения поддерживается, только если D3DPBLENDCAPS \_ блендфактор задан в **Сркблендкапс** или **дестблендкапс** членах [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="c51ce-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ инвблендфактор**</span><span class="sxs-lookup"><span data-stu-id="c51ce-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-140">Инвертированный коэффициент смешения цветов, используемый средством смешения буферов кадров.</span><span class="sxs-lookup"><span data-stu-id="c51ce-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="c51ce-141">Этот режим наложения поддерживается только в том случае, если \_ бит БЛЕНДФАКТОР D3DPBLENDCAPS установлен в **Сркблендкапс** или **дестблендкапс** членов [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="c51ce-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="c51ce-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="c51ce-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-143">Коэффициент смешения равен (Псаутколор \[ 1 \] <sub>r</sub>, псаутколор \[ 1 \] <sub>g</sub>, псаутколор \[ 1 \] <sub>b</sub>, не используется).</span><span class="sxs-lookup"><span data-stu-id="c51ce-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="c51ce-144">См. раздел [наложение целевого объекта прорисовки](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="c51ce-144">See [Render Target Blending](#render-target-blending).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c51ce-145">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c51ce-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c51ce-146">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c51ce-146">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c51ce-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="c51ce-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-148">Коэффициент смешения равен (1-Псаутколор \[ 1 \] <sub>r</sub>, 1-псаутколор \[ 1 \] <sub>g</sub>, 1-псаутколор \[ 1 \] <sub>b</sub>, не используется)).</span><span class="sxs-lookup"><span data-stu-id="c51ce-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="c51ce-149">См. раздел [наложение целевого объекта прорисовки](#render-target-blending).</span><span class="sxs-lookup"><span data-stu-id="c51ce-149">See [Render Target Blending](#render-target-blending).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c51ce-150">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c51ce-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c51ce-151">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c51ce-151">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c51ce-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c51ce-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c51ce-153">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="c51ce-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c51ce-154">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="c51ce-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c51ce-155">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="c51ce-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c51ce-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c51ce-156">Remarks</span></span>

<span data-ttu-id="c51ce-157">В приведенных выше описаниях элементов значения RGBA источника и назначения обозначаются подстрочными индексами s и d.</span><span class="sxs-lookup"><span data-stu-id="c51ce-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="c51ce-158">Значения в этом перечислимом типе используются в следующих состояниях рендеринга:</span><span class="sxs-lookup"><span data-stu-id="c51ce-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="c51ce-159">D3DRS \_ дестбленд</span><span class="sxs-lookup"><span data-stu-id="c51ce-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="c51ce-160">D3DRS \_ сркбленд</span><span class="sxs-lookup"><span data-stu-id="c51ce-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="c51ce-161">D3DRS \_ дестблендалфа</span><span class="sxs-lookup"><span data-stu-id="c51ce-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="c51ce-162">D3DRS \_ сркблендалфа</span><span class="sxs-lookup"><span data-stu-id="c51ce-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="c51ce-163">См. [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="c51ce-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="c51ce-164">Наложение целевого объекта прорисовки</span><span class="sxs-lookup"><span data-stu-id="c51ce-164">Render Target Blending</span></span>

<span data-ttu-id="c51ce-165">В Direct3D 9Ex улучшены возможности отрисовки текста.</span><span class="sxs-lookup"><span data-stu-id="c51ce-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="c51ce-166">Для отрисовки шрифтов с четким типом обычно требуется два прохода.</span><span class="sxs-lookup"><span data-stu-id="c51ce-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="c51ce-167">Чтобы устранить второй проход, можно использовать шейдер пикселей для вывода двух цветов, которые можно вызвать Псаутколор \[ 0 \] и псаутколор \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="c51ce-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="c51ce-168">Первый цвет будет содержать стандартные 3 цветовых компонента (RGB).</span><span class="sxs-lookup"><span data-stu-id="c51ce-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="c51ce-169">Второй цвет будет содержать три альфа-компонента (по одному для каждого компонента первого цвета).</span><span class="sxs-lookup"><span data-stu-id="c51ce-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="c51ce-170">Эти новые режимы наложения используются только для отрисовки текста на первом объекте отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c51ce-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="c51ce-171">Требования</span><span class="sxs-lookup"><span data-stu-id="c51ce-171">Requirements</span></span>



| <span data-ttu-id="c51ce-172">Требование</span><span class="sxs-lookup"><span data-stu-id="c51ce-172">Requirement</span></span> | <span data-ttu-id="c51ce-173">Значение</span><span class="sxs-lookup"><span data-stu-id="c51ce-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c51ce-174">Header</span><span class="sxs-lookup"><span data-stu-id="c51ce-174">Header</span></span><br/> | <dl> <span data-ttu-id="c51ce-175"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c51ce-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c51ce-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c51ce-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51ce-177">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="c51ce-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
