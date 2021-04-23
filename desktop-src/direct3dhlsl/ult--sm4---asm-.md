---
title: метры (SM4-ASM)
description: Покомпонентное векторное целое число без знака, меньшее, чем сравнение.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996883"
---
# <a name="ult-sm4---asm"></a><span data-ttu-id="80d62-103">метры (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="80d62-103">ult (sm4 - asm)</span></span>

<span data-ttu-id="80d62-104">Покомпонентное векторное целое число без знака, меньшее, чем сравнение.</span><span class="sxs-lookup"><span data-stu-id="80d62-104">Component-wise vector unsigned integer less-than comparison.</span></span>



| <span data-ttu-id="80d62-105">метры dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="80d62-105">ult dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="80d62-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="80d62-106">Item</span></span>                                                            | <span data-ttu-id="80d62-107">Описание</span><span class="sxs-lookup"><span data-stu-id="80d62-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="80d62-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="80d62-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="80d62-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="80d62-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="80d62-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="80d62-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="80d62-111">\[в \] значении, сравниваемом с *src1*.</span><span class="sxs-lookup"><span data-stu-id="80d62-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="80d62-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="80d62-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="80d62-113">\[в \] значении, сравниваемом с *src1*.</span><span class="sxs-lookup"><span data-stu-id="80d62-113">\[in\] The value to compare to *src1*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="80d62-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="80d62-114">Remarks</span></span>

<span data-ttu-id="80d62-115">Выполняет сравнение целых чисел без знака (*src0*  <  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="80d62-115">Performs the unsigned integer comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="80d62-116">Если сравнение истинно, эта инструкция возвращает значение 0xFFFFFFFF для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="80d62-116">If the comparison is true, this instruction returns 0xFFFFFFFF for that component.</span></span> <span data-ttu-id="80d62-117">В противном случае возвращается 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="80d62-117">Otherwise it returns 0x0000000.</span></span>

<span data-ttu-id="80d62-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="80d62-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="80d62-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="80d62-119">Vertex Shader</span></span> | <span data-ttu-id="80d62-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="80d62-120">Geometry Shader</span></span> | <span data-ttu-id="80d62-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="80d62-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="80d62-122">x</span><span class="sxs-lookup"><span data-stu-id="80d62-122">x</span></span>             | <span data-ttu-id="80d62-123">x</span><span class="sxs-lookup"><span data-stu-id="80d62-123">x</span></span>               | <span data-ttu-id="80d62-124">x</span><span class="sxs-lookup"><span data-stu-id="80d62-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="80d62-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="80d62-125">Minimum Shader Model</span></span>

<span data-ttu-id="80d62-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="80d62-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="80d62-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="80d62-127">Shader Model</span></span>                                              | <span data-ttu-id="80d62-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="80d62-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="80d62-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="80d62-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="80d62-130">да</span><span class="sxs-lookup"><span data-stu-id="80d62-130">yes</span></span>       |
| [<span data-ttu-id="80d62-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="80d62-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="80d62-132">да</span><span class="sxs-lookup"><span data-stu-id="80d62-132">yes</span></span>       |
| [<span data-ttu-id="80d62-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="80d62-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="80d62-134">да</span><span class="sxs-lookup"><span data-stu-id="80d62-134">yes</span></span>       |
| [<span data-ttu-id="80d62-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80d62-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="80d62-136">Нет</span><span class="sxs-lookup"><span data-stu-id="80d62-136">no</span></span>        |
| [<span data-ttu-id="80d62-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80d62-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="80d62-138">Нет</span><span class="sxs-lookup"><span data-stu-id="80d62-138">no</span></span>        |
| [<span data-ttu-id="80d62-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80d62-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="80d62-140">Нет</span><span class="sxs-lookup"><span data-stu-id="80d62-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="80d62-141">См. также</span><span class="sxs-lookup"><span data-stu-id="80d62-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d62-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="80d62-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





