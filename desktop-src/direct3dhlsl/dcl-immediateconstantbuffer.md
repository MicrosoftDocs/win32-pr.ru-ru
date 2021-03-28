---
title: dcl_immediateConstantBuffer (SM4-ASM)
description: дкл \_ иммедиатеконстантбуффер (SM4-ASM)
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335651"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a><span data-ttu-id="39df9-103">дкл \_ иммедиатеконстантбуффер (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="39df9-103">dcl\_immediateConstantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="39df9-104">Объявляет буфер немедленных констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="39df9-104">Declares a shader immediate-constant buffer.</span></span>



| <span data-ttu-id="39df9-105">дкл \_ иммедиатеконстантбуффер *значение (s)*</span><span class="sxs-lookup"><span data-stu-id="39df9-105">dcl\_immediateConstantBuffer *value(s)*</span></span> |
|-----------------------------------------|



 

<dl> <dt>

<span data-ttu-id="39df9-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*значения (с)*</span><span class="sxs-lookup"><span data-stu-id="39df9-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*</span></span>
</dt> <dd>

<span data-ttu-id="39df9-107">\[в \] буфере должно содержать по крайней мере одно значение, но не более 4096 значений.</span><span class="sxs-lookup"><span data-stu-id="39df9-107">\[in\] The buffer must contain at least one value, but not more than 4096 values.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="39df9-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="39df9-108">Remarks</span></span>

<span data-ttu-id="39df9-109">Шейдер может иметь один непосредственный постоянный буфер.</span><span class="sxs-lookup"><span data-stu-id="39df9-109">A shader is allowed one immediate-constant buffer.</span></span> <span data-ttu-id="39df9-110">Доступ к буферу немедленных констант осуществляется так же, как и постоянный буфер с динамической индексацией.</span><span class="sxs-lookup"><span data-stu-id="39df9-110">An immediate-constant buffer is accessed just like a constant buffer with dynamic indexing.</span></span>

<span data-ttu-id="39df9-111">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="39df9-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="39df9-112">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="39df9-112">Vertex Shader</span></span> | <span data-ttu-id="39df9-113">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="39df9-113">Geometry Shader</span></span> | <span data-ttu-id="39df9-114">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="39df9-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="39df9-115">x</span><span class="sxs-lookup"><span data-stu-id="39df9-115">x</span></span>             | <span data-ttu-id="39df9-116">x</span><span class="sxs-lookup"><span data-stu-id="39df9-116">x</span></span>               | <span data-ttu-id="39df9-117">x</span><span class="sxs-lookup"><span data-stu-id="39df9-117">x</span></span>            |



 

<span data-ttu-id="39df9-118">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="39df9-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="39df9-119">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="39df9-119">Minimum Shader Model</span></span>

<span data-ttu-id="39df9-120">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="39df9-120">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="39df9-121">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="39df9-121">Shader Model</span></span>                                              | <span data-ttu-id="39df9-122">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="39df9-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="39df9-123">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="39df9-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="39df9-124">да</span><span class="sxs-lookup"><span data-stu-id="39df9-124">yes</span></span>       |
| [<span data-ttu-id="39df9-125">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="39df9-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="39df9-126">да</span><span class="sxs-lookup"><span data-stu-id="39df9-126">yes</span></span>       |
| [<span data-ttu-id="39df9-127">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="39df9-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="39df9-128">да</span><span class="sxs-lookup"><span data-stu-id="39df9-128">yes</span></span>       |
| [<span data-ttu-id="39df9-129">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39df9-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="39df9-130">Нет</span><span class="sxs-lookup"><span data-stu-id="39df9-130">no</span></span>        |
| [<span data-ttu-id="39df9-131">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39df9-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="39df9-132">Нет</span><span class="sxs-lookup"><span data-stu-id="39df9-132">no</span></span>        |
| [<span data-ttu-id="39df9-133">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39df9-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="39df9-134">Нет</span><span class="sxs-lookup"><span data-stu-id="39df9-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="39df9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="39df9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39df9-136">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39df9-136">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




