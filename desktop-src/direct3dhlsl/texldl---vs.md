---
title: текслдл — VS
description: Пример текстуры с определенным образцом. Определенный mipmap уровень детализации должен быть указан в качестве четвертого компонента координаты текстуры. | текслдл — VS
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081776"
---
# <a name="texldl---vs"></a><span data-ttu-id="599ac-105">текслдл — VS</span><span class="sxs-lookup"><span data-stu-id="599ac-105">texldl - vs</span></span>

<span data-ttu-id="599ac-106">Пример текстуры с определенным образцом.</span><span class="sxs-lookup"><span data-stu-id="599ac-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="599ac-107">Определенный mipmap уровень детализации должен быть указан в качестве четвертого компонента координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="599ac-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="599ac-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="599ac-108">Syntax</span></span>



| <span data-ttu-id="599ac-109">текслдл DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="599ac-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="599ac-110">Где:</span><span class="sxs-lookup"><span data-stu-id="599ac-110">Where:</span></span>

-   <span data-ttu-id="599ac-111">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="599ac-111">dst is a destination register.</span></span>
-   <span data-ttu-id="599ac-112">src0 — это исходный регистр, предоставляющий координаты текстуры для образца текстуры.</span><span class="sxs-lookup"><span data-stu-id="599ac-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="599ac-113">src1 идентифицирует регистры исходного образца \# , где \# указывает, какой номер образца текстуры следует вычислить.</span><span class="sxs-lookup"><span data-stu-id="599ac-113">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="599ac-114">Этот образец связан с текстурой и состоянием элемента управления, определенным перечислением [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (например, D3DSAMP \_ минфилтер).</span><span class="sxs-lookup"><span data-stu-id="599ac-114">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="599ac-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="599ac-115">Remarks</span></span>



| <span data-ttu-id="599ac-116">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="599ac-116">Vertex shader versions</span></span> | <span data-ttu-id="599ac-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="599ac-117">1\_1</span></span> | <span data-ttu-id="599ac-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="599ac-118">2\_0</span></span> | <span data-ttu-id="599ac-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="599ac-119">2\_x</span></span> | <span data-ttu-id="599ac-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="599ac-120">2\_sw</span></span> | <span data-ttu-id="599ac-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="599ac-121">3\_0</span></span> | <span data-ttu-id="599ac-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="599ac-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="599ac-123">текслдл</span><span class="sxs-lookup"><span data-stu-id="599ac-123">texldl</span></span>                 |      |      |      |       | <span data-ttu-id="599ac-124">x</span><span class="sxs-lookup"><span data-stu-id="599ac-124">x</span></span>    | <span data-ttu-id="599ac-125">x</span><span class="sxs-lookup"><span data-stu-id="599ac-125">x</span></span>     |



 

<span data-ttu-id="599ac-126">текслдл ищет набор текстур на этапе образца, на который ссылается src1.</span><span class="sxs-lookup"><span data-stu-id="599ac-126">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="599ac-127">Уровень детализации выбирается из src0. w.</span><span class="sxs-lookup"><span data-stu-id="599ac-127">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="599ac-128">Это значение может быть отрицательным, в этом случае выбранным уровнем детализации является "начальном одна" (самая большая схема) с МАГФИЛТЕР.</span><span class="sxs-lookup"><span data-stu-id="599ac-128">This value can be negative, in which case the level-of-detail selected is the "zeroth one" (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="599ac-129">Поскольку src0. w является значением с плавающей запятой, значение дробной части используется для интерполяции (если МИПФИЛТЕР ЛИНЕЙный) между двумя уровнями MIP.</span><span class="sxs-lookup"><span data-stu-id="599ac-129">Because src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="599ac-130">Состояния образцов МИПМАПЛОДБИАС и МАКСМИПЛЕВЕЛ соблюдаются.</span><span class="sxs-lookup"><span data-stu-id="599ac-130">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="599ac-131">Дополнительные сведения о состояниях образцов см. в разделе [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="599ac-131">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="599ac-132">Если программа шейдера выполняет выборку из образца, не имеющего набора текстур, то значение 0001 получается в регистре назначения.</span><span class="sxs-lookup"><span data-stu-id="599ac-132">If a shader program samples from a sampler that does not have a texture set, 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="599ac-133">Это приближение к алгоритму ссылочного устройства.</span><span class="sxs-lookup"><span data-stu-id="599ac-133">This is an approximation to the reference device algorithm.</span></span>


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
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="599ac-134">Ограничения.</span><span class="sxs-lookup"><span data-stu-id="599ac-134">Restrictions:</span></span>

-   <span data-ttu-id="599ac-135">Координаты текстуры не должны масштабироваться по размеру текстуры.</span><span class="sxs-lookup"><span data-stu-id="599ac-135">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="599ac-136">DST должен быть [временным регистром](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="599ac-136">dst must be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="599ac-137">DST может принимать маску записи.</span><span class="sxs-lookup"><span data-stu-id="599ac-137">dst can accept a write mask.</span></span> <span data-ttu-id="599ac-138">См. раздел [назначение масок регистров](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span><span class="sxs-lookup"><span data-stu-id="599ac-138">See [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span></span>
-   <span data-ttu-id="599ac-139">По умолчанию отсутствующие компоненты имеют значение 0 или 1 и зависят от формата текстуры.</span><span class="sxs-lookup"><span data-stu-id="599ac-139">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="599ac-140">src1 должен представлять собой [образец (Direct3D 9 ASM-VS)](dx9-graphics-reference-asm-vs-registers-sampler.md) \# .</span><span class="sxs-lookup"><span data-stu-id="599ac-140">src1 must be a [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="599ac-141">src1 не может использовать модификатор отрицания.</span><span class="sxs-lookup"><span data-stu-id="599ac-141">src1 may not use a negate modifier.</span></span> <span data-ttu-id="599ac-142">src1 может использовать свиззле, который применяется после выборки, прежде чем будет учитываться маска записи.</span><span class="sxs-lookup"><span data-stu-id="599ac-142">src1 may use swizzle, which is applied after sampling before the write mask is honored.</span></span> <span data-ttu-id="599ac-143">Образец должен быть объявлен (с использованием [дкл \_ самплертипе (SM3-VS ASM)](dcl-samplertype---vs.md)) в начале шейдера.</span><span class="sxs-lookup"><span data-stu-id="599ac-143">The sampler must have been declared (using [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="599ac-144">Количество координат, необходимых для выполнения образца текстуры, зависит от того, как был объявлен образец.</span><span class="sxs-lookup"><span data-stu-id="599ac-144">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="599ac-145">Если он был объявлен как куб, требуется Координата текстуры из трех компонентов (. RGB).</span><span class="sxs-lookup"><span data-stu-id="599ac-145">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="599ac-146">Проверка обеспечивает достаточный уровень координат, предоставляемых текслдл, для измерения текстуры, объявленного для образца.</span><span class="sxs-lookup"><span data-stu-id="599ac-146">Validation enforces that coordinates provided to texldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="599ac-147">Однако не гарантируется, что приложение фактически устанавливает текстуру (через API) с измерениями, равными измерению, объявленному для образца.</span><span class="sxs-lookup"><span data-stu-id="599ac-147">However, it is not guaranteed that the application actually set a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="599ac-148">В этом случае среда выполнения попытается обнаружить несоответствия (возможно, только при отладке).</span><span class="sxs-lookup"><span data-stu-id="599ac-148">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="599ac-149">Выборка текстуры с меньшим количеством измерений, чем есть в координатах текстуры, будет разрешена, и предполагается, что будут игнорироваться дополнительные компоненты координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="599ac-149">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed, and will be assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="599ac-150">И наоборот, выборка текстуры с большим количеством измерений, имеющихся в координатах текстуры, не допускается.</span><span class="sxs-lookup"><span data-stu-id="599ac-150">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is not allowed.</span></span>
-   <span data-ttu-id="599ac-151">Если src0 (координата текстуры) является [временным регистром](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), то должны быть предварительно записаны компоненты, необходимые для поиска (описанного выше).</span><span class="sxs-lookup"><span data-stu-id="599ac-151">If the src0 (texture coordinate) is a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="599ac-152">В результате выборки неподписанных текстур RGB значения float будут находиться в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="599ac-152">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="599ac-153">Текстуры с выборками будут иметь значения float от-1,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="599ac-153">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="599ac-154">При выборке текстур с плавающей запятой Float16 означает, что данные будут находиться в диапазоне от MAX \_ Float16.</span><span class="sxs-lookup"><span data-stu-id="599ac-154">When sampling floating point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="599ac-155">Float32 означает, что будет использоваться максимальный диапазон конвейера.</span><span class="sxs-lookup"><span data-stu-id="599ac-155">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="599ac-156">Выборка за пределами одного из диапазонов не определена.</span><span class="sxs-lookup"><span data-stu-id="599ac-156">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="599ac-157">Нет зависимого ограничения на чтение.</span><span class="sxs-lookup"><span data-stu-id="599ac-157">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="599ac-158">См. также</span><span class="sxs-lookup"><span data-stu-id="599ac-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="599ac-159">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="599ac-159">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
