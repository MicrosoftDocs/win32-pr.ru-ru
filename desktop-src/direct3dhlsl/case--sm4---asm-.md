---
title: Case (SM4-ASM)
description: Метка в инструкции switch.
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983845"
---
# <a name="case-sm4---asm"></a><span data-ttu-id="65041-103">Case (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="65041-103">case (sm4 - asm)</span></span>

<span data-ttu-id="65041-104">Метка в инструкции switch.</span><span class="sxs-lookup"><span data-stu-id="65041-104">A label in a switch instruction.</span></span>



| <span data-ttu-id="65041-105">случай \[ немедленных 32-бит\]</span><span class="sxs-lookup"><span data-stu-id="65041-105">case \[32-bit immediate\]</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="65041-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="65041-106">Remarks</span></span>

<span data-ttu-id="65041-107">Так как циклы можно использовать только **в том случае** , если код не добавлен, несколько **вариантов** (включая [значение по умолчанию](default--sm4---asm-.md)) могут иметь один и тот же блок кода.</span><span class="sxs-lookup"><span data-stu-id="65041-107">Because falling through **cases** is valid only if there is no code added, multiple **cases** (including [default](default--sm4---asm-.md)) can share the same code block.</span></span>

<span data-ttu-id="65041-108">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="65041-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="65041-109">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="65041-109">Vertex Shader</span></span> | <span data-ttu-id="65041-110">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="65041-110">Geometry Shader</span></span> | <span data-ttu-id="65041-111">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="65041-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="65041-112">x</span><span class="sxs-lookup"><span data-stu-id="65041-112">x</span></span>             | <span data-ttu-id="65041-113">x</span><span class="sxs-lookup"><span data-stu-id="65041-113">x</span></span>               | <span data-ttu-id="65041-114">x</span><span class="sxs-lookup"><span data-stu-id="65041-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="65041-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65041-115">Minimum Shader Model</span></span>

<span data-ttu-id="65041-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="65041-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="65041-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="65041-117">Shader Model</span></span>                                              | <span data-ttu-id="65041-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="65041-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="65041-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="65041-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="65041-120">да</span><span class="sxs-lookup"><span data-stu-id="65041-120">yes</span></span>       |
| [<span data-ttu-id="65041-121">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="65041-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="65041-122">да</span><span class="sxs-lookup"><span data-stu-id="65041-122">yes</span></span>       |
| [<span data-ttu-id="65041-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="65041-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="65041-124">да</span><span class="sxs-lookup"><span data-stu-id="65041-124">yes</span></span>       |
| [<span data-ttu-id="65041-125">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65041-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="65041-126">Нет</span><span class="sxs-lookup"><span data-stu-id="65041-126">no</span></span>        |
| [<span data-ttu-id="65041-127">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65041-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="65041-128">Нет</span><span class="sxs-lookup"><span data-stu-id="65041-128">no</span></span>        |
| [<span data-ttu-id="65041-129">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65041-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="65041-130">Нет</span><span class="sxs-lookup"><span data-stu-id="65041-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="65041-131">См. также</span><span class="sxs-lookup"><span data-stu-id="65041-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65041-132">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="65041-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




