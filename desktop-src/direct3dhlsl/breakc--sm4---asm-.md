---
title: бреакк (SM4-ASM)
description: Условно перемещает точку выполнения в инструкцию после следующей ендлуп или ендсвитч.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412191"
---
# <a name="breakc-sm4---asm"></a><span data-ttu-id="f49db-103">бреакк (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f49db-103">breakc (sm4 - asm)</span></span>

<span data-ttu-id="f49db-104">Условно перемещает точку выполнения в инструкцию после следующей [ендлуп](endloop--sm4---asm-.md) или [ендсвитч](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="f49db-104">Conditionally moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="f49db-105">бреакк { \_ z </span><span class="sxs-lookup"><span data-stu-id="f49db-105">breakc{\_z</span></span>\|<span data-ttu-id="f49db-106">\_NZ} src0. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="f49db-106">\_nz} src0.select\_component</span></span> |
|------------------------------------------|



 



| <span data-ttu-id="f49db-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="f49db-107">Item</span></span>                                                            | <span data-ttu-id="f49db-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f49db-108">Description</span></span>                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f49db-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f49db-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f49db-110">\[в \] компоненте, для которого необходимо проверить условие.</span><span class="sxs-lookup"><span data-stu-id="f49db-110">\[in\] The component on which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f49db-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="f49db-111">Remarks</span></span>

<span data-ttu-id="f49db-112">Формат маркера содержит смещение соответствующей инструкции **ендлуп** в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="f49db-112">The token format contains the offset of the corresponding **endloop** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="f49db-113">В следующем примере показана инструкция **бреакк** .</span><span class="sxs-lookup"><span data-stu-id="f49db-113">The following example shows the **breakc** instruction.</span></span>


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



<span data-ttu-id="f49db-114">Эта инструкция должна находиться в **цикле** / **ендлуп** или **switch** / **ендсвитч**.</span><span class="sxs-lookup"><span data-stu-id="f49db-114">This instruction must appear within a **loop**/**endloop** or **switch**/**endswitch**.</span></span>

<span data-ttu-id="f49db-115">32-разрядный регистр, предоставляемый *src0* , тестируется на битовом уровне.</span><span class="sxs-lookup"><span data-stu-id="f49db-115">The 32-bit register supplied by *src0* is tested at a bit level.</span></span> <span data-ttu-id="f49db-116">Если любой бит не равен нулю, **бреакк \_ NZ** выполняет перерыв.</span><span class="sxs-lookup"><span data-stu-id="f49db-116">If any bit is nonzero, **breakc\_nz** will perform the break.</span></span> <span data-ttu-id="f49db-117">Если все биты равны нулю, **бреакк \_ z** будет выполнять перерыв.</span><span class="sxs-lookup"><span data-stu-id="f49db-117">If all bits are zero, **breakc\_z** will perform the break.</span></span>

<span data-ttu-id="f49db-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="f49db-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f49db-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="f49db-119">Vertex Shader</span></span> | <span data-ttu-id="f49db-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="f49db-120">Geometry Shader</span></span> | <span data-ttu-id="f49db-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="f49db-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f49db-122">x</span><span class="sxs-lookup"><span data-stu-id="f49db-122">x</span></span>             | <span data-ttu-id="f49db-123">x</span><span class="sxs-lookup"><span data-stu-id="f49db-123">x</span></span>               | <span data-ttu-id="f49db-124">x</span><span class="sxs-lookup"><span data-stu-id="f49db-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f49db-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f49db-125">Minimum Shader Model</span></span>

<span data-ttu-id="f49db-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f49db-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f49db-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f49db-127">Shader Model</span></span>                                              | <span data-ttu-id="f49db-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f49db-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f49db-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f49db-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f49db-130">да</span><span class="sxs-lookup"><span data-stu-id="f49db-130">yes</span></span>       |
| [<span data-ttu-id="f49db-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="f49db-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f49db-132">да</span><span class="sxs-lookup"><span data-stu-id="f49db-132">yes</span></span>       |
| [<span data-ttu-id="f49db-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f49db-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f49db-134">да</span><span class="sxs-lookup"><span data-stu-id="f49db-134">yes</span></span>       |
| [<span data-ttu-id="f49db-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f49db-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f49db-136">Нет</span><span class="sxs-lookup"><span data-stu-id="f49db-136">no</span></span>        |
| [<span data-ttu-id="f49db-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f49db-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f49db-138">Нет</span><span class="sxs-lookup"><span data-stu-id="f49db-138">no</span></span>        |
| [<span data-ttu-id="f49db-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f49db-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f49db-140">Нет</span><span class="sxs-lookup"><span data-stu-id="f49db-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f49db-141">См. также</span><span class="sxs-lookup"><span data-stu-id="f49db-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f49db-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f49db-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





