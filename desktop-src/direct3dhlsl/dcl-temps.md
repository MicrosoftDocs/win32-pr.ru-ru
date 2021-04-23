---
title: dcl_temps (SM4-ASM)
description: дкл \_ Temps (SM4-ASM)
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc3a468575b30836d4574edb13c4fc77a3505fc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996967"
---
# <a name="dcl_temps-sm4---asm"></a><span data-ttu-id="8a66a-103">дкл \_ Temps (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8a66a-103">dcl\_temps (sm4 - asm)</span></span>

<span data-ttu-id="8a66a-104">Объявляет временные регистры.</span><span class="sxs-lookup"><span data-stu-id="8a66a-104">Declares temporary registers.</span></span>



| <span data-ttu-id="8a66a-105">дкл \_ Temps N</span><span class="sxs-lookup"><span data-stu-id="8a66a-105">dcl\_temps N</span></span> |
|--------------|



 



| <span data-ttu-id="8a66a-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="8a66a-106">Item</span></span>                                                   | <span data-ttu-id="8a66a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8a66a-107">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a66a-108"><span id="N"></span><span id="n"></span>*\N*</span><span class="sxs-lookup"><span data-stu-id="8a66a-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="8a66a-109">\[\]количество временных регистров.</span><span class="sxs-lookup"><span data-stu-id="8a66a-109">\[in\] The number of temporary registers.</span></span><br/> |



 

<span data-ttu-id="8a66a-110">Каждый регистр содержит место для 32-разрядного значения из четырех компонентов.</span><span class="sxs-lookup"><span data-stu-id="8a66a-110">Each register has space for a 32-bit four-component value.</span></span> <span data-ttu-id="8a66a-111">Общее число временных и [индексируемых временных](dcl-indexabletemp.md) регистров должно быть меньше или равно 4096.</span><span class="sxs-lookup"><span data-stu-id="8a66a-111">The total number of temporary and [indexable-temporary](dcl-indexabletemp.md) registers must be less than or equal to 4096.</span></span>

<span data-ttu-id="8a66a-112">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8a66a-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8a66a-113">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="8a66a-113">Vertex Shader</span></span> | <span data-ttu-id="8a66a-114">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="8a66a-114">Geometry Shader</span></span> | <span data-ttu-id="8a66a-115">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="8a66a-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8a66a-116">x</span><span class="sxs-lookup"><span data-stu-id="8a66a-116">x</span></span>             | <span data-ttu-id="8a66a-117">x</span><span class="sxs-lookup"><span data-stu-id="8a66a-117">x</span></span>               | <span data-ttu-id="8a66a-118">x</span><span class="sxs-lookup"><span data-stu-id="8a66a-118">x</span></span>            |



 

<span data-ttu-id="8a66a-119">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="8a66a-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="8a66a-120">Например, .</span><span class="sxs-lookup"><span data-stu-id="8a66a-120">Example</span></span>

<span data-ttu-id="8a66a-121">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="8a66a-121">Here is an example.</span></span>


```
dcl_temps 10; // Declare r0-r9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="8a66a-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8a66a-122">Minimum Shader Model</span></span>

<span data-ttu-id="8a66a-123">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8a66a-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8a66a-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8a66a-124">Shader Model</span></span>                                              | <span data-ttu-id="8a66a-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a66a-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8a66a-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8a66a-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8a66a-127">да</span><span class="sxs-lookup"><span data-stu-id="8a66a-127">yes</span></span>       |
| [<span data-ttu-id="8a66a-128">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8a66a-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8a66a-129">да</span><span class="sxs-lookup"><span data-stu-id="8a66a-129">yes</span></span>       |
| [<span data-ttu-id="8a66a-130">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8a66a-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8a66a-131">да</span><span class="sxs-lookup"><span data-stu-id="8a66a-131">yes</span></span>       |
| [<span data-ttu-id="8a66a-132">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a66a-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8a66a-133">Нет</span><span class="sxs-lookup"><span data-stu-id="8a66a-133">no</span></span>        |
| [<span data-ttu-id="8a66a-134">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a66a-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8a66a-135">Нет</span><span class="sxs-lookup"><span data-stu-id="8a66a-135">no</span></span>        |
| [<span data-ttu-id="8a66a-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a66a-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8a66a-137">Нет</span><span class="sxs-lookup"><span data-stu-id="8a66a-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8a66a-138">См. также</span><span class="sxs-lookup"><span data-stu-id="8a66a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a66a-139">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a66a-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





