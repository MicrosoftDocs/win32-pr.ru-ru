---
title: ps_2_x
description: Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13e5daf7c3a4b41e5b27b1c20f8b1f5f8355c325
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997119"
---
# <a name="ps_2_x"></a><span data-ttu-id="8a0a9-105">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8a0a9-105">ps\_2\_x</span></span>

<span data-ttu-id="8a0a9-106">Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="8a0a9-107">Регистрирует перенос данных в ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="8a0a9-108">Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="8a0a9-109">[инструкции по PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) содержат список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-109">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="8a0a9-110">[в \_ \_ регистрах PS 2 x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) перечислены различные типы регистров, используемые вершиной шейдера ALU.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-110">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="8a0a9-111">[Модификаторы](dx9-graphics-reference-asm-ps-registers-modifiers.md) Используются для изменения способа работы инструкции.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="8a0a9-112">[Маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) определяет, какие компоненты записываются в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="8a0a9-113">[Модификаторы исходного регистра Pixel Shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="8a0a9-114">[Исходный регистр группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="8a0a9-115">Динамическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="8a0a9-115">Dynamic Flow Control</span></span>

<span data-ttu-id="8a0a9-116">[**Динамикфловконтролдепс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) представляет глубину вложения динамических инструкций по управлению потоком: [Если](if-bool---ps.md), если задано [значение \_](if-pred---ps.md) [, if, \_](if-comp---ps.md)то if [-PS](break---ps.md)или [break- \_ PS](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="8a0a9-116">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="8a0a9-117">Значение равно глубине вложения \_ блока if.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-117">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="8a0a9-118">Если это ограничение равно нулю, устройство не поддерживает инструкции динамического управления потоком.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-118">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="8a0a9-119">Количество временных регистров</span><span class="sxs-lookup"><span data-stu-id="8a0a9-119">Number of Temporary Registers</span></span>

<span data-ttu-id="8a0a9-120">Количество временных регистров, поддерживаемое устройством.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-120">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="8a0a9-121">Диапазон — от 12 до 32.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-121">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="8a0a9-122">Глубина вложения статического управления потоком</span><span class="sxs-lookup"><span data-stu-id="8a0a9-122">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="8a0a9-123">[**Статикфловконтролдепс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) представляет глубину вложения двух типов статических инструкций по управлению потоком: « [цикл](loop---ps.md)  / [](rep---ps.md) » и « [вызов](call---ps.md)  / [каллнз](callnz-bool---ps.md)».</span><span class="sxs-lookup"><span data-stu-id="8a0a9-123">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="8a0a9-124">инструкции цикла/REP могут быть вложены до **статикфловконтролдепс** Deep.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-124">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="8a0a9-125">По отдельности, инструкции Call/каллнз можно вложить в **статикфловконтролдепс** глубину.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-125">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="8a0a9-126">Число слотов инструкций</span><span class="sxs-lookup"><span data-stu-id="8a0a9-126">Number of Instruction Slots</span></span>

<span data-ttu-id="8a0a9-127">Число слотов инструкций может варьироваться от 96 до 512 и задается параметром [**макспикселшадеринструктионслотс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span><span class="sxs-lookup"><span data-stu-id="8a0a9-127">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="8a0a9-128">Общее число инструкций, которые могут выполняться, определяется **макспикселшадеринструктионсексекутед**.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-128">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="8a0a9-129">Это значение может быть больше, чем количество слотов инструкций из-за вызовов циклов и подпрограмм.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-129">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="8a0a9-130">Произвольный Свиззле</span><span class="sxs-lookup"><span data-stu-id="8a0a9-130">Arbitrary Swizzle</span></span>

<span data-ttu-id="8a0a9-131">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ арбитрарисвиззле**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , то поддерживается произвольный свиззле.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-131">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="8a0a9-132">См. раздел [Source Register группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="8a0a9-132">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="8a0a9-133">Инструкции по градиенту</span><span class="sxs-lookup"><span data-stu-id="8a0a9-133">Gradient Instructions</span></span>

<span data-ttu-id="8a0a9-134">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , то поддерживаются инструкции градиента.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-134">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="8a0a9-135">См. раздел [ДСКС-PS](dsx---ps.md), [ДСИ-PS](dsy---ps.md)и [текслдд-PS](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="8a0a9-135">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="8a0a9-136">Предикация</span><span class="sxs-lookup"><span data-stu-id="8a0a9-136">Predication</span></span>

<span data-ttu-id="8a0a9-137">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ затенения**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , инструкция затенения поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-137">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="8a0a9-138">См. раздел [Регистрация предиката](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="8a0a9-138">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="8a0a9-139">Зависимое ограничение чтения</span><span class="sxs-lookup"><span data-stu-id="8a0a9-139">Dependent Read Limit</span></span>

<span data-ttu-id="8a0a9-140">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ нодепендентреадлимит**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , зависимые ограничения чтения отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-140">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="8a0a9-141">Предел для инструкции текстуры</span><span class="sxs-lookup"><span data-stu-id="8a0a9-141">Texture Instruction Limit</span></span>

<span data-ttu-id="8a0a9-142">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ нотексинструктионлимит**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , инструкции по текстуре не превышены.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-142">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="8a0a9-143">Число образцов</span><span class="sxs-lookup"><span data-stu-id="8a0a9-143">Sampler Count</span></span>

<span data-ttu-id="8a0a9-144">Число доступных образцов для пробных текстур равно 16.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-144">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a0a9-145">См. также</span><span class="sxs-lookup"><span data-stu-id="8a0a9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a0a9-146">Шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="8a0a9-146">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 