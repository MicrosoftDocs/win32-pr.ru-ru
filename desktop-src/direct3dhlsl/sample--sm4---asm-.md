---
title: Пример (SM4-ASM)
description: Выборка данных из указанного элемента или текстуры с использованием указанного адреса и режима фильтрации, определенного заданным образцом. | Пример (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000201"
---
# <a name="sample-sm4---asm"></a><span data-ttu-id="3d049-104">Пример (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3d049-104">sample (sm4 - asm)</span></span>

<span data-ttu-id="3d049-105">Выборка данных из указанного элемента или текстуры с использованием указанного адреса и режима фильтрации, определенного заданным образцом.</span><span class="sxs-lookup"><span data-stu-id="3d049-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="3d049-106">Пример \[ \_ аоффимми (u, v, w) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер</span><span class="sxs-lookup"><span data-stu-id="3d049-106">sample\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3d049-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="3d049-107">Item</span></span>                                                                                                               | <span data-ttu-id="3d049-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3d049-108">Description</span></span>                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d049-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3d049-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="3d049-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="3d049-110">\[in\] The address of the result of the operation.</span></span><br/>                                      |
| <span data-ttu-id="3d049-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="3d049-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="3d049-112">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d049-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="3d049-113">Дополнительные сведения см. в разделе **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="3d049-113">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="3d049-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="3d049-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="3d049-115">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d049-115">\[in\] A texture register.</span></span> <span data-ttu-id="3d049-116">Дополнительные сведения см. в разделе **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="3d049-116">For more information, see the **Remarks** section.</span></span><br/>           |
| <span data-ttu-id="3d049-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="3d049-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="3d049-118">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="3d049-118">\[in\] A sampler register.</span></span> <span data-ttu-id="3d049-119">Дополнительные сведения см. в разделе **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="3d049-119">For more information, see the **Remarks** section.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="3d049-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d049-120">Remarks</span></span>

<span data-ttu-id="3d049-121">Исходные данные могут поступать из любого типа ресурсов, кроме буферов.</span><span class="sxs-lookup"><span data-stu-id="3d049-121">The source data may come from any Resource Type, other than Buffers.</span></span>

<span data-ttu-id="3d049-122">*сркаддресс* предоставляет набор координат текстуры, необходимых для выполнения образца, в виде значений с плавающей запятой, ссылающихся на нормализованное пространство текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d049-122">*srcAddress* provides the set of texture coordinates needed to perform the sample, as floating point values referencing normalized space in the texture.</span></span> <span data-ttu-id="3d049-123">Режимы переноса адресов (перенос/зеркальное отображение, зажим, границы и т. д.) применяются к координатам текстуры за пределами \[ 0... 1 \] диапазон, взятый из состояния выборки \# , и применяется после того, как к координатам текстуры применяется любое смещение адреса.</span><span class="sxs-lookup"><span data-stu-id="3d049-123">Address wrapping modes (wrap/mirror/clamp/border etc.) are applied for texture coordinates outside \[0...1\] range, taken from the sampler state (s\#), and applied after any address offset is applied to texture coordinates.</span></span>

<span data-ttu-id="3d049-124">*сркресаурце* — это регистр текстуры (t \# ).</span><span class="sxs-lookup"><span data-stu-id="3d049-124">*srcResource* is a texture register (t\#).</span></span> <span data-ttu-id="3d049-125">Это просто заполнитель для текстуры, включая тип возвращаемых данных для ресурса, для которого выполняется выборка.</span><span class="sxs-lookup"><span data-stu-id="3d049-125">This is simply a placeholder for a texture, including the return data type of the resource being sampled.</span></span> <span data-ttu-id="3d049-126">Все эти сведения объявляются в преамбуле шейдера.</span><span class="sxs-lookup"><span data-stu-id="3d049-126">All of this information is declared in the Shader preamble.</span></span> <span data-ttu-id="3d049-127">Фактический ресурс для выборки привязывается к шейдеру снаружи в области \# (для t \# ).</span><span class="sxs-lookup"><span data-stu-id="3d049-127">The actual resource to be sampled is bound to the Shader externally at slot \# (for t\#).</span></span>

<span data-ttu-id="3d049-128">*срксамплер* — это регистры образцов.</span><span class="sxs-lookup"><span data-stu-id="3d049-128">*srcSampler* is a sampler register (s).</span></span> <span data-ttu-id="3d049-129">Это просто заполнитель для коллекции элементов управления фильтрации, таких как точка и линейная, функции текстурирования и элементы управления, поддерживающие перенос адресов.</span><span class="sxs-lookup"><span data-stu-id="3d049-129">This is simply a placeholder for a collection of filtering controls such as point vs. linear, mipmapping and address wrapping controls.</span></span>

<span data-ttu-id="3d049-130">Набор сведений, необходимых оборудованию для выполнения выборки, разбит на две ортогональные части.</span><span class="sxs-lookup"><span data-stu-id="3d049-130">The set of information required for the hardware to perform sampling is split into two orthogonal pieces.</span></span> <span data-ttu-id="3d049-131">Сначала регистр текстуры предоставляет сведения о типе данных, включая, например, сведения о том, содержит ли текстуру данные SRGB.</span><span class="sxs-lookup"><span data-stu-id="3d049-131">First, the texture register provides source data type information including, for example, information about whether the texture contains SRGB data.</span></span> <span data-ttu-id="3d049-132">Он также ссылается на фактическую выборке памяти.</span><span class="sxs-lookup"><span data-stu-id="3d049-132">It also references the actual memory being sampled.</span></span> <span data-ttu-id="3d049-133">Во вторых, регистр образца определяет применяемый режим фильтрации.</span><span class="sxs-lookup"><span data-stu-id="3d049-133">Second, the sampler register defines the filtering mode to apply.</span></span>

### <a name="array-resources"></a><span data-ttu-id="3d049-134">Ресурсы массива</span><span class="sxs-lookup"><span data-stu-id="3d049-134">Array Resources</span></span>

<span data-ttu-id="3d049-135">Для массивов Texture1D компонент *сркаддресс* g (POS-свиззле) выбирает, из какого среза массива нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="3d049-135">For Texture1D Arrays, the *srcAddress* g component (POS-swizzle) selects which Array Slice to fetch from.</span></span> <span data-ttu-id="3d049-136">Это всегда обрабатывается как масштабированное значение с плавающей запятой, а не нормализованное пространство для стандартных координат текстуры, и к значению применяется округление до ближайшего значения, за которым следует срез для доступного диапазона Буффераррай.</span><span class="sxs-lookup"><span data-stu-id="3d049-136">This is always treated as a scaled float value, rather than the normalized space for standard texture coordinates, and a round-to-nearest even is applied on the value, followed by a clamp to the available BufferArray range.</span></span>

<span data-ttu-id="3d049-137">Для массивов Texture2D компонент *сркаддресс* b (POS-свиззле) выбирает срез массива для выборки, в противном случае используя ту же семантику, описанную для массивов Texture1D.</span><span class="sxs-lookup"><span data-stu-id="3d049-137">For Texture2D Arrays, the *srcAddress* b component (POS-swizzle) selects which Array Slice to fetch from, otherwise using the same semantics described for Texture1D Arrays .</span></span>

### <a name="address-offset"></a><span data-ttu-id="3d049-138">Смещение адреса</span><span class="sxs-lookup"><span data-stu-id="3d049-138">Address Offset</span></span>

<span data-ttu-id="3d049-139">Необязательный \[ \_ суффикс аоффимми (u, v, w) \] (смещение адреса непосредственно целым числом) указывает, что координаты текстуры для образца должны быть смещены на набор предоставленных шаг текселя значений целых констант.</span><span class="sxs-lookup"><span data-stu-id="3d049-139">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the sample are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="3d049-140">Литеральные значения представляют собой набор из 4-разрядных чисел 2, имеющих целочисленный диапазон \[ — 8, 7 \] .</span><span class="sxs-lookup"><span data-stu-id="3d049-140">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="3d049-141">Этот модификатор определен для всех ресурсов, включая Texture1D/2D-массивы и Texture3D, но он не определен для Текстурекубе.</span><span class="sxs-lookup"><span data-stu-id="3d049-141">This modifier is defined for all Resources, including Texture1D/2D Arrays and Texture3D, but it is undefined for TextureCube.</span></span>

<span data-ttu-id="3d049-142">Оборудование может воспользоваться преимуществами немедленного знания о том, что обходной объем пикселей текстуры по общему расположению выполняется с помощью набора примеров инструкций.</span><span class="sxs-lookup"><span data-stu-id="3d049-142">Hardware can take advantage of immediate knowledge that a traversal over some footprint of texels about a common location is being performed by a set of sample instructions.</span></span> <span data-ttu-id="3d049-143">Это можно передать с помощью \_ аоффимми (u, v, w).</span><span class="sxs-lookup"><span data-stu-id="3d049-143">This can be conveyed using \_aoffimmi(u,v,w).</span></span>

<span data-ttu-id="3d049-144">Смещения добавляются к координатам текстуры в шаг текселя пространстве относительно каждого доступного миплевел.</span><span class="sxs-lookup"><span data-stu-id="3d049-144">The offsets are added to the texture coordinates, in texel space, relative to each miplevel being accessed.</span></span> <span data-ttu-id="3d049-145">Поэтому, несмотря на то, что координаты текстуры предоставляются в виде нормализованных значений float, смещение применяет шаг текселя целое число.</span><span class="sxs-lookup"><span data-stu-id="3d049-145">So even though texture coordinates are provided as normalized float values, the offset applies a texel-space integer offset.</span></span>

<span data-ttu-id="3d049-146">Смещения адресов не применяются вдоль оси массива Texture1D и двумерных массивов.</span><span class="sxs-lookup"><span data-stu-id="3d049-146">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="3d049-147">\_компоненты аоффимми v, w игнорируются для Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="3d049-147">\_aoffimmi v,w components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="3d049-148">\_компонент аоффимми w не учитывается для Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="3d049-148">\_aoffimmi w component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="3d049-149">Режимы переноса адресов (перенос/зеркальное отображение, зажим, границы и т. д.) из состояния выборки \# применяются после применения смещения адреса к координатам текстуры.</span><span class="sxs-lookup"><span data-stu-id="3d049-149">Address wrapping modes (wrap/mirror/clamp/border etc.) from the sampler state (s\#) are applied after any address offset is applied to texture coordinates.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="3d049-150">Контроль возвращаемого типа</span><span class="sxs-lookup"><span data-stu-id="3d049-150">Return Type Control</span></span>

<span data-ttu-id="3d049-151">Формат данных, возвращаемый образцом в регистр назначения, определяется форматом ресурса ( \_ Формат DXGI), \* привязанным к параметру *сркресаурце* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="3d049-151">The data format returned by the sample to the destination register is determined by the resource format (DXGI\_FORMAT\*) bound to the *srcResource* parameter (t\#).</span></span> <span data-ttu-id="3d049-152">Например, если указанное значение t \# привязано к ресурсу с форматом \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, то операция выборки преобразует пример пикселей текстуры из гаммы 2,0 в 1,0, примените фильтрацию, и результат записывается в регистр назначения в виде значений с плавающей запятой в диапазоне \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="3d049-152">For example, if the specified t\# was bound with a resource with format DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB, then the sampling operation will convert sampled texels from gamma 2.0 to 1.0, apply filtering, and the result will written to the destination register as floating point values in the range \[0..1\].</span></span>

<span data-ttu-id="3d049-153">Возвращаемые значения — это 4 вектора (с использованием значений по умолчанию, относящихся к формату для компонентов, которые не представлены в формате).</span><span class="sxs-lookup"><span data-stu-id="3d049-153">Returned values are 4-vectors (with format-specific defaults for components not present in the format).</span></span> <span data-ttu-id="3d049-154">Свиззле On *сркресаурце* определяет, как свиззле результат из 4 компонентов, который возвращается из примера или фильтра текстуры, после чего параметр. Mask на *dest* определяет, какие компоненты в *destе* будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="3d049-154">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture sample/filter, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="3d049-155">Когда **Пример** считывает 32-разрядное значение с плавающей запятой в 32-разрядный регистр с выборкой точек (без фильтрации), он может или не может сбрасывать ненормальные значения, но в противном случае числа не изменяются.</span><span class="sxs-lookup"><span data-stu-id="3d049-155">When **sample** reads a 32-bit float value into a 32-bit register, with point sampling (no filtering), it may or may not flush denormal values, but otherwise numbers are unmodified.</span></span> <span data-ttu-id="3d049-156">Если неопределенность с выборкой значений Point является проблемой для приложения, используйте инструкцию [LD](ld--sm4---asm-.md) , гарантирующую, что 32-разрядные значения с плавающей запятой считываются без изменений.</span><span class="sxs-lookup"><span data-stu-id="3d049-156">If the uncertainty with point sampling denormal values is an issue for an application,use the [ld](ld--sm4---asm-.md) instruction, which guarantees that 32-bit float values are read unmodified.</span></span>

### <a name="lod-calculation"></a><span data-ttu-id="3d049-157">Вычисление Лод</span><span class="sxs-lookup"><span data-stu-id="3d049-157">LOD Calculation</span></span>

<span data-ttu-id="3d049-158">Дополнительные сведения о вычислении производных элементов в процессе определения Лод для фильтрации см. в разделе [наследование \_ RTX](deriv-rtx--sm4---asm-.md) и [наследование \_ РТИ](deriv-rty--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="3d049-158">For details on how derivatives are calculated in the process of determining LOD for filtering, see [deriv\_rtx](deriv-rtx--sm4---asm-.md) and [deriv\_rty](deriv-rty--sm4---asm-.md).</span></span> <span data-ttu-id="3d049-159">В **образце** инструкции неявно вычисляются производные от координат текстуры с помощью того же определения, которое используются в инструкциях **порожденного** шейдера.</span><span class="sxs-lookup"><span data-stu-id="3d049-159">The **sample** instruction implicitly computes derivatives on the texture coordinates using the same definition that the **deriv** Shader instructions use.</span></span> <span data-ttu-id="3d049-160">Это не относится к [образцам \_ l](sample-l--sm4---asm-.md) или [Sample \_ d](sample-d--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="3d049-160">This does not apply to [sample\_l](sample-l--sm4---asm-.md) or [sample\_d](sample-d--sm4---asm-.md) instructions.</span></span> <span data-ttu-id="3d049-161">Для этих инструкций Лод или производные приложения предоставляются непосредственно приложением.</span><span class="sxs-lookup"><span data-stu-id="3d049-161">For those instructions, LOD or derivatives are provided directly by the application.</span></span>

<span data-ttu-id="3d049-162">Для **примера** инструкции реализации могут использовать одни и те же вычисления Лод во всех 4 пикселях в формате 2x2 (но не в более крупной области) или выполнять вычисления Лод на уровне отдельных пикселей.</span><span class="sxs-lookup"><span data-stu-id="3d049-162">For the **sample** instruction, implementations can choose to share the same LOD calculation across all 4 pixels in a 2x2 stamp (but no larger area), or perform per-pixel LOD calculations.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="3d049-163">Прочие сведения</span><span class="sxs-lookup"><span data-stu-id="3d049-163">Miscellaneous Details</span></span>

<span data-ttu-id="3d049-164">Для buffer & Texture1D, *сркаддресс* . Гба Components (POS-свиззле), игнорируются.</span><span class="sxs-lookup"><span data-stu-id="3d049-164">For Buffer & Texture1D, *srcAddress* .gba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="3d049-165">Для массивов Texture1D компоненты *сркаддресс* . BA (POS-свиззле) игнорируются.</span><span class="sxs-lookup"><span data-stu-id="3d049-165">For Texture1D Arrays, *srcAddress* .ba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="3d049-166">Для Texture2Ds, *сркаддресс* . компонент (POS-свиззле) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3d049-166">For Texture2Ds, *srcAddress* .a component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="3d049-167">При попытке получить из входного слота, к которому не привязано ничего, возвращается значение 0 для всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="3d049-167">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="3d049-168">Ограничения</span><span class="sxs-lookup"><span data-stu-id="3d049-168">Restrictions</span></span>

-   <span data-ttu-id="3d049-169">*сркресаурце* должен быть \# регистром t.</span><span class="sxs-lookup"><span data-stu-id="3d049-169">*srcResource* must be a t\# register.</span></span> <span data-ttu-id="3d049-170">*сркресаурце* не может быть константбуффер, который не может быть привязан к \# регистрам t.</span><span class="sxs-lookup"><span data-stu-id="3d049-170">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="3d049-171">*срксамплер* должен быть \# регистром s.</span><span class="sxs-lookup"><span data-stu-id="3d049-171">*srcSampler* must be an s\# register.</span></span>
-   <span data-ttu-id="3d049-172">Относительная адресация в *сркресаурце* или *срксамплер* не разрешена.</span><span class="sxs-lookup"><span data-stu-id="3d049-172">Relative addressing on *srcResource* or *srcSampler* is not permitted.</span></span>
-   <span data-ttu-id="3d049-173">*сркаддресс* должен быть временным (r \# /X \# ), константбуффер (CB \# ), входным (v \# ) или непосредственным значением (с).</span><span class="sxs-lookup"><span data-stu-id="3d049-173">*srcAddress* must be a temp (r\#/x\#), constantBuffer (cb\#), input (v\#) register or immediate value(s).</span></span>
-   <span data-ttu-id="3d049-174">*dest* должен быть временным (r \# /x \# ) или выходным \* \# регистром (o).</span><span class="sxs-lookup"><span data-stu-id="3d049-174">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>
-   <span data-ttu-id="3d049-175">\_аоффимми (u, v, w) не разрешено для Текстурекубес.</span><span class="sxs-lookup"><span data-stu-id="3d049-175">\_aoffimmi(u,v,w) is not permitted for TextureCubes.</span></span>

<span data-ttu-id="3d049-176">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="3d049-176">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3d049-177">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="3d049-177">Vertex Shader</span></span> | <span data-ttu-id="3d049-178">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="3d049-178">Geometry Shader</span></span> | <span data-ttu-id="3d049-179">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="3d049-179">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="3d049-180">x</span><span class="sxs-lookup"><span data-stu-id="3d049-180">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3d049-181">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3d049-181">Minimum Shader Model</span></span>

<span data-ttu-id="3d049-182">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="3d049-182">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3d049-183">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3d049-183">Shader Model</span></span>                                              | <span data-ttu-id="3d049-184">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3d049-184">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3d049-185">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3d049-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3d049-186">да</span><span class="sxs-lookup"><span data-stu-id="3d049-186">yes</span></span>       |
| [<span data-ttu-id="3d049-187">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="3d049-187">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3d049-188">да</span><span class="sxs-lookup"><span data-stu-id="3d049-188">yes</span></span>       |
| [<span data-ttu-id="3d049-189">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="3d049-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3d049-190">да</span><span class="sxs-lookup"><span data-stu-id="3d049-190">yes</span></span>       |
| [<span data-ttu-id="3d049-191">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d049-191">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3d049-192">Нет</span><span class="sxs-lookup"><span data-stu-id="3d049-192">no</span></span>        |
| [<span data-ttu-id="3d049-193">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d049-193">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3d049-194">Нет</span><span class="sxs-lookup"><span data-stu-id="3d049-194">no</span></span>        |
| [<span data-ttu-id="3d049-195">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d049-195">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3d049-196">Нет</span><span class="sxs-lookup"><span data-stu-id="3d049-196">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3d049-197">См. также</span><span class="sxs-lookup"><span data-stu-id="3d049-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d049-198">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d049-198">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





