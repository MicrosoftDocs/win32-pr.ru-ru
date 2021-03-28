---
title: ушр (SM4-ASM)
description: Сдвиг вправо. | ушр (SM4-ASM)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c48b706afb1223a5289f93b5ca393a89c36e915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273436"
---
# <a name="ushr-sm4---asm"></a><span data-ttu-id="fdbb6-104">ушр (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fdbb6-104">ushr (sm4 - asm)</span></span>

<span data-ttu-id="fdbb6-105">Сдвиг вправо.</span><span class="sxs-lookup"><span data-stu-id="fdbb6-105">Shift right.</span></span>



| <span data-ttu-id="fdbb6-106">ушр dest \[ . Mask \] , src0 \[ . свиззле \] , src1. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="fdbb6-106">ushr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="fdbb6-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="fdbb6-107">Item</span></span>                                                            | <span data-ttu-id="fdbb6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fdbb6-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fdbb6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fdbb6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fdbb6-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="fdbb6-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="fdbb6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fdbb6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fdbb6-112">\[в \] компонентах для сдвига.</span><span class="sxs-lookup"><span data-stu-id="fdbb6-112">\[in\] The components to shift.</span></span><br/>                    |
| <span data-ttu-id="fdbb6-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="fdbb6-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="fdbb6-114">\[в \] поле объем для сдвига *src0*.</span><span class="sxs-lookup"><span data-stu-id="fdbb6-114">\[in\] The amount to shift *src0*.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="fdbb6-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="fdbb6-115">Remarks</span></span>

<span data-ttu-id="fdbb6-116">Эта инструкция выполняет ориентированную на компоненты смену каждого 32-битного значения в *src0* прямо на число беззнаковых разрядов, предоставленное в ЛСБ 5 бит (диапазон 0-31) в *src1. Выберите \_ компонент*, вставив 0.</span><span class="sxs-lookup"><span data-stu-id="fdbb6-116">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="fdbb6-117">Результат 32-бит на компонент помещается в *dest*.</span><span class="sxs-lookup"><span data-stu-id="fdbb6-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="fdbb6-118">Счетчик — это скалярное значение, применяемое ко всем компонентам.</span><span class="sxs-lookup"><span data-stu-id="fdbb6-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="fdbb6-119">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="fdbb6-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fdbb6-120">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fdbb6-120">Vertex Shader</span></span> | <span data-ttu-id="fdbb6-121">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="fdbb6-121">Geometry Shader</span></span> | <span data-ttu-id="fdbb6-122">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fdbb6-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fdbb6-123">x</span><span class="sxs-lookup"><span data-stu-id="fdbb6-123">x</span></span>             | <span data-ttu-id="fdbb6-124">x</span><span class="sxs-lookup"><span data-stu-id="fdbb6-124">x</span></span>               | <span data-ttu-id="fdbb6-125">x</span><span class="sxs-lookup"><span data-stu-id="fdbb6-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fdbb6-126">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fdbb6-126">Minimum Shader Model</span></span>

<span data-ttu-id="fdbb6-127">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fdbb6-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fdbb6-128">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fdbb6-128">Shader Model</span></span>                                              | <span data-ttu-id="fdbb6-129">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fdbb6-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fdbb6-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="fdbb6-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fdbb6-131">да</span><span class="sxs-lookup"><span data-stu-id="fdbb6-131">yes</span></span>       |
| [<span data-ttu-id="fdbb6-132">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="fdbb6-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fdbb6-133">да</span><span class="sxs-lookup"><span data-stu-id="fdbb6-133">yes</span></span>       |
| [<span data-ttu-id="fdbb6-134">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="fdbb6-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fdbb6-135">да</span><span class="sxs-lookup"><span data-stu-id="fdbb6-135">yes</span></span>       |
| [<span data-ttu-id="fdbb6-136">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdbb6-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fdbb6-137">Нет</span><span class="sxs-lookup"><span data-stu-id="fdbb6-137">no</span></span>        |
| [<span data-ttu-id="fdbb6-138">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdbb6-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fdbb6-139">Нет</span><span class="sxs-lookup"><span data-stu-id="fdbb6-139">no</span></span>        |
| [<span data-ttu-id="fdbb6-140">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdbb6-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fdbb6-141">Нет</span><span class="sxs-lookup"><span data-stu-id="fdbb6-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fdbb6-142">См. также</span><span class="sxs-lookup"><span data-stu-id="fdbb6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdbb6-143">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fdbb6-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





