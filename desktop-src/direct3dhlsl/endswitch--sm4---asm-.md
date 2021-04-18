---
title: ендсвитч (SM4-ASM)
description: Завершает оператор switch.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523a4008ab976ee299758349d57c6e32a3f336b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412125"
---
# <a name="endswitch-sm4---asm"></a><span data-ttu-id="b6cd4-103">ендсвитч (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b6cd4-103">endswitch (sm4 - asm)</span></span>

<span data-ttu-id="b6cd4-104">Завершает оператор [switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="b6cd4-104">Ends a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="b6cd4-105">ендсвитч</span><span class="sxs-lookup"><span data-stu-id="b6cd4-105">endswitch</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="b6cd4-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6cd4-106">Remarks</span></span>

<span data-ttu-id="b6cd4-107">Формат маркера содержит смещение соответствующей инструкции switch в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="b6cd4-107">The token format contains the offset of the corresponding switch instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="b6cd4-108">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="b6cd4-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b6cd4-109">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b6cd4-109">Vertex Shader</span></span> | <span data-ttu-id="b6cd4-110">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="b6cd4-110">Geometry Shader</span></span> | <span data-ttu-id="b6cd4-111">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b6cd4-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b6cd4-112">x</span><span class="sxs-lookup"><span data-stu-id="b6cd4-112">x</span></span>             | <span data-ttu-id="b6cd4-113">x</span><span class="sxs-lookup"><span data-stu-id="b6cd4-113">x</span></span>               | <span data-ttu-id="b6cd4-114">x</span><span class="sxs-lookup"><span data-stu-id="b6cd4-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b6cd4-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b6cd4-115">Minimum Shader Model</span></span>

<span data-ttu-id="b6cd4-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b6cd4-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b6cd4-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b6cd4-117">Shader Model</span></span>                                              | <span data-ttu-id="b6cd4-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b6cd4-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b6cd4-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b6cd4-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b6cd4-120">да</span><span class="sxs-lookup"><span data-stu-id="b6cd4-120">yes</span></span>       |
| [<span data-ttu-id="b6cd4-121">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="b6cd4-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b6cd4-122">да</span><span class="sxs-lookup"><span data-stu-id="b6cd4-122">yes</span></span>       |
| [<span data-ttu-id="b6cd4-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="b6cd4-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b6cd4-124">да</span><span class="sxs-lookup"><span data-stu-id="b6cd4-124">yes</span></span>       |
| [<span data-ttu-id="b6cd4-125">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6cd4-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b6cd4-126">Нет</span><span class="sxs-lookup"><span data-stu-id="b6cd4-126">no</span></span>        |
| [<span data-ttu-id="b6cd4-127">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6cd4-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b6cd4-128">Нет</span><span class="sxs-lookup"><span data-stu-id="b6cd4-128">no</span></span>        |
| [<span data-ttu-id="b6cd4-129">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6cd4-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b6cd4-130">Нет</span><span class="sxs-lookup"><span data-stu-id="b6cd4-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b6cd4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b6cd4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6cd4-132">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6cd4-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




