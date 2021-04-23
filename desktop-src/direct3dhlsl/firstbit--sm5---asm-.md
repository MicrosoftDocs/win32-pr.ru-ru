---
title: фирстбит (SM5-ASM)
description: Находит первый бит, заданный в числе, из ЛСБ или из самого начала.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335624"
---
# <a name="firstbit-sm5---asm"></a><span data-ttu-id="5c89a-103">фирстбит (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5c89a-103">firstbit (sm5 - asm)</span></span>

<span data-ttu-id="5c89a-104">Находит первый бит, заданный в числе, из ЛСБ или из самого начала.</span><span class="sxs-lookup"><span data-stu-id="5c89a-104">Finds the first bit set in a number, either from LSB or MSB.</span></span>



| <span data-ttu-id="5c89a-105">фирстбит { \_ Привет </span><span class="sxs-lookup"><span data-stu-id="5c89a-105">firstbit{\_hi</span></span>\|<span data-ttu-id="5c89a-106">\_Lo</span><span class="sxs-lookup"><span data-stu-id="5c89a-106">\_lo\</span></span>|<span data-ttu-id="5c89a-107">\_Ши} dest \[ . Mask \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="5c89a-107">\_shi} dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="5c89a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="5c89a-108">Item</span></span>                                                            | <span data-ttu-id="5c89a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5c89a-109">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c89a-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5c89a-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5c89a-111">\[в \] целочисленном положении первого бита в *src0* , начиная с ЛСБ для фирстбит в \_ фирстбит \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="5c89a-111">\[in\] The integer position of the first bit set in *src0* starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span><br/> |
| <span data-ttu-id="5c89a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5c89a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5c89a-113">\[во \] входном целочисленном параметре.</span><span class="sxs-lookup"><span data-stu-id="5c89a-113">\[in\] The input integer.</span></span><br/>                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="5c89a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c89a-114">Remarks</span></span>

<span data-ttu-id="5c89a-115">Эта операция возвращает целочисленное значение первого бита, заданного в 32-разрядном входном параметре, начиная с ЛСБ для фирстбит \_ или для фирстбит \_ Hi.</span><span class="sxs-lookup"><span data-stu-id="5c89a-115">This operation returns the integer position of the first bit set in the 32-bit input starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span> <span data-ttu-id="5c89a-116">Например, фирстбит \_ в 0x00000001 возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="5c89a-116">For example firstbit\_lo on 0x00000001 returns 0.</span></span> <span data-ttu-id="5c89a-117">фирстбит \_ Hi on 0x10000000 возвращает значение 3.</span><span class="sxs-lookup"><span data-stu-id="5c89a-117">firstbit\_hi on 0x10000000 returns 3.</span></span>

<span data-ttu-id="5c89a-118">фирстбит \_ Ши (s for со знаком) возвращает первый 0 из нуля, если число отрицательное; в противном случае возвращается первый 1 из самого старшего.</span><span class="sxs-lookup"><span data-stu-id="5c89a-118">firstbit\_shi (s for signed) returns the first 0 from the MSB if the number is negative; otherwise it returns the first 1 from the MSB.</span></span>

<span data-ttu-id="5c89a-119">Все варианты инструкции возвращают ~ 0 (0xFFFFFFFF в 32-разрядном регистре), если совпадений не найдено.</span><span class="sxs-lookup"><span data-stu-id="5c89a-119">All variants of the instruction return ~0 (0xffffffff in 32-bit register) if no match is found.</span></span>

<span data-ttu-id="5c89a-120">Используйте эту инструкцию, чтобы быстро перечислить биты набора битов или найти максимальную степень числа 2 в числе.</span><span class="sxs-lookup"><span data-stu-id="5c89a-120">Use this instruction to quickly enumerate set bits in a bitfield, or find the largest power of 2 in a number.</span></span>

<span data-ttu-id="5c89a-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="5c89a-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5c89a-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="5c89a-122">Vertex</span></span> | <span data-ttu-id="5c89a-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5c89a-123">Hull</span></span> | <span data-ttu-id="5c89a-124">Домен</span><span class="sxs-lookup"><span data-stu-id="5c89a-124">Domain</span></span> | <span data-ttu-id="5c89a-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5c89a-125">Geometry</span></span> | <span data-ttu-id="5c89a-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5c89a-126">Pixel</span></span> | <span data-ttu-id="5c89a-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5c89a-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5c89a-128">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-128">X</span></span>      | <span data-ttu-id="5c89a-129">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-129">X</span></span>    | <span data-ttu-id="5c89a-130">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-130">X</span></span>      | <span data-ttu-id="5c89a-131">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-131">X</span></span>        | <span data-ttu-id="5c89a-132">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-132">X</span></span>     | <span data-ttu-id="5c89a-133">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-133">X</span></span>       |



 

## <a name="mimimum-shader-model"></a><span data-ttu-id="5c89a-134">Модель шейдера минимальный</span><span class="sxs-lookup"><span data-stu-id="5c89a-134">Mimimum Shader Model</span></span>

<span data-ttu-id="5c89a-135">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5c89a-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5c89a-136">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5c89a-136">Shader Model</span></span>                                              | <span data-ttu-id="5c89a-137">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="5c89a-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5c89a-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5c89a-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5c89a-139">да</span><span class="sxs-lookup"><span data-stu-id="5c89a-139">yes</span></span>       |
| [<span data-ttu-id="5c89a-140">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="5c89a-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5c89a-141">Нет</span><span class="sxs-lookup"><span data-stu-id="5c89a-141">no</span></span>        |
| [<span data-ttu-id="5c89a-142">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="5c89a-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5c89a-143">Нет</span><span class="sxs-lookup"><span data-stu-id="5c89a-143">no</span></span>        |
| [<span data-ttu-id="5c89a-144">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c89a-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5c89a-145">Нет</span><span class="sxs-lookup"><span data-stu-id="5c89a-145">no</span></span>        |
| [<span data-ttu-id="5c89a-146">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c89a-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5c89a-147">Нет</span><span class="sxs-lookup"><span data-stu-id="5c89a-147">no</span></span>        |
| [<span data-ttu-id="5c89a-148">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c89a-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5c89a-149">Нет</span><span class="sxs-lookup"><span data-stu-id="5c89a-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5c89a-150">См. также</span><span class="sxs-lookup"><span data-stu-id="5c89a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c89a-151">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c89a-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





