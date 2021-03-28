---
title: ps_2_0
description: Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983613"
---
# <a name="ps_2_0"></a><span data-ttu-id="dc275-105">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dc275-105">ps\_2\_0</span></span>

<span data-ttu-id="dc275-106">Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей.</span><span class="sxs-lookup"><span data-stu-id="dc275-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="dc275-107">Регистрирует перенос данных в ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="dc275-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="dc275-108">Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.</span><span class="sxs-lookup"><span data-stu-id="dc275-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="dc275-109">[инструкции по PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) содержат список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="dc275-109">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="dc275-110">[в \_ \_ регистрах PS 2 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) перечислены различные типы регистров, используемые вершиной шейдера ALU.</span><span class="sxs-lookup"><span data-stu-id="dc275-110">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="dc275-111">[Модификаторы](dx9-graphics-reference-asm-ps-registers-modifiers.md) Используются для изменения способа работы инструкции.</span><span class="sxs-lookup"><span data-stu-id="dc275-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="dc275-112">[Маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) определяет, какие компоненты записываются в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="dc275-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="dc275-113">[Модификаторы исходного регистра Pixel Shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="dc275-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="dc275-114">[Исходный регистр группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.</span><span class="sxs-lookup"><span data-stu-id="dc275-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="dc275-115">Число инструкций</span><span class="sxs-lookup"><span data-stu-id="dc275-115">Instruction Count</span></span>

<span data-ttu-id="dc275-116">Шейдеры имеют ограничения для максимального числа инструкций.</span><span class="sxs-lookup"><span data-stu-id="dc275-116">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="dc275-117">Общее число слотов инструкций: 96 (арифметические действия 64 и текстура 32).</span><span class="sxs-lookup"><span data-stu-id="dc275-117">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="dc275-118">Число образцов</span><span class="sxs-lookup"><span data-stu-id="dc275-118">Sampler Count</span></span>

<span data-ttu-id="dc275-119">Число доступных образцов для пробных текстур равно 16.</span><span class="sxs-lookup"><span data-stu-id="dc275-119">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc275-120">См. также</span><span class="sxs-lookup"><span data-stu-id="dc275-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc275-121">Шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="dc275-121">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




