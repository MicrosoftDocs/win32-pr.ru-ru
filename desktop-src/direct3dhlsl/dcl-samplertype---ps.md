---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Объявите образец построителя текстуры.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069381"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="4eea9-103">дкл \_ самплертипе (SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="4eea9-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="4eea9-104">Объявите образец построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="4eea9-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eea9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4eea9-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="4eea9-106">дкл \_ самплертипе s\#</span><span class="sxs-lookup"><span data-stu-id="4eea9-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="4eea9-107">где:</span><span class="sxs-lookup"><span data-stu-id="4eea9-107">where:</span></span>

-   <span data-ttu-id="4eea9-108">\_Самплертипе определяет тип данных образца.</span><span class="sxs-lookup"><span data-stu-id="4eea9-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="4eea9-109">Определяет, сколько координат требуется для каждой координаты текстуры при выборки.</span><span class="sxs-lookup"><span data-stu-id="4eea9-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="4eea9-110">Определены следующие измерения координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="4eea9-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="4eea9-111">\_двухмерном</span><span class="sxs-lookup"><span data-stu-id="4eea9-111">\_2d</span></span>
    -   <span data-ttu-id="4eea9-112">\_Куба</span><span class="sxs-lookup"><span data-stu-id="4eea9-112">\_cube</span></span>
    -   <span data-ttu-id="4eea9-113">\_тома</span><span class="sxs-lookup"><span data-stu-id="4eea9-113">\_volume</span></span>
-   <span data-ttu-id="4eea9-114">s \# определяет образец, где s — это аббревиатура для образца, а \# — номер образца.</span><span class="sxs-lookup"><span data-stu-id="4eea9-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="4eea9-115">Пробы являются псевдо-регистром, так как вы не можете напрямую считывать их или записывать.</span><span class="sxs-lookup"><span data-stu-id="4eea9-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eea9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4eea9-116">Remarks</span></span>



| <span data-ttu-id="4eea9-117">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="4eea9-117">Pixel shader versions</span></span> | <span data-ttu-id="4eea9-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="4eea9-118">1\_1</span></span> | <span data-ttu-id="4eea9-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="4eea9-119">1\_2</span></span> | <span data-ttu-id="4eea9-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4eea9-120">1\_3</span></span> | <span data-ttu-id="4eea9-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="4eea9-121">1\_4</span></span> | <span data-ttu-id="4eea9-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4eea9-122">2\_0</span></span> | <span data-ttu-id="4eea9-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4eea9-123">2\_x</span></span> | <span data-ttu-id="4eea9-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4eea9-124">2\_sw</span></span> | <span data-ttu-id="4eea9-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4eea9-125">3\_0</span></span> | <span data-ttu-id="4eea9-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4eea9-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4eea9-127">дкл \_ самплертипе</span><span class="sxs-lookup"><span data-stu-id="4eea9-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="4eea9-128">x</span><span class="sxs-lookup"><span data-stu-id="4eea9-128">x</span></span>    | <span data-ttu-id="4eea9-129">x</span><span class="sxs-lookup"><span data-stu-id="4eea9-129">x</span></span>    | <span data-ttu-id="4eea9-130">x</span><span class="sxs-lookup"><span data-stu-id="4eea9-130">x</span></span>     | <span data-ttu-id="4eea9-131">x</span><span class="sxs-lookup"><span data-stu-id="4eea9-131">x</span></span>    | <span data-ttu-id="4eea9-132">x</span><span class="sxs-lookup"><span data-stu-id="4eea9-132">x</span></span>     |



 

<span data-ttu-id="4eea9-133">Все \_ инструкции самплертипе дкл должны располагаться перед первой исполняемой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="4eea9-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="4eea9-134">Например, .</span><span class="sxs-lookup"><span data-stu-id="4eea9-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="4eea9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="4eea9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eea9-136">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="4eea9-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




