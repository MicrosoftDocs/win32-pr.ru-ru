---
title: dcl_input Вприм (SM4-ASM)
description: дкл \_ input вприм (SM4-ASM)
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9742c6066d66d7aa4121c1d1d1df98a37cb0147e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412241"
---
# <a name="dcl_input-vprim-sm4---asm"></a><span data-ttu-id="5f6a4-103">дкл \_ input вприм (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5f6a4-103">dcl\_input vPrim (sm4 - asm)</span></span>

<span data-ttu-id="5f6a4-104">Объявляет, что шейдер Geometry использует скалярный входной регистр Вприм.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-104">Declares that a geometry shader uses its scalar input-register vPrim.</span></span>



| <span data-ttu-id="5f6a4-105">дкл \_ входные *вприм*</span><span class="sxs-lookup"><span data-stu-id="5f6a4-105">dcl\_input *vPrim*</span></span> |
|--------------------|



 



| <span data-ttu-id="5f6a4-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="5f6a4-106">Item</span></span>                                                                                       | <span data-ttu-id="5f6a4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5f6a4-107">Description</span></span>                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f6a4-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*вприм*</span><span class="sxs-lookup"><span data-stu-id="5f6a4-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span></span><br/> | <span data-ttu-id="5f6a4-109">\[в \] 32-разрядном скаляре, которое можно применить к каждому внутреннему примитиву в шейдере Geometry.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-109">\[in\] A 32-bit scalar, which can be applied to each interior primitive in a geometry shader.</span></span><br/> |



 

<span data-ttu-id="5f6a4-110">Скаляр не может применяться к любым смежным примитивам.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-110">The scalar cannot be applied to any adjacent primitives.</span></span>

<span data-ttu-id="5f6a4-111">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="5f6a4-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5f6a4-112">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="5f6a4-112">Vertex Shader</span></span> | <span data-ttu-id="5f6a4-113">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="5f6a4-113">Geometry Shader</span></span> | <span data-ttu-id="5f6a4-114">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="5f6a4-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="5f6a4-115">x</span><span class="sxs-lookup"><span data-stu-id="5f6a4-115">x</span></span>               |              |



 

<span data-ttu-id="5f6a4-116">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-116">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="5f6a4-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5f6a4-117">Minimum Shader Model</span></span>

<span data-ttu-id="5f6a4-118">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="5f6a4-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5f6a4-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="5f6a4-119">Shader Model</span></span>                                              | <span data-ttu-id="5f6a4-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="5f6a4-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5f6a4-121">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5f6a4-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5f6a4-122">да</span><span class="sxs-lookup"><span data-stu-id="5f6a4-122">yes</span></span>       |
| [<span data-ttu-id="5f6a4-123">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="5f6a4-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5f6a4-124">да</span><span class="sxs-lookup"><span data-stu-id="5f6a4-124">yes</span></span>       |
| [<span data-ttu-id="5f6a4-125">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="5f6a4-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5f6a4-126">да</span><span class="sxs-lookup"><span data-stu-id="5f6a4-126">yes</span></span>       |
| [<span data-ttu-id="5f6a4-127">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f6a4-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5f6a4-128">Нет</span><span class="sxs-lookup"><span data-stu-id="5f6a4-128">no</span></span>        |
| [<span data-ttu-id="5f6a4-129">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f6a4-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5f6a4-130">Нет</span><span class="sxs-lookup"><span data-stu-id="5f6a4-130">no</span></span>        |
| [<span data-ttu-id="5f6a4-131">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f6a4-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5f6a4-132">Нет</span><span class="sxs-lookup"><span data-stu-id="5f6a4-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5f6a4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="5f6a4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f6a4-134">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5f6a4-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





