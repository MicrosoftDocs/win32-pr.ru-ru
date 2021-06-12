---
title: vs_2_0
description: Сведения о vs_2_0, программируемом шейдере вершин, который состоит из набора инструкций, которые работают с данными вершин.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010857"
---
# <a name="vs_2_0"></a><span data-ttu-id="77398-103">VS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="77398-103">vs\_2\_0</span></span>

<span data-ttu-id="77398-104">Программируемый шейдер вершин состоит из набора инструкций, которые работают с данными вершин.</span><span class="sxs-lookup"><span data-stu-id="77398-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="77398-105">Регистрирует перенос данных в ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="77398-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="77398-106">Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.</span><span class="sxs-lookup"><span data-stu-id="77398-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="77398-107">[Инструкции — VS \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) содержит список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="77398-107">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="77398-108">[Регистры — VS \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) содержит различные типы регистров, используемые вершиной шейдера ALU.</span><span class="sxs-lookup"><span data-stu-id="77398-108">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="77398-109">[Модификаторы регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers.md) используются для изменения способа работы инструкции.</span><span class="sxs-lookup"><span data-stu-id="77398-109">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="77398-110">[Модификаторы исходного регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="77398-110">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="77398-111">[Исходный регистр группирующие](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.</span><span class="sxs-lookup"><span data-stu-id="77398-111">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="77398-112">[Маскирование регистров назначения](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) определяет, какие компоненты записываются в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="77398-112">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="77398-113">Число инструкций</span><span class="sxs-lookup"><span data-stu-id="77398-113">Instruction Count</span></span>

<span data-ttu-id="77398-114">Каждый шейдер вершин может содержать до 256 инструкций.</span><span class="sxs-lookup"><span data-stu-id="77398-114">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="77398-115">Количество выполняемых инструкций может быть намного выше (из-за поддержки цикла или представителя) и ограничено D3DCAPS9. Максвшадеринструктионсексекутед, который должен быть не менее 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="77398-115">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77398-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="77398-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77398-117">Шейдеры вершин</span><span class="sxs-lookup"><span data-stu-id="77398-117">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




