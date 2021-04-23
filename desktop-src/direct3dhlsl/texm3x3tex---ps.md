---
title: texm3x3tex-PS
description: Выполняет умножение матрицы 3x3 и использует результат для поиска текстур. texm3x3tex должен использоваться с двумя инструкциями texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412251"
---
# <a name="texm3x3tex---ps"></a><span data-ttu-id="703cb-104">texm3x3tex-PS</span><span class="sxs-lookup"><span data-stu-id="703cb-104">texm3x3tex - ps</span></span>

<span data-ttu-id="703cb-105">Выполняет умножение матрицы 3x3 и использует результат для поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="703cb-105">Performs a 3x3 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="703cb-106">texm3x3tex должен использоваться с двумя инструкциями [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="703cb-106">texm3x3tex must be used with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="703cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="703cb-107">Syntax</span></span>



| <span data-ttu-id="703cb-108">texm3x3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="703cb-108">texm3x3tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="703cb-109">где</span><span class="sxs-lookup"><span data-stu-id="703cb-109">where</span></span>

-   <span data-ttu-id="703cb-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="703cb-110">dst is the destination register.</span></span>
-   <span data-ttu-id="703cb-111">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="703cb-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="703cb-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="703cb-112">Remarks</span></span>



| <span data-ttu-id="703cb-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="703cb-113">Pixel shader versions</span></span> | <span data-ttu-id="703cb-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="703cb-114">1\_1</span></span> | <span data-ttu-id="703cb-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="703cb-115">1\_2</span></span> | <span data-ttu-id="703cb-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="703cb-116">1\_3</span></span> | <span data-ttu-id="703cb-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="703cb-117">1\_4</span></span> | <span data-ttu-id="703cb-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="703cb-118">2\_0</span></span> | <span data-ttu-id="703cb-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="703cb-119">2\_x</span></span> | <span data-ttu-id="703cb-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="703cb-120">2\_sw</span></span> | <span data-ttu-id="703cb-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="703cb-121">3\_0</span></span> | <span data-ttu-id="703cb-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="703cb-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="703cb-123">texm3x3tex</span><span class="sxs-lookup"><span data-stu-id="703cb-123">texm3x3tex</span></span>            | <span data-ttu-id="703cb-124">x</span><span class="sxs-lookup"><span data-stu-id="703cb-124">x</span></span>    | <span data-ttu-id="703cb-125">x</span><span class="sxs-lookup"><span data-stu-id="703cb-125">x</span></span>    | <span data-ttu-id="703cb-126">x</span><span class="sxs-lookup"><span data-stu-id="703cb-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="703cb-127">Эта инструкция используется в качестве завершающей из трех инструкций, представляющих операцию умножения матрицы 3x3, за которой следует Поиск текстуры.</span><span class="sxs-lookup"><span data-stu-id="703cb-127">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation, followed by a texture lookup.</span></span> <span data-ttu-id="703cb-128">Матрица 3x3 состоит из координат текстуры третьего этапа текстуры и двух предшествующих стадий текстуры.</span><span class="sxs-lookup"><span data-stu-id="703cb-128">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="703cb-129">Полученный вектор с тремя компонентами (u, v, w) используется для выборки текстуры на этапе 3.</span><span class="sxs-lookup"><span data-stu-id="703cb-129">The resulting three-component vector (u,v,w) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="703cb-130">Любая текстура, назначенная предшествующим двум стадиям текстуры, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="703cb-130">Any texture assigned to the preceding two texture stages is ignored.</span></span> <span data-ttu-id="703cb-131">Матрица 3x3, как правило, полезна для ориентации обычного вектора на правильное пространство тангенса для отрисовки поверхности.</span><span class="sxs-lookup"><span data-stu-id="703cb-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="703cb-132">Эта инструкция должна использоваться с инструкцией texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="703cb-132">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="703cb-133">Регистры текстур должны использовать следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="703cb-133">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



<span data-ttu-id="703cb-134">Ниже приведены более подробные сведения о том, как выполняется умножение 3X3.</span><span class="sxs-lookup"><span data-stu-id="703cb-134">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="703cb-135">Первая инструкция texm3x3pad выполняет первую строку умножения<sup>, чтобы найти u.</sup></span><span class="sxs-lookup"><span data-stu-id="703cb-135">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="703cb-136">u<sup>"</sup> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="703cb-136">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="703cb-137">Вторая инструкция texm3x3pad выполняет вторую строку умножения, чтобы<sup>найти v.</sup></span><span class="sxs-lookup"><span data-stu-id="703cb-137">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="703cb-138">v<sup>'</sup> = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="703cb-138">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="703cb-139">Инструкция texm3x3spec выполняет третью строку умножения, чтобы<sup>найти w.</sup></span><span class="sxs-lookup"><span data-stu-id="703cb-139">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="703cb-140">w<sup>"</sup> = TextureCoordinates (этап m + 2)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="703cb-140">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="703cb-141">Наконец, примеры инструкций texm3x3tex t (m + 2) с (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) и сохраняют результат в t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="703cb-141">Lastly, the texm3x3tex instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="703cb-142">t (m + 2)<sub>RGBA</sub> = текстуресампле (этап m + 2)<sub>RGBA</sub> с использованием (<sup>u, v, w</sup> )<sup>в</sup> качестве координат.<sup></sup></span><span class="sxs-lookup"><span data-stu-id="703cb-142">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates.</span></span>

## <a name="examples"></a><span data-ttu-id="703cb-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="703cb-143">Examples</span></span>

<span data-ttu-id="703cb-144">Ниже приведен пример шейдера с идентифицированными картами текстур и идентифицированными стадиями текстуры.</span><span class="sxs-lookup"><span data-stu-id="703cb-144">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



<span data-ttu-id="703cb-145">Для этого примера требуется следующая Настройка этапа текстуры.</span><span class="sxs-lookup"><span data-stu-id="703cb-145">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="703cb-146">Этапу 0 назначается Текстурная схема с обычными данными.</span><span class="sxs-lookup"><span data-stu-id="703cb-146">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="703cb-147">Часто это называется картой выпуклости.</span><span class="sxs-lookup"><span data-stu-id="703cb-147">This is often referred to as a bump map.</span></span> <span data-ttu-id="703cb-148">Для каждого шаг текселя данные имеют (XYZ) нормали.</span><span class="sxs-lookup"><span data-stu-id="703cb-148">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="703cb-149">Набор координат текстуры 0 определяет способ выборки этой обычной схемы.</span><span class="sxs-lookup"><span data-stu-id="703cb-149">Texture coordinate set 0 defines how to sample this normal map.</span></span>
-   <span data-ttu-id="703cb-150">Набор координат текстуры 1 назначается строке 1 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="703cb-150">Texture coordinate set 1 is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="703cb-151">Любая текстура, назначенная этапу 1, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="703cb-151">Any texture assigned to stage 1 is ignored.</span></span>
-   <span data-ttu-id="703cb-152">Набор координат текстуры 2 назначается строке 2 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="703cb-152">Texture coordinate set 2 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="703cb-153">Любая текстура, назначенная этапу 2, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="703cb-153">Any texture assigned to stage 2 is ignored.</span></span>
-   <span data-ttu-id="703cb-154">Набор координат текстуры 3 назначается строке 3 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="703cb-154">Texture coordinate set 3 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="703cb-155">Для уточняющего запроса преобразованного трехмерного вектора необходимо задать для параметра "этап 3" значение "уровень" или "текстура Куба".</span><span class="sxs-lookup"><span data-stu-id="703cb-155">A volume or cube texture should be set to stage 3 for lookup by the transformed 3D vector.</span></span>

## <a name="related-topics"></a><span data-ttu-id="703cb-156">См. также</span><span class="sxs-lookup"><span data-stu-id="703cb-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="703cb-157">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="703cb-157">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




