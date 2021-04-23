---
title: vs_2_x
description: Программируемый шейдер вершин состоит из набора инструкций, которые работают с данными вершин. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488040"
---
# <a name="vs_2_x"></a><span data-ttu-id="5f264-105">VS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5f264-105">vs\_2\_x</span></span>

<span data-ttu-id="5f264-106">Программируемый шейдер вершин состоит из набора инструкций, которые работают с данными вершин.</span><span class="sxs-lookup"><span data-stu-id="5f264-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="5f264-107">Регистрирует перенос данных в ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="5f264-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="5f264-108">Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.</span><span class="sxs-lookup"><span data-stu-id="5f264-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="5f264-109">Версия шейдера вершин и \_ 2 \_ x расширяет набор функций, поддерживаемый VS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="5f264-109">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="5f264-110">Каждая дополнительная функция представлена соответствующим ограничением в структуре [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) в [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span><span class="sxs-lookup"><span data-stu-id="5f264-110">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="5f264-111">Чтобы использовать любые расширенные функции, представленные этими ограничениями, необходимо указать версию шейдера вершин в VS \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="5f264-111">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="5f264-112">[Инструкции — VS \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) содержит список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="5f264-112">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="5f264-113">[Регистры-VS \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) перечисляет различные типы регистров, используемые вершиной шейдера ALU.</span><span class="sxs-lookup"><span data-stu-id="5f264-113">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="5f264-114">[Модификаторы регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers.md) используются для изменения способа работы инструкции.</span><span class="sxs-lookup"><span data-stu-id="5f264-114">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="5f264-115">[Модификаторы исходного регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="5f264-115">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="5f264-116">[Исходный регистр группирующие](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.</span><span class="sxs-lookup"><span data-stu-id="5f264-116">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="5f264-117">[Маскирование регистров назначения](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) определяет, какие компоненты записываются в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="5f264-117">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="5f264-118">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="5f264-118">New Features</span></span>

<span data-ttu-id="5f264-119">Ниже перечислены новые возможности.</span><span class="sxs-lookup"><span data-stu-id="5f264-119">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="5f264-120">Динамическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="5f264-120">Dynamic Flow Control</span></span>

<span data-ttu-id="5f264-121">Если [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, поддерживаются следующие инструкции динамического управления потоком:</span><span class="sxs-lookup"><span data-stu-id="5f264-121">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="5f264-122">Если \_ comp-VS</span><span class="sxs-lookup"><span data-stu-id="5f264-122">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="5f264-123">разделение и сравнение</span><span class="sxs-lookup"><span data-stu-id="5f264-123">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="5f264-124">прерывание \_ comp-VS</span><span class="sxs-lookup"><span data-stu-id="5f264-124">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="5f264-125">Если также задан параметр [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , поддерживаются следующие дополнительные инструкции по управлению потоком:</span><span class="sxs-lookup"><span data-stu-id="5f264-125">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="5f264-126">сетп \_ comp-VS</span><span class="sxs-lookup"><span data-stu-id="5f264-126">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="5f264-127">Если пред-VS</span><span class="sxs-lookup"><span data-stu-id="5f264-127">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="5f264-128">каллнз, пред. VS</span><span class="sxs-lookup"><span data-stu-id="5f264-128">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="5f264-129">бреакп — VS</span><span class="sxs-lookup"><span data-stu-id="5f264-129">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="5f264-130">Диапазон значений для глубины динамического управления потоком — от 0 до 24 и равен глубине вложения инструкций динамического управления потоком (Дополнительные сведения см. в разделе [ограничения вложений управления потоком](dx9-graphics-reference-asm-vs-instructions-flow-control.md) ).</span><span class="sxs-lookup"><span data-stu-id="5f264-130">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="5f264-131">Если это ограничение равно нулю, устройство не поддерживает инструкции динамического управления потоком.</span><span class="sxs-lookup"><span data-stu-id="5f264-131">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="5f264-132">Количество временных регистров</span><span class="sxs-lookup"><span data-stu-id="5f264-132">Number of Temporary Registers</span></span>

<span data-ttu-id="5f264-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) представляет количество [временных регистров](dx9-graphics-reference-asm-vs-registers-temporary.md), поддерживаемое устройством.</span><span class="sxs-lookup"><span data-stu-id="5f264-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="5f264-134">Диапазон значений для этого ограничения — от 12 до 32.</span><span class="sxs-lookup"><span data-stu-id="5f264-134">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="5f264-135">Глубина вложения статического управления потоком</span><span class="sxs-lookup"><span data-stu-id="5f264-135">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="5f264-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) представляет глубину вложенности двух типов статических инструкций по управлению потоком: [цикл-VS](loop---vs.md) / [-представитель](rep---vs.md) и [Call-VS](call---vs.md) / [каллнз bool-VS](callnz-bool---vs.md), / [Если логические действия-VS](if-bool---vs.md). циклы VS/представитель-VS, вложенные в D3DVS20CAPS.</span><span class="sxs-lookup"><span data-stu-id="5f264-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="5f264-137">По отдельности, инструкция Call-VS/каллнз bool-VS может быть вложена в D3DVS20CAPS глубину.</span><span class="sxs-lookup"><span data-stu-id="5f264-137">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="5f264-138">Если также задано D3DVS20CAPS, то [каллнз "пред-VS](callnz-pred---vs.md) " учитывает глубину вложения Call-VS/каллнз bool-VS/if bool-VS (см. Дополнительные сведения об [ограничениях вложения управления потоком](dx9-graphics-reference-asm-vs-instructions-flow-control.md) ).</span><span class="sxs-lookup"><span data-stu-id="5f264-138">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="5f264-139">Предикация</span><span class="sxs-lookup"><span data-stu-id="5f264-139">Predication</span></span>

<span data-ttu-id="5f264-140">Если задано [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) , устройство поддерживает [сетп \_ comp-VS](setp-comp---vs.md) и инструкцию затенения.</span><span class="sxs-lookup"><span data-stu-id="5f264-140">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="5f264-141">Если D3DVS20CAPS также больше 0, поддерживаются следующие дополнительные инструкции динамического управления потоком:</span><span class="sxs-lookup"><span data-stu-id="5f264-141">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="5f264-142">Если пред-VS</span><span class="sxs-lookup"><span data-stu-id="5f264-142">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="5f264-143">каллнз, пред. VS</span><span class="sxs-lookup"><span data-stu-id="5f264-143">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="5f264-144">бреакп — VS</span><span class="sxs-lookup"><span data-stu-id="5f264-144">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="5f264-145">Число инструкций</span><span class="sxs-lookup"><span data-stu-id="5f264-145">Instruction Count</span></span>

<span data-ttu-id="5f264-146">Каждый шейдер вершин может содержать до 256 инструкций.</span><span class="sxs-lookup"><span data-stu-id="5f264-146">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="5f264-147">Количество выполняемых инструкций может быть намного выше (из-за поддержки цикла/представителя) и ограничено [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), которое должно быть не менее 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="5f264-147">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f264-148">См. также</span><span class="sxs-lookup"><span data-stu-id="5f264-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f264-149">Шейдеры вершин</span><span class="sxs-lookup"><span data-stu-id="5f264-149">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 