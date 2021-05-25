---
description: Гибкие константы формата вершин или коды ФВФ используются для описания содержимого вершин, чередующихся в одном потоке данных, который будет обрабатываться конвейером с фиксированной функцией.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a088dda530904c320720371c76601fd4fb254481
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343269"
---
# <a name="d3dfvf"></a><span data-ttu-id="72617-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="72617-103">D3DFVF</span></span>

<span data-ttu-id="72617-104">Гибкие константы формата вершин или коды ФВФ используются для описания содержимого вершин, чередующихся в одном потоке данных, который будет обрабатываться конвейером с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="72617-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="72617-105">Флаги данных вершин</span><span class="sxs-lookup"><span data-stu-id="72617-105">Vertex Data Flags</span></span>

<span data-ttu-id="72617-106">Следующие флаги описывают формат вершины.</span><span class="sxs-lookup"><span data-stu-id="72617-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="72617-107">Сведения о форматах вершин см. в разделе [фиксированная функция Фвф Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="72617-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



| <span data-ttu-id="72617-108">\#определенно</span><span class="sxs-lookup"><span data-stu-id="72617-108">\#define</span></span>                            | <span data-ttu-id="72617-109">Описание</span><span class="sxs-lookup"><span data-stu-id="72617-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="72617-110">Порядок данных и тип</span><span class="sxs-lookup"><span data-stu-id="72617-110">Data order and type</span></span>                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72617-111">D3DFVF \_ диффузный</span><span class="sxs-lookup"><span data-stu-id="72617-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="72617-112">Формат вершины включает компонент рассеянного цвета.</span><span class="sxs-lookup"><span data-stu-id="72617-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="72617-113">DWORD в порядке ARGB.</span><span class="sxs-lookup"><span data-stu-id="72617-113">DWORD in ARGB order.</span></span> <span data-ttu-id="72617-114">См. [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="72617-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="72617-115">D3DFVF, \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="72617-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="72617-116">Формат вершины включает вектор нормали вершины.</span><span class="sxs-lookup"><span data-stu-id="72617-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="72617-117">Этот флаг нельзя использовать с \_ флагом D3DFVF ксизрхв.</span><span class="sxs-lookup"><span data-stu-id="72617-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="72617-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="72617-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="72617-119">D3DFVF \_ псизе</span><span class="sxs-lookup"><span data-stu-id="72617-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="72617-120">Формат вершины, указанный в кегле.</span><span class="sxs-lookup"><span data-stu-id="72617-120">Vertex format specified in point size.</span></span> <span data-ttu-id="72617-121">Этот размер выражается в единицах области камеры для вершин, которые не преобразуются и освещены, и в единицах устройства для преобразованных и освещенных вершин.</span><span class="sxs-lookup"><span data-stu-id="72617-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="72617-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="72617-122">float</span></span>                                                                                                     |
| <span data-ttu-id="72617-123">\_Зеркальное отражение D3DFVF</span><span class="sxs-lookup"><span data-stu-id="72617-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="72617-124">Формат вершины включает компонент зеркального цвета.</span><span class="sxs-lookup"><span data-stu-id="72617-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="72617-125">DWORD в порядке ARGB.</span><span class="sxs-lookup"><span data-stu-id="72617-125">DWORD in ARGB order.</span></span> <span data-ttu-id="72617-126">См. [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="72617-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="72617-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="72617-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="72617-128">Формат вершины включает в себя расположение непреобразованной вершины.</span><span class="sxs-lookup"><span data-stu-id="72617-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="72617-129">Этот флаг нельзя использовать с \_ флагом D3DFVF ксизрхв.</span><span class="sxs-lookup"><span data-stu-id="72617-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="72617-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="72617-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="72617-131">D3DFVF \_ ксизрхв</span><span class="sxs-lookup"><span data-stu-id="72617-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="72617-132">Формат вершины включает в себя расположение преобразованной вершины.</span><span class="sxs-lookup"><span data-stu-id="72617-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="72617-133">Этот флаг нельзя использовать с \_ \_ обычными флагами D3DFVF XYZ или D3DFVF.</span><span class="sxs-lookup"><span data-stu-id="72617-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="72617-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="72617-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="72617-135">D3DFVF \_ XYZB1 через D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="72617-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="72617-136">Формат вершины содержит данные о положении и соответствующее число значений весов (бета-версии), используемых для многоматричных операций смешения вершин.</span><span class="sxs-lookup"><span data-stu-id="72617-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="72617-137">В настоящее время в Direct3D можно смешивать до трех весовых значений и четырех матриц смешения.</span><span class="sxs-lookup"><span data-stu-id="72617-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="72617-138">Дополнительные сведения об использовании матриц смешения см. в разделе [индексированное смешение вершин (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="72617-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="72617-139">1, 2 или 3 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="72617-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="72617-140">При \_ использовании D3DFVF ластбета \_ UBYTE4 последний вес смешения обрабатывается как DWORD.</span><span class="sxs-lookup"><span data-stu-id="72617-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="72617-141">D3DFVF \_ ксизв</span><span class="sxs-lookup"><span data-stu-id="72617-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="72617-142">Формат вершины содержит преобразованные и обрезанные данные (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="72617-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="72617-143">Процессвертицес не вызывает Clipper, вместо вывода данных в координатах клипа.</span><span class="sxs-lookup"><span data-stu-id="72617-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="72617-144">Эта константа предназначена для и может использоваться только с, программируемым конвейером вершин.</span><span class="sxs-lookup"><span data-stu-id="72617-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="72617-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="72617-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="72617-146">Флаги текстуры</span><span class="sxs-lookup"><span data-stu-id="72617-146">Texture Flags</span></span>

<span data-ttu-id="72617-147">Следующие флаги описывают флаги текстуры, используемые конвейером с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="72617-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="72617-148">\#определенно</span><span class="sxs-lookup"><span data-stu-id="72617-148">\#define</span></span>                          | <span data-ttu-id="72617-149">Описание</span><span class="sxs-lookup"><span data-stu-id="72617-149">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72617-150">D3DFVF \_ TEX0 — D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="72617-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="72617-151">Число наборов координат текстуры для этой вершины.</span><span class="sxs-lookup"><span data-stu-id="72617-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="72617-152">Фактические значения для этих флагов не являются последовательными.</span><span class="sxs-lookup"><span data-stu-id="72617-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="72617-153">D3DFVF \_ текскурдсизен (курдиндекс)</span><span class="sxs-lookup"><span data-stu-id="72617-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="72617-154">Определите набор данных для координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="72617-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="72617-155">n указывает размер координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="72617-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="72617-156">Курдиндекс указывает номер индекса координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="72617-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="72617-157">См. раздел [**D3DFVF \_ Текскурдсизен**](d3dfvf-texcoordsizen.md) and [текстурные координаты и этапы текстуры](texture-coordinates.md).</span><span class="sxs-lookup"><span data-stu-id="72617-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="72617-158">Флаги Маски</span><span class="sxs-lookup"><span data-stu-id="72617-158">Mask Flags</span></span>

<span data-ttu-id="72617-159">Следующие флаги описывают Флаги Маски, используемые конвейером с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="72617-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="72617-160">\#определенно</span><span class="sxs-lookup"><span data-stu-id="72617-160">\#define</span></span>                             | <span data-ttu-id="72617-161">Описание</span><span class="sxs-lookup"><span data-stu-id="72617-161">Description</span></span>                                           |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="72617-162">\_Маска расположения \_ D3DFVF</span><span class="sxs-lookup"><span data-stu-id="72617-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="72617-163">Маска для битов позиций.</span><span class="sxs-lookup"><span data-stu-id="72617-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="72617-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="72617-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="72617-165">Значения маски для зарезервированных битов в ФВФ.</span><span class="sxs-lookup"><span data-stu-id="72617-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="72617-166">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="72617-166">Do not use.</span></span> |
| <span data-ttu-id="72617-167">D3DFVF \_ текскаунт \_ Маска</span><span class="sxs-lookup"><span data-stu-id="72617-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="72617-168">Значение маски для битов флагов текстуры.</span><span class="sxs-lookup"><span data-stu-id="72617-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="72617-169">Прочие флаги</span><span class="sxs-lookup"><span data-stu-id="72617-169">Miscellaneous Flags</span></span>

<span data-ttu-id="72617-170">Следующие флаги описывают различные флаги, используемые конвейером с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="72617-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="72617-171">#определенно</span><span class="sxs-lookup"><span data-stu-id="72617-171">#define</span></span></td>
<td><span data-ttu-id="72617-172">Описание</span><span class="sxs-lookup"><span data-stu-id="72617-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72617-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="72617-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="72617-174">Последнее поле бета-версии в данных о положении вершины будет иметь тип D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="72617-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="72617-175">Данные в полях бета-версии используются с обложкой палитры матрицы для указания индексов матрицы.</span><span class="sxs-lookup"><span data-stu-id="72617-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72617-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="72617-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="72617-177">Последнее поле бета-версии в данных о положении вершины будет иметь тип UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="72617-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="72617-178">Данные в полях бета-версии используются с обложкой палитры матрицы для указания индексов матрицы.</span><span class="sxs-lookup"><span data-stu-id="72617-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="72617-179">Заданный ФВФ объявляется как: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="72617-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="72617-180">Вес и Матриксиндицес включены в бета-версию [5], где D3DFVF_LASTBETA_UBYTE4 говорит о том, что последний DWORD в бета-версии [5] имеет тип UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="72617-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72617-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="72617-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="72617-182">Число битов, на которое смещается целочисленное значение, определяющее число координат текстуры для вершины.</span><span class="sxs-lookup"><span data-stu-id="72617-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="72617-183">Это значение можно использовать, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="72617-183">This value might be used as shown below.</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a><span data-ttu-id="72617-184">Примеры</span><span class="sxs-lookup"><span data-stu-id="72617-184">Examples</span></span>

<span data-ttu-id="72617-185">В следующих примерах показаны другие общие сочетания флагов.</span><span class="sxs-lookup"><span data-stu-id="72617-185">The following examples show other common flag combinations.</span></span>


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a><span data-ttu-id="72617-186">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="72617-186">Constant Information</span></span>



| <span data-ttu-id="72617-187">Требование</span><span class="sxs-lookup"><span data-stu-id="72617-187">Requirement</span></span>                         | <span data-ttu-id="72617-188">Значение</span><span class="sxs-lookup"><span data-stu-id="72617-188">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="72617-189">Заголовок</span><span class="sxs-lookup"><span data-stu-id="72617-189">Header</span></span>                   | <span data-ttu-id="72617-190">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="72617-190">d3d9types.h</span></span> |
| <span data-ttu-id="72617-191">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="72617-191">Minimum operating system</span></span> | <span data-ttu-id="72617-192">Windows 98</span><span class="sxs-lookup"><span data-stu-id="72617-192">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="72617-193">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="72617-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72617-194">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="72617-194">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="72617-195">Фиксированные коды ФВФ функций (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="72617-195">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="72617-196">Смешение геометрических объектов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="72617-196">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 



