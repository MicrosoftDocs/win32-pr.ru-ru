---
title: континуек (SM4-ASM)
description: Условно продолжение выполнения в начале текущего цикла.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983844"
---
# <a name="continuec-sm4---asm"></a><span data-ttu-id="9fff9-103">континуек (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9fff9-103">continuec (sm4 - asm)</span></span>

<span data-ttu-id="9fff9-104">Условно продолжение выполнения в начале текущего цикла.</span><span class="sxs-lookup"><span data-stu-id="9fff9-104">Conditionally continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="9fff9-105">континуек { \_ z </span><span class="sxs-lookup"><span data-stu-id="9fff9-105">continuec{\_z</span></span>\|<span data-ttu-id="9fff9-106">\_NZ} src0. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="9fff9-106">\_nz} src0.select\_component</span></span> |
|---------------------------------------------|



 



| <span data-ttu-id="9fff9-107">Термин</span><span class="sxs-lookup"><span data-stu-id="9fff9-107">Term</span></span>                                                            | <span data-ttu-id="9fff9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9fff9-108">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="9fff9-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9fff9-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9fff9-110">\[в \] компоненте, для которого необходимо проверить условие.</span><span class="sxs-lookup"><span data-stu-id="9fff9-110">\[in\] The component against which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9fff9-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="9fff9-111">Remarks</span></span>

<span data-ttu-id="9fff9-112">**континуек** можно использовать только внутри [цикла](loop--sm4---asm-.md) или [ендлуп](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="9fff9-112">**continuec** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="9fff9-113">В следующем примере показано, как использовать инструкцию **континуек** .</span><span class="sxs-lookup"><span data-stu-id="9fff9-113">The following example shows how to use the **continuec** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



<span data-ttu-id="9fff9-114">Формат маркера содержит смещение соответствующей инструкции Loop в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="9fff9-114">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="9fff9-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="9fff9-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9fff9-116">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="9fff9-116">Vertex Shader</span></span> | <span data-ttu-id="9fff9-117">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="9fff9-117">Geometry Shader</span></span> | <span data-ttu-id="9fff9-118">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="9fff9-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9fff9-119">x</span><span class="sxs-lookup"><span data-stu-id="9fff9-119">x</span></span>             | <span data-ttu-id="9fff9-120">x</span><span class="sxs-lookup"><span data-stu-id="9fff9-120">x</span></span>               | <span data-ttu-id="9fff9-121">x</span><span class="sxs-lookup"><span data-stu-id="9fff9-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9fff9-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9fff9-122">Minimum Shader Model</span></span>

<span data-ttu-id="9fff9-123">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="9fff9-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9fff9-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9fff9-124">Shader Model</span></span>                                              | <span data-ttu-id="9fff9-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9fff9-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9fff9-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9fff9-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9fff9-127">да</span><span class="sxs-lookup"><span data-stu-id="9fff9-127">yes</span></span>       |
| [<span data-ttu-id="9fff9-128">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="9fff9-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9fff9-129">да</span><span class="sxs-lookup"><span data-stu-id="9fff9-129">yes</span></span>       |
| [<span data-ttu-id="9fff9-130">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="9fff9-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9fff9-131">да</span><span class="sxs-lookup"><span data-stu-id="9fff9-131">yes</span></span>       |
| [<span data-ttu-id="9fff9-132">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9fff9-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9fff9-133">Нет</span><span class="sxs-lookup"><span data-stu-id="9fff9-133">no</span></span>        |
| [<span data-ttu-id="9fff9-134">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9fff9-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9fff9-135">Нет</span><span class="sxs-lookup"><span data-stu-id="9fff9-135">no</span></span>        |
| [<span data-ttu-id="9fff9-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9fff9-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9fff9-137">Нет</span><span class="sxs-lookup"><span data-stu-id="9fff9-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9fff9-138">См. также</span><span class="sxs-lookup"><span data-stu-id="9fff9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fff9-139">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9fff9-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





