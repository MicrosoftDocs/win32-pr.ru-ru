---
title: ретк (SM4-ASM)
description: Условное возвращение.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983881"
---
# <a name="retc-sm4---asm"></a><span data-ttu-id="c4cd3-103">ретк (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c4cd3-103">retc (sm4 - asm)</span></span>

<span data-ttu-id="c4cd3-104">Условное возвращение.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-104">Conditional return.</span></span>



| <span data-ttu-id="c4cd3-105">ретк { \_ z </span><span class="sxs-lookup"><span data-stu-id="c4cd3-105">retc{\_z</span></span>\|<span data-ttu-id="c4cd3-106">\_NZ} src0. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="c4cd3-106">\_nz} src0.select\_component</span></span> |
|----------------------------------------|



 



| <span data-ttu-id="c4cd3-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="c4cd3-107">Item</span></span>                                                            | <span data-ttu-id="c4cd3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c4cd3-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c4cd3-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c4cd3-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c4cd3-110">\[в \] регистре для проверки условия.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-110">\[in\] The register to test the condition against.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4cd3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4cd3-111">Remarks</span></span>

<span data-ttu-id="c4cd3-112">Если внутри подпрограммы эта инструкция возвращается к инструкции после вызова.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-112">If within a subroutine, this instruction conditionally returns to the instruction after the call.</span></span> <span data-ttu-id="c4cd3-113">Если не входит в подпрограмму, эта инструкция завершает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-113">If not inside a subroutine, this instruction terminates program execution.</span></span>

<span data-ttu-id="c4cd3-114">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-114">The following example shows how to use this instruction.</span></span>

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a><span data-ttu-id="c4cd3-115">Ограничения</span><span class="sxs-lookup"><span data-stu-id="c4cd3-115">Restrictions</span></span>

-   <span data-ttu-id="c4cd3-116">**ретк** может появляться в любом месте программы, любое количество раз.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-116">**retc** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="c4cd3-117">Последняя инструкция в основной программе или подпрограмме не может быть **ретк \_ z** или **ретк \_ NZ**.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-117">The last instruction in a main program or subroutine cannot be a **retc\_z** or **retc\_nz**.</span></span> <span data-ttu-id="c4cd3-118">Вместо этого можно использовать безусловное значение [RET](ret--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="c4cd3-118">Instead, the unconditional [ret](ret--sm4---asm-.md) can be used.</span></span>
-   <span data-ttu-id="c4cd3-119">32-разрядный регистр, предоставляемый *src0* , тестируется на битовом уровне.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-119">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="c4cd3-120">Если любой бит не равен нулю, Return **\_ NZ** возвратит.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-120">If any bit is nonzero, **ret\_nz** will return.</span></span> <span data-ttu-id="c4cd3-121">Если все биты равны нулю, **ретк \_ z** возвратит значение.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-121">If all bits are zero, **retc\_z** will return.</span></span>

<span data-ttu-id="c4cd3-122">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c4cd3-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c4cd3-123">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c4cd3-123">Vertex Shader</span></span> | <span data-ttu-id="c4cd3-124">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="c4cd3-124">Geometry Shader</span></span> | <span data-ttu-id="c4cd3-125">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c4cd3-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c4cd3-126">x</span><span class="sxs-lookup"><span data-stu-id="c4cd3-126">x</span></span>             | <span data-ttu-id="c4cd3-127">x</span><span class="sxs-lookup"><span data-stu-id="c4cd3-127">x</span></span>               | <span data-ttu-id="c4cd3-128">x</span><span class="sxs-lookup"><span data-stu-id="c4cd3-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c4cd3-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c4cd3-129">Minimum Shader Model</span></span>

<span data-ttu-id="c4cd3-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="c4cd3-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c4cd3-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c4cd3-131">Shader Model</span></span>                                              | <span data-ttu-id="c4cd3-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c4cd3-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c4cd3-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c4cd3-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c4cd3-134">да</span><span class="sxs-lookup"><span data-stu-id="c4cd3-134">yes</span></span>       |
| [<span data-ttu-id="c4cd3-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c4cd3-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c4cd3-136">да</span><span class="sxs-lookup"><span data-stu-id="c4cd3-136">yes</span></span>       |
| [<span data-ttu-id="c4cd3-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c4cd3-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c4cd3-138">да</span><span class="sxs-lookup"><span data-stu-id="c4cd3-138">yes</span></span>       |
| [<span data-ttu-id="c4cd3-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4cd3-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c4cd3-140">Нет</span><span class="sxs-lookup"><span data-stu-id="c4cd3-140">no</span></span>        |
| [<span data-ttu-id="c4cd3-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4cd3-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c4cd3-142">Нет</span><span class="sxs-lookup"><span data-stu-id="c4cd3-142">no</span></span>        |
| [<span data-ttu-id="c4cd3-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4cd3-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c4cd3-144">Нет</span><span class="sxs-lookup"><span data-stu-id="c4cd3-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c4cd3-145">См. также</span><span class="sxs-lookup"><span data-stu-id="c4cd3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4cd3-146">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4cd3-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





