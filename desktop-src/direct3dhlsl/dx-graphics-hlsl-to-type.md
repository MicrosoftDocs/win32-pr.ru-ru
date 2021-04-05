---
title: Объект текстуры
description: В Direct3D 10 вы указываете пробы и текстуры независимо друг от друга. Выбор текстуры реализуется с помощью объекта шаблонной текстуры. Этот объект шаблона-текстуры имеет конкретный формат, возвращает конкретный тип и реализует несколько методов.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- HLSL объекта текстуры
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104273675"
---
# <a name="texture-object"></a><span data-ttu-id="9a690-105">Объект текстуры</span><span class="sxs-lookup"><span data-stu-id="9a690-105">Texture Object</span></span>

<span data-ttu-id="9a690-106">В Direct3D 10 вы указываете пробы и текстуры независимо друг от друга. Выбор текстуры реализуется с помощью объекта шаблонной текстуры.</span><span class="sxs-lookup"><span data-stu-id="9a690-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="9a690-107">Этот объект шаблона-текстуры имеет конкретный формат, возвращает конкретный тип и реализует несколько методов.</span><span class="sxs-lookup"><span data-stu-id="9a690-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a690-108">Различия между Direct3D9 и Direct3D10: в Direct3D 9 пробы привязаны к конкретным текстурам; в Direct3D 10 текстуры и пробы являются независимыми объектами.</span><span class="sxs-lookup"><span data-stu-id="9a690-108">Differences between Direct3D9 and Direct3D10: In Direct3D 9, samplers are bound to specific textures; in Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="9a690-109">Каждый объект шаблона текстуры реализует методы выборки текстур, принимающие текстуру и образец в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="9a690-109">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span><br/> |



 

<span data-ttu-id="9a690-110">Ниже приведен синтаксис для создания всех объектов текстуры (за исключением многовыборочных объектов).</span><span class="sxs-lookup"><span data-stu-id="9a690-110">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="9a690-111">\[ <  > \] *Имя* типа Object1;</span><span class="sxs-lookup"><span data-stu-id="9a690-111">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="9a690-112">Для многовыборочных объектов (Texture2DMS и Texture2DMSArray) требуется, чтобы размер текстуры был явно указан и выражается в виде числа выборок.</span><span class="sxs-lookup"><span data-stu-id="9a690-112">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="9a690-113">\[ < *Тип Object2, имя выборки* > \] ;</span><span class="sxs-lookup"><span data-stu-id="9a690-113">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="9a690-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a690-114">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a690-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a690-115">Item</span></span></th>
<th><span data-ttu-id="9a690-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9a690-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a690-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="9a690-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="9a690-118">Объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="9a690-118">A texture object.</span></span> <span data-ttu-id="9a690-119">Должен иметь один из следующих типов.</span><span class="sxs-lookup"><span data-stu-id="9a690-119">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9a690-120">Тип Object1</span><span class="sxs-lookup"><span data-stu-id="9a690-120">Object1 Type</span></span></th>
<th><span data-ttu-id="9a690-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9a690-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9a690-122">Буфер</span><span class="sxs-lookup"><span data-stu-id="9a690-122">Buffer</span></span></td>
<td><span data-ttu-id="9a690-123">Буфер</span><span class="sxs-lookup"><span data-stu-id="9a690-123">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a690-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9a690-124">Texture1D</span></span></td>
<td><span data-ttu-id="9a690-125">Текстура 1D</span><span class="sxs-lookup"><span data-stu-id="9a690-125">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a690-126">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="9a690-126">Texture1DArray</span></span></td>
<td><span data-ttu-id="9a690-127">Массив одномерной текстуры</span><span class="sxs-lookup"><span data-stu-id="9a690-127">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a690-128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="9a690-128">Texture2D</span></span></td>
<td><span data-ttu-id="9a690-129">Двухмерная текстура</span><span class="sxs-lookup"><span data-stu-id="9a690-129">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a690-130">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="9a690-130">Texture2DArray</span></span></td>
<td><span data-ttu-id="9a690-131">Массив двумерных текстур</span><span class="sxs-lookup"><span data-stu-id="9a690-131">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a690-132">Texture3D</span><span class="sxs-lookup"><span data-stu-id="9a690-132">Texture3D</span></span></td>
<td><span data-ttu-id="9a690-133">Трехмерная текстура</span><span class="sxs-lookup"><span data-stu-id="9a690-133">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a690-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="9a690-134">TextureCube</span></span></td>
<td><span data-ttu-id="9a690-135">Текстура Куба</span><span class="sxs-lookup"><span data-stu-id="9a690-135">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a690-136">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="9a690-136">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="9a690-137">Массив текстур Куба</span><span class="sxs-lookup"><span data-stu-id="9a690-137">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a690-138">Тип Object2</span><span class="sxs-lookup"><span data-stu-id="9a690-138">Object2 Type</span></span></td>
<td><span data-ttu-id="9a690-139">Описание</span><span class="sxs-lookup"><span data-stu-id="9a690-139">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a690-140">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="9a690-140">Texture2DMS</span></span></td>
<td><span data-ttu-id="9a690-141">Плоская многовыборочная текстура</span><span class="sxs-lookup"><span data-stu-id="9a690-141">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a690-142">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="9a690-142">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="9a690-143">Массив двумерных текстур с многовыборочной выборкой</span><span class="sxs-lookup"><span data-stu-id="9a690-143">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="9a690-144">Тип буфера поддерживает большинство методов объекта текстуры, за исключением измерений.</span><span class="sxs-lookup"><span data-stu-id="9a690-144">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="9a690-145">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9a690-145">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="9a690-146">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9a690-146">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a690-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Тип</em></span><span class="sxs-lookup"><span data-stu-id="9a690-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="9a690-148">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="9a690-148">Optional.</span></span> <span data-ttu-id="9a690-149">Любой <a href="dx-graphics-hlsl-scalar.md">скалярный тип HLSL</a> или <a href="dx-graphics-hlsl-vector.md"><strong>тип HLSL Vector</strong></a>, заключенный в угловые скобки.</span><span class="sxs-lookup"><span data-stu-id="9a690-149">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="9a690-150">Тип по умолчанию — <strong>float4</strong>.</span><span class="sxs-lookup"><span data-stu-id="9a690-150">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a690-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Безымян</em></span><span class="sxs-lookup"><span data-stu-id="9a690-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="9a690-152">Строка ASCII, указывающая имя объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="9a690-152">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a690-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Регистрируют</em></span><span class="sxs-lookup"><span data-stu-id="9a690-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="9a690-154">Число выборок (диапазоны от 1 до 128).</span><span class="sxs-lookup"><span data-stu-id="9a690-154">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="9a690-155">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a690-155">Example 1</span></span>

<span data-ttu-id="9a690-156">Ниже приведен пример объявления объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="9a690-156">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="9a690-157">Методы объекта текстуры</span><span class="sxs-lookup"><span data-stu-id="9a690-157">Texture Object Methods</span></span>

<span data-ttu-id="9a690-158">Каждый объект текстуры реализует определенные методы; Ниже приведена таблица, в которой перечислены все методы.</span><span class="sxs-lookup"><span data-stu-id="9a690-158">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="9a690-159">Чтобы узнать, какие объекты могут использовать этот метод, см. справочную страницу по каждому из методов.</span><span class="sxs-lookup"><span data-stu-id="9a690-159">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="9a690-160">Метод текстуры</span><span class="sxs-lookup"><span data-stu-id="9a690-160">Texture Method</span></span>                                                                     | <span data-ttu-id="9a690-161">Описание</span><span class="sxs-lookup"><span data-stu-id="9a690-161">Description</span></span>                                                                                                       | <span data-ttu-id="9a690-162">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a690-162">vs\_4\_0</span></span> | <span data-ttu-id="9a690-163">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a690-163">vs\_4\_1</span></span>  | <span data-ttu-id="9a690-164">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a690-164">ps\_4\_0</span></span> | <span data-ttu-id="9a690-165">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a690-165">ps\_4\_1</span></span>  | <span data-ttu-id="9a690-166">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a690-166">gs\_4\_0</span></span> | <span data-ttu-id="9a690-167">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="9a690-167">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="9a690-168">калкулателевелофдетаил</span><span class="sxs-lookup"><span data-stu-id="9a690-168">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="9a690-169">Вычислите Лод, возвращая результат с фиксацией.</span><span class="sxs-lookup"><span data-stu-id="9a690-169">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="9a690-170">x</span><span class="sxs-lookup"><span data-stu-id="9a690-170">x</span></span>         |          |           |
| [<span data-ttu-id="9a690-171">калкулателевелофдетаилунклампед</span><span class="sxs-lookup"><span data-stu-id="9a690-171">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="9a690-172">Вычислите Лод, возвращая несрезный результат.</span><span class="sxs-lookup"><span data-stu-id="9a690-172">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="9a690-173">x</span><span class="sxs-lookup"><span data-stu-id="9a690-173">x</span></span>         |          |           |
| [<span data-ttu-id="9a690-174">Собрать</span><span class="sxs-lookup"><span data-stu-id="9a690-174">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="9a690-175">Получает четыре образца (только красный компонент), которые будут использоваться для интерполяции билинейной при выборке текстуры.</span><span class="sxs-lookup"><span data-stu-id="9a690-175">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="9a690-176">x</span><span class="sxs-lookup"><span data-stu-id="9a690-176">x</span></span>         |          | <span data-ttu-id="9a690-177">x</span><span class="sxs-lookup"><span data-stu-id="9a690-177">x</span></span>         |          | <span data-ttu-id="9a690-178">x</span><span class="sxs-lookup"><span data-stu-id="9a690-178">x</span></span>         |
| [<span data-ttu-id="9a690-179">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="9a690-179">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="9a690-180">Возвращает измерение текстуры для указанного уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="9a690-180">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="9a690-181">x</span><span class="sxs-lookup"><span data-stu-id="9a690-181">x</span></span>        | <span data-ttu-id="9a690-182">x</span><span class="sxs-lookup"><span data-stu-id="9a690-182">x</span></span>         | <span data-ttu-id="9a690-183">x</span><span class="sxs-lookup"><span data-stu-id="9a690-183">x</span></span>        | <span data-ttu-id="9a690-184">x</span><span class="sxs-lookup"><span data-stu-id="9a690-184">x</span></span>         | <span data-ttu-id="9a690-185">x</span><span class="sxs-lookup"><span data-stu-id="9a690-185">x</span></span>        | <span data-ttu-id="9a690-186">x</span><span class="sxs-lookup"><span data-stu-id="9a690-186">x</span></span>         |
| [<span data-ttu-id="9a690-187">Измерения (многопримерные)</span><span class="sxs-lookup"><span data-stu-id="9a690-187">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="9a690-188">Возвращает измерение текстуры для указанного уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="9a690-188">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="9a690-189">x</span><span class="sxs-lookup"><span data-stu-id="9a690-189">x</span></span>         |          | <span data-ttu-id="9a690-190">x</span><span class="sxs-lookup"><span data-stu-id="9a690-190">x</span></span>         |          | <span data-ttu-id="9a690-191">x</span><span class="sxs-lookup"><span data-stu-id="9a690-191">x</span></span>         |
| [<span data-ttu-id="9a690-192">жетсамплепоситион</span><span class="sxs-lookup"><span data-stu-id="9a690-192">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="9a690-193">Возвращает расположение указанного образца.</span><span class="sxs-lookup"><span data-stu-id="9a690-193">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="9a690-194">x</span><span class="sxs-lookup"><span data-stu-id="9a690-194">x</span></span>         |          | <span data-ttu-id="9a690-195">x</span><span class="sxs-lookup"><span data-stu-id="9a690-195">x</span></span>         |          | <span data-ttu-id="9a690-196">x</span><span class="sxs-lookup"><span data-stu-id="9a690-196">x</span></span>         |
| [<span data-ttu-id="9a690-197">Загрузить</span><span class="sxs-lookup"><span data-stu-id="9a690-197">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="9a690-198">Загрузка данных без фильтрации или выборки.</span><span class="sxs-lookup"><span data-stu-id="9a690-198">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="9a690-199">x</span><span class="sxs-lookup"><span data-stu-id="9a690-199">x</span></span>        | <span data-ttu-id="9a690-200">x</span><span class="sxs-lookup"><span data-stu-id="9a690-200">x</span></span>         | <span data-ttu-id="9a690-201">x</span><span class="sxs-lookup"><span data-stu-id="9a690-201">x</span></span>        | <span data-ttu-id="9a690-202">x</span><span class="sxs-lookup"><span data-stu-id="9a690-202">x</span></span>         | <span data-ttu-id="9a690-203">x</span><span class="sxs-lookup"><span data-stu-id="9a690-203">x</span></span>        | <span data-ttu-id="9a690-204">x</span><span class="sxs-lookup"><span data-stu-id="9a690-204">x</span></span>         |
| [<span data-ttu-id="9a690-205">Загрузка (многовыборочная)</span><span class="sxs-lookup"><span data-stu-id="9a690-205">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="9a690-206">Загрузка данных без фильтрации или выборки.</span><span class="sxs-lookup"><span data-stu-id="9a690-206">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="9a690-207">x</span><span class="sxs-lookup"><span data-stu-id="9a690-207">x</span></span>         | <span data-ttu-id="9a690-208">x</span><span class="sxs-lookup"><span data-stu-id="9a690-208">x</span></span>        | <span data-ttu-id="9a690-209">x</span><span class="sxs-lookup"><span data-stu-id="9a690-209">x</span></span>         |          | <span data-ttu-id="9a690-210">x</span><span class="sxs-lookup"><span data-stu-id="9a690-210">x</span></span>         |
| [<span data-ttu-id="9a690-211">Образец</span><span class="sxs-lookup"><span data-stu-id="9a690-211">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="9a690-212">Пример текстуры.</span><span class="sxs-lookup"><span data-stu-id="9a690-212">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="9a690-213">x</span><span class="sxs-lookup"><span data-stu-id="9a690-213">x</span></span>        | <span data-ttu-id="9a690-214">x</span><span class="sxs-lookup"><span data-stu-id="9a690-214">x</span></span>         |          |           |
| [<span data-ttu-id="9a690-215">самплебиас</span><span class="sxs-lookup"><span data-stu-id="9a690-215">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="9a690-216">Пример текстуры после применения значения смещения к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="9a690-216">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="9a690-217">x</span><span class="sxs-lookup"><span data-stu-id="9a690-217">x</span></span>        | <span data-ttu-id="9a690-218">x</span><span class="sxs-lookup"><span data-stu-id="9a690-218">x</span></span>         |          |           |
| [<span data-ttu-id="9a690-219">самплекмп</span><span class="sxs-lookup"><span data-stu-id="9a690-219">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="9a690-220">Пример текстуры с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="9a690-220">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="9a690-221">x</span><span class="sxs-lookup"><span data-stu-id="9a690-221">x</span></span>        | <span data-ttu-id="9a690-222">x</span><span class="sxs-lookup"><span data-stu-id="9a690-222">x</span></span>         |          |           |
| [<span data-ttu-id="9a690-223">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="9a690-223">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="9a690-224">Пример текстуры (только для mipmap уровня 0) с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="9a690-224">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="9a690-225">x</span><span class="sxs-lookup"><span data-stu-id="9a690-225">x</span></span>        | <span data-ttu-id="9a690-226">x</span><span class="sxs-lookup"><span data-stu-id="9a690-226">x</span></span>         | <span data-ttu-id="9a690-227">x</span><span class="sxs-lookup"><span data-stu-id="9a690-227">x</span></span>        | <span data-ttu-id="9a690-228">x</span><span class="sxs-lookup"><span data-stu-id="9a690-228">x</span></span>         | <span data-ttu-id="9a690-229">x</span><span class="sxs-lookup"><span data-stu-id="9a690-229">x</span></span>        | <span data-ttu-id="9a690-230">x</span><span class="sxs-lookup"><span data-stu-id="9a690-230">x</span></span>         |
| [<span data-ttu-id="9a690-231">самплеград</span><span class="sxs-lookup"><span data-stu-id="9a690-231">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="9a690-232">Пример текстуры с помощью градиента, влияющей на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="9a690-232">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="9a690-233">x</span><span class="sxs-lookup"><span data-stu-id="9a690-233">x</span></span>        | <span data-ttu-id="9a690-234">x</span><span class="sxs-lookup"><span data-stu-id="9a690-234">x</span></span>         | <span data-ttu-id="9a690-235">x</span><span class="sxs-lookup"><span data-stu-id="9a690-235">x</span></span>        | <span data-ttu-id="9a690-236">x</span><span class="sxs-lookup"><span data-stu-id="9a690-236">x</span></span>         | <span data-ttu-id="9a690-237">x</span><span class="sxs-lookup"><span data-stu-id="9a690-237">x</span></span>        | <span data-ttu-id="9a690-238">x</span><span class="sxs-lookup"><span data-stu-id="9a690-238">x</span></span>         |
| [<span data-ttu-id="9a690-239">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="9a690-239">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="9a690-240">Пример текстуры на указанном уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="9a690-240">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="9a690-241">x</span><span class="sxs-lookup"><span data-stu-id="9a690-241">x</span></span>        | <span data-ttu-id="9a690-242">x</span><span class="sxs-lookup"><span data-stu-id="9a690-242">x</span></span>         | <span data-ttu-id="9a690-243">x</span><span class="sxs-lookup"><span data-stu-id="9a690-243">x</span></span>        | <span data-ttu-id="9a690-244">x</span><span class="sxs-lookup"><span data-stu-id="9a690-244">x</span></span>         | <span data-ttu-id="9a690-245">x</span><span class="sxs-lookup"><span data-stu-id="9a690-245">x</span></span>        | <span data-ttu-id="9a690-246">x</span><span class="sxs-lookup"><span data-stu-id="9a690-246">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="9a690-247">Тип возвращаемых данных</span><span class="sxs-lookup"><span data-stu-id="9a690-247">Return Type</span></span>

<span data-ttu-id="9a690-248">Тип возвращаемого значения для метода объекта текстуры — float4, если не указано иное, за исключением объектов текстур с несколькими примерами, которые всегда требуют указания типа и числа выборки.</span><span class="sxs-lookup"><span data-stu-id="9a690-248">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="9a690-249">Тип возвращаемого значения совпадает с типом ресурса текстуры ([**\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="9a690-249">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="9a690-250">Иными словами, это может быть любой из следующих типов.</span><span class="sxs-lookup"><span data-stu-id="9a690-250">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="9a690-251">Тип</span><span class="sxs-lookup"><span data-stu-id="9a690-251">Type</span></span>                       | <span data-ttu-id="9a690-252">Описание</span><span class="sxs-lookup"><span data-stu-id="9a690-252">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a690-253">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9a690-253">float</span></span>                      | <span data-ttu-id="9a690-254">32-разрядное число с плавающей запятой (см. раздел [правила с плавающей запятой](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) для отличий от IEEE float)</span><span class="sxs-lookup"><span data-stu-id="9a690-254">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="9a690-255">INT</span><span class="sxs-lookup"><span data-stu-id="9a690-255">int</span></span>                        | <span data-ttu-id="9a690-256">32-битное целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="9a690-256">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="9a690-257">unsigned int</span><span class="sxs-lookup"><span data-stu-id="9a690-257">unsigned int</span></span>               | <span data-ttu-id="9a690-258">32-битное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="9a690-258">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="9a690-259">снорм</span><span class="sxs-lookup"><span data-stu-id="9a690-259">snorm</span></span>                      | <span data-ttu-id="9a690-260">32-разрядное число с плавающей запятой в диапазоне от 1 до 1 включительно (см. раздел [правила с плавающей запятой](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) для отличий от IEEE float).</span><span class="sxs-lookup"><span data-stu-id="9a690-260">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="9a690-261">unorm</span><span class="sxs-lookup"><span data-stu-id="9a690-261">unorm</span></span>                      | <span data-ttu-id="9a690-262">32-bit float в диапазоне от 0 до 1 включительно (см. раздел [правила с плавающей запятой](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) для отличий от IEEE float)</span><span class="sxs-lookup"><span data-stu-id="9a690-262">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="9a690-263">любой тип или структура текстуры</span><span class="sxs-lookup"><span data-stu-id="9a690-263">any texture type or struct</span></span> | <span data-ttu-id="9a690-264">Число возвращаемых компонентов должно быть в диапазоне от 1 до 3 включительно.</span><span class="sxs-lookup"><span data-stu-id="9a690-264">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="9a690-265">Кроме того, тип возвращаемого значения может быть любым типом текстуры, включая структуру, но он должен быть меньше 4 компонентов, например типа float1, возвращающего один компонент.</span><span class="sxs-lookup"><span data-stu-id="9a690-265">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="9a690-266">Значения по умолчанию для отсутствующих компонентов в текстуре</span><span class="sxs-lookup"><span data-stu-id="9a690-266">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="9a690-267">Значение по умолчанию для отсутствующих компонентов в типе ресурса текстуры равно нулю для любого компонента, кроме альфа-компонента (A); значение по умолчанию для отсутствующего A равно единице.</span><span class="sxs-lookup"><span data-stu-id="9a690-267">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="9a690-268">Способ, которым этот элемент появляется в шейдере, зависит от типа ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="9a690-268">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="9a690-269">Он принимает форму первого типизированного компонента, который фактически содержится в типе ресурса текстуры (начиная слева в порядке RGBA).</span><span class="sxs-lookup"><span data-stu-id="9a690-269">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="9a690-270">Если это форма UNORM или FLOAT, значение по умолчанию для отсутствующего A равно 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="9a690-270">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="9a690-271">Если форма имеет вид Синт или UINT, значением по умолчанию для Missing является 0x1.</span><span class="sxs-lookup"><span data-stu-id="9a690-271">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="9a690-272">Например, когда шейдер считывает тип ресурса текстуры [**\_ \_ R24 \_ UNORM \_ x8 \_ типа DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , значения по умолчанию для G и B равны нулю, а значение по умолчанию — 1,0 f; когда шейдер считывает тип ресурса текстуры [**\_ \_ R16G16 \_ uint в формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , значение по умолчанию для B равно нулю, а значение по умолчанию — 0X00000001; когда шейдер считывает тип ресурса текстуры [**\_ \_ R16 \_ Синт в формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , значения по умолчанию для G и B равны нулю, а значение по умолчанию — 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="9a690-272">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="9a690-273">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9a690-273">Example 2</span></span>

<span data-ttu-id="9a690-274">Ниже приведен пример выборки текстуры с помощью метода текстуры.</span><span class="sxs-lookup"><span data-stu-id="9a690-274">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="9a690-275">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9a690-275">Minimum Shader Model</span></span>

<span data-ttu-id="9a690-276">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="9a690-276">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9a690-277">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9a690-277">Shader Model</span></span>                                                        | <span data-ttu-id="9a690-278">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9a690-278">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="9a690-279">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="9a690-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="9a690-280">да</span><span class="sxs-lookup"><span data-stu-id="9a690-280">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9a690-281">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a690-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a690-282">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="9a690-282">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

