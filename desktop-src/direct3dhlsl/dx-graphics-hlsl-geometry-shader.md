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
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2019
ms.locfileid: "103785289"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="ed42c-105">Объект Geometry-Shader</span><span class="sxs-lookup"><span data-stu-id="ed42c-105">Geometry-Shader Object</span></span>

<span data-ttu-id="ed42c-106">Объект Geometry-Shader обрабатывает все примитивы.</span><span class="sxs-lookup"><span data-stu-id="ed42c-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="ed42c-107">Используйте следующий синтаксис, чтобы объявить объект Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="ed42c-107">Use the following syntax to declare a geometry-shader object.</span></span>



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed42c-108">\[максвертекскаунт (*нумвертс*) \] void *Шадернаме* ( *тип PrimitiveType DataType Name \[ нумелементс \]*, InOut *стреамаутпутобжект* );</span><span class="sxs-lookup"><span data-stu-id="ed42c-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="ed42c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed42c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed42c-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[максвертекскаунт (*нумвертс*)\]</span><span class="sxs-lookup"><span data-stu-id="ed42c-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="ed42c-111">\[в \] объявлении для максимального числа создаваемых вершин.</span><span class="sxs-lookup"><span data-stu-id="ed42c-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="ed42c-112">\[максвертекскаунт () \] — обязательное ключевое слово; квадратные скобки и круглые скобки являются обязательными символами для правильного синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ed42c-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="ed42c-113">*Нумвертс* — целое число, представляющее количество вершин.</span><span class="sxs-lookup"><span data-stu-id="ed42c-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="ed42c-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*шадернаме*</span><span class="sxs-lookup"><span data-stu-id="ed42c-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="ed42c-115">\[в \] строке ASCII, содержащей уникальное имя для функции Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="ed42c-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="ed42c-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Имя типа данных тип PrimitiveType \[ нумелементс \]*</span><span class="sxs-lookup"><span data-stu-id="ed42c-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="ed42c-117">*Тип PrimitiveType* -примитивный тип, который определяет порядок примитивных данных.</span><span class="sxs-lookup"><span data-stu-id="ed42c-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="ed42c-118">Тип-примитив</span><span class="sxs-lookup"><span data-stu-id="ed42c-118">Primitive Type</span></span> | <span data-ttu-id="ed42c-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ed42c-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="ed42c-120">*точки*</span><span class="sxs-lookup"><span data-stu-id="ed42c-120">*point*</span></span>        | <span data-ttu-id="ed42c-121">Список точек</span><span class="sxs-lookup"><span data-stu-id="ed42c-121">Point list</span></span>                                                    |
| <span data-ttu-id="ed42c-122">*line*</span><span class="sxs-lookup"><span data-stu-id="ed42c-122">*line*</span></span>         | <span data-ttu-id="ed42c-123">Линейный список или полоса строк</span><span class="sxs-lookup"><span data-stu-id="ed42c-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="ed42c-124">*значок*</span><span class="sxs-lookup"><span data-stu-id="ed42c-124">*triangle*</span></span>     | <span data-ttu-id="ed42c-125">Список треугольников или полоса треугольников</span><span class="sxs-lookup"><span data-stu-id="ed42c-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="ed42c-126">*линеадж*</span><span class="sxs-lookup"><span data-stu-id="ed42c-126">*lineadj*</span></span>      | <span data-ttu-id="ed42c-127">Список линий с соседкой или линейной полосой с соседкой</span><span class="sxs-lookup"><span data-stu-id="ed42c-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="ed42c-128">*трианглеадж*</span><span class="sxs-lookup"><span data-stu-id="ed42c-128">*triangleadj*</span></span>  | <span data-ttu-id="ed42c-129">Список треугольников с соседкой или треугольной полосой с соседкой</span><span class="sxs-lookup"><span data-stu-id="ed42c-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="ed42c-130">*Тип данных*  -  \[ в \] типе входных данных аргумент может иметь любой [тип данных HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="ed42c-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="ed42c-131">*Name* — имя аргумента; Это строка ASCII.</span><span class="sxs-lookup"><span data-stu-id="ed42c-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="ed42c-132">*Нумелементс* — размер массива входных данных, который зависит от *тип PrimitiveType* , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ed42c-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="ed42c-133">Тип-примитив</span><span class="sxs-lookup"><span data-stu-id="ed42c-133">Primitive Type</span></span> | <span data-ttu-id="ed42c-134">нумелементс</span><span class="sxs-lookup"><span data-stu-id="ed42c-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed42c-135">*точки*</span><span class="sxs-lookup"><span data-stu-id="ed42c-135">*point*</span></span>        | <span data-ttu-id="ed42c-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ed42c-136">\[1\]</span></span><br/> <span data-ttu-id="ed42c-137">Вы действуете только на один момент времени.</span><span class="sxs-lookup"><span data-stu-id="ed42c-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="ed42c-138">*line*</span><span class="sxs-lookup"><span data-stu-id="ed42c-138">*line*</span></span>         | <span data-ttu-id="ed42c-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ed42c-139">\[2\]</span></span><br/> <span data-ttu-id="ed42c-140">Для линии требуется две вершины.</span><span class="sxs-lookup"><span data-stu-id="ed42c-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="ed42c-141">*значок*</span><span class="sxs-lookup"><span data-stu-id="ed42c-141">*triangle*</span></span>     | <span data-ttu-id="ed42c-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="ed42c-142">\[3\]</span></span><br/> <span data-ttu-id="ed42c-143">Для треугольника требуется три вершины.</span><span class="sxs-lookup"><span data-stu-id="ed42c-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="ed42c-144">*линеадж*</span><span class="sxs-lookup"><span data-stu-id="ed42c-144">*lineadj*</span></span>      | <span data-ttu-id="ed42c-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="ed42c-145">\[4\]</span></span><br/> <span data-ttu-id="ed42c-146">У линеадж есть две конечные точки; Поэтому требуется четыре вершины.</span><span class="sxs-lookup"><span data-stu-id="ed42c-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="ed42c-147">*трианглеадж*</span><span class="sxs-lookup"><span data-stu-id="ed42c-147">*triangleadj*</span></span>  | <span data-ttu-id="ed42c-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="ed42c-148">\[6\]</span></span><br/> <span data-ttu-id="ed42c-149">Трианглеадж границы еще три треугольника; Поэтому для него требуется шесть вершин.</span><span class="sxs-lookup"><span data-stu-id="ed42c-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ed42c-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*стреамаутпутобжект*</span><span class="sxs-lookup"><span data-stu-id="ed42c-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="ed42c-151">Объявление [объекта потока вывода](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="ed42c-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed42c-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed42c-152">Return Value</span></span>

<span data-ttu-id="ed42c-153">None</span><span class="sxs-lookup"><span data-stu-id="ed42c-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="ed42c-154">Remarks</span><span class="sxs-lookup"><span data-stu-id="ed42c-154">Remarks</span></span>

<span data-ttu-id="ed42c-155">На следующей диаграмме показаны различные типы-примитивы для объекта шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="ed42c-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![Иллюстрация различных типов-примитивов для объекта шейдера Geometry](images/d3d11-gsinputs1.png)

<span data-ttu-id="ed42c-157">На следующей диаграмме показаны вызовы шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="ed42c-157">The following diagram shows geometry shader invocations.</span></span>

![Иллюстрация вызовов шейдера Geometry](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="ed42c-159">Примеры</span><span class="sxs-lookup"><span data-stu-id="ed42c-159">Examples</span></span>

<span data-ttu-id="ed42c-160">В этом примере из упражнения 1 в [семинаре по модели шейдера Direct3D 10 4,0](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="ed42c-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


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



## <a name="minimum-shader-model"></a><span data-ttu-id="ed42c-161">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ed42c-161">Minimum Shader Model</span></span>

<span data-ttu-id="ed42c-162">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ed42c-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="ed42c-163">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ed42c-163">Shader Model</span></span>                                                        | <span data-ttu-id="ed42c-164">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ed42c-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="ed42c-165">[Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров</span><span class="sxs-lookup"><span data-stu-id="ed42c-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="ed42c-166">да</span><span class="sxs-lookup"><span data-stu-id="ed42c-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="ed42c-167">См. также</span><span class="sxs-lookup"><span data-stu-id="ed42c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed42c-168">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ed42c-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





