---
title: texm3x3spec-PS
description: Выполняет умножение матрицы 3x3 и использует результат для выполнения поиска текстур. Это можно использовать для отражения отражений и сопоставления среды. texm3x3spec необходимо использовать в сочетании с двумя инструкциями texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412163"
---
# <a name="texm3x3spec---ps"></a><span data-ttu-id="6fdb4-105">texm3x3spec-PS</span><span class="sxs-lookup"><span data-stu-id="6fdb4-105">texm3x3spec - ps</span></span>

<span data-ttu-id="6fdb4-106">Выполняет умножение матрицы 3x3 и использует результат для выполнения поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-106">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="6fdb4-107">Это можно использовать для отражения отражений и сопоставления среды.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-107">This can be used for specular reflection and environment mapping.</span></span> <span data-ttu-id="6fdb4-108">texm3x3spec необходимо использовать в сочетании с двумя инструкциями [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="6fdb4-108">texm3x3spec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdb4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fdb4-109">Syntax</span></span>



| <span data-ttu-id="6fdb4-110">texm3x3spec DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="6fdb4-110">texm3x3spec dst, src0, src1</span></span> |
|-----------------------------|



 

<span data-ttu-id="6fdb4-111">где</span><span class="sxs-lookup"><span data-stu-id="6fdb4-111">where</span></span>

-   <span data-ttu-id="6fdb4-112">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-112">dst is the destination register.</span></span>
-   <span data-ttu-id="6fdb4-113">src0 и src1 являются исходными регистрами.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-113">src0 and src1 are source registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fdb4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6fdb4-114">Remarks</span></span>



| <span data-ttu-id="6fdb4-115">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="6fdb4-115">Pixel shader versions</span></span> | <span data-ttu-id="6fdb4-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="6fdb4-116">1\_1</span></span> | <span data-ttu-id="6fdb4-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="6fdb4-117">1\_2</span></span> | <span data-ttu-id="6fdb4-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6fdb4-118">1\_3</span></span> | <span data-ttu-id="6fdb4-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="6fdb4-119">1\_4</span></span> | <span data-ttu-id="6fdb4-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fdb4-120">2\_0</span></span> | <span data-ttu-id="6fdb4-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6fdb4-121">2\_x</span></span> | <span data-ttu-id="6fdb4-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fdb4-122">2\_sw</span></span> | <span data-ttu-id="6fdb4-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fdb4-123">3\_0</span></span> | <span data-ttu-id="6fdb4-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fdb4-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6fdb4-125">texm3x3spec</span><span class="sxs-lookup"><span data-stu-id="6fdb4-125">texm3x3spec</span></span>           | <span data-ttu-id="6fdb4-126">x</span><span class="sxs-lookup"><span data-stu-id="6fdb4-126">x</span></span>    | <span data-ttu-id="6fdb4-127">x</span><span class="sxs-lookup"><span data-stu-id="6fdb4-127">x</span></span>    | <span data-ttu-id="6fdb4-128">x</span><span class="sxs-lookup"><span data-stu-id="6fdb4-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="6fdb4-129">Эта инструкция выполняет последнюю строку матрицы 3x3, использует полученный вектор в качестве обычного вектора для отражения вектора с глазом, а затем использует отраженный вектор для выполнения поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-129">This instruction performs the final row of a 3x3 matrix multiply, uses the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector to perform a texture lookup.</span></span> <span data-ttu-id="6fdb4-130">Шейдер считывает вектор глаза-Ray из регистра констант.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-130">The shader reads the eye-ray vector from a constant register.</span></span> <span data-ttu-id="6fdb4-131">Матрица 3x3, как правило, полезна для ориентации обычного вектора на правильное пространство тангенса для отрисовки поверхности.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="6fdb4-132">Матрица 3x3 состоит из координат текстуры третьего этапа текстуры и двух предшествующих стадий текстуры.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-132">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="6fdb4-133">Полученный Вектор отражения POST (u, v, w) используется для выборки текстуры на заключительном этапе текстуры.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-133">The resulting post reflection vector (u,v,w) is used to sample the texture on the final texture stage.</span></span> <span data-ttu-id="6fdb4-134">Любая текстура, назначенная предшествующим двум стадиям текстуры, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-134">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="6fdb4-135">Эта инструкция должна использоваться с двумя инструкциями texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-135">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="6fdb4-136">Регистры текстур должны использовать следующую последовательность.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-136">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



<span data-ttu-id="6fdb4-137">Первая инструкция texm3x3pad выполняет первую строку умножения<sup>, чтобы найти u.</sup></span><span class="sxs-lookup"><span data-stu-id="6fdb4-137">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="6fdb4-138">u<sup>"</sup> = TextureCoordinates (этап m)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="6fdb4-138">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="6fdb4-139">Вторая инструкция texm3x3pad выполняет вторую строку умножения, чтобы<sup>найти v.</sup></span><span class="sxs-lookup"><span data-stu-id="6fdb4-139">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="6fdb4-140">v<sup>'</sup> = TextureCoordinates (этап m + 1)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="6fdb4-140">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="6fdb4-141">Инструкция texm3x3spec выполняет третью строку умножения, чтобы<sup>найти w.</sup></span><span class="sxs-lookup"><span data-stu-id="6fdb4-141">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="6fdb4-142">w<sup>"</sup> = TextureCoordinates (этап m + 2)<sub>УВВ</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="6fdb4-142">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="6fdb4-143">Затем инструкция texm3x3spec выполняет вычисление отражения.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-143">The texm3x3spec instruction then does a reflection calculation.</span></span>

<span data-ttu-id="6fdb4-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E</span><span class="sxs-lookup"><span data-stu-id="6fdb4-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="6fdb4-145">где значение обычного N задается</span><span class="sxs-lookup"><span data-stu-id="6fdb4-145">// where the normal N is given by</span></span>

<span data-ttu-id="6fdb4-146">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="6fdb4-146">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="6fdb4-147">и глаз. вектор E передается регистром констант</span><span class="sxs-lookup"><span data-stu-id="6fdb4-147">// and the eye-ray vector E is given by the constant register</span></span>

<span data-ttu-id="6fdb4-148">E = c \# (любой регистр константы — можно использовать C0, C1, C2 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="6fdb4-148">// E = c\# (Any constant register--c0, c1, c2, etc.--can be used)</span></span>

<span data-ttu-id="6fdb4-149">Наконец, примеры инструкций texm3x3spec t (m + 2) с (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) и сохраняют результат в t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="6fdb4-149">Lastly, the texm3x3spec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="6fdb4-150">t (m + 2)<sub>RGBA</sub> = текстуресампле (этап m + 2)<sub>RGBA</sub> с использованием (<sup>u, v, w</sup> )<sup>в</sup> качестве координат<sup></sup></span><span class="sxs-lookup"><span data-stu-id="6fdb4-150">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="6fdb4-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="6fdb4-151">Examples</span></span>

<span data-ttu-id="6fdb4-152">Ниже приведен пример шейдера с текстурными картами и идентифицированными стадиями текстуры.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-152">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



<span data-ttu-id="6fdb4-153">Для этого примера требуется следующая Настройка этапа текстуры.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-153">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="6fdb4-154">Этапу 0 назначается Текстурная схема с обычными данными.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-154">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="6fdb4-155">Часто это называется картой выпуклости.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-155">This is often referred to as a bump map.</span></span> <span data-ttu-id="6fdb4-156">Для каждого шаг текселя данные имеют (XYZ) нормали.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-156">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="6fdb4-157">Координаты текстуры на этапе n определяют, где следует выделать образец этой обычной схемы.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-157">Texture coordinates at stage n defines where to sample this normal map.</span></span>
-   <span data-ttu-id="6fdb4-158">Набор координат текстуры m назначается строке 1 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-158">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="6fdb4-159">Любая текстура, назначенная этапу m, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-159">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="6fdb4-160">Набор координат текстуры m + 1 назначается строке 2 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-160">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="6fdb4-161">Любая текстура, назначенная этапу m + 1, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-161">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="6fdb4-162">Набор координат текстуры m + 2 назначается строке 3 матрицы 3X3.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-162">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="6fdb4-163">Этапу m + 2 назначается том или текстура текстуры Куба.</span><span class="sxs-lookup"><span data-stu-id="6fdb4-163">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="6fdb4-164">Текстура предоставляет данные цвета (RGBA).</span><span class="sxs-lookup"><span data-stu-id="6fdb4-164">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="6fdb4-165">Глаз. вектор E имеет постоянный регистр E = c \# .</span><span class="sxs-lookup"><span data-stu-id="6fdb4-165">The eye-ray vector E is given by a constant register E = c\#.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fdb4-166">См. также</span><span class="sxs-lookup"><span data-stu-id="6fdb4-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fdb4-167">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="6fdb4-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




