---
title: Switch (SM4-ASM)
description: Передает управление другому блоку операторов в теле переключателя в зависимости от значения селектора.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069348"
---
# <a name="switch-sm4---asm"></a><span data-ttu-id="52088-103">Switch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="52088-103">switch (sm4 - asm)</span></span>

<span data-ttu-id="52088-104">Передает управление другому блоку операторов в теле переключателя в зависимости от значения селектора.</span><span class="sxs-lookup"><span data-stu-id="52088-104">Transfers control to a different statement block within the switch body depending on the value of a selector.</span></span>



| <span data-ttu-id="52088-105">переключить src0. выбранный \_ компонент</span><span class="sxs-lookup"><span data-stu-id="52088-105">switch src0.selected\_component</span></span> |
|---------------------------------|



 



| <span data-ttu-id="52088-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="52088-106">Item</span></span>                                                            | <span data-ttu-id="52088-107">Описание</span><span class="sxs-lookup"><span data-stu-id="52088-107">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="52088-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="52088-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="52088-109">\[в \] селекторе для оператора switch.</span><span class="sxs-lookup"><span data-stu-id="52088-109">\[in\] The selector for the switch statement.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52088-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="52088-110">Remarks</span></span>

<span data-ttu-id="52088-111">Конструкция **переключателя** / [ендсвитч](endswitch--sm4---asm-.md) ведет себя в точности так же, как конструкция **switch** на языке C, со следующим исключением: для инструкций D3D11 [case](case--sm4---asm-.md) / [по умолчанию](default--sm4---asm-.md) , которые переходят к следующему **варианту** / **по умолчанию** без [разрыва](break--sm4---asm-.md) , не может содержать никакого кода.</span><span class="sxs-lookup"><span data-stu-id="52088-111">A **switch**/[endswitch](endswitch--sm4---asm-.md) construct behaves exactly as a **switch** construct in the C language, with the following exception: for D3D11 [case](case--sm4---asm-.md)/[default](default--sm4---asm-.md) statements that fall through to the next **case**/**default** without a [break](break--sm4---asm-.md) cannot have any code in them.</span></span> <span data-ttu-id="52088-112">Для последовательного отображения нескольких инструкций **case** , в том числе **значений по умолчанию**, совместное использование одного и того же блока кода разрешено.</span><span class="sxs-lookup"><span data-stu-id="52088-112">It is permitted for multiple **case** statements, including **default**, to appear sequentially, sharing the same code block.</span></span>

<span data-ttu-id="52088-113">Условие должно быть 32-битным компонентом Register или непосредственным количеством.</span><span class="sxs-lookup"><span data-stu-id="52088-113">The condition must be a 32-bit register component or immediate quantity.</span></span> <span data-ttu-id="52088-114">Сравнение на равенство является побитовым (целочисленным).</span><span class="sxs-lookup"><span data-stu-id="52088-114">The equality comparison is bitwise (integer).</span></span>

<span data-ttu-id="52088-115">Как и в случае с любой инструкцией шейдера в D3D11, оборудование может или не реализовывать конструкцию **switch** напрямую.</span><span class="sxs-lookup"><span data-stu-id="52088-115">As with any Shader instruction in the D3D11, hardware may or may not implement the **switch** construct directly.</span></span>

<span data-ttu-id="52088-116">Операторы **switch** могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="52088-116">**Switch** statements can be nested.</span></span> <span data-ttu-id="52088-117">Каждый блок **переключателя** считается равным 1 уровню в соответствии с ограничением глубины вложения управления потоком, равным 64 на подпрограммы и Main, независимо от количества инструкций **case** .</span><span class="sxs-lookup"><span data-stu-id="52088-117">Each **switch** block counts as 1 level against the flow control nesting depth limit of 64 per subroutine and main, independent of the number of **case** statements.</span></span> <span data-ttu-id="52088-118">Компилятор HLSL не будет создавать подпрограммы, превышающие это ограничение.</span><span class="sxs-lookup"><span data-stu-id="52088-118">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="52088-119">Поведение инструкций потока управления свыше 64 уровней в каждой подподпрограмме не определено.</span><span class="sxs-lookup"><span data-stu-id="52088-119">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="52088-120">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="52088-120">The following example shows how to use this instruction.</span></span>

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

<span data-ttu-id="52088-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="52088-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="52088-122">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="52088-122">Vertex Shader</span></span> | <span data-ttu-id="52088-123">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="52088-123">Geometry Shader</span></span> | <span data-ttu-id="52088-124">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="52088-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="52088-125">x</span><span class="sxs-lookup"><span data-stu-id="52088-125">x</span></span>             | <span data-ttu-id="52088-126">x</span><span class="sxs-lookup"><span data-stu-id="52088-126">x</span></span>               | <span data-ttu-id="52088-127">x</span><span class="sxs-lookup"><span data-stu-id="52088-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="52088-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="52088-128">Minimum Shader Model</span></span>

<span data-ttu-id="52088-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="52088-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="52088-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="52088-130">Shader Model</span></span>                                              | <span data-ttu-id="52088-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="52088-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="52088-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="52088-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="52088-133">да</span><span class="sxs-lookup"><span data-stu-id="52088-133">yes</span></span>       |
| [<span data-ttu-id="52088-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="52088-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="52088-135">да</span><span class="sxs-lookup"><span data-stu-id="52088-135">yes</span></span>       |
| [<span data-ttu-id="52088-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="52088-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="52088-137">да</span><span class="sxs-lookup"><span data-stu-id="52088-137">yes</span></span>       |
| [<span data-ttu-id="52088-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="52088-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="52088-139">Нет</span><span class="sxs-lookup"><span data-stu-id="52088-139">no</span></span>        |
| [<span data-ttu-id="52088-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="52088-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="52088-141">Нет</span><span class="sxs-lookup"><span data-stu-id="52088-141">no</span></span>        |
| [<span data-ttu-id="52088-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="52088-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="52088-143">Нет</span><span class="sxs-lookup"><span data-stu-id="52088-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="52088-144">См. также</span><span class="sxs-lookup"><span data-stu-id="52088-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52088-145">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="52088-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





