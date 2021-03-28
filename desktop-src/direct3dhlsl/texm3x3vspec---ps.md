---
title: texm3x3vspec-PS
description: Выполняет умножение матрицы 3x3 и использует результат для выполнения поиска текстур.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987085"
---
# <a name="texm3x3vspec---ps"></a><span data-ttu-id="eb1e9-103">texm3x3vspec-PS</span><span class="sxs-lookup"><span data-stu-id="eb1e9-103">texm3x3vspec - ps</span></span>

<span data-ttu-id="eb1e9-104">Выполняет умножение матрицы 3x3 и использует результат для выполнения поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-104">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="eb1e9-105">Его можно использовать для отражения отражений и для сопоставления среды, если вектор-Ray не является константой.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-105">This can be used for specular reflection and environment mapping where the eye-ray vector is not constant.</span></span> <span data-ttu-id="eb1e9-106">texm3x3vspec необходимо использовать в сочетании с двумя инструкциями [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="eb1e9-106">texm3x3vspec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span> <span data-ttu-id="eb1e9-107">Если для глаза-Ray используется константа, инструкция [texm3x3spec-PS](texm3x3spec---ps.md) выполняет ту же матрицу умножения и поиск текстур.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-107">If the eye-ray vector is constant, the [texm3x3spec - ps](texm3x3spec---ps.md) instruction will perform the same matrix multiply and texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb1e9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb1e9-108">Syntax</span></span>



| <span data-ttu-id="eb1e9-109">texm3x3vspec DST, src</span><span class="sxs-lookup"><span data-stu-id="eb1e9-109">texm3x3vspec dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="eb1e9-110">где</span><span class="sxs-lookup"><span data-stu-id="eb1e9-110">where</span></span>

-   <span data-ttu-id="eb1e9-111">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-111">dst is the destination register.</span></span>
-   <span data-ttu-id="eb1e9-112">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-112">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb1e9-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb1e9-113">Remarks</span></span>



| <span data-ttu-id="eb1e9-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="eb1e9-114">Pixel shader versions</span></span> | <span data-ttu-id="eb1e9-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="eb1e9-115">1\_1</span></span> | <span data-ttu-id="eb1e9-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="eb1e9-116">1\_2</span></span> | <span data-ttu-id="eb1e9-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="eb1e9-117">1\_3</span></span> | <span data-ttu-id="eb1e9-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="eb1e9-118">1\_4</span></span> | <span data-ttu-id="eb1e9-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eb1e9-119">2\_0</span></span> | <span data-ttu-id="eb1e9-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="eb1e9-120">2\_x</span></span> | <span data-ttu-id="eb1e9-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="eb1e9-121">2\_sw</span></span> | <span data-ttu-id="eb1e9-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eb1e9-122">3\_0</span></span> | <span data-ttu-id="eb1e9-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="eb1e9-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="eb1e9-124">texm3x3vspec</span><span class="sxs-lookup"><span data-stu-id="eb1e9-124">texm3x3vspec</span></span>          | <span data-ttu-id="eb1e9-125">x</span><span class="sxs-lookup"><span data-stu-id="eb1e9-125">x</span></span>    | <span data-ttu-id="eb1e9-126">x</span><span class="sxs-lookup"><span data-stu-id="eb1e9-126">x</span></span>    | <span data-ttu-id="eb1e9-127">x</span><span class="sxs-lookup"><span data-stu-id="eb1e9-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="eb1e9-128">Эта инструкция выполняет последнюю строку операции умножения матрицы 3x3, интерпретирует полученный вектор в качестве обычного вектора для отражения вектора с глазами-Ray, а затем использует отраженный вектор в качестве адреса текстуры для поиска текстуры.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-128">This instruction performs the final row of a 3x3 matrix multiply operation, interprets the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector as a texture address for a texture lookup.</span></span> <span data-ttu-id="eb1e9-129">Он работает так же, как [texm3x3spec-PS](texm3x3spec---ps.md), за исключением того, что вектор глаза-Ray взят из четвертого компонента координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-129">It works just like [texm3x3spec - ps](texm3x3spec---ps.md), except that the eye-ray vector is taken from the fourth component of the texture coordinates.</span></span> <span data-ttu-id="eb1e9-130">Матрица 3x3, как правило, полезна для ориентации обычного вектора на правильное пространство тангенса для отрисовки поверхности.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-130">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="eb1e9-131">Матрица 3x3 состоит из координат текстуры третьего этапа текстуры и двух предшествующих стадий текстуры.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-131">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="eb1e9-132">Полученный вектор после отражения (УВВ) используется для выборки текстуры на этапе 3.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-132">The resulting post-reflection vector (UVW) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="eb1e9-133">Любая текстура, назначенная предшествующим двум стадиям текстуры, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-133">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="eb1e9-134">Эта инструкция должна использоваться с инструкцией texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-134">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="eb1e9-135">Регистры текстур должны использовать следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-135">Texture registers must use the following sequence.</span></span>


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



<span data-ttu-id="eb1e9-136">Первая инструкция texm3x3pad выполняет первую строку умножения<sup>, чтобы найти u.</sup></span><span class="sxs-lookup"><span data-stu-id="eb1e9-136">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="eb1e9-137">u<sup>"</sup> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="eb1e9-137">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n) <sub>RGB</sub></span></span>

<span data-ttu-id="eb1e9-138">Вторая инструкция texm3x3pad выполняет вторую строку умножения, чтобы<sup>найти v.</sup></span><span class="sxs-lookup"><span data-stu-id="eb1e9-138">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="eb1e9-139">v<sup>'</sup> = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="eb1e9-139">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="eb1e9-140">Инструкция texm3x3spec выполняет третью строку умножения, чтобы<sup>найти w.</sup></span><span class="sxs-lookup"><span data-stu-id="eb1e9-140">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="eb1e9-141">w<sup>"</sup> = TextureCoordinates (этап m + 2)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="eb1e9-141">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="eb1e9-142">Инструкция texm3x3vspec также выполняет вычисление отражения.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-142">The texm3x3vspec instruction also does a reflection calculation.</span></span>

<span data-ttu-id="eb1e9-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E</span><span class="sxs-lookup"><span data-stu-id="eb1e9-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="eb1e9-144">где значение обычного N задается</span><span class="sxs-lookup"><span data-stu-id="eb1e9-144">// where the normal N is given by</span></span>

<span data-ttu-id="eb1e9-145">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="eb1e9-145">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="eb1e9-146">и глаз. вектор E передается</span><span class="sxs-lookup"><span data-stu-id="eb1e9-146">// and the eye-ray vector E is given by</span></span>

<span data-ttu-id="eb1e9-147">E = (TextureCoordinates (этап m)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="eb1e9-147">// E = (TextureCoordinates(stage m)<sub>Q</sub> ,</span></span>

<span data-ttu-id="eb1e9-148">TextureCoordinates (этап m + 1)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="eb1e9-148">// TextureCoordinates(stage m+1)<sub>Q</sub> ,</span></span>

<span data-ttu-id="eb1e9-149">TextureCoordinates (этап m + 2)<sub>Q</sub> )</span><span class="sxs-lookup"><span data-stu-id="eb1e9-149">// TextureCoordinates(stage m+2)<sub>Q</sub> )</span></span>

<span data-ttu-id="eb1e9-150">Наконец, примеры инструкций texm3x3vspec t (m + 2) с (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) и сохраняют результат в t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="eb1e9-150">Lastly, the texm3x3vspec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>)and stores the result in t(m+2).</span></span>

<span data-ttu-id="eb1e9-151">t (m + 2)<sub>RGBA</sub> = текстуресампле (этап m + 2)<sub>RGBA</sub> с использованием (<sup>u, v, w</sup> )<sup>в</sup> качестве координат<sup></sup></span><span class="sxs-lookup"><span data-stu-id="eb1e9-151">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="eb1e9-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="eb1e9-152">Examples</span></span>

<span data-ttu-id="eb1e9-153">Ниже приведен пример шейдера с идентифицированными картами текстур и идентифицированными стадиями текстуры.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-153">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



<span data-ttu-id="eb1e9-154">Для этого примера требуется следующая Настройка этапа текстуры.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-154">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="eb1e9-155">Этапу 0 назначается Текстурная схема с обычными данными.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-155">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="eb1e9-156">Часто это называется картой выпуклости.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-156">This is often referred to as a bump map.</span></span> <span data-ttu-id="eb1e9-157">Для каждого шаг текселя данные имеют (XYZ) нормали.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-157">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="eb1e9-158">Координаты текстуры на этапе n определяют способ выборки этой обычной схемы.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-158">Texture coordinates at stage n defines how to sample this normal map.</span></span>
-   <span data-ttu-id="eb1e9-159">Набор координат текстуры m назначается строке 1 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-159">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="eb1e9-160">Любая текстура, назначенная этапу m, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-160">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="eb1e9-161">Набор координат текстуры m + 1 назначается строке 2 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-161">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="eb1e9-162">Любая текстура, назначенная этапу m + 1, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-162">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="eb1e9-163">Набор координат текстуры m + 2 назначается строке 3 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-163">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="eb1e9-164">Этапу m + 2 назначается том или текстура текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-164">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="eb1e9-165">Текстура предоставляет данные цвета (RGBA).</span><span class="sxs-lookup"><span data-stu-id="eb1e9-165">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="eb1e9-166">В инструкции четвертого компонента (q) данных координат текстуры на этапах m, m + 1 и m + 2 передается элемент «глаз» вектора E.</span><span class="sxs-lookup"><span data-stu-id="eb1e9-166">The eye-ray vector E is passed into the instruction in the fourth component (q) of the texture coordinate data at stages m, m+1, and m+2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb1e9-167">См. также</span><span class="sxs-lookup"><span data-stu-id="eb1e9-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb1e9-168">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="eb1e9-168">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




