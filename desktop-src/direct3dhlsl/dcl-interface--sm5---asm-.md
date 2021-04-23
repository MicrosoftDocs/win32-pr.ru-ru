---
title: dcl_interface (SM5-ASM)
description: Объявите указатели на таблицу функций (интерфейсы). | dcl_interface (SM5-ASM)
ms.assetid: 5A4D911E-7117-409B-8FDC-9CEC2C185C15
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61435e06d0d5b88bb82ca91f758646d7911d3bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998083"
---
# <a name="dcl_interface-sm5---asm"></a><span data-ttu-id="0d3c8-104">\_интерфейс дкл (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0d3c8-104">dcl\_interface (sm5 - asm)</span></span>

<span data-ttu-id="0d3c8-105">Объявите указатели на таблицу функций (интерфейсы).</span><span class="sxs-lookup"><span data-stu-id="0d3c8-105">Declare function table pointers (interfaces).</span></span>



| <span data-ttu-id="0d3c8-106">\_интерфейс дкл FP \# \[ размера массива \] \[ нумкаллситес \] = {ft \# , ft \# ,...}</span><span class="sxs-lookup"><span data-stu-id="0d3c8-106">dcl\_interface fp\#\[arraySize\]\[numCallSites\] = {ft\#, ft\#, ...}</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="0d3c8-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="0d3c8-107">Item</span></span>                                                          | <span data-ttu-id="0d3c8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0d3c8-108">Description</span></span>                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="0d3c8-109"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="0d3c8-109"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/> | <span data-ttu-id="0d3c8-110">\[в \] указателях таблицы функций.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-110">\[in\] The function table pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d3c8-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d3c8-111">Remarks</span></span>

<span data-ttu-id="0d3c8-112">Прежде чем использовать шейдер, каждый интерфейс должен быть привязан к API.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-112">Each interface needs to be bound from the API before the shader is usable.</span></span> <span data-ttu-id="0d3c8-113">Привязка предоставляет ссылку на одну из таблиц функций, чтобы можно было заполнить слоты метода.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-113">Binding gives a reference to one of the function tables so that the method slots can be filled in.</span></span> <span data-ttu-id="0d3c8-114">Компилятор не будет создавать указатели для объектов, на которые нет ссылок.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-114">The compiler will not generate pointers for unreferenced objects.</span></span>

<span data-ttu-id="0d3c8-115">Указатель таблицы функций имеет полный набор областей методов, чтобы избежать дополнительного уровня косвенного обращения, которое потребовалось для представления указателя на объект C++ в виде указателя на таблицу vtable.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-115">A function table pointer has a full set of method slots to avoid the extra level of indirection that a C++ pointer-to- pointer-to-vtable representation would require.</span></span> <span data-ttu-id="0d3c8-116">Это также потребует, чтобы эти указатели были пятью кортежами.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-116">That would also require that this pointers be 5-tuples.</span></span> <span data-ttu-id="0d3c8-117">В модели виртуального деструктуры HLSL всегда известно, какие глобальные переменные и входные данные используются для вызова, чтобы мы могли настроить таблицы для каждого корневого объекта.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-117">In the HLSL virtual inlining model it's always known what global variable/input is used for a call so we can set up tables per root object.</span></span>

<span data-ttu-id="0d3c8-118">Объявления указателей функций указывают, какие таблицы функций допустимы для использования с ними.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-118">Function pointer declarations indicate which function tables are legal to use with them.</span></span> <span data-ttu-id="0d3c8-119">Это также позволяет получить производную информацию о корреляции методов.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-119">This also allows derivation of method correlation information.</span></span>

<span data-ttu-id="0d3c8-120">Первое \[ \] объявление интерфейса — это размер массива.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-120">The first \[\] of an interface declaration is the array size.</span></span> <span data-ttu-id="0d3c8-121">Если используется динамическое индексирование, объявление будет указывать, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-121">If dynamic indexing is used the declaration will indicate that as shown.</span></span> <span data-ttu-id="0d3c8-122">Массив указателей интерфейсов может индексироваться статически. также не требуется, чтобы массивы указателей интерфейсов имели динамическую индексацию.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-122">An array of interface pointers can be indexed statically also, it is not required that arrays of interface pointers mean dynamic indexing.</span></span>

<span data-ttu-id="0d3c8-123">Нумерация указателей интерфейсов начинается с 0 для первого объявления и затем принимает размер массива в учетной записи, поэтому первым указателем после четырех входных массивов Fp0 \[ 4 \] \[ 1 будет \] fp4 \[ \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="0d3c8-123">Numbering of interface pointers starts at 0 for the first declaration and subsequently takes array size into account, so the first pointer after a four entry array fp0\[4\]\[1\] would be fp4\[\]\[\].</span></span>

<span data-ttu-id="0d3c8-124">Вторым \[ \] объявлением интерфейса является количество мест вызова, которые должны соответствовать числу фрагментов в каждой таблице, на которую ссылается объявление.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-124">The second \[\] of an interface declaration is the number of call sites, which must match the number of bodies in each table referenced in the declaration.</span></span>

<span data-ttu-id="0d3c8-125">Нет границ для количества вариантов таблицы функций (ft), которые \# могут быть перечислены в объявлении интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-125">There are no bounds to how many function table (ft\#) choices can be listed in an interface declaration.</span></span>

<span data-ttu-id="0d3c8-126">Данная таблица функций (ft \# ) может появляться в одном или нескольких объявлениях интерфейса более одного раза.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-126">A given function table (ft\#) can appear more than once in one or more interface declarations.</span></span>

### <a name="restrictions"></a><span data-ttu-id="0d3c8-127">Ограничения</span><span class="sxs-lookup"><span data-stu-id="0d3c8-127">Restrictions</span></span>

-   <span data-ttu-id="0d3c8-128">Число сайтов объектов в шейдере, которое является суммой для всех объявлений *FP \#* их \[ \] объявлений размера массива, не должно превышать 253.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-128">The number of object sites in a shader, which is the sum across all *fp\#* declarations of their \[arraySize\] declarations, must be no more than 253.</span></span> <span data-ttu-id="0d3c8-129">Это число соответствует числу **этих** указателей.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-129">This number corresponds to how many **this** pointers can be present.</span></span> <span data-ttu-id="0d3c8-130">Среда выполнения применяет это ограничение 253, чтобы иметь ограниченный размер DDI для связи с данными указателя.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-130">The runtime enforces this 253 limit to keep a bound on the size of the DDI for communicating this pointer data.</span></span>
-   <span data-ttu-id="0d3c8-131">Число сайтов вызова в шейдере, которое является суммой для всех инструкций фкалл в количестве потенциальных целей ветвления, не должно превышать 4096.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-131">The number of call sites in a shader, which is the sum across all fcall statements of the number of potential branch targets, must be no more than 4096.</span></span>

    <span data-ttu-id="0d3c8-132">Например, [фкалл](fcall--sm5---asm-.md) , использующий статический индекс для первого *плоского \[ \] \[ \]* измерения, считается одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="0d3c8-132">For example, an [fcall](fcall--sm5---asm-.md) that uses a static index for the first *fp\[\]\[\]* dimension counts as one:</span></span>

    `                       fcall fp0[0][0]         // +1`

    <span data-ttu-id="0d3c8-133">**Фкалл** , использующий динамический индекс, считается числом элементов в массиве (первым \[ \] из **\_ интерфейса дкл**):</span><span class="sxs-lookup"><span data-stu-id="0d3c8-133">An **fcall** that uses a dynamic index counts as the number of elements in the array (first \[\] of **dcl\_interface**):</span></span>

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    <span data-ttu-id="0d3c8-134">Это ограничение позволяет некоторым реализациям легко подобрать таблицы, выделенные в теле функции, в постоянном хранилище, аналогичном буферу.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-134">This limit helps some implementations easily fit tables of function body selections in constant buffer-like storage.</span></span>

<span data-ttu-id="0d3c8-135">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0d3c8-135">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0d3c8-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="0d3c8-136">Vertex</span></span> | <span data-ttu-id="0d3c8-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0d3c8-137">Hull</span></span> | <span data-ttu-id="0d3c8-138">Домен</span><span class="sxs-lookup"><span data-stu-id="0d3c8-138">Domain</span></span> | <span data-ttu-id="0d3c8-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0d3c8-139">Geometry</span></span> | <span data-ttu-id="0d3c8-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0d3c8-140">Pixel</span></span> | <span data-ttu-id="0d3c8-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0d3c8-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0d3c8-142">X</span><span class="sxs-lookup"><span data-stu-id="0d3c8-142">X</span></span>      | <span data-ttu-id="0d3c8-143">X</span><span class="sxs-lookup"><span data-stu-id="0d3c8-143">X</span></span>    | <span data-ttu-id="0d3c8-144">X</span><span class="sxs-lookup"><span data-stu-id="0d3c8-144">X</span></span>      | <span data-ttu-id="0d3c8-145">X</span><span class="sxs-lookup"><span data-stu-id="0d3c8-145">X</span></span>        | <span data-ttu-id="0d3c8-146">X</span><span class="sxs-lookup"><span data-stu-id="0d3c8-146">X</span></span>     | <span data-ttu-id="0d3c8-147">X</span><span class="sxs-lookup"><span data-stu-id="0d3c8-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0d3c8-148">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0d3c8-148">Minimum Shader Model</span></span>

<span data-ttu-id="0d3c8-149">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0d3c8-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0d3c8-150">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0d3c8-150">Shader Model</span></span>                                              | <span data-ttu-id="0d3c8-151">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0d3c8-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0d3c8-152">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0d3c8-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0d3c8-153">да</span><span class="sxs-lookup"><span data-stu-id="0d3c8-153">yes</span></span>       |
| [<span data-ttu-id="0d3c8-154">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0d3c8-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0d3c8-155">Нет</span><span class="sxs-lookup"><span data-stu-id="0d3c8-155">no</span></span>        |
| [<span data-ttu-id="0d3c8-156">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0d3c8-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0d3c8-157">Нет</span><span class="sxs-lookup"><span data-stu-id="0d3c8-157">no</span></span>        |
| [<span data-ttu-id="0d3c8-158">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0d3c8-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0d3c8-159">Нет</span><span class="sxs-lookup"><span data-stu-id="0d3c8-159">no</span></span>        |
| [<span data-ttu-id="0d3c8-160">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0d3c8-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0d3c8-161">Нет</span><span class="sxs-lookup"><span data-stu-id="0d3c8-161">no</span></span>        |
| [<span data-ttu-id="0d3c8-162">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0d3c8-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0d3c8-163">Нет</span><span class="sxs-lookup"><span data-stu-id="0d3c8-163">no</span></span>        |



 

<span data-ttu-id="0d3c8-164">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают эту инструкцию для UAV и SRV.</span><span class="sxs-lookup"><span data-stu-id="0d3c8-164">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d3c8-165">См. также</span><span class="sxs-lookup"><span data-stu-id="0d3c8-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d3c8-166">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0d3c8-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





