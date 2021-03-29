---
title: Выходные регистры
description: Выходные регистры
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996743"
---
# <a name="output-registers"></a><span data-ttu-id="354ca-103">Выходные регистры</span><span class="sxs-lookup"><span data-stu-id="354ca-103">Output Registers</span></span>

-   <span data-ttu-id="354ca-104">Регистр цвета вершин</span><span class="sxs-lookup"><span data-stu-id="354ca-104">Vertex Color Register</span></span>
-   <span data-ttu-id="354ca-105">Регистр тумана</span><span class="sxs-lookup"><span data-stu-id="354ca-105">Fog Register</span></span>
-   <span data-ttu-id="354ca-106">\_Регистр позиций</span><span class="sxs-lookup"><span data-stu-id="354ca-106">Position\_Register</span></span>
-   <span data-ttu-id="354ca-107">\_Регистр размера \_ точки</span><span class="sxs-lookup"><span data-stu-id="354ca-107">Point\_Size\_Register</span></span>
-   <span data-ttu-id="354ca-108">\_Регистр координаты \_ текстуры</span><span class="sxs-lookup"><span data-stu-id="354ca-108">Texture\_Coordinate\_Register</span></span>

<span data-ttu-id="354ca-109">Именам регистров предшествуют строчная буква o, указывающая, что выходные регистры доступны только на запись.</span><span class="sxs-lookup"><span data-stu-id="354ca-109">Register names are preceded by a lowercase letter o, indicating that the output registers are write-only.</span></span>

## <a name="vertex-color-register---od0-od1"></a><span data-ttu-id="354ca-110">Регистр цветов вершин — oD0, oD1</span><span class="sxs-lookup"><span data-stu-id="354ca-110">Vertex Color Register - oD0, oD1</span></span>

<span data-ttu-id="354ca-111">oD0 — это регистр рассеянного цвета.</span><span class="sxs-lookup"><span data-stu-id="354ca-111">oD0 is the diffuse color register.</span></span> <span data-ttu-id="354ca-112">oD1 — регистр отраженного цвета.</span><span class="sxs-lookup"><span data-stu-id="354ca-112">oD1 is the specular color register.</span></span> <span data-ttu-id="354ca-113">Значение oD0 интерполируются и записывается во входной цвет регистр 0 (v0) шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="354ca-113">The oD0 value is interpolated and is written to the input color register 0 (v0) of the pixel shader.</span></span> <span data-ttu-id="354ca-114">Значение oD1 интерполируются и записывается во входной цвет регистр 1 (v1) шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="354ca-114">The oD1 value is interpolated and written to the input color register 1 (v1) of the pixel shader.</span></span> <span data-ttu-id="354ca-115">Дополнительные сведения о цветовых регистрах шейдера пикселей см. в разделе registers.</span><span class="sxs-lookup"><span data-stu-id="354ca-115">For more information about pixel shader color registers, see Registers.</span></span>



| <span data-ttu-id="354ca-116">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="354ca-116">Vertex shader versions</span></span> | <span data-ttu-id="354ca-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="354ca-117">1\_1</span></span> | <span data-ttu-id="354ca-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-118">2\_0</span></span> | <span data-ttu-id="354ca-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-119">2\_sw</span></span> | <span data-ttu-id="354ca-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="354ca-120">2\_x</span></span> | <span data-ttu-id="354ca-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-121">3\_0</span></span> | <span data-ttu-id="354ca-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-122">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="354ca-123">Регистр цвета вершин</span><span class="sxs-lookup"><span data-stu-id="354ca-123">Vertex Color Register</span></span>  | <span data-ttu-id="354ca-124">x</span><span class="sxs-lookup"><span data-stu-id="354ca-124">x</span></span>    | <span data-ttu-id="354ca-125">x</span><span class="sxs-lookup"><span data-stu-id="354ca-125">x</span></span>    | <span data-ttu-id="354ca-126">x</span><span class="sxs-lookup"><span data-stu-id="354ca-126">x</span></span>     | <span data-ttu-id="354ca-127">x</span><span class="sxs-lookup"><span data-stu-id="354ca-127">x</span></span>    |      |       |



 

## <a name="fog-register---ofog"></a><span data-ttu-id="354ca-128">Регистр тумана — Офог</span><span class="sxs-lookup"><span data-stu-id="354ca-128">Fog Register - oFog</span></span>

<span data-ttu-id="354ca-129">Регистры значений выходных тумана.</span><span class="sxs-lookup"><span data-stu-id="354ca-129">The output fog value registers.</span></span> <span data-ttu-id="354ca-130">Значение — это коэффициент тумана для интерполяции, который затем направляется в таблицу тумана.</span><span class="sxs-lookup"><span data-stu-id="354ca-130">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="354ca-131">Используется только скалярный компонент x-компонента тумана.</span><span class="sxs-lookup"><span data-stu-id="354ca-131">Only the scalar x-component of the fog is used.</span></span> <span data-ttu-id="354ca-132">Перед передачей в средство программной прорисовки значения отправляются между нулем и единицей.</span><span class="sxs-lookup"><span data-stu-id="354ca-132">Values are clamped between zero and one before passing to the rasterizer.</span></span>



| <span data-ttu-id="354ca-133">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="354ca-133">Vertex shader versions</span></span> | <span data-ttu-id="354ca-134">1\_1</span><span class="sxs-lookup"><span data-stu-id="354ca-134">1\_1</span></span> | <span data-ttu-id="354ca-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-135">2\_0</span></span> | <span data-ttu-id="354ca-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-136">2\_sw</span></span> | <span data-ttu-id="354ca-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="354ca-137">2\_x</span></span> | <span data-ttu-id="354ca-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-138">3\_0</span></span> | <span data-ttu-id="354ca-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-139">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="354ca-140">Регистр тумана</span><span class="sxs-lookup"><span data-stu-id="354ca-140">Fog Register</span></span>           | <span data-ttu-id="354ca-141">x</span><span class="sxs-lookup"><span data-stu-id="354ca-141">x</span></span>    | <span data-ttu-id="354ca-142">x</span><span class="sxs-lookup"><span data-stu-id="354ca-142">x</span></span>    | <span data-ttu-id="354ca-143">x</span><span class="sxs-lookup"><span data-stu-id="354ca-143">x</span></span>     | <span data-ttu-id="354ca-144">x</span><span class="sxs-lookup"><span data-stu-id="354ca-144">x</span></span>    |      |       |



 

## <a name="position-register---opos"></a><span data-ttu-id="354ca-145">Регистр позиций — oPos</span><span class="sxs-lookup"><span data-stu-id="354ca-145">Position Register - oPos</span></span>

<span data-ttu-id="354ca-146">Регистрация расположения выходных данных.</span><span class="sxs-lookup"><span data-stu-id="354ca-146">The output position registers.</span></span> <span data-ttu-id="354ca-147">Значение является позицией в однородной вырезанной области.</span><span class="sxs-lookup"><span data-stu-id="354ca-147">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="354ca-148">Это значение должно быть записано шейдером вершин.</span><span class="sxs-lookup"><span data-stu-id="354ca-148">This value must be written by the vertex shader.</span></span>



| <span data-ttu-id="354ca-149">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="354ca-149">Vertex shader versions</span></span> | <span data-ttu-id="354ca-150">1\_1</span><span class="sxs-lookup"><span data-stu-id="354ca-150">1\_1</span></span> | <span data-ttu-id="354ca-151">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-151">2\_0</span></span> | <span data-ttu-id="354ca-152">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-152">2\_sw</span></span> | <span data-ttu-id="354ca-153">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="354ca-153">2\_x</span></span> | <span data-ttu-id="354ca-154">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-154">3\_0</span></span> | <span data-ttu-id="354ca-155">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-155">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="354ca-156">Регистр позиций</span><span class="sxs-lookup"><span data-stu-id="354ca-156">Position Register</span></span>      | <span data-ttu-id="354ca-157">x</span><span class="sxs-lookup"><span data-stu-id="354ca-157">x</span></span>    | <span data-ttu-id="354ca-158">x</span><span class="sxs-lookup"><span data-stu-id="354ca-158">x</span></span>    | <span data-ttu-id="354ca-159">x</span><span class="sxs-lookup"><span data-stu-id="354ca-159">x</span></span>     | <span data-ttu-id="354ca-160">x</span><span class="sxs-lookup"><span data-stu-id="354ca-160">x</span></span>    |      |       |



 

## <a name="point-size-register---opts"></a><span data-ttu-id="354ca-161">Регистр размера точки — наведении</span><span class="sxs-lookup"><span data-stu-id="354ca-161">Point Size Register - oPts</span></span>

<span data-ttu-id="354ca-162">Регистры выходных данных размера точки вывода.</span><span class="sxs-lookup"><span data-stu-id="354ca-162">The output point-size registers.</span></span> <span data-ttu-id="354ca-163">Используется только скалярный x-компонент размера точки.</span><span class="sxs-lookup"><span data-stu-id="354ca-163">Only the scalar x-component of the point size is used.</span></span>



| <span data-ttu-id="354ca-164">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="354ca-164">Vertex shader versions</span></span> | <span data-ttu-id="354ca-165">1\_1</span><span class="sxs-lookup"><span data-stu-id="354ca-165">1\_1</span></span> | <span data-ttu-id="354ca-166">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-166">2\_0</span></span> | <span data-ttu-id="354ca-167">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-167">2\_sw</span></span> | <span data-ttu-id="354ca-168">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="354ca-168">2\_x</span></span> | <span data-ttu-id="354ca-169">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-169">3\_0</span></span> | <span data-ttu-id="354ca-170">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-170">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="354ca-171">Регистр размера точки</span><span class="sxs-lookup"><span data-stu-id="354ca-171">Point Size Register</span></span>    | <span data-ttu-id="354ca-172">x</span><span class="sxs-lookup"><span data-stu-id="354ca-172">x</span></span>    | <span data-ttu-id="354ca-173">x</span><span class="sxs-lookup"><span data-stu-id="354ca-173">x</span></span>    | <span data-ttu-id="354ca-174">x</span><span class="sxs-lookup"><span data-stu-id="354ca-174">x</span></span>     | <span data-ttu-id="354ca-175">x</span><span class="sxs-lookup"><span data-stu-id="354ca-175">x</span></span>    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a><span data-ttu-id="354ca-176">Регистрация координаты текстуры — oT0 в oT7</span><span class="sxs-lookup"><span data-stu-id="354ca-176">Texture Coordinate Register - oT0 to oT7</span></span>

<span data-ttu-id="354ca-177">Выходные координаты выходной текстуры регистрируются.</span><span class="sxs-lookup"><span data-stu-id="354ca-177">The output texture coordinates registers.</span></span> <span data-ttu-id="354ca-178">В частности, это массив регистров выходных данных, которые просматриваются и используются в качестве координат текстуры на стадиях выборки текстуры. Эти данные передаются в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="354ca-178">Specifically, these are an array of output data registers that are iterated and used as texture coordinates by the texture sampling stages routing data to the pixel shader.</span></span>



| <span data-ttu-id="354ca-179">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="354ca-179">Vertex shader versions</span></span>      | <span data-ttu-id="354ca-180">1\_1</span><span class="sxs-lookup"><span data-stu-id="354ca-180">1\_1</span></span> | <span data-ttu-id="354ca-181">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-181">2\_0</span></span> | <span data-ttu-id="354ca-182">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-182">2\_sw</span></span> | <span data-ttu-id="354ca-183">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="354ca-183">2\_x</span></span> | <span data-ttu-id="354ca-184">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="354ca-184">3\_0</span></span> | <span data-ttu-id="354ca-185">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="354ca-185">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="354ca-186">Регистр координаты текстуры</span><span class="sxs-lookup"><span data-stu-id="354ca-186">Texture Coordinate Register</span></span> | <span data-ttu-id="354ca-187">x</span><span class="sxs-lookup"><span data-stu-id="354ca-187">x</span></span>    | <span data-ttu-id="354ca-188">x</span><span class="sxs-lookup"><span data-stu-id="354ca-188">x</span></span>    | <span data-ttu-id="354ca-189">x</span><span class="sxs-lookup"><span data-stu-id="354ca-189">x</span></span>     | <span data-ttu-id="354ca-190">x</span><span class="sxs-lookup"><span data-stu-id="354ca-190">x</span></span>    |      |       |



 

<span data-ttu-id="354ca-191">При записи в регистр текстурных координат рекомендуется передавать в качестве измерения соответствующей карты текстуры только столько чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="354ca-191">When writing to a texture coordinate register, it is recommended to pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="354ca-192">Управление значениями, передаваемыми с помощью модификатора.</span><span class="sxs-lookup"><span data-stu-id="354ca-192">Control the values passed with a modifier.</span></span> <span data-ttu-id="354ca-193">Например, используйте. XY для двухмерной текстурной гиперкарты.</span><span class="sxs-lookup"><span data-stu-id="354ca-193">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="354ca-194">Если для этапа текстуры включена проекция текстуры, все четыре значения с плавающей запятой должны быть записаны в соответствующий регистр текстуры.</span><span class="sxs-lookup"><span data-stu-id="354ca-194">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span>

<span data-ttu-id="354ca-195">\*При использовании программируемого конвейера любой из флагов преобразования текстуры D3DTTFF должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="354ca-195">Any of the D3DTTFF\* texture transform flags should be zero when the programmable pipeline is being used.</span></span>

### <a name="texture-coordinate-range"></a><span data-ttu-id="354ca-196">Диапазон координат текстуры</span><span class="sxs-lookup"><span data-stu-id="354ca-196">Texture Coordinate Range</span></span>

<span data-ttu-id="354ca-197">Данные вершин объекта предоставляют координаты текстуры ввода.</span><span class="sxs-lookup"><span data-stu-id="354ca-197">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="354ca-198">Объекты, которые не используют мозаичные текстуры, обычно имеют координаты текстуры в диапазоне \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="354ca-198">Objects that do not used tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="354ca-199">Объекты, использующие мозаичные текстуры, такие как ландшафта, обычно имеют координаты текстуры в диапазоне от \[ -?, +? \] где?</span><span class="sxs-lookup"><span data-stu-id="354ca-199">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-?,+?\] where ?</span></span> <span data-ttu-id="354ca-200">может быть большим числом с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="354ca-200">can be a large floating point number.</span></span>

<span data-ttu-id="354ca-201">Интерполяция текстурных координат выполняется для данных вершин для растрирования.</span><span class="sxs-lookup"><span data-stu-id="354ca-201">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="354ca-202">Во время растрирования координаты текстуры интерполируются между вершинами объекта, изменены с помощью переноса текстур и масштабируются по размеру текстуры (также принимая во внимание режим адресации текстуры) для создания целочисленного индекса.</span><span class="sxs-lookup"><span data-stu-id="354ca-202">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping and scaled by the texture size (also taking into account texture address mode) to produce an integer index.</span></span> <span data-ttu-id="354ca-203">Затем индекс используется для поиска текстур.</span><span class="sxs-lookup"><span data-stu-id="354ca-203">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="354ca-204">Макстекстуререпеат можно использовать для определения того, сколько раз можно выполнить мозаичное заполнение текстуры.</span><span class="sxs-lookup"><span data-stu-id="354ca-204">MaxTextureRepeat can be used to determine how many times a texture can be tiled.</span></span>

<span data-ttu-id="354ca-205">Если координаты текстуры считываются непосредственно в пиксельный шейдер (с помощью текскурд или текскрд), диапазон координат текстуры зависит от инструкции и версии построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="354ca-205">If texture coordinates are read directly into a pixel shader (using texcoord or texcrd), the texture coordinate range depends on the instruction and the pixel shader version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="354ca-206">См. также</span><span class="sxs-lookup"><span data-stu-id="354ca-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="354ca-207">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="354ca-207">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




