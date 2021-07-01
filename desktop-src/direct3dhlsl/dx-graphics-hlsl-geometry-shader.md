---
title: Объект Geometry-Shader
description: Объект Geometry-Shader обрабатывает все примитивы. Используйте следующий синтаксис, чтобы объявить объект Geometry-Shader.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- максвертекскаунт (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120619"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="2c925-105">Объект Geometry-Shader</span><span class="sxs-lookup"><span data-stu-id="2c925-105">Geometry-Shader Object</span></span>

<span data-ttu-id="2c925-106">Объект Geometry-Shader обрабатывает все примитивы.</span><span class="sxs-lookup"><span data-stu-id="2c925-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="2c925-107">Используйте следующий синтаксис, чтобы объявить объект Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="2c925-107">Use the following syntax to declare a geometry-shader object.</span></span>

<span data-ttu-id="2c925-108">\[максвертекскаунт (*нумвертс*) \] void *Шадернаме* ( *тип PrimitiveType DataType Name \[ нумелементс \]*, InOut *стреамаутпутобжект* );</span><span class="sxs-lookup"><span data-stu-id="2c925-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="2c925-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c925-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c925-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[максвертекскаунт (*нумвертс*)\]</span><span class="sxs-lookup"><span data-stu-id="2c925-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="2c925-111">\[в \] объявлении для максимального числа создаваемых вершин.</span><span class="sxs-lookup"><span data-stu-id="2c925-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="2c925-112">\[максвертекскаунт () \] — обязательное ключевое слово; квадратные скобки и круглые скобки являются обязательными символами для правильного синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="2c925-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="2c925-113">*Нумвертс* — целое число, представляющее количество вершин.</span><span class="sxs-lookup"><span data-stu-id="2c925-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="2c925-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*шадернаме*</span><span class="sxs-lookup"><span data-stu-id="2c925-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="2c925-115">\[в \] строке ASCII, содержащей уникальное имя для функции Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="2c925-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="2c925-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Имя типа данных тип PrimitiveType \[ нумелементс \]*</span><span class="sxs-lookup"><span data-stu-id="2c925-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="2c925-117">*Тип PrimitiveType* -примитивный тип, который определяет порядок примитивных данных.</span><span class="sxs-lookup"><span data-stu-id="2c925-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="2c925-118">Тип-примитив</span><span class="sxs-lookup"><span data-stu-id="2c925-118">Primitive Type</span></span> | <span data-ttu-id="2c925-119">Описание</span><span class="sxs-lookup"><span data-stu-id="2c925-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="2c925-120">*точки*</span><span class="sxs-lookup"><span data-stu-id="2c925-120">*point*</span></span>        | <span data-ttu-id="2c925-121">Список точек</span><span class="sxs-lookup"><span data-stu-id="2c925-121">Point list</span></span>                                                    |
| <span data-ttu-id="2c925-122">*line*</span><span class="sxs-lookup"><span data-stu-id="2c925-122">*line*</span></span>         | <span data-ttu-id="2c925-123">Линейный список или полоса строк</span><span class="sxs-lookup"><span data-stu-id="2c925-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="2c925-124">*треугольник*</span><span class="sxs-lookup"><span data-stu-id="2c925-124">*triangle*</span></span>     | <span data-ttu-id="2c925-125">Список треугольников или полоса треугольников</span><span class="sxs-lookup"><span data-stu-id="2c925-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="2c925-126">*линеадж*</span><span class="sxs-lookup"><span data-stu-id="2c925-126">*lineadj*</span></span>      | <span data-ttu-id="2c925-127">Список линий с соседкой или линейной полосой с соседкой</span><span class="sxs-lookup"><span data-stu-id="2c925-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="2c925-128">*трианглеадж*</span><span class="sxs-lookup"><span data-stu-id="2c925-128">*triangleadj*</span></span>  | <span data-ttu-id="2c925-129">Список треугольников с соседкой или треугольной полосой с соседкой</span><span class="sxs-lookup"><span data-stu-id="2c925-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="2c925-130">*Тип данных*  -  \[ в \] типе входных данных аргумент может иметь любой [тип данных HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="2c925-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="2c925-131">*Name* — имя аргумента; Это строка ASCII.</span><span class="sxs-lookup"><span data-stu-id="2c925-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="2c925-132">*Нумелементс* — размер массива входных данных, который зависит от *тип PrimitiveType* , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2c925-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="2c925-133">Тип-примитив</span><span class="sxs-lookup"><span data-stu-id="2c925-133">Primitive Type</span></span> | <span data-ttu-id="2c925-134">нумелементс</span><span class="sxs-lookup"><span data-stu-id="2c925-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c925-135">*точки*</span><span class="sxs-lookup"><span data-stu-id="2c925-135">*point*</span></span>        | <span data-ttu-id="2c925-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2c925-136">\[1\]</span></span><br/> <span data-ttu-id="2c925-137">Вы действуете только на один момент времени.</span><span class="sxs-lookup"><span data-stu-id="2c925-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="2c925-138">*line*</span><span class="sxs-lookup"><span data-stu-id="2c925-138">*line*</span></span>         | <span data-ttu-id="2c925-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2c925-139">\[2\]</span></span><br/> <span data-ttu-id="2c925-140">Для линии требуется две вершины.</span><span class="sxs-lookup"><span data-stu-id="2c925-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="2c925-141">*треугольник*</span><span class="sxs-lookup"><span data-stu-id="2c925-141">*triangle*</span></span>     | <span data-ttu-id="2c925-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="2c925-142">\[3\]</span></span><br/> <span data-ttu-id="2c925-143">Для треугольника требуется три вершины.</span><span class="sxs-lookup"><span data-stu-id="2c925-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="2c925-144">*линеадж*</span><span class="sxs-lookup"><span data-stu-id="2c925-144">*lineadj*</span></span>      | <span data-ttu-id="2c925-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="2c925-145">\[4\]</span></span><br/> <span data-ttu-id="2c925-146">У линеадж есть две конечные точки; Поэтому требуется четыре вершины.</span><span class="sxs-lookup"><span data-stu-id="2c925-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="2c925-147">*трианглеадж*</span><span class="sxs-lookup"><span data-stu-id="2c925-147">*triangleadj*</span></span>  | <span data-ttu-id="2c925-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="2c925-148">\[6\]</span></span><br/> <span data-ttu-id="2c925-149">Трианглеадж границы еще три треугольника; Поэтому для него требуется шесть вершин.</span><span class="sxs-lookup"><span data-stu-id="2c925-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c925-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*стреамаутпутобжект*</span><span class="sxs-lookup"><span data-stu-id="2c925-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="2c925-151">Объявление [объекта потока вывода](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="2c925-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c925-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c925-152">Return Value</span></span>

<span data-ttu-id="2c925-153">None</span><span class="sxs-lookup"><span data-stu-id="2c925-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="2c925-154">Remarks</span><span class="sxs-lookup"><span data-stu-id="2c925-154">Remarks</span></span>

<span data-ttu-id="2c925-155">На следующей диаграмме показаны различные типы-примитивы для объекта шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="2c925-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![Иллюстрация различных типов-примитивов для объекта шейдера Geometry](images/d3d11-gsinputs1.png)

<span data-ttu-id="2c925-157">На следующей диаграмме показаны вызовы шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="2c925-157">The following diagram shows geometry shader invocations.</span></span>

![Иллюстрация вызовов шейдера Geometry](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="2c925-159">Примеры</span><span class="sxs-lookup"><span data-stu-id="2c925-159">Examples</span></span>

<span data-ttu-id="2c925-160">В этом примере из упражнения 1 в [семинаре по модели шейдера Direct3D 10 4,0](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="2c925-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="2c925-161">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2c925-161">Minimum Shader Model</span></span>

<span data-ttu-id="2c925-162">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="2c925-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="2c925-163">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2c925-163">Shader Model</span></span>                                                        | <span data-ttu-id="2c925-164">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2c925-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="2c925-165">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="2c925-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="2c925-166">yes</span><span class="sxs-lookup"><span data-stu-id="2c925-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="2c925-167">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2c925-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c925-168">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="2c925-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





