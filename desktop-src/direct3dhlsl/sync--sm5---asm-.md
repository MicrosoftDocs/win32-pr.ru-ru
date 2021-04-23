---
title: Синхронизация (SM5-ASM)
description: Синхронизация группы потоков или барьер памяти.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996999"
---
# <a name="sync-sm5---asm"></a><span data-ttu-id="e3d13-103">Синхронизация (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e3d13-103">sync (sm5 - asm)</span></span>

<span data-ttu-id="e3d13-104">Синхронизация группы потоков или барьер памяти.</span><span class="sxs-lookup"><span data-stu-id="e3d13-104">Thread group sync or memory barrier.</span></span>



| <span data-ttu-id="e3d13-105">\[ \_ углобал синхронизации </span><span class="sxs-lookup"><span data-stu-id="e3d13-105">sync\[\_uglobal</span></span>\|<span data-ttu-id="e3d13-106">\_уграуп \] \[ \_ g \] \[ \_ t\]</span><span class="sxs-lookup"><span data-stu-id="e3d13-106">\_ugroup\]\[\_g\]\[\_t\]</span></span> |
|-------------------------------------------|



 

## <a name="remarks"></a><span data-ttu-id="e3d13-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3d13-107">Remarks</span></span>

<span data-ttu-id="e3d13-108">**Sync** содержит параметры \_ углобал, \_ уграуп, \_ g и \_ t.</span><span class="sxs-lookup"><span data-stu-id="e3d13-108">**Sync** has options \_uglobal, \_ugroup, \_g and \_t.</span></span>

<span data-ttu-id="e3d13-109">В шейдере пикселей допускается только **\_ углобал синхронизации** .</span><span class="sxs-lookup"><span data-stu-id="e3d13-109">In the pixel shader, only **sync\_uglobal** is allowed.</span></span>

<span data-ttu-id="e3d13-110">В шейдере COMPUTE \_ необходимо указать (углобал или \_ уграуп \* ) и/или \_ g.</span><span class="sxs-lookup"><span data-stu-id="e3d13-110">In the compute shader, (\_uglobal or \_ugroup\*) and/or \_g must be specified.</span></span> <span data-ttu-id="e3d13-111">\_t является необязательным дополнением.</span><span class="sxs-lookup"><span data-stu-id="e3d13-111">\_t is optional in addition.</span></span>

### <a name="_uglobal"></a><span data-ttu-id="e3d13-112">\_углобал</span><span class="sxs-lookup"><span data-stu-id="e3d13-112">\_uglobal</span></span>

<span data-ttu-id="e3d13-113">Глобальная \# граница памяти u (UAV).</span><span class="sxs-lookup"><span data-stu-id="e3d13-113">Global u\# (UAV) memory fence.</span></span>

<span data-ttu-id="e3d13-114">Все предыдущие \# операции чтения и записи в памяти, выполняемые этим потоком в порядке программ, становятся видимыми для всех потоков во всем GPU до последующего \# обращения к памяти u в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="e3d13-114">All prior u\# memory reads/writes by this thread in program order are made visible to all threads on the entire GPU before any subsequent u\# memory accesses by this thread.</span></span> <span data-ttu-id="e3d13-115">Вся часть графического процессора в определении заменяется областью "менее чем глобальная" в одном случае, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="e3d13-115">The entire GPU part of the definition is replaced by a less-than-global scope in one case, described below.</span></span>

<span data-ttu-id="e3d13-116">Это относится ко всей UAV памяти, привязанной к текущему этапу шейдера.</span><span class="sxs-lookup"><span data-stu-id="e3d13-116">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="e3d13-117">\_углобал доступен в шейдере вычислений и шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="e3d13-117">\_uglobal is available in the compute shader or pixel shader.</span></span>

<span data-ttu-id="e3d13-118">Для всех привязанных UAV, которые не были объявлены шейдером как глобально согласованными, \_ граница углобал u \# Memory имеет видимость только в текущей группе потоков шейдера вычислений для этого UAV, как если бы это \_ уграуп, а не \_ углобал.</span><span class="sxs-lookup"><span data-stu-id="e3d13-118">For any bound UAV that has not been declared by the shader as Globally Coherent, the \_uglobal u\# memory fence only has visibility within the current compute shader thread-group for that UAV, as if it is \_ugroup instead of \_uglobal.</span></span> <span data-ttu-id="e3d13-119">Эта проблема относится только к выпуску COMPUTE Shader, так как шейдер пикселей должен объявлять все Уавс как глобально согласованные.</span><span class="sxs-lookup"><span data-stu-id="e3d13-119">This issue only applies to the compute shader, since the pixel shader must declare all UAVs as Globally Coherent.</span></span>

### <a name="_ugroup"></a><span data-ttu-id="e3d13-120">\_уграуп</span><span class="sxs-lookup"><span data-stu-id="e3d13-120">\_ugroup</span></span>

<span data-ttu-id="e3d13-121">Ограждение области группы потоков u \# (UAV).</span><span class="sxs-lookup"><span data-stu-id="e3d13-121">Thread group scope u\# (UAV) memory fence.</span></span>

<span data-ttu-id="e3d13-122">Все предыдущие \# операции чтения или записи в памяти, выполняемые этим потоком в порядке программ, становятся видимыми для всех потоков в группе потоков до последующего \# обращения к памяти u в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="e3d13-122">All prior u\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent u\# memory accesses by this thread.</span></span>

<span data-ttu-id="e3d13-123">Это относится ко всей UAV памяти, привязанной к текущему этапу шейдера.</span><span class="sxs-lookup"><span data-stu-id="e3d13-123">This applies to all UAV memory bound at the current shader stage.</span></span>

<span data-ttu-id="e3d13-124">\_уграуп доступен только в шейдере COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="e3d13-124">\_ugroup is available in the compute shader only.</span></span>

<span data-ttu-id="e3d13-125">\_Значение, если уграуп предоставляется для некоторых реализаций.</span><span class="sxs-lookup"><span data-stu-id="e3d13-125">If \_ugroup is exposed, for some implementations.</span></span> <span data-ttu-id="e3d13-126">Преимуществом указания \_ уграуп вместо \_ углобал является то, что операция **синхронизации** может быть выполнена быстрее.</span><span class="sxs-lookup"><span data-stu-id="e3d13-126">The advantage of specifying \_ugroup instead of \_uglobal is that the **sync** operation can complete more quickly.</span></span>

<span data-ttu-id="e3d13-127">Другие реализации не отличают \_ уграуп от \_ углобал, поэтому обе операции эквивалентны и ведут себя как \_ углобал.</span><span class="sxs-lookup"><span data-stu-id="e3d13-127">Other implementations do not distinguish \_ugroup from \_uglobal, so both operations are equivalent and behave like \_uglobal.</span></span> <span data-ttu-id="e3d13-128">Приложения могут указать их намерение, запрашивая наиболее узкую область **синхронизации** .</span><span class="sxs-lookup"><span data-stu-id="e3d13-128">Applications can specify their intent by requesting the narrowest scope of **sync** necessary.</span></span>

<span data-ttu-id="e3d13-129">Даже если конкретная UAV объявлена как глобально согласованная, \_ операция **синхронизации** уграуп будет работать более эффективно на этом UAV, если глобальное препятствие не требуется.</span><span class="sxs-lookup"><span data-stu-id="e3d13-129">Even if a particular UAV is declared as Globally Coherent, a \_ugroup **sync** operation will function more efficiently on that UAV if a global barrier is not required.</span></span>

### <a name="_g"></a><span data-ttu-id="e3d13-130">\_модуле</span><span class="sxs-lookup"><span data-stu-id="e3d13-130">\_g</span></span>

<span data-ttu-id="e3d13-131">\#граница g (общая память группы потоков).</span><span class="sxs-lookup"><span data-stu-id="e3d13-131">g\# (thread group shared memory) fence.</span></span>

<span data-ttu-id="e3d13-132">Все предыдущие операции \# чтения или записи в памяти для этого потока в порядке программы становятся видимыми для всех потоков в группе потоков до последующего \# доступа к памяти в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="e3d13-132">All prior g\# memory reads or writes by this thread in program order are made visible to all threads in the thread group before any subsequent g\# memory accesses by this thread.</span></span>

<span data-ttu-id="e3d13-133">Это относится ко всей общей памяти группы текущего потока \# .</span><span class="sxs-lookup"><span data-stu-id="e3d13-133">This applies to all of the current thread group's g\# shared memory.</span></span>

<span data-ttu-id="e3d13-134">\_g доступен только в шейдере COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="e3d13-134">\_g is available in the compute shader only.</span></span>

### <a name="_t"></a><span data-ttu-id="e3d13-135">\_t</span><span class="sxs-lookup"><span data-stu-id="e3d13-135">\_t</span></span>

<span data-ttu-id="e3d13-136">Синхронизация группы потоков. Все потоки в одной группе потоков (которые могут совместно использовать общий набор общих пространств реестра) будут выполняться до того места, где они достигают этой инструкции до того, как любой поток сможет продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="e3d13-136">Thread group sync. All threads within a single thread group (those that can share access to a common set of shared register space) will be executed up to the point where they reach this instruction before any thread can continue.</span></span>

<span data-ttu-id="e3d13-137">\_t не может размещаться в динамическом элементе управления потоком (ветви, которые могут изменяться в группе потоков), но могут присутствовать в едином потоке управления, где все потоки в группе выбирают один и тот же путь.</span><span class="sxs-lookup"><span data-stu-id="e3d13-137">\_t cannot be placed in dynamic flow control, (branches which could vary within a thread group), but can be present in uniform flow control, where all threads in the group pick the same path.</span></span>

<span data-ttu-id="e3d13-138">\_t доступен только в шейдере COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="e3d13-138">\_t is available in the compute shader only.</span></span>

<span data-ttu-id="e3d13-139">Ниже приведен список вариантов «Sync» вычислений COMPUTE Shader.</span><span class="sxs-lookup"><span data-stu-id="e3d13-139">The following is a listing of compute shader ‘sync’ variants.</span></span>

-   <span data-ttu-id="e3d13-140">Синхронизация \_ g</span><span class="sxs-lookup"><span data-stu-id="e3d13-140">sync\_g</span></span>
-   <span data-ttu-id="e3d13-141">\_уграуп синхронизации\*</span><span class="sxs-lookup"><span data-stu-id="e3d13-141">sync\_ugroup\*</span></span>
-   <span data-ttu-id="e3d13-142">\_углобал синхронизации</span><span class="sxs-lookup"><span data-stu-id="e3d13-142">sync\_uglobal</span></span>
-   <span data-ttu-id="e3d13-143">Синхронизация \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="e3d13-143">sync\_g\_t</span></span>
-   <span data-ttu-id="e3d13-144">\_уграуп синхронизации \_ t\*</span><span class="sxs-lookup"><span data-stu-id="e3d13-144">sync\_ugroup\_t\*</span></span>
-   <span data-ttu-id="e3d13-145">\_углобал синхронизации \_ t</span><span class="sxs-lookup"><span data-stu-id="e3d13-145">sync\_uglobal\_t</span></span>
-   <span data-ttu-id="e3d13-146">Синхронизация \_ уграуп \_ g\*</span><span class="sxs-lookup"><span data-stu-id="e3d13-146">sync\_ugroup\_g\*</span></span>
-   <span data-ttu-id="e3d13-147">Синхронизация \_ углобал \_ g</span><span class="sxs-lookup"><span data-stu-id="e3d13-147">sync\_uglobal\_g</span></span>
-   <span data-ttu-id="e3d13-148">Синхронизация \_ уграуп \_ g \_ t\*</span><span class="sxs-lookup"><span data-stu-id="e3d13-148">sync\_ugroup\_g\_t\*</span></span>
-   <span data-ttu-id="e3d13-149">Синхронизация \_ углобал \_ g \_ t</span><span class="sxs-lookup"><span data-stu-id="e3d13-149">sync\_uglobal\_g\_t</span></span>

<span data-ttu-id="e3d13-150">\*У вариантов с \_ уграуп может не быть цели КОМПИЛЯТОРА HLSL, в предыдущем обсуждении в \_ разделе уграуп выше.</span><span class="sxs-lookup"><span data-stu-id="e3d13-150">\*Variants with \_ugroup may not be targeted by the HLSL compiler, per the earlier discussion in the \_ugroup section above.</span></span>

<span data-ttu-id="e3d13-151">Список вариантов синхронизации пиксельного шейдера включает \_ только углобал синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e3d13-151">Listing of pixel shader sync variants include sync\_uglobal only.</span></span>

<span data-ttu-id="e3d13-152">Границы памяти предотвращают Переупорядочение инструкций по компиляторам или оборудованию в ограждении.</span><span class="sxs-lookup"><span data-stu-id="e3d13-152">Memory fences prevent affected instructions from being reordered by compilers or hardware across the fence.</span></span>

<span data-ttu-id="e3d13-153">Несколько операций чтения из одного адреса с помощью вызова шейдера, которые не разделены барьерами памяти или записи в адрес, можно свернуть вместе.</span><span class="sxs-lookup"><span data-stu-id="e3d13-153">Multiple reads from the same address by a shader invocation that are not separated by memory barriers or writes to the address can be collapsed together.</span></span> <span data-ttu-id="e3d13-154">Это относится и к операциям записи.</span><span class="sxs-lookup"><span data-stu-id="e3d13-154">The same applies to writes.</span></span> <span data-ttu-id="e3d13-155">Доступ, разделенный барьером, не может быть объединен или перемещен в пределах барьера.</span><span class="sxs-lookup"><span data-stu-id="e3d13-155">Accesses separated by a barrier cannot be merged or moved across the barrier.</span></span>

<span data-ttu-id="e3d13-156">Границы памяти не являются обязательными для атомарных операций с определенным адресом различными потоками для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="e3d13-156">Memory fences are not necessary for atomic operations to a given address by different threads to function correctly.</span></span> <span data-ttu-id="e3d13-157">Ограждения необходимы, когда операции Atomic и/или Load/Store должны быть синхронизированы друг с другом, так как они появляются в отдельных потоках с точки зрения других потоков.</span><span class="sxs-lookup"><span data-stu-id="e3d13-157">Fences are needed when atomics and/or load/store operations need to be synchronized with respect to each other as they appear in individual threads from the point of view of other threads.</span></span>

<span data-ttu-id="e3d13-158">В построителе пиксельных шейдеров инструкции по [удалению](discard--sm4---asm-.md) подразумевают \_ углобал границу синхронизации. в этом случае нельзя изменить порядок этих инструкций в случае **отмены**.</span><span class="sxs-lookup"><span data-stu-id="e3d13-158">In the pixel shader, [discard](discard--sm4---asm-.md) instructions imply a sync\_uglobal fence, in that instructions cannot be reordered across the **discard**.</span></span> <span data-ttu-id="e3d13-159">Синхронизация \_ углобал в вспомогательных точках (которые выполняются только для поддержки производных) или отклоненных пикселов может и не влиять.</span><span class="sxs-lookup"><span data-stu-id="e3d13-159">sync\_uglobal in helper pixels (which run only to support derivatives) or discarded pixels may or may not have any affect.</span></span> <span data-ttu-id="e3d13-160">Не разрешается использовать вспомогательные или Отклоненные Пиксели для записи в Уавс, если в случае отмены записи выдаются после удаления.</span><span class="sxs-lookup"><span data-stu-id="e3d13-160">It is not allowed for helper or discarded pixels to write to UAVs if, in the case of discard, the writes are issued after the discard.</span></span> <span data-ttu-id="e3d13-161">Возвращаемые значения из Уавс не могут участвовать в производных вычислениях.</span><span class="sxs-lookup"><span data-stu-id="e3d13-161">Returned values from UAVs are not allowed to contribute to derivative calculations.</span></span> <span data-ttu-id="e3d13-162">Поэтому независимо от того, \_ учитывается ли синхронизация u для вспомогательных точек или когда она выдается после удаления, затеи.</span><span class="sxs-lookup"><span data-stu-id="e3d13-162">Therefore whether or not sync\_u is honored for helper pixels or when issued after a discard is moot.</span></span>

<span data-ttu-id="e3d13-163">\_инструкция CS 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="e3d13-163">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="e3d13-164">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="e3d13-164">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e3d13-165">Вершина</span><span class="sxs-lookup"><span data-stu-id="e3d13-165">Vertex</span></span> | <span data-ttu-id="e3d13-166">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e3d13-166">Hull</span></span> | <span data-ttu-id="e3d13-167">Домен</span><span class="sxs-lookup"><span data-stu-id="e3d13-167">Domain</span></span> | <span data-ttu-id="e3d13-168">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e3d13-168">Geometry</span></span> | <span data-ttu-id="e3d13-169">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e3d13-169">Pixel</span></span> | <span data-ttu-id="e3d13-170">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e3d13-170">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e3d13-171">X</span><span class="sxs-lookup"><span data-stu-id="e3d13-171">X</span></span>     | <span data-ttu-id="e3d13-172">X</span><span class="sxs-lookup"><span data-stu-id="e3d13-172">X</span></span>       |



 

<span data-ttu-id="e3d13-173">Так как Уавс доступны на всех стадиях шейдера для Direct3D 11,1, вариант **Sync \_ углобал** этой инструкции применяется ко всем этапам шейдера для среды выполнения Direct3D 11,1, которая доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e3d13-173">Because UAVs are available at all shader stages for Direct3D 11.1, the **sync\_uglobal** variant of this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e3d13-174">Вершина</span><span class="sxs-lookup"><span data-stu-id="e3d13-174">Vertex</span></span> | <span data-ttu-id="e3d13-175">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e3d13-175">Hull</span></span> | <span data-ttu-id="e3d13-176">Домен</span><span class="sxs-lookup"><span data-stu-id="e3d13-176">Domain</span></span> | <span data-ttu-id="e3d13-177">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e3d13-177">Geometry</span></span> | <span data-ttu-id="e3d13-178">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e3d13-178">Pixel</span></span> | <span data-ttu-id="e3d13-179">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e3d13-179">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e3d13-180">X</span><span class="sxs-lookup"><span data-stu-id="e3d13-180">X</span></span>      | <span data-ttu-id="e3d13-181">X</span><span class="sxs-lookup"><span data-stu-id="e3d13-181">X</span></span>    | <span data-ttu-id="e3d13-182">X</span><span class="sxs-lookup"><span data-stu-id="e3d13-182">X</span></span>      | <span data-ttu-id="e3d13-183">X</span><span class="sxs-lookup"><span data-stu-id="e3d13-183">X</span></span>        | <span data-ttu-id="e3d13-184">X</span><span class="sxs-lookup"><span data-stu-id="e3d13-184">X</span></span>     | <span data-ttu-id="e3d13-185">X</span><span class="sxs-lookup"><span data-stu-id="e3d13-185">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e3d13-186">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e3d13-186">Minimum Shader Model</span></span>

<span data-ttu-id="e3d13-187">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e3d13-187">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e3d13-188">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e3d13-188">Shader Model</span></span>                                              | <span data-ttu-id="e3d13-189">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e3d13-189">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e3d13-190">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e3d13-190">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e3d13-191">да</span><span class="sxs-lookup"><span data-stu-id="e3d13-191">yes</span></span>       |
| [<span data-ttu-id="e3d13-192">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="e3d13-192">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e3d13-193">Нет</span><span class="sxs-lookup"><span data-stu-id="e3d13-193">no</span></span>        |
| [<span data-ttu-id="e3d13-194">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e3d13-194">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e3d13-195">Нет</span><span class="sxs-lookup"><span data-stu-id="e3d13-195">no</span></span>        |
| [<span data-ttu-id="e3d13-196">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3d13-196">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e3d13-197">Нет</span><span class="sxs-lookup"><span data-stu-id="e3d13-197">no</span></span>        |
| [<span data-ttu-id="e3d13-198">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3d13-198">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e3d13-199">Нет</span><span class="sxs-lookup"><span data-stu-id="e3d13-199">no</span></span>        |
| [<span data-ttu-id="e3d13-200">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3d13-200">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e3d13-201">Нет</span><span class="sxs-lookup"><span data-stu-id="e3d13-201">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e3d13-202">См. также</span><span class="sxs-lookup"><span data-stu-id="e3d13-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3d13-203">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e3d13-203">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




