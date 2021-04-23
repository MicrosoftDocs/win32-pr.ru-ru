---
title: texm3x3-PS
description: Выполняет умножение матрицы 3x3 при использовании в сочетании с двумя инструкциями texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983837"
---
# <a name="texm3x3---ps"></a><span data-ttu-id="f578c-103">texm3x3-PS</span><span class="sxs-lookup"><span data-stu-id="f578c-103">texm3x3 - ps</span></span>

<span data-ttu-id="f578c-104">Выполняет умножение матрицы 3x3 при использовании в сочетании с двумя инструкциями [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="f578c-104">Performs a 3x3 matrix multiply when used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f578c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f578c-105">Syntax</span></span>



| <span data-ttu-id="f578c-106">texm3x3 DST, src</span><span class="sxs-lookup"><span data-stu-id="f578c-106">texm3x3 dst, src</span></span> |
|------------------|



 

<span data-ttu-id="f578c-107">где</span><span class="sxs-lookup"><span data-stu-id="f578c-107">where</span></span>

-   <span data-ttu-id="f578c-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="f578c-108">dst is the destination register.</span></span>
-   <span data-ttu-id="f578c-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f578c-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f578c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="f578c-110">Remarks</span></span>



| <span data-ttu-id="f578c-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="f578c-111">Pixel shader versions</span></span> | <span data-ttu-id="f578c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="f578c-112">1\_1</span></span> | <span data-ttu-id="f578c-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="f578c-113">1\_2</span></span> | <span data-ttu-id="f578c-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f578c-114">1\_3</span></span> | <span data-ttu-id="f578c-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="f578c-115">1\_4</span></span> | <span data-ttu-id="f578c-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f578c-116">2\_0</span></span> | <span data-ttu-id="f578c-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f578c-117">2\_x</span></span> | <span data-ttu-id="f578c-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f578c-118">2\_sw</span></span> | <span data-ttu-id="f578c-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f578c-119">3\_0</span></span> | <span data-ttu-id="f578c-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f578c-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f578c-121">texm3x3</span><span class="sxs-lookup"><span data-stu-id="f578c-121">texm3x3</span></span>               |      | <span data-ttu-id="f578c-122">x</span><span class="sxs-lookup"><span data-stu-id="f578c-122">x</span></span>    | <span data-ttu-id="f578c-123">x</span><span class="sxs-lookup"><span data-stu-id="f578c-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="f578c-124">Эта инструкция аналогична инструкции [texm3x3tex-PS](texm3x3tex---ps.md) без поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="f578c-124">This instruction is the same as the [texm3x3tex - ps](texm3x3tex---ps.md) instruction, without the texture lookup.</span></span>

<span data-ttu-id="f578c-125">Эта инструкция используется в качестве завершающей из трех инструкций, представляющих операцию умножения матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="f578c-125">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation.</span></span> <span data-ttu-id="f578c-126">Матрица 3x3 состоит из координат текстуры третьего этапа текстуры и двух предшествующих стадий текстуры.</span><span class="sxs-lookup"><span data-stu-id="f578c-126">The 3x3 matrix is comprised of the texture coordinates of the third texture stage, and by the two preceding texture stages.</span></span> <span data-ttu-id="f578c-127">Любая текстура, назначенная любому из трех стадий текстуры, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f578c-127">Any texture assigned to any of the three texture stages is ignored.</span></span>

<span data-ttu-id="f578c-128">Эта инструкция должна использоваться с двумя инструкциями texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="f578c-128">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="f578c-129">Регистры текстур должны следовать следующей последовательности.</span><span class="sxs-lookup"><span data-stu-id="f578c-129">Texture registers must follow the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



<span data-ttu-id="f578c-130">Ниже приведены более подробные сведения о том, как выполняется умножение 3X3.</span><span class="sxs-lookup"><span data-stu-id="f578c-130">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="f578c-131">Первая инструкция texm3x3pad выполняет первую строку умножения<sup>, чтобы найти u.</sup></span><span class="sxs-lookup"><span data-stu-id="f578c-131">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="f578c-132">u<sup>"</sup> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f578c-132">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="f578c-133">Вторая инструкция texm3x3pad выполняет вторую строку умножения, чтобы<sup>найти v.</sup></span><span class="sxs-lookup"><span data-stu-id="f578c-133">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="f578c-134">v<sup>'</sup> = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f578c-134">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="f578c-135">Инструкция texm3x3tex выполняет третью строку умножения, чтобы<sup>найти w.</sup></span><span class="sxs-lookup"><span data-stu-id="f578c-135">The texm3x3tex instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="f578c-136">w<sup>"</sup> = TextureCoordinates (этап m + 2)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="f578c-136">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="f578c-137">Поместите результат матрицы в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="f578c-137">Place the result of the matrix multiply in the destination register.</span></span>

<span data-ttu-id="f578c-138">t (m + 2)<sub>RGBA</sub> =<sup>(u,</sup> <sup>v, w, 1</sup> )<sup></sup></span><span class="sxs-lookup"><span data-stu-id="f578c-138">t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f578c-139">См. также</span><span class="sxs-lookup"><span data-stu-id="f578c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f578c-140">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="f578c-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




