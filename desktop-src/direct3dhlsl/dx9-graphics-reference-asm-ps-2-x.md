---
title: ps_2_x
description: Сведения о ps_2_x, программируемом шейдере пикселей, который состоит из набора инструкций, которые работают с данными пикселей.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010877"
---
# <a name="ps_2_x"></a><span data-ttu-id="2e7cc-103">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2e7cc-103">ps\_2\_x</span></span>

<span data-ttu-id="2e7cc-104">Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="2e7cc-105">Регистрирует перенос данных в ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="2e7cc-106">Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="2e7cc-107">[инструкции по PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) содержат список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-107">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="2e7cc-108">[в \_ \_ регистрах PS 2 x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) перечислены различные типы регистров, используемые вершиной шейдера ALU.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-108">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="2e7cc-109">[Модификаторы](dx9-graphics-reference-asm-ps-registers-modifiers.md) Используются для изменения способа работы инструкции.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="2e7cc-110">[Маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) определяет, какие компоненты записываются в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="2e7cc-111">[Модификаторы исходного регистра Pixel Shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="2e7cc-112">[Исходный регистр группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="2e7cc-113">Динамическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="2e7cc-113">Dynamic Flow Control</span></span>

<span data-ttu-id="2e7cc-114">[**Динамикфловконтролдепс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) представляет глубину вложения динамических инструкций по управлению потоком: [Если](if-bool---ps.md), если задано [значение \_](if-pred---ps.md) [, if, \_](if-comp---ps.md)то if [-PS](break---ps.md)или [break- \_ PS](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="2e7cc-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="2e7cc-115">Значение равно глубине вложения \_ блока if.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-115">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="2e7cc-116">Если это ограничение равно нулю, устройство не поддерживает инструкции динамического управления потоком.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-116">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="2e7cc-117">Количество временных регистров</span><span class="sxs-lookup"><span data-stu-id="2e7cc-117">Number of Temporary Registers</span></span>

<span data-ttu-id="2e7cc-118">Количество временных регистров, поддерживаемое устройством.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-118">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="2e7cc-119">Диапазон — от 12 до 32.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-119">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="2e7cc-120">Глубина вложения статического управления потоком</span><span class="sxs-lookup"><span data-stu-id="2e7cc-120">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="2e7cc-121">[**Статикфловконтролдепс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) представляет глубину вложения двух типов статических инструкций по управлению потоком: « [цикл](loop---ps.md)  / [](rep---ps.md) » и « [вызов](call---ps.md)  / [каллнз](callnz-bool---ps.md)».</span><span class="sxs-lookup"><span data-stu-id="2e7cc-121">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="2e7cc-122">инструкции цикла/REP могут быть вложены до **статикфловконтролдепс** Deep.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-122">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="2e7cc-123">По отдельности, инструкции Call/каллнз можно вложить в **статикфловконтролдепс** глубину.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-123">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="2e7cc-124">Число слотов инструкций</span><span class="sxs-lookup"><span data-stu-id="2e7cc-124">Number of Instruction Slots</span></span>

<span data-ttu-id="2e7cc-125">Число слотов инструкций может варьироваться от 96 до 512 и задается параметром [**макспикселшадеринструктионслотс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span><span class="sxs-lookup"><span data-stu-id="2e7cc-125">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="2e7cc-126">Общее число инструкций, которые могут выполняться, определяется **макспикселшадеринструктионсексекутед**.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-126">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="2e7cc-127">Это значение может быть больше, чем количество слотов инструкций из-за вызовов циклов и подпрограмм.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-127">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="2e7cc-128">Произвольный Свиззле</span><span class="sxs-lookup"><span data-stu-id="2e7cc-128">Arbitrary Swizzle</span></span>

<span data-ttu-id="2e7cc-129">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ арбитрарисвиззле**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , то поддерживается произвольный свиззле.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-129">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="2e7cc-130">См. раздел [Source Register группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="2e7cc-130">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="2e7cc-131">Инструкции по градиенту</span><span class="sxs-lookup"><span data-stu-id="2e7cc-131">Gradient Instructions</span></span>

<span data-ttu-id="2e7cc-132">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , то поддерживаются инструкции градиента.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-132">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="2e7cc-133">См. раздел [ДСКС-PS](dsx---ps.md), [ДСИ-PS](dsy---ps.md)и [текслдд-PS](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="2e7cc-133">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="2e7cc-134">Предикация</span><span class="sxs-lookup"><span data-stu-id="2e7cc-134">Predication</span></span>

<span data-ttu-id="2e7cc-135">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ затенения**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , инструкция затенения поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-135">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="2e7cc-136">См. раздел [Регистрация предиката](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="2e7cc-136">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="2e7cc-137">Зависимое ограничение чтения</span><span class="sxs-lookup"><span data-stu-id="2e7cc-137">Dependent Read Limit</span></span>

<span data-ttu-id="2e7cc-138">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ нодепендентреадлимит**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , зависимые ограничения чтения отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-138">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="2e7cc-139">Предел для инструкции текстуры</span><span class="sxs-lookup"><span data-stu-id="2e7cc-139">Texture Instruction Limit</span></span>

<span data-ttu-id="2e7cc-140">Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ нотексинструктионлимит**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , инструкции по текстуре не превышены.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-140">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="2e7cc-141">Число образцов</span><span class="sxs-lookup"><span data-stu-id="2e7cc-141">Sampler Count</span></span>

<span data-ttu-id="2e7cc-142">Число доступных образцов для пробных текстур равно 16.</span><span class="sxs-lookup"><span data-stu-id="2e7cc-142">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e7cc-143">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2e7cc-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e7cc-144">Шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="2e7cc-144">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 