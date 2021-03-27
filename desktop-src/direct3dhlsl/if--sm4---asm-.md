---
title: If (SM4-ASM)
description: Ветвь на основе логического или результата.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996850"
---
# <a name="if-sm4---asm"></a><span data-ttu-id="8e164-103">If (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8e164-103">if (sm4 - asm)</span></span>

<span data-ttu-id="8e164-104">Ветвь на основе логического или результата.</span><span class="sxs-lookup"><span data-stu-id="8e164-104">Branch based on logical OR result.</span></span>



| <span data-ttu-id="8e164-105">If { \_ z </span><span class="sxs-lookup"><span data-stu-id="8e164-105">if{\_z</span></span>\|<span data-ttu-id="8e164-106">\_NZ} src0. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="8e164-106">\_nz} src0.select\_component</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="8e164-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="8e164-107">Item</span></span>                                                            | <span data-ttu-id="8e164-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8e164-108">Description</span></span>                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="8e164-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8e164-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8e164-110">\[в \] содержит компонент, для которого необходимо проверить условие.</span><span class="sxs-lookup"><span data-stu-id="8e164-110">\[in\] Contains the component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e164-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="8e164-111">Remarks</span></span>

<span data-ttu-id="8e164-112">Формат токена содержит смещение соответствующей инструкции endif в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="8e164-112">The token format contains the offset of the corresponding endif instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="8e164-113">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="8e164-113">The following example shows how to use this instruction.</span></span>

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a><span data-ttu-id="8e164-114">Ограничения</span><span class="sxs-lookup"><span data-stu-id="8e164-114">Restrictions</span></span>

-   <span data-ttu-id="8e164-115">Исходные операнды (если 4 вектора компонентов) должны использовать один селектор компонента.</span><span class="sxs-lookup"><span data-stu-id="8e164-115">The source operands (if 4 component vectors) must use a single component selector.</span></span>
-   <span data-ttu-id="8e164-116">32-разрядный регистр, предоставляемый *src0* , тестируется на битовом уровне.</span><span class="sxs-lookup"><span data-stu-id="8e164-116">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="8e164-117">Если любой бит не равен нулю, **Если \_ z** будет иметь значение true.</span><span class="sxs-lookup"><span data-stu-id="8e164-117">If any bit is nonzero, **if\_z** will be true.</span></span> <span data-ttu-id="8e164-118">Значение, если все биты равны нулю, **Если \_ NZ** будет иметь значение true.</span><span class="sxs-lookup"><span data-stu-id="8e164-118">If all bits are zero, **if\_nz** will be true.</span></span>
-   <span data-ttu-id="8e164-119">Блоки управления потоком могут вкладывать до 64 глубины в одну подпрограммы (и главную).</span><span class="sxs-lookup"><span data-stu-id="8e164-119">Flow control blocks can nest up to 64 deep per subroutine (and main).</span></span> <span data-ttu-id="8e164-120">Компилятор HLSL не будет создавать подпрограммы, превышающие это ограничение.</span><span class="sxs-lookup"><span data-stu-id="8e164-120">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="8e164-121">Поведение инструкций потока управления свыше 64 уровней в глубину (по подподпрограмме) не определено.</span><span class="sxs-lookup"><span data-stu-id="8e164-121">Behavior of control flow instructions beyond 64 levels deep (per subroutine) is undefined.</span></span>

<span data-ttu-id="8e164-122">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8e164-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8e164-123">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="8e164-123">Vertex Shader</span></span> | <span data-ttu-id="8e164-124">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="8e164-124">Geometry Shader</span></span> | <span data-ttu-id="8e164-125">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="8e164-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8e164-126">x</span><span class="sxs-lookup"><span data-stu-id="8e164-126">x</span></span>             | <span data-ttu-id="8e164-127">x</span><span class="sxs-lookup"><span data-stu-id="8e164-127">x</span></span>               | <span data-ttu-id="8e164-128">x</span><span class="sxs-lookup"><span data-stu-id="8e164-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8e164-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8e164-129">Minimum Shader Model</span></span>

<span data-ttu-id="8e164-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8e164-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8e164-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8e164-131">Shader Model</span></span>                                              | <span data-ttu-id="8e164-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8e164-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8e164-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8e164-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8e164-134">да</span><span class="sxs-lookup"><span data-stu-id="8e164-134">yes</span></span>       |
| [<span data-ttu-id="8e164-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8e164-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8e164-136">да</span><span class="sxs-lookup"><span data-stu-id="8e164-136">yes</span></span>       |
| [<span data-ttu-id="8e164-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8e164-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8e164-138">да</span><span class="sxs-lookup"><span data-stu-id="8e164-138">yes</span></span>       |
| [<span data-ttu-id="8e164-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e164-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8e164-140">Нет</span><span class="sxs-lookup"><span data-stu-id="8e164-140">no</span></span>        |
| [<span data-ttu-id="8e164-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e164-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8e164-142">Нет</span><span class="sxs-lookup"><span data-stu-id="8e164-142">no</span></span>        |
| [<span data-ttu-id="8e164-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e164-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8e164-144">Нет</span><span class="sxs-lookup"><span data-stu-id="8e164-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8e164-145">См. также</span><span class="sxs-lookup"><span data-stu-id="8e164-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e164-146">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e164-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





