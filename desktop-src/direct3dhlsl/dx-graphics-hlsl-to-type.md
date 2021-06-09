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
ms.openlocfilehash: 4d1881ba4a88e97e978e2646c92d276bb9763ffd
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825774"
---
# <a name="texture-object"></a><span data-ttu-id="d804e-105">Объект текстуры</span><span class="sxs-lookup"><span data-stu-id="d804e-105">Texture Object</span></span>

<span data-ttu-id="d804e-106">В Direct3D 10 вы указываете пробы и текстуры независимо друг от друга. Выбор текстуры реализуется с помощью объекта шаблонной текстуры.</span><span class="sxs-lookup"><span data-stu-id="d804e-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="d804e-107">Этот объект шаблона-текстуры имеет конкретный формат, возвращает конкретный тип и реализует несколько методов.</span><span class="sxs-lookup"><span data-stu-id="d804e-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>

<span data-ttu-id="d804e-108">Различия между Direct3D9 и Direct3D10:</span><span class="sxs-lookup"><span data-stu-id="d804e-108">Differences between Direct3D9 and Direct3D10:</span></span>

- <span data-ttu-id="d804e-109">В Direct3D 9 пробы привязаны к конкретным текстурам.</span><span class="sxs-lookup"><span data-stu-id="d804e-109">In Direct3D 9, samplers are bound to specific textures.</span></span>
- <span data-ttu-id="d804e-110">В Direct3D 10 текстуры и пробы являются независимыми объектами.</span><span class="sxs-lookup"><span data-stu-id="d804e-110">In Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="d804e-111">Каждый объект шаблона текстуры реализует методы выборки текстур, принимающие текстуру и образец в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="d804e-111">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span>



 

<span data-ttu-id="d804e-112">Ниже приведен синтаксис для создания всех объектов текстуры (за исключением многовыборочных объектов).</span><span class="sxs-lookup"><span data-stu-id="d804e-112">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="d804e-113">\[ <  > \] *Имя* типа Object1;</span><span class="sxs-lookup"><span data-stu-id="d804e-113">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="d804e-114">Для многовыборочных объектов (Texture2DMS и Texture2DMSArray) требуется, чтобы размер текстуры был явно указан и выражается в виде числа выборок.</span><span class="sxs-lookup"><span data-stu-id="d804e-114">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="d804e-115">\[ < *Тип Object2, имя выборки* > \] ;</span><span class="sxs-lookup"><span data-stu-id="d804e-115">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d804e-116">Параметры</span><span class="sxs-lookup"><span data-stu-id="d804e-116">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d804e-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="d804e-117">Item</span></span></th>
<th><span data-ttu-id="d804e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d804e-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d804e-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="d804e-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="d804e-120">Объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="d804e-120">A texture object.</span></span> <span data-ttu-id="d804e-121">Должен иметь один из следующих типов.</span><span class="sxs-lookup"><span data-stu-id="d804e-121">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d804e-122">Тип Object1</span><span class="sxs-lookup"><span data-stu-id="d804e-122">Object1 Type</span></span></th>
<th><span data-ttu-id="d804e-123">Описание</span><span class="sxs-lookup"><span data-stu-id="d804e-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d804e-124">Буфер</span><span class="sxs-lookup"><span data-stu-id="d804e-124">Buffer</span></span></td>
<td><span data-ttu-id="d804e-125">Буфер</span><span class="sxs-lookup"><span data-stu-id="d804e-125">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="d804e-126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d804e-126">Texture1D</span></span></td>
<td><span data-ttu-id="d804e-127">Текстура 1D</span><span class="sxs-lookup"><span data-stu-id="d804e-127">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d804e-128">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d804e-128">Texture1DArray</span></span></td>
<td><span data-ttu-id="d804e-129">Массив одномерной текстуры</span><span class="sxs-lookup"><span data-stu-id="d804e-129">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d804e-130">Texture2D</span><span class="sxs-lookup"><span data-stu-id="d804e-130">Texture2D</span></span></td>
<td><span data-ttu-id="d804e-131">Двухмерная текстура</span><span class="sxs-lookup"><span data-stu-id="d804e-131">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d804e-132">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d804e-132">Texture2DArray</span></span></td>
<td><span data-ttu-id="d804e-133">Массив двумерных текстур</span><span class="sxs-lookup"><span data-stu-id="d804e-133">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d804e-134">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d804e-134">Texture3D</span></span></td>
<td><span data-ttu-id="d804e-135">Трехмерная текстура</span><span class="sxs-lookup"><span data-stu-id="d804e-135">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d804e-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="d804e-136">TextureCube</span></span></td>
<td><span data-ttu-id="d804e-137">Текстура Куба</span><span class="sxs-lookup"><span data-stu-id="d804e-137">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d804e-138">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="d804e-138">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="d804e-139">Массив текстур Куба</span><span class="sxs-lookup"><span data-stu-id="d804e-139">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d804e-140">Тип Object2</span><span class="sxs-lookup"><span data-stu-id="d804e-140">Object2 Type</span></span></td>
<td><span data-ttu-id="d804e-141">Описание</span><span class="sxs-lookup"><span data-stu-id="d804e-141">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d804e-142">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="d804e-142">Texture2DMS</span></span></td>
<td><span data-ttu-id="d804e-143">Плоская многовыборочная текстура</span><span class="sxs-lookup"><span data-stu-id="d804e-143">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d804e-144">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="d804e-144">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="d804e-145">Массив двумерных текстур с многовыборочной выборкой</span><span class="sxs-lookup"><span data-stu-id="d804e-145">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="d804e-146">Тип буфера поддерживает большинство методов объекта текстуры, за исключением измерений.</span><span class="sxs-lookup"><span data-stu-id="d804e-146">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="d804e-147">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="d804e-147">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="d804e-148">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="d804e-148">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d804e-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Тип</em></span><span class="sxs-lookup"><span data-stu-id="d804e-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="d804e-150">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d804e-150">Optional.</span></span> <span data-ttu-id="d804e-151">Любой <a href="dx-graphics-hlsl-scalar.md">скалярный тип HLSL</a> или <a href="dx-graphics-hlsl-vector.md"><strong>тип HLSL Vector</strong></a>, заключенный в угловые скобки.</span><span class="sxs-lookup"><span data-stu-id="d804e-151">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="d804e-152">Тип по умолчанию — <strong>float4</strong>.</span><span class="sxs-lookup"><span data-stu-id="d804e-152">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d804e-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Безымян</em></span><span class="sxs-lookup"><span data-stu-id="d804e-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="d804e-154">Строка ASCII, указывающая имя объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="d804e-154">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d804e-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Регистрируют</em></span><span class="sxs-lookup"><span data-stu-id="d804e-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="d804e-156">Число выборок (диапазоны от 1 до 128).</span><span class="sxs-lookup"><span data-stu-id="d804e-156">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="d804e-157">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d804e-157">Example 1</span></span>

<span data-ttu-id="d804e-158">Ниже приведен пример объявления объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="d804e-158">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="d804e-159">Методы объекта текстуры</span><span class="sxs-lookup"><span data-stu-id="d804e-159">Texture Object Methods</span></span>

<span data-ttu-id="d804e-160">Каждый объект текстуры реализует определенные методы; Ниже приведена таблица, в которой перечислены все методы.</span><span class="sxs-lookup"><span data-stu-id="d804e-160">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="d804e-161">Чтобы узнать, какие объекты могут использовать этот метод, см. справочную страницу по каждому из методов.</span><span class="sxs-lookup"><span data-stu-id="d804e-161">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="d804e-162">Метод текстуры</span><span class="sxs-lookup"><span data-stu-id="d804e-162">Texture Method</span></span>                                                                     | <span data-ttu-id="d804e-163">Описание</span><span class="sxs-lookup"><span data-stu-id="d804e-163">Description</span></span>                                                                                                       | <span data-ttu-id="d804e-164">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d804e-164">vs\_4\_0</span></span> | <span data-ttu-id="d804e-165">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d804e-165">vs\_4\_1</span></span>  | <span data-ttu-id="d804e-166">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d804e-166">ps\_4\_0</span></span> | <span data-ttu-id="d804e-167">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d804e-167">ps\_4\_1</span></span>  | <span data-ttu-id="d804e-168">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d804e-168">gs\_4\_0</span></span> | <span data-ttu-id="d804e-169">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d804e-169">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="d804e-170">калкулателевелофдетаил</span><span class="sxs-lookup"><span data-stu-id="d804e-170">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="d804e-171">Вычислите Лод, возвращая результат с фиксацией.</span><span class="sxs-lookup"><span data-stu-id="d804e-171">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="d804e-172">x</span><span class="sxs-lookup"><span data-stu-id="d804e-172">x</span></span>         |          |           |
| [<span data-ttu-id="d804e-173">калкулателевелофдетаилунклампед</span><span class="sxs-lookup"><span data-stu-id="d804e-173">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="d804e-174">Вычислите Лод, возвращая несрезный результат.</span><span class="sxs-lookup"><span data-stu-id="d804e-174">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="d804e-175">x</span><span class="sxs-lookup"><span data-stu-id="d804e-175">x</span></span>         |          |           |
| [<span data-ttu-id="d804e-176">Собрать</span><span class="sxs-lookup"><span data-stu-id="d804e-176">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="d804e-177">Получает четыре образца (только красный компонент), которые будут использоваться для интерполяции билинейной при выборке текстуры.</span><span class="sxs-lookup"><span data-stu-id="d804e-177">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="d804e-178">x</span><span class="sxs-lookup"><span data-stu-id="d804e-178">x</span></span>         |          | <span data-ttu-id="d804e-179">x</span><span class="sxs-lookup"><span data-stu-id="d804e-179">x</span></span>         |          | <span data-ttu-id="d804e-180">x</span><span class="sxs-lookup"><span data-stu-id="d804e-180">x</span></span>         |
| [<span data-ttu-id="d804e-181">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="d804e-181">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="d804e-182">Возвращает измерение текстуры для указанного уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="d804e-182">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="d804e-183">x</span><span class="sxs-lookup"><span data-stu-id="d804e-183">x</span></span>        | <span data-ttu-id="d804e-184">x</span><span class="sxs-lookup"><span data-stu-id="d804e-184">x</span></span>         | <span data-ttu-id="d804e-185">x</span><span class="sxs-lookup"><span data-stu-id="d804e-185">x</span></span>        | <span data-ttu-id="d804e-186">x</span><span class="sxs-lookup"><span data-stu-id="d804e-186">x</span></span>         | <span data-ttu-id="d804e-187">x</span><span class="sxs-lookup"><span data-stu-id="d804e-187">x</span></span>        | <span data-ttu-id="d804e-188">x</span><span class="sxs-lookup"><span data-stu-id="d804e-188">x</span></span>         |
| [<span data-ttu-id="d804e-189">Измерения (многопримерные)</span><span class="sxs-lookup"><span data-stu-id="d804e-189">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="d804e-190">Возвращает измерение текстуры для указанного уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="d804e-190">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="d804e-191">x</span><span class="sxs-lookup"><span data-stu-id="d804e-191">x</span></span>         |          | <span data-ttu-id="d804e-192">x</span><span class="sxs-lookup"><span data-stu-id="d804e-192">x</span></span>         |          | <span data-ttu-id="d804e-193">x</span><span class="sxs-lookup"><span data-stu-id="d804e-193">x</span></span>         |
| [<span data-ttu-id="d804e-194">жетсамплепоситион</span><span class="sxs-lookup"><span data-stu-id="d804e-194">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="d804e-195">Возвращает расположение указанного образца.</span><span class="sxs-lookup"><span data-stu-id="d804e-195">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="d804e-196">x</span><span class="sxs-lookup"><span data-stu-id="d804e-196">x</span></span>         |          | <span data-ttu-id="d804e-197">x</span><span class="sxs-lookup"><span data-stu-id="d804e-197">x</span></span>         |          | <span data-ttu-id="d804e-198">x</span><span class="sxs-lookup"><span data-stu-id="d804e-198">x</span></span>         |
| [<span data-ttu-id="d804e-199">Загрузить</span><span class="sxs-lookup"><span data-stu-id="d804e-199">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="d804e-200">Загрузка данных без фильтрации или выборки.</span><span class="sxs-lookup"><span data-stu-id="d804e-200">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="d804e-201">x</span><span class="sxs-lookup"><span data-stu-id="d804e-201">x</span></span>        | <span data-ttu-id="d804e-202">x</span><span class="sxs-lookup"><span data-stu-id="d804e-202">x</span></span>         | <span data-ttu-id="d804e-203">x</span><span class="sxs-lookup"><span data-stu-id="d804e-203">x</span></span>        | <span data-ttu-id="d804e-204">x</span><span class="sxs-lookup"><span data-stu-id="d804e-204">x</span></span>         | <span data-ttu-id="d804e-205">x</span><span class="sxs-lookup"><span data-stu-id="d804e-205">x</span></span>        | <span data-ttu-id="d804e-206">x</span><span class="sxs-lookup"><span data-stu-id="d804e-206">x</span></span>         |
| [<span data-ttu-id="d804e-207">Загрузка (многовыборочная)</span><span class="sxs-lookup"><span data-stu-id="d804e-207">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="d804e-208">Загрузка данных без фильтрации или выборки.</span><span class="sxs-lookup"><span data-stu-id="d804e-208">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="d804e-209">x</span><span class="sxs-lookup"><span data-stu-id="d804e-209">x</span></span>         | <span data-ttu-id="d804e-210">x</span><span class="sxs-lookup"><span data-stu-id="d804e-210">x</span></span>        | <span data-ttu-id="d804e-211">x</span><span class="sxs-lookup"><span data-stu-id="d804e-211">x</span></span>         |          | <span data-ttu-id="d804e-212">x</span><span class="sxs-lookup"><span data-stu-id="d804e-212">x</span></span>         |
| [<span data-ttu-id="d804e-213">Образец</span><span class="sxs-lookup"><span data-stu-id="d804e-213">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="d804e-214">Пример текстуры.</span><span class="sxs-lookup"><span data-stu-id="d804e-214">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="d804e-215">x</span><span class="sxs-lookup"><span data-stu-id="d804e-215">x</span></span>        | <span data-ttu-id="d804e-216">x</span><span class="sxs-lookup"><span data-stu-id="d804e-216">x</span></span>         |          |           |
| [<span data-ttu-id="d804e-217">самплебиас</span><span class="sxs-lookup"><span data-stu-id="d804e-217">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="d804e-218">Пример текстуры после применения значения смещения к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="d804e-218">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="d804e-219">x</span><span class="sxs-lookup"><span data-stu-id="d804e-219">x</span></span>        | <span data-ttu-id="d804e-220">x</span><span class="sxs-lookup"><span data-stu-id="d804e-220">x</span></span>         |          |           |
| [<span data-ttu-id="d804e-221">самплекмп</span><span class="sxs-lookup"><span data-stu-id="d804e-221">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="d804e-222">Пример текстуры с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="d804e-222">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="d804e-223">x</span><span class="sxs-lookup"><span data-stu-id="d804e-223">x</span></span>        | <span data-ttu-id="d804e-224">x</span><span class="sxs-lookup"><span data-stu-id="d804e-224">x</span></span>         |          |           |
| [<span data-ttu-id="d804e-225">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="d804e-225">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="d804e-226">Пример текстуры (только для mipmap уровня 0) с использованием значения сравнения для отклонения выборок.</span><span class="sxs-lookup"><span data-stu-id="d804e-226">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="d804e-227">x</span><span class="sxs-lookup"><span data-stu-id="d804e-227">x</span></span>        | <span data-ttu-id="d804e-228">x</span><span class="sxs-lookup"><span data-stu-id="d804e-228">x</span></span>         | <span data-ttu-id="d804e-229">x</span><span class="sxs-lookup"><span data-stu-id="d804e-229">x</span></span>        | <span data-ttu-id="d804e-230">x</span><span class="sxs-lookup"><span data-stu-id="d804e-230">x</span></span>         | <span data-ttu-id="d804e-231">x</span><span class="sxs-lookup"><span data-stu-id="d804e-231">x</span></span>        | <span data-ttu-id="d804e-232">x</span><span class="sxs-lookup"><span data-stu-id="d804e-232">x</span></span>         |
| [<span data-ttu-id="d804e-233">самплеград</span><span class="sxs-lookup"><span data-stu-id="d804e-233">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="d804e-234">Пример текстуры с помощью градиента, влияющей на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="d804e-234">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="d804e-235">x</span><span class="sxs-lookup"><span data-stu-id="d804e-235">x</span></span>        | <span data-ttu-id="d804e-236">x</span><span class="sxs-lookup"><span data-stu-id="d804e-236">x</span></span>         | <span data-ttu-id="d804e-237">x</span><span class="sxs-lookup"><span data-stu-id="d804e-237">x</span></span>        | <span data-ttu-id="d804e-238">x</span><span class="sxs-lookup"><span data-stu-id="d804e-238">x</span></span>         | <span data-ttu-id="d804e-239">x</span><span class="sxs-lookup"><span data-stu-id="d804e-239">x</span></span>        | <span data-ttu-id="d804e-240">x</span><span class="sxs-lookup"><span data-stu-id="d804e-240">x</span></span>         |
| [<span data-ttu-id="d804e-241">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="d804e-241">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="d804e-242">Пример текстуры на указанном уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="d804e-242">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="d804e-243">x</span><span class="sxs-lookup"><span data-stu-id="d804e-243">x</span></span>        | <span data-ttu-id="d804e-244">x</span><span class="sxs-lookup"><span data-stu-id="d804e-244">x</span></span>         | <span data-ttu-id="d804e-245">x</span><span class="sxs-lookup"><span data-stu-id="d804e-245">x</span></span>        | <span data-ttu-id="d804e-246">x</span><span class="sxs-lookup"><span data-stu-id="d804e-246">x</span></span>         | <span data-ttu-id="d804e-247">x</span><span class="sxs-lookup"><span data-stu-id="d804e-247">x</span></span>        | <span data-ttu-id="d804e-248">x</span><span class="sxs-lookup"><span data-stu-id="d804e-248">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="d804e-249">Тип возвращаемых данных</span><span class="sxs-lookup"><span data-stu-id="d804e-249">Return Type</span></span>

<span data-ttu-id="d804e-250">Тип возвращаемого значения для метода объекта текстуры — float4, если не указано иное, за исключением объектов текстур с несколькими примерами, которые всегда требуют указания типа и числа выборки.</span><span class="sxs-lookup"><span data-stu-id="d804e-250">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="d804e-251">Тип возвращаемого значения совпадает с типом ресурса текстуры ([**\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="d804e-251">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="d804e-252">Иными словами, это может быть любой из следующих типов.</span><span class="sxs-lookup"><span data-stu-id="d804e-252">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="d804e-253">Type</span><span class="sxs-lookup"><span data-stu-id="d804e-253">Type</span></span>                       | <span data-ttu-id="d804e-254">Описание</span><span class="sxs-lookup"><span data-stu-id="d804e-254">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d804e-255">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d804e-255">float</span></span>                      | <span data-ttu-id="d804e-256">32-разрядное число с плавающей запятой (см. раздел [правила с плавающей запятой](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) для отличий от IEEE float)</span><span class="sxs-lookup"><span data-stu-id="d804e-256">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="d804e-257">INT</span><span class="sxs-lookup"><span data-stu-id="d804e-257">int</span></span>                        | <span data-ttu-id="d804e-258">32-битное целое число со знаком</span><span class="sxs-lookup"><span data-stu-id="d804e-258">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="d804e-259">unsigned int</span><span class="sxs-lookup"><span data-stu-id="d804e-259">unsigned int</span></span>               | <span data-ttu-id="d804e-260">32-битное целое число без знака</span><span class="sxs-lookup"><span data-stu-id="d804e-260">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="d804e-261">снорм</span><span class="sxs-lookup"><span data-stu-id="d804e-261">snorm</span></span>                      | <span data-ttu-id="d804e-262">32-разрядное число с плавающей запятой в диапазоне от 1 до 1 включительно (см. раздел [правила с плавающей запятой](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) для отличий от IEEE float).</span><span class="sxs-lookup"><span data-stu-id="d804e-262">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="d804e-263">unorm</span><span class="sxs-lookup"><span data-stu-id="d804e-263">unorm</span></span>                      | <span data-ttu-id="d804e-264">32-bit float в диапазоне от 0 до 1 включительно (см. раздел [правила с плавающей запятой](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) для отличий от IEEE float)</span><span class="sxs-lookup"><span data-stu-id="d804e-264">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="d804e-265">любой тип или структура текстуры</span><span class="sxs-lookup"><span data-stu-id="d804e-265">any texture type or struct</span></span> | <span data-ttu-id="d804e-266">Число возвращаемых компонентов должно быть в диапазоне от 1 до 3 включительно.</span><span class="sxs-lookup"><span data-stu-id="d804e-266">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="d804e-267">Кроме того, тип возвращаемого значения может быть любым типом текстуры, включая структуру, но он должен быть меньше 4 компонентов, например типа float1, возвращающего один компонент.</span><span class="sxs-lookup"><span data-stu-id="d804e-267">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="d804e-268">Значения по умолчанию для отсутствующих компонентов в текстуре</span><span class="sxs-lookup"><span data-stu-id="d804e-268">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="d804e-269">Значение по умолчанию для отсутствующих компонентов в типе ресурса текстуры равно нулю для любого компонента, кроме альфа-компонента (A); значение по умолчанию для отсутствующего A равно единице.</span><span class="sxs-lookup"><span data-stu-id="d804e-269">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="d804e-270">Способ, которым этот элемент появляется в шейдере, зависит от типа ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="d804e-270">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="d804e-271">Он принимает форму первого типизированного компонента, который фактически содержится в типе ресурса текстуры (начиная слева в порядке RGBA).</span><span class="sxs-lookup"><span data-stu-id="d804e-271">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="d804e-272">Если это форма UNORM или FLOAT, значение по умолчанию для отсутствующего A равно 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="d804e-272">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="d804e-273">Если форма имеет вид Синт или UINT, значением по умолчанию для Missing является 0x1.</span><span class="sxs-lookup"><span data-stu-id="d804e-273">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="d804e-274">Например, когда шейдер считывает тип ресурса текстуры [**\_ \_ R24 \_ UNORM \_ x8 \_ типа DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , значения по умолчанию для G и B равны нулю, а значение по умолчанию — 1,0 f; когда шейдер считывает тип ресурса текстуры [**\_ \_ R16G16 \_ uint в формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , значение по умолчанию для B равно нулю, а значение по умолчанию — 0X00000001; когда шейдер считывает тип ресурса текстуры [**\_ \_ R16 \_ Синт в формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) , значения по умолчанию для G и B равны нулю, а значение по умолчанию — 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="d804e-274">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="d804e-275">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d804e-275">Example 2</span></span>

<span data-ttu-id="d804e-276">Ниже приведен пример выборки текстуры с помощью метода текстуры.</span><span class="sxs-lookup"><span data-stu-id="d804e-276">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="d804e-277">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d804e-277">Minimum Shader Model</span></span>

<span data-ttu-id="d804e-278">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d804e-278">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="d804e-279">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d804e-279">Shader Model</span></span>                                                        | <span data-ttu-id="d804e-280">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d804e-280">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="d804e-281">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="d804e-281">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="d804e-282">Да</span><span class="sxs-lookup"><span data-stu-id="d804e-282">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d804e-283">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d804e-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d804e-284">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d804e-284">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

