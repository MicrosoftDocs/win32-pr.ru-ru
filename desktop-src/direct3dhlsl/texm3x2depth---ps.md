---
title: texm3x2depth-PS
description: Вычислите значение глубины, которое будет использоваться при тестировании глубины для этого пикселя.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983853"
---
# <a name="texm3x2depth---ps"></a><span data-ttu-id="0c706-103">texm3x2depth-PS</span><span class="sxs-lookup"><span data-stu-id="0c706-103">texm3x2depth - ps</span></span>

<span data-ttu-id="0c706-104">Вычислите значение глубины, которое будет использоваться при тестировании глубины для этого пикселя.</span><span class="sxs-lookup"><span data-stu-id="0c706-104">Calculate the depth value to be used in depth testing for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c706-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c706-105">Syntax</span></span>



| <span data-ttu-id="0c706-106">texm3x2depth DST, src</span><span class="sxs-lookup"><span data-stu-id="0c706-106">texm3x2depth dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="0c706-107">где</span><span class="sxs-lookup"><span data-stu-id="0c706-107">where</span></span>

-   <span data-ttu-id="0c706-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="0c706-108">dst is the destination register.</span></span>
-   <span data-ttu-id="0c706-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="0c706-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c706-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c706-110">Remarks</span></span>



| <span data-ttu-id="0c706-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="0c706-111">Pixel shader versions</span></span> | <span data-ttu-id="0c706-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="0c706-112">1\_1</span></span> | <span data-ttu-id="0c706-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="0c706-113">1\_2</span></span> | <span data-ttu-id="0c706-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0c706-114">1\_3</span></span> | <span data-ttu-id="0c706-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="0c706-115">1\_4</span></span> | <span data-ttu-id="0c706-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0c706-116">2\_0</span></span> | <span data-ttu-id="0c706-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0c706-117">2\_x</span></span> | <span data-ttu-id="0c706-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0c706-118">2\_sw</span></span> | <span data-ttu-id="0c706-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0c706-119">3\_0</span></span> | <span data-ttu-id="0c706-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0c706-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0c706-121">texm3x2depth</span><span class="sxs-lookup"><span data-stu-id="0c706-121">texm3x2depth</span></span>          |      |      | <span data-ttu-id="0c706-122">x</span><span class="sxs-lookup"><span data-stu-id="0c706-122">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="0c706-123">Эта инструкция должна использоваться с инструкцией [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0c706-123">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="0c706-124">При использовании этих двух инструкций регистры текстур должны использовать следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="0c706-124">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



<span data-ttu-id="0c706-125">Вычисление глубины выполняется после использования операции с продуктом с точкой для поиска z и w.</span><span class="sxs-lookup"><span data-stu-id="0c706-125">The depth calculation is done after using a dot product operation to find z and w.</span></span> <span data-ttu-id="0c706-126">Ниже приведены более подробные сведения о том, как выполняется вычисление глубины.</span><span class="sxs-lookup"><span data-stu-id="0c706-126">Here is more detail about how the depth calculation is accomplished.</span></span>

<span data-ttu-id="0c706-127">Инструкция texm3x2pad вычисляет z.</span><span class="sxs-lookup"><span data-stu-id="0c706-127">The texm3x2pad instruction calculates z.</span></span>

<span data-ttu-id="0c706-128">z = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0c706-128">z = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0c706-129">Инструкция texm3x2depth вычисляет w.</span><span class="sxs-lookup"><span data-stu-id="0c706-129">The texm3x2depth instruction calculates w.</span></span>

<span data-ttu-id="0c706-130">w = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0c706-130">w = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0c706-131">Вычислите глубину и сохраните результат в t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="0c706-131">Calculate depth and store the result in t(m+1).</span></span>


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



<span data-ttu-id="0c706-132">Вычисленная глубина помечена для использования в тесте глубины пикселя, заменяя существующее тестовое значение глубины для пикселя.</span><span class="sxs-lookup"><span data-stu-id="0c706-132">The calculated depth is tagged to be used in the depth test for the pixel, replacing the existing depth test value for the pixel.</span></span>

<span data-ttu-id="0c706-133">Не забудьте обозначить z/w в диапазоне (0-1).</span><span class="sxs-lookup"><span data-stu-id="0c706-133">Be sure to clamp z/w to be in the range of (0-1).</span></span> <span data-ttu-id="0c706-134">Если z/w находится за пределами этого диапазона, результат, хранящийся в буфере глубины, будет неопределенным.</span><span class="sxs-lookup"><span data-stu-id="0c706-134">If z/w is outside this range, the result stored in the depth buffer will be undefined.</span></span>

<span data-ttu-id="0c706-135">После выполнения texm3x2depth регистр t (m + 1) больше недоступен для использования в шейдере.</span><span class="sxs-lookup"><span data-stu-id="0c706-135">After running texm3x2depth, register t(m+1) is no longer available for use in the shader.</span></span>

<span data-ttu-id="0c706-136">При использовании множественной выборки использование этой инструкции исключает большую часть преимуществ буфера глубины более высокого разрешения.</span><span class="sxs-lookup"><span data-stu-id="0c706-136">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="0c706-137">Так как шейдер пикселей выполняется один раз для каждого пикселя, для каждого из сравниваемых тестов глубины должно использоваться одно значение глубины, полученное texm3x2depth или [тексдепс-PS](texdepth---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0c706-137">Because the pixel shader runs once per pixel, the single depth value output by texm3x2depth or [texdepth - ps](texdepth---ps.md) will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c706-138">См. также</span><span class="sxs-lookup"><span data-stu-id="0c706-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c706-139">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="0c706-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




