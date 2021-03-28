---
title: метка (SM4-ASM)
description: Указывает начало подпрограммы.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784953"
---
# <a name="label-sm4---asm"></a><span data-ttu-id="f6883-103">метка (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f6883-103">label (sm4 - asm)</span></span>

<span data-ttu-id="f6883-104">Указывает начало подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="f6883-104">Indicates the beginning of a subroutine.</span></span>



| <span data-ttu-id="f6883-105">Метка l\#</span><span class="sxs-lookup"><span data-stu-id="f6883-105">label l\#</span></span> |
|-----------|



 



| <span data-ttu-id="f6883-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="f6883-106">Item</span></span>                                                       | <span data-ttu-id="f6883-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f6883-107">Description</span></span>                         |
|------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="f6883-108"><span id="l_"></span><span id="L_"></span>*н\#*</span><span class="sxs-lookup"><span data-stu-id="f6883-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="f6883-109">\[в \] поле номер метки.</span><span class="sxs-lookup"><span data-stu-id="f6883-109">\[in\] The label number.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6883-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6883-110">Remarks</span></span>

<span data-ttu-id="f6883-111">**Метка** может присутствовать непосредственно после инструкции [**RET**](ret--sm4---asm-.md) , которая не вложена ни в какие инструкции управления потоком.</span><span class="sxs-lookup"><span data-stu-id="f6883-111">A **label** can only appear directly after a [**ret**](ret--sm4---asm-.md) instruction which is not nested in any flow control statements.</span></span>

<span data-ttu-id="f6883-112">Код, предшествующий первой **метке** в программе, является основной программой.</span><span class="sxs-lookup"><span data-stu-id="f6883-112">The code before the first **label** in a program is the main program.</span></span> <span data-ttu-id="f6883-113">Все подпрограммы отображаются в конце программы, обозначенные инструкциями **Label** .</span><span class="sxs-lookup"><span data-stu-id="f6883-113">All subroutines appear at the end of the program, indicated by **label** statements.</span></span>

<span data-ttu-id="f6883-114">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="f6883-114">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

<span data-ttu-id="f6883-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="f6883-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f6883-116">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="f6883-116">Vertex Shader</span></span> | <span data-ttu-id="f6883-117">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="f6883-117">Geometry Shader</span></span> | <span data-ttu-id="f6883-118">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="f6883-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f6883-119">x</span><span class="sxs-lookup"><span data-stu-id="f6883-119">x</span></span>             | <span data-ttu-id="f6883-120">x</span><span class="sxs-lookup"><span data-stu-id="f6883-120">x</span></span>               | <span data-ttu-id="f6883-121">x</span><span class="sxs-lookup"><span data-stu-id="f6883-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f6883-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f6883-122">Minimum Shader Model</span></span>

<span data-ttu-id="f6883-123">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f6883-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f6883-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f6883-124">Shader Model</span></span>                                              | <span data-ttu-id="f6883-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6883-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f6883-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f6883-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f6883-127">да</span><span class="sxs-lookup"><span data-stu-id="f6883-127">yes</span></span>       |
| [<span data-ttu-id="f6883-128">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="f6883-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f6883-129">да</span><span class="sxs-lookup"><span data-stu-id="f6883-129">yes</span></span>       |
| [<span data-ttu-id="f6883-130">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f6883-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f6883-131">да</span><span class="sxs-lookup"><span data-stu-id="f6883-131">yes</span></span>       |
| [<span data-ttu-id="f6883-132">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6883-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f6883-133">Нет</span><span class="sxs-lookup"><span data-stu-id="f6883-133">no</span></span>        |
| [<span data-ttu-id="f6883-134">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6883-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f6883-135">Нет</span><span class="sxs-lookup"><span data-stu-id="f6883-135">no</span></span>        |
| [<span data-ttu-id="f6883-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6883-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f6883-137">Нет</span><span class="sxs-lookup"><span data-stu-id="f6883-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f6883-138">См. также</span><span class="sxs-lookup"><span data-stu-id="f6883-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6883-139">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6883-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





