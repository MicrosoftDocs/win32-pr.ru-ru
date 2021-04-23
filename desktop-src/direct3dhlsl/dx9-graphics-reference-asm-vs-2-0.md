---
title: vs_2_0
description: Программируемый шейдер вершин состоит из набора инструкций, которые работают с данными вершин. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983733"
---
# <a name="vs_2_0"></a><span data-ttu-id="22930-105">VS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="22930-105">vs\_2\_0</span></span>

<span data-ttu-id="22930-106">Программируемый шейдер вершин состоит из набора инструкций, которые работают с данными вершин.</span><span class="sxs-lookup"><span data-stu-id="22930-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="22930-107">Регистрирует перенос данных в ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="22930-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="22930-108">Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.</span><span class="sxs-lookup"><span data-stu-id="22930-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="22930-109">[Инструкции — VS \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) содержит список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="22930-109">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="22930-110">[Регистры — VS \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) содержит различные типы регистров, используемые вершиной шейдера ALU.</span><span class="sxs-lookup"><span data-stu-id="22930-110">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="22930-111">[Модификаторы регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers.md) используются для изменения способа работы инструкции.</span><span class="sxs-lookup"><span data-stu-id="22930-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="22930-112">[Модификаторы исходного регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="22930-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="22930-113">[Исходный регистр группирующие](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.</span><span class="sxs-lookup"><span data-stu-id="22930-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="22930-114">[Маскирование регистров назначения](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) определяет, какие компоненты записываются в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="22930-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="22930-115">Число инструкций</span><span class="sxs-lookup"><span data-stu-id="22930-115">Instruction Count</span></span>

<span data-ttu-id="22930-116">Каждый шейдер вершин может содержать до 256 инструкций.</span><span class="sxs-lookup"><span data-stu-id="22930-116">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="22930-117">Количество выполняемых инструкций может быть намного выше (из-за поддержки цикла или представителя) и ограничено D3DCAPS9. Максвшадеринструктионсексекутед, который должен быть не менее 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="22930-117">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22930-118">См. также</span><span class="sxs-lookup"><span data-stu-id="22930-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22930-119">Шейдеры вершин</span><span class="sxs-lookup"><span data-stu-id="22930-119">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




