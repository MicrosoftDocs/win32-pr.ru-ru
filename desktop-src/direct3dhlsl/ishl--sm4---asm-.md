---
title: Ишл (SM4-ASM)
description: Сдвиг влево. | Ишл (SM4-ASM)
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e14225f8c8b0e46cf0ba6eda61f96e4563a904e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998158"
---
# <a name="ishl-sm4---asm"></a><span data-ttu-id="08d47-104">Ишл (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="08d47-104">ishl (sm4 - asm)</span></span>

<span data-ttu-id="08d47-105">Сдвиг влево.</span><span class="sxs-lookup"><span data-stu-id="08d47-105">Shift left.</span></span>



| <span data-ttu-id="08d47-106">dest \[ . Mask \] , src0 \[ . свиззле \] , src1. Select \_ Component</span><span class="sxs-lookup"><span data-stu-id="08d47-106">dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="08d47-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="08d47-107">Item</span></span>                                                            | <span data-ttu-id="08d47-108">Описание</span><span class="sxs-lookup"><span data-stu-id="08d47-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="08d47-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="08d47-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="08d47-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="08d47-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="08d47-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="08d47-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="08d47-112">\[в \] содержит значения для сдвига.</span><span class="sxs-lookup"><span data-stu-id="08d47-112">\[in\] Contains the values to be shifted.</span></span><br/>          |
| <span data-ttu-id="08d47-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="08d47-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="08d47-114">\[в \] содержит сумму сдвига.</span><span class="sxs-lookup"><span data-stu-id="08d47-114">\[in\] Contains the shift amount.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="08d47-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="08d47-115">Remarks</span></span>

<span data-ttu-id="08d47-116">Эта инструкция выполняет ориентированную на компоненты смену каждого 32-битного значения в *src0* влево на число беззнаковых целых чисел, предоставленное в ЛСБ 5 бит (диапазон 0-31) в *src1. Выберите \_ компонент*, вставив 0.</span><span class="sxs-lookup"><span data-stu-id="08d47-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="08d47-117">Результаты 32-бит на компонент помещаются в *dest*.</span><span class="sxs-lookup"><span data-stu-id="08d47-117">The 32-bit per component results are placed in *dest*.</span></span> <span data-ttu-id="08d47-118">Счетчик — это скалярное значение, применяемое ко всем компонентам.</span><span class="sxs-lookup"><span data-stu-id="08d47-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="08d47-119">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="08d47-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="08d47-120">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="08d47-120">Vertex Shader</span></span> | <span data-ttu-id="08d47-121">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="08d47-121">Geometry Shader</span></span> | <span data-ttu-id="08d47-122">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="08d47-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="08d47-123">x</span><span class="sxs-lookup"><span data-stu-id="08d47-123">x</span></span>             | <span data-ttu-id="08d47-124">x</span><span class="sxs-lookup"><span data-stu-id="08d47-124">x</span></span>               | <span data-ttu-id="08d47-125">x</span><span class="sxs-lookup"><span data-stu-id="08d47-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="08d47-126">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="08d47-126">Minimum Shader Model</span></span>

<span data-ttu-id="08d47-127">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="08d47-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="08d47-128">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="08d47-128">Shader Model</span></span>                                              | <span data-ttu-id="08d47-129">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="08d47-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="08d47-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="08d47-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="08d47-131">да</span><span class="sxs-lookup"><span data-stu-id="08d47-131">yes</span></span>       |
| [<span data-ttu-id="08d47-132">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="08d47-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="08d47-133">да</span><span class="sxs-lookup"><span data-stu-id="08d47-133">yes</span></span>       |
| [<span data-ttu-id="08d47-134">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="08d47-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="08d47-135">да</span><span class="sxs-lookup"><span data-stu-id="08d47-135">yes</span></span>       |
| [<span data-ttu-id="08d47-136">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08d47-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="08d47-137">Нет</span><span class="sxs-lookup"><span data-stu-id="08d47-137">no</span></span>        |
| [<span data-ttu-id="08d47-138">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08d47-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="08d47-139">Нет</span><span class="sxs-lookup"><span data-stu-id="08d47-139">no</span></span>        |
| [<span data-ttu-id="08d47-140">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08d47-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="08d47-141">Нет</span><span class="sxs-lookup"><span data-stu-id="08d47-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="08d47-142">См. также</span><span class="sxs-lookup"><span data-stu-id="08d47-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d47-143">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08d47-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





