---
title: Аргументы функции
description: Функция принимает один или несколько входных аргументов. для объявления каждого аргумента используйте следующий синтаксис.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412438"
---
# <a name="function-arguments"></a><span data-ttu-id="03041-103">Аргументы функции</span><span class="sxs-lookup"><span data-stu-id="03041-103">Function Arguments</span></span>

<span data-ttu-id="03041-104">Функция принимает один или несколько входных аргументов. для объявления каждого аргумента используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="03041-104">A function takes one or more input arguments; use the following syntax to declare each argument.</span></span>



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="03041-105">**\[\]Имя типа инпутмодифиер \[ : семантика \] \[ интерполатионмодифиер \] \[ = инициализаторы\]**</span><span class="sxs-lookup"><span data-stu-id="03041-105">**\[InputModifier\] Type Name \[: Semantic\] \[InterpolationModifier\] \[= Initializers\]**</span></span> |



 

<span data-ttu-id="03041-106">\[\]Имя типа модификатора \[ : семантика \] \[ : модификатор интерполяции \] \[ = инициализаторы\]</span><span class="sxs-lookup"><span data-stu-id="03041-106">\[Modifier\] Type Name \[: Semantic\] \[: Interpolation Modifier\] \[= Initializer(s)\]</span></span>

<span data-ttu-id="03041-107">Если имеется несколько аргументов функции, они разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="03041-107">If there are multiple function arguments, they are separated by commas.</span></span>

## <a name="parameters"></a><span data-ttu-id="03041-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="03041-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03041-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="03041-109">Item</span></span></th>
<th><span data-ttu-id="03041-110">Описание</span><span class="sxs-lookup"><span data-stu-id="03041-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03041-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>инпутмодифиер</strong></span><span class="sxs-lookup"><span data-stu-id="03041-111"><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong></span></span><br/></td>
<td><span data-ttu-id="03041-112">Необязательный термин, который определяет аргумент как вход, выход или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="03041-112">Optional term that identifies an argument as an input, an output, or both.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03041-113">Значение</span><span class="sxs-lookup"><span data-stu-id="03041-113">Value</span></span></td>
<td><span data-ttu-id="03041-114">Описание</span><span class="sxs-lookup"><span data-stu-id="03041-114">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03041-115"><strong>in</strong></span><span class="sxs-lookup"><span data-stu-id="03041-115"><strong>in</strong></span></span></td>
<td><span data-ttu-id="03041-116">Только входные данные</span><span class="sxs-lookup"><span data-stu-id="03041-116">Input only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03041-117"><strong>Inout</strong></span><span class="sxs-lookup"><span data-stu-id="03041-117"><strong>inout</strong></span></span></td>
<td><span data-ttu-id="03041-118">Входные и выходные данные</span><span class="sxs-lookup"><span data-stu-id="03041-118">Input and an output</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03041-119"><strong>out</strong></span><span class="sxs-lookup"><span data-stu-id="03041-119"><strong>out</strong></span></span></td>
<td><span data-ttu-id="03041-120">Только вывод</span><span class="sxs-lookup"><span data-stu-id="03041-120">Output only</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03041-121"><strong>счет</strong></span><span class="sxs-lookup"><span data-stu-id="03041-121"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="03041-122">Входные только постоянные данные</span><span class="sxs-lookup"><span data-stu-id="03041-122">Input only constant data</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="03041-123">Параметры всегда передаются по значению.</span><span class="sxs-lookup"><span data-stu-id="03041-123">Parameters are always passed by value.</span></span> <span data-ttu-id="03041-124">в указывает, что значение параметра должно быть скопировано из вызывающего приложения перед началом функции.</span><span class="sxs-lookup"><span data-stu-id="03041-124">in indicates that the value of the parameter should be copied in from the calling application before the function begins.</span></span> <span data-ttu-id="03041-125">out указывает, что последнее значение параметра должно быть скопировано и возвращено вызывающему приложению при возврате функции.</span><span class="sxs-lookup"><span data-stu-id="03041-125">out indicates that the last value of the parameter should be copied out, and returned to the calling application when the function returns.</span></span> <span data-ttu-id="03041-126">параметр InOut является сокращением для указания обоих типов.</span><span class="sxs-lookup"><span data-stu-id="03041-126">inout is a shorthand for specifying both.</span></span></p>
<p><span data-ttu-id="03041-127">Универсальное значение берется из регистра констант; Каждый вызов шейдера вершин или шейдер пикселей имеет одинаковое начальное значение для универсальной переменной.</span><span class="sxs-lookup"><span data-stu-id="03041-127">A uniform value comes from a constant register; each vertex shader or pixel shader invocation see the same initial value for a uniform variable.</span></span> <span data-ttu-id="03041-128">Глобальные переменные обрабатываются так, как если бы они были объявлены единообразно.</span><span class="sxs-lookup"><span data-stu-id="03041-128">Global variables are treated as if they are declared uniform.</span></span> <span data-ttu-id="03041-129">Для функций, не относящихся к верхнему уровню, универсальный код является синонимом <strong>в</strong>.</span><span class="sxs-lookup"><span data-stu-id="03041-129">For non-top-level functions, uniform is synonymous with <strong>in</strong>.</span></span> <span data-ttu-id="03041-130">Если использование параметра не указано, предполагается, что используется <strong>параметр.</strong></span><span class="sxs-lookup"><span data-stu-id="03041-130">If no parameter usage is specified, the parameter usage is assumed to be <strong>in</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03041-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="03041-131"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="03041-132">Тип аргумента; может быть любым допустимым <a href="dx-graphics-hlsl-data-types.md">типом</a>HLSL.</span><span class="sxs-lookup"><span data-stu-id="03041-132">The argument type; can be any valid HLSL <a href="dx-graphics-hlsl-data-types.md">type</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03041-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Безымян</strong></span><span class="sxs-lookup"><span data-stu-id="03041-133"><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="03041-134">Строка ASCII, однозначно определяющая имя функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="03041-134">An ASCII string that uniquely identifies the name of the shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03041-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Семантическ</strong></span><span class="sxs-lookup"><span data-stu-id="03041-135"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semantic</strong></span></span></p></td>
<td><p><span data-ttu-id="03041-136">Необязательная строка, определяющая предполагаемое использование данных (см. раздел <a href="dx-graphics-hlsl-semantics.md">семантика (DirectX HLSL)</a>).</span><span class="sxs-lookup"><span data-stu-id="03041-136">Optional string that identifies the intended usage of the data (see <a href="dx-graphics-hlsl-semantics.md">Semantics (DirectX HLSL)</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03041-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>интерполатионмодифиер</strong></span><span class="sxs-lookup"><span data-stu-id="03041-137"><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></span></span></p></td>
<td><p><span data-ttu-id="03041-138">Необязательный <a href="dx-graphics-hlsl-struct.md">Модификатор интерполяции</a> , позволяющий шейдеру определить метод интерполяции.</span><span class="sxs-lookup"><span data-stu-id="03041-138">Optional <a href="dx-graphics-hlsl-struct.md">interpolation modifier</a> which allows a shader to determine the method of interpolation.</span></span> <span data-ttu-id="03041-139">Модификатор интерполяции для аргумента функции применяется только к аргументу, используемому в качестве входных данных для функции шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="03041-139">An interpolation modifier on a function argument only applies to an argument used as an input to a pixel shader function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03041-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Инициализаторы</strong></span><span class="sxs-lookup"><span data-stu-id="03041-140"><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Initializers</strong></span></span></p></td>
<td><p><span data-ttu-id="03041-141">Необязательные значения для инициализации; для инициализации типов данных с несколькими компонентами требуется несколько значений.</span><span class="sxs-lookup"><span data-stu-id="03041-141">Optional values for initialization; multiple values are required to initialize multi-component data types.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="03041-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="03041-142">Remarks</span></span>

<span data-ttu-id="03041-143">Аргументы функции перечислены в объявлении функции в списке аргументов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="03041-143">Function arguments are listed in a comma-separated argument list in a function declaration.</span></span> <span data-ttu-id="03041-144">Как и в функциях C, у каждого аргумента должно быть объявлено имя параметра и тип. аргумент функции HLSL может включать семантическое, начальное значение, а входные шейдеры пикселей могут включать тип интерполяции.</span><span class="sxs-lookup"><span data-stu-id="03041-144">As in C functions, each argument must have a parameter name and type declared; an argument to an HLSL function optionally can include a semantic, an initial value, and a pixel shader input can include an interpolation type.</span></span>

<span data-ttu-id="03041-145">*Типом* аргумента функции может быть структура, которая может включать модификатор интерполяции для каждого члена.</span><span class="sxs-lookup"><span data-stu-id="03041-145">The *Type* of a function argument could be a structure, which could include a per-member interpolation modifier.</span></span> <span data-ttu-id="03041-146">Если аргумент функции также имеет модификатор интерполяции, модификатор аргумента функции переопределяет модификаторы интерполяции, объявленные в типе.</span><span class="sxs-lookup"><span data-stu-id="03041-146">If the function argument also has an interpolation modifier, the function argument modifier overrides interpolation modifiers declared within the Type.</span></span>

## <a name="examples"></a><span data-ttu-id="03041-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="03041-147">Examples</span></span>

<span data-ttu-id="03041-148">В этом примере (из [образца BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) показаны однородные и неоднородные входные данные функции шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="03041-148">This example (from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) illustrates uniform and non-uniform inputs to a vertex shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="03041-149">В этом примере (из [примера контентстреаминг](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) используется входная структура для передачи аргументов в функцию шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="03041-149">This example (from the [ContentStreaming Sample](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) uses an input structure to pass arguments to a pixel shader function.</span></span>


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a><span data-ttu-id="03041-150">См. также</span><span class="sxs-lookup"><span data-stu-id="03041-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03041-151">Функции (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03041-151">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





