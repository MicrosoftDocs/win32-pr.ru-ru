---
title: тексдепс-PS
description: Вычислите значения глубины, которые будут использоваться в тесте сравнения буферов глубины для этого пикселя.
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103889988"
---
# <a name="texdepth---ps"></a><span data-ttu-id="2e7b3-103">тексдепс-PS</span><span class="sxs-lookup"><span data-stu-id="2e7b3-103">texdepth - ps</span></span>

<span data-ttu-id="2e7b3-104">Вычислите значения глубины, которые будут использоваться в тесте сравнения буферов глубины для этого пикселя.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-104">Calculate depth values to be used in the depth buffer comparison test for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e7b3-105">Syntax</span></span>



| <span data-ttu-id="2e7b3-106">тексдепс DST</span><span class="sxs-lookup"><span data-stu-id="2e7b3-106">texdepth dst</span></span> |
|--------------|



 

<span data-ttu-id="2e7b3-107">где</span><span class="sxs-lookup"><span data-stu-id="2e7b3-107">where</span></span>

-   <span data-ttu-id="2e7b3-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7b3-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e7b3-109">Remarks</span></span>



| <span data-ttu-id="2e7b3-110">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="2e7b3-110">Pixel shader versions</span></span> | <span data-ttu-id="2e7b3-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="2e7b3-111">1\_1</span></span> | <span data-ttu-id="2e7b3-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="2e7b3-112">1\_2</span></span> | <span data-ttu-id="2e7b3-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2e7b3-113">1\_3</span></span> | <span data-ttu-id="2e7b3-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="2e7b3-114">1\_4</span></span> | <span data-ttu-id="2e7b3-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e7b3-115">2\_0</span></span> | <span data-ttu-id="2e7b3-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2e7b3-116">2\_x</span></span> | <span data-ttu-id="2e7b3-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2e7b3-117">2\_sw</span></span> | <span data-ttu-id="2e7b3-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e7b3-118">3\_0</span></span> | <span data-ttu-id="2e7b3-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2e7b3-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2e7b3-120">тексдепс</span><span class="sxs-lookup"><span data-stu-id="2e7b3-120">texdepth</span></span>              |      |      |      | <span data-ttu-id="2e7b3-121">x</span><span class="sxs-lookup"><span data-stu-id="2e7b3-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="2e7b3-122">Эта инструкция использует R5. r/R5. g в тесте сравнения буферов глубины для этого пикселя.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-122">This instruction uses r5.r / r5.g in the depth buffer comparison test for this pixel.</span></span> <span data-ttu-id="2e7b3-123">Данные в синих и альфа-каналах игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-123">The data in the blue and alpha channels is ignored.</span></span> <span data-ttu-id="2e7b3-124">Если R5. g = 0, результат R5. r/R5. g = 1,0.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-124">If r5.g = 0, the result of r5.r / r5.g = 1.0.</span></span>

<span data-ttu-id="2e7b3-125">Временная регистрация R5 — единственный регистр, который может использовать эта инструкция.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-125">Temporary register r5 is the only register that this instruction can use.</span></span>

<span data-ttu-id="2e7b3-126">После выполнения этой инструкции временная регистрация R5 недоступна для дополнительного использования в шейдере.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-126">After executing this instruction, temporary register r5 is unavailable for additional use in the shader.</span></span>

<span data-ttu-id="2e7b3-127">При использовании множественной выборки использование этой инструкции исключает большую часть преимуществ буфера глубины более высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-127">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="2e7b3-128">Поскольку шейдер пикселей выполняется один раз для каждого пикселя, для каждого из сравниваемых тестов глубины должно использоваться одно значение глубины, полученное [texm3x2depth-PS](texm3x2depth---ps.md) или тексдепс.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-128">Because the pixel shader runs once per pixel, the single depth value output by [texm3x2depth - ps](texm3x2depth---ps.md) or texdepth will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="examples"></a><span data-ttu-id="2e7b3-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="2e7b3-129">Examples</span></span>

<span data-ttu-id="2e7b3-130">Ниже приведен пример использования тексдепс.</span><span class="sxs-lookup"><span data-stu-id="2e7b3-130">Here is an example using texdepth.</span></span>


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a><span data-ttu-id="2e7b3-131">См. также</span><span class="sxs-lookup"><span data-stu-id="2e7b3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e7b3-132">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="2e7b3-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




