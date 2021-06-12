---
title: ps_2_0
description: Сведения о ps_2_0, программируемом шейдере пикселей, который состоит из набора инструкций, которые работают с данными пикселей.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010987"
---
# <a name="ps_2_0"></a><span data-ttu-id="4b568-103">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b568-103">ps\_2\_0</span></span>

<span data-ttu-id="4b568-104">Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей.</span><span class="sxs-lookup"><span data-stu-id="4b568-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="4b568-105">Регистрирует перенос данных в ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="4b568-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="4b568-106">Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.</span><span class="sxs-lookup"><span data-stu-id="4b568-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="4b568-107">[инструкции по PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) содержат список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="4b568-107">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="4b568-108">[в \_ \_ регистрах PS 2 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) перечислены различные типы регистров, используемые вершиной шейдера ALU.</span><span class="sxs-lookup"><span data-stu-id="4b568-108">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="4b568-109">[Модификаторы](dx9-graphics-reference-asm-ps-registers-modifiers.md) Используются для изменения способа работы инструкции.</span><span class="sxs-lookup"><span data-stu-id="4b568-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="4b568-110">[Маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) определяет, какие компоненты записываются в реестре назначения.</span><span class="sxs-lookup"><span data-stu-id="4b568-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="4b568-111">[Модификаторы исходного регистра Pixel Shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="4b568-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="4b568-112">[Исходный регистр группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.</span><span class="sxs-lookup"><span data-stu-id="4b568-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="4b568-113">Число инструкций</span><span class="sxs-lookup"><span data-stu-id="4b568-113">Instruction Count</span></span>

<span data-ttu-id="4b568-114">Шейдеры имеют ограничения для максимального числа инструкций.</span><span class="sxs-lookup"><span data-stu-id="4b568-114">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="4b568-115">Общее число слотов инструкций: 96 (арифметические действия 64 и текстура 32).</span><span class="sxs-lookup"><span data-stu-id="4b568-115">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="4b568-116">Число образцов</span><span class="sxs-lookup"><span data-stu-id="4b568-116">Sampler Count</span></span>

<span data-ttu-id="4b568-117">Число доступных образцов для пробных текстур равно 16.</span><span class="sxs-lookup"><span data-stu-id="4b568-117">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b568-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4b568-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b568-119">Шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="4b568-119">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




