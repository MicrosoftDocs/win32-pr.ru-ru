---
title: текслдл-PS
description: Пример текстуры с определенным образцом. Определенный mipmap уровень детализации должен быть указан в качестве четвертого компонента координаты текстуры. | текслдл-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986229"
---
# <a name="texldl---ps"></a><span data-ttu-id="cbbce-105">текслдл-PS</span><span class="sxs-lookup"><span data-stu-id="cbbce-105">texldl - ps</span></span>

<span data-ttu-id="cbbce-106">Пример текстуры с определенным образцом.</span><span class="sxs-lookup"><span data-stu-id="cbbce-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="cbbce-107">Определенный mipmap уровень детализации должен быть указан в качестве четвертого компонента координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbbce-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbbce-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbbce-108">Syntax</span></span>



| <span data-ttu-id="cbbce-109">текслдл DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="cbbce-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="cbbce-110">Где:</span><span class="sxs-lookup"><span data-stu-id="cbbce-110">Where:</span></span>

-   <span data-ttu-id="cbbce-111">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="cbbce-111">dst is a destination register.</span></span>
-   <span data-ttu-id="cbbce-112">src0 — это исходный регистр, предоставляющий координаты текстуры для образца текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbbce-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="cbbce-113">См. раздел [регистрация координат текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="cbbce-113">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="cbbce-114">src1 идентифицирует регистры исходного образца \# , где \# указывает, какой номер образца текстуры следует вычислить.</span><span class="sxs-lookup"><span data-stu-id="cbbce-114">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="cbbce-115">Этот образец связан с текстурой и состоянием элемента управления, определенным перечислением [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (например, D3DSAMP \_ минфилтер).</span><span class="sxs-lookup"><span data-stu-id="cbbce-115">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="cbbce-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cbbce-116">Remarks</span></span>



| <span data-ttu-id="cbbce-117">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="cbbce-117">Pixel shader versions</span></span> | <span data-ttu-id="cbbce-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="cbbce-118">1\_1</span></span> | <span data-ttu-id="cbbce-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="cbbce-119">1\_2</span></span> | <span data-ttu-id="cbbce-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cbbce-120">1\_3</span></span> | <span data-ttu-id="cbbce-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="cbbce-121">1\_4</span></span> | <span data-ttu-id="cbbce-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbbce-122">2\_0</span></span> | <span data-ttu-id="cbbce-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cbbce-123">2\_x</span></span> | <span data-ttu-id="cbbce-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cbbce-124">2\_sw</span></span> | <span data-ttu-id="cbbce-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cbbce-125">3\_0</span></span> | <span data-ttu-id="cbbce-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cbbce-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="cbbce-127">текслдл</span><span class="sxs-lookup"><span data-stu-id="cbbce-127">texldl</span></span>                |      |      |      |      |      |      |       | <span data-ttu-id="cbbce-128">x</span><span class="sxs-lookup"><span data-stu-id="cbbce-128">x</span></span>    | <span data-ttu-id="cbbce-129">x</span><span class="sxs-lookup"><span data-stu-id="cbbce-129">x</span></span>     |



 

<span data-ttu-id="cbbce-130">текслдл ищет набор текстур на этапе образца, на который ссылается src1.</span><span class="sxs-lookup"><span data-stu-id="cbbce-130">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="cbbce-131">Уровень детализации выбирается из src0. w.</span><span class="sxs-lookup"><span data-stu-id="cbbce-131">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="cbbce-132">Это значение может быть отрицательным, в этом случае выбранным уровнем детализации является начальном одна (самая крупная схема) с МАГФИЛТЕР.</span><span class="sxs-lookup"><span data-stu-id="cbbce-132">This value can be negative in which case the level-of-detail selected is the zeroth one (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="cbbce-133">Так как src0. w является значением с плавающей запятой, значение дробной части используется для интерполяции (если МИПФИЛТЕР ЛИНЕЙный) между двумя уровнями MIP.</span><span class="sxs-lookup"><span data-stu-id="cbbce-133">Since src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="cbbce-134">Состояния образцов МИПМАПЛОДБИАС и МАКСМИПЛЕВЕЛ соблюдаются.</span><span class="sxs-lookup"><span data-stu-id="cbbce-134">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="cbbce-135">Дополнительные сведения о состояниях образцов см. в разделе [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="cbbce-135">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="cbbce-136">Если программа шейдера выполняет выборку из образца, не имеющего набора текстур, то выдается значение 0001 в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="cbbce-136">If a shader program samples from a sampler that does not have a texture set, then 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="cbbce-137">Ниже приведен примерный алгоритм, который следует использовать в качестве эталонного устройства:</span><span class="sxs-lookup"><span data-stu-id="cbbce-137">The following is a rough algorithm that the reference device follows:</span></span>


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="cbbce-138">Ограничения.</span><span class="sxs-lookup"><span data-stu-id="cbbce-138">Restrictions:</span></span>

-   <span data-ttu-id="cbbce-139">Координаты текстуры не должны масштабироваться по размеру текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbbce-139">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="cbbce-140">DST должен быть [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="cbbce-140">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="cbbce-141">DST может принимать вритемаск.</span><span class="sxs-lookup"><span data-stu-id="cbbce-141">dst can accept a writemask.</span></span> <span data-ttu-id="cbbce-142">См. раздел " [маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)".</span><span class="sxs-lookup"><span data-stu-id="cbbce-142">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="cbbce-143">По умолчанию отсутствующие компоненты имеют значение 0 или 1 и зависят от формата текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbbce-143">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="cbbce-144">src1 должны быть [образцами (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# .</span><span class="sxs-lookup"><span data-stu-id="cbbce-144">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="cbbce-145">src1 не может использовать модификатор отрицания (см. раздел [маска записи регистра назначения](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="cbbce-145">src1 may not use a negate modifier (see [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span></span> <span data-ttu-id="cbbce-146">src1 может использовать свиззле (см. [исходный регистр группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), который применяется после выборки, но перед маской записи (см. запись маски записи назначения).</span><span class="sxs-lookup"><span data-stu-id="cbbce-146">src1 may use swizzle (see [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), which is applied after sampling, but before the write mask (see Destination Register Write Mask) is honored.</span></span> <span data-ttu-id="cbbce-147">Образец должен быть объявлен (с помощью [дкл \_ самплертипе (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) в начале шейдера.</span><span class="sxs-lookup"><span data-stu-id="cbbce-147">The sampler must have been declared (using [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="cbbce-148">Количество координат, необходимых для выполнения образца текстуры, зависит от того, как был объявлен образец.</span><span class="sxs-lookup"><span data-stu-id="cbbce-148">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="cbbce-149">Если он был объявлен как куб, требуется Координата текстуры из трех компонентов (. RGB).</span><span class="sxs-lookup"><span data-stu-id="cbbce-149">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="cbbce-150">Проверка обеспечивает достаточный уровень координат, предоставляемых да \_ ЛДЛ для измерения текстуры, объявленного для образца.</span><span class="sxs-lookup"><span data-stu-id="cbbce-150">Validation enforces that coordinates provided to tex\_ldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="cbbce-151">Однако не гарантируется, что приложение фактически устанавливает текстуру (через API) с измерениями, равными измерению, объявленному для образца.</span><span class="sxs-lookup"><span data-stu-id="cbbce-151">However, it is not guaranteed that the application actually sets a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="cbbce-152">В этом случае среда выполнения попытается обнаружить несоответствия (возможно, только при отладке).</span><span class="sxs-lookup"><span data-stu-id="cbbce-152">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="cbbce-153">Выборка текстуры с меньшим количеством измерений, чем есть в координатах текстуры, будет разрешена и предполагается игнорировать дополнительные компоненты координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="cbbce-153">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed and assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="cbbce-154">И наоборот, выборка текстуры с большим количеством измерений, имеющихся в координатах текстуры, недопустима.</span><span class="sxs-lookup"><span data-stu-id="cbbce-154">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is illegal.</span></span>
-   <span data-ttu-id="cbbce-155">Если src0 (координата текстуры) является [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md), компоненты, необходимые для поиска (описанные выше), должны быть предварительно записаны.</span><span class="sxs-lookup"><span data-stu-id="cbbce-155">If the src0 (texture coordinate) is [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="cbbce-156">В результате выборки неподписанных текстур RGB значения float будут находиться в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="cbbce-156">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="cbbce-157">Текстуры с выборками будут иметь значения float от-1,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="cbbce-157">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="cbbce-158">При выборке текстур с плавающей запятой Float16 означает, что данные будут находиться в диапазоне от MAX \_ Float16.</span><span class="sxs-lookup"><span data-stu-id="cbbce-158">When sampling floating-point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="cbbce-159">Float32 означает, что будет использоваться максимальный диапазон конвейера.</span><span class="sxs-lookup"><span data-stu-id="cbbce-159">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="cbbce-160">Выборка за пределами одного из диапазонов не определена.</span><span class="sxs-lookup"><span data-stu-id="cbbce-160">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="cbbce-161">Нет зависимого ограничения на чтение.</span><span class="sxs-lookup"><span data-stu-id="cbbce-161">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbbce-162">См. также</span><span class="sxs-lookup"><span data-stu-id="cbbce-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbbce-163">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="cbbce-163">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
