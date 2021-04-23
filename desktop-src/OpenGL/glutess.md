---
title: Функция Глутесскаллбакк (GLU. h)
description: Функция Глутесскаллбакк определяет обратный вызов для объекта тесселяции.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- Функция Глутесскаллбакк OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989263"
---
# <a name="glutesscallback-function"></a><span data-ttu-id="355e2-104">Функция Глутесскаллбакк</span><span class="sxs-lookup"><span data-stu-id="355e2-104">gluTessCallback function</span></span>

<span data-ttu-id="355e2-105">Функция **глутесскаллбакк** определяет обратный вызов для объекта тесселяции.</span><span class="sxs-lookup"><span data-stu-id="355e2-105">The **gluTessCallback** function defines a callback for a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="355e2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="355e2-106">Syntax</span></span>


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="355e2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="355e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="355e2-108">*тесс*</span><span class="sxs-lookup"><span data-stu-id="355e2-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="355e2-109">Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="355e2-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="355e2-110">*какую*</span><span class="sxs-lookup"><span data-stu-id="355e2-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="355e2-111">Определяемый обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="355e2-111">The callback being defined.</span></span> <span data-ttu-id="355e2-112">Допустимы следующие значения: GLU \_ Тесс \_ Begin, Glu \_ Тесс \_ Begin \_ Data, Glu Тесс, \_ \_ \_ флаг Glu \_ ТЕСС \_ ребра \_ \_ , Glu \_ Тесс \_ вершина, Glu \_ ТЕСС \_ вершинные данные \_ , Glu \_ ТЕСС \_ End, GLU \_ Тесс \_ конечные \_ данные, Glu \_ Тесс \_ Combine, Glu \_ Тесс \_ объединить \_ данные, Glu \_ Тесс \_ Error и Glu \_ Тесс \_ данные об ошибках \_ .</span><span class="sxs-lookup"><span data-stu-id="355e2-112">The following values are valid: GLU\_TESS\_BEGIN, GLU\_TESS\_BEGIN\_DATA, GLU\_TESS\_EDGE\_FLAG, GLU\_TESS\_EDGE\_FLAG\_DATA, GLU\_TESS\_VERTEX, GLU\_TESS\_VERTEX\_DATA, GLU\_TESS\_END, GLU\_TESS\_END\_DATA, GLU\_TESS\_COMBINE, GLU\_TESS\_COMBINE\_DATA, GLU\_TESS\_ERROR, and GLU\_TESS\_ERROR\_DATA.</span></span>

<span data-ttu-id="355e2-113">Дополнительные сведения об этих обратных вызовах см. в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="355e2-113">For more information on these callbacks, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="355e2-114">*FN*</span><span class="sxs-lookup"><span data-stu-id="355e2-114">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="355e2-115">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="355e2-115">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="355e2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="355e2-116">Return value</span></span>

<span data-ttu-id="355e2-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="355e2-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="355e2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="355e2-118">Remarks</span></span>

<span data-ttu-id="355e2-119">Используйте **глутесскаллбакк** для указания обратного вызова, который будет использоваться объектом тесселяции.</span><span class="sxs-lookup"><span data-stu-id="355e2-119">Use **gluTessCallback** to specify a callback to be used by a tessellation object.</span></span> <span data-ttu-id="355e2-120">Если указанный обратный вызов уже определен, он заменяется.</span><span class="sxs-lookup"><span data-stu-id="355e2-120">If the specified callback is already defined, then it is replaced.</span></span> <span data-ttu-id="355e2-121">Если *fn* имеет **значение NULL**, то существующий обратный вызов становится неопределенным.</span><span class="sxs-lookup"><span data-stu-id="355e2-121">If *fn* is **NULL**, then the existing callback becomes undefined.</span></span>

<span data-ttu-id="355e2-122">Объект тесселяции использует эти обратные вызовы для описания того, как заданный многоугольник разбивается на треугольники.</span><span class="sxs-lookup"><span data-stu-id="355e2-122">The tessellation object uses these callbacks to describe how a polygon that you specify is broken into triangles.</span></span>

<span data-ttu-id="355e2-123">Существует две версии каждого обратного вызова, один с данными многоугольников, который можно определить, и один без.</span><span class="sxs-lookup"><span data-stu-id="355e2-123">There are two versions of each callback, one with polygon data that you can define and one without.</span></span> <span data-ttu-id="355e2-124">Если указаны обе версии конкретного обратного вызова, будут использоваться обратный вызов с указанными данными многоугольников.</span><span class="sxs-lookup"><span data-stu-id="355e2-124">If both versions of a particular callback are specified, the callback with the polygon data you specify will be used.</span></span> <span data-ttu-id="355e2-125">Параметр *\_ данных Polygon* объекта [**глутессбегинполигон**](glutessbeginpolygon.md) является копией указателя, который был указан при вызове **глутессбегинполигон** .</span><span class="sxs-lookup"><span data-stu-id="355e2-125">The *polygon\_data* parameter of [**gluTessBeginPolygon**](glutessbeginpolygon.md) is a copy of the pointer that was specified when **gluTessBeginPolygon** was called.</span></span>

<span data-ttu-id="355e2-126">Ниже приведены допустимые обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="355e2-126">The following are valid callbacks:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="355e2-127">Обратный вызов</span><span class="sxs-lookup"><span data-stu-id="355e2-127">Callback</span></span></th>
<th><span data-ttu-id="355e2-128">Описание</span><span class="sxs-lookup"><span data-stu-id="355e2-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="355e2-129">GLU_TESS_BEGIN</span><span class="sxs-lookup"><span data-stu-id="355e2-129">GLU_TESS_BEGIN</span></span></td>
<td><span data-ttu-id="355e2-130">Обратный вызов GLU_TESS_BEGIN вызывается как <a href="glbegin.md"><strong>глбегин</strong></a> для указания начала (треугольника) примитива.</span><span class="sxs-lookup"><span data-stu-id="355e2-130">The GLU_TESS_BEGIN callback is invoked like <a href="glbegin.md"><strong>glBegin</strong></a> to indicate the start of a (triangle) primitive.</span></span> <span data-ttu-id="355e2-131">Функция принимает один аргумент типа <strong>гленум</strong>.</span><span class="sxs-lookup"><span data-stu-id="355e2-131">The function takes a single argument of type <strong>GLenum</strong>.</span></span> <span data-ttu-id="355e2-132">Если для свойства GLU_TESS_BOUNDARY_ONLY задано значение GL_FALSE, для аргумента задается значение GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP или GL_TRIANGLES.</span><span class="sxs-lookup"><span data-stu-id="355e2-132">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_FALSE, the argument is set to either GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, or GL_TRIANGLES.</span></span> <span data-ttu-id="355e2-133">Если для свойства GLU_TESS_BOUNDARY_ONLY задано значение GL_TRUE, аргументу присваивается значение GL_LINE_LOOP.</span><span class="sxs-lookup"><span data-stu-id="355e2-133">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_TRUE, the argument is set to GL_LINE_LOOP.</span></span> <span data-ttu-id="355e2-134">Прототип функции для этого обратного вызова выглядит следующим образом: <strong>void</strong> <strong>Begin</strong> ( <em>тип</em><strong>гленум</strong> );</span><span class="sxs-lookup"><span data-stu-id="355e2-134">The function prototype for this callback is as follows: <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>type</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="355e2-135">GLU_TESS_BEGIN_DATA</span><span class="sxs-lookup"><span data-stu-id="355e2-135">GLU_TESS_BEGIN_DATA</span></span></td>
<td><span data-ttu-id="355e2-136">GLU_TESS_BEGIN_DATA совпадает с обратным вызовом GLU_TESS_BEGIN, за исключением того, что он принимает дополнительный аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="355e2-136">GLU_TESS_BEGIN_DATA is the same as the GLU_TESS_BEGIN callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="355e2-137">Этот указатель идентичен непрозрачному указателю, указанному при вызове <a href="glutessbeginpolygon.md"><strong>глутессбегинполигон</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-137">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="355e2-138">Прототип функции для этого обратного вызова: <strong>void</strong> <strong>бегиндата</strong> (<strong></strong> <em>тип</em>гленум, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="355e2-138">The function prototype for this callback is: <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="355e2-139">GLU_TESS_EDGE_FLAG</span><span class="sxs-lookup"><span data-stu-id="355e2-139">GLU_TESS_EDGE_FLAG</span></span></td>
<td><span data-ttu-id="355e2-140">Обратный вызов GLU_TESS_EDGE_FLAG аналогичен <a href="gledgeflag-functions.md"><strong>гледжефлаг</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-140">The GLU_TESS_EDGE_FLAG callback is similar to <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span></span> <span data-ttu-id="355e2-141">Функция принимает один логический флаг, указывающий, какие грани находятся на границе многоугольника.</span><span class="sxs-lookup"><span data-stu-id="355e2-141">The function takes a single Boolean flag that indicates which edges lie on the polygon boundary.</span></span> <span data-ttu-id="355e2-142">Если флаг имеет значение GL_TRUE, каждая вершина, расположенная ниже, начинает ребро, которое зависит от границы многоугольника; то есть ребро, которое отделяет внутреннюю область от внешней.</span><span class="sxs-lookup"><span data-stu-id="355e2-142">If the flag is GL_TRUE, then each vertex that follows begins an edge that lies on the polygon boundary; that is, an edge which separates an interior region from an exterior one.</span></span> <span data-ttu-id="355e2-143">Если флаг имеет значение GL_FALSE, каждая вершина, расположенная ниже, начинает ребро, которое находится внутри многоугольника.</span><span class="sxs-lookup"><span data-stu-id="355e2-143">If the flag is GL_FALSE, then each vertex that follows begins an edge that lies in the polygon interior.</span></span> <span data-ttu-id="355e2-144">Перед обратным вызовом первого вершин вызывается обратный вызов GLU_TESS_EDGE_FLAG (если он определен).</span><span class="sxs-lookup"><span data-stu-id="355e2-144">The GLU_TESS_EDGE_FLAG callback (if defined) is invoked before the first vertex callback is made.</span></span> <span data-ttu-id="355e2-145">Так как вентиляторы треугольника и ленты треугольников не поддерживают пограничные флаги, обратный вызов не вызывается с GL_TRIANGLE_FAN или GL_TRIANGLE_STRIP, если предоставлен обратный вызов пограничной флага.</span><span class="sxs-lookup"><span data-stu-id="355e2-145">Because triangle fans and triangle strips do not support edge flags, the begin callback is not called with GL_TRIANGLE_FAN or GL_TRIANGLE_STRIP if an edge flag callback is provided.</span></span> <span data-ttu-id="355e2-146">Вместо этого вентиляторы и полосы преобразуются в независимые треугольники.</span><span class="sxs-lookup"><span data-stu-id="355e2-146">Instead, the fans and strips are converted to independent triangles.</span></span> <span data-ttu-id="355e2-147">Прототип функции для этого обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="355e2-147">The function prototype for this callback is:</span></span><br/> <span data-ttu-id="355e2-148"><strong>void</strong> <strong>еджефлаг</strong> (<strong></strong> <em>флаг</em>глбулеан);</span><span class="sxs-lookup"><span data-stu-id="355e2-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>flag</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="355e2-149">GLU_TESS_EDGE_FLAG_DATA</span><span class="sxs-lookup"><span data-stu-id="355e2-149">GLU_TESS_EDGE_FLAG_DATA</span></span></td>
<td><span data-ttu-id="355e2-150">Обратный вызов GLU_TESS_EDGE_FLAG_DATA совпадает с обратным вызовом GLU_TESS_EDGE_FLAG, за исключением того, что он принимает дополнительный аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="355e2-150">The GLU_TESS_EDGE_FLAG_DATA callback is the same as the GLU_TESS_EDGE_FLAG callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="355e2-151">Этот указатель идентичен непрозрачному указателю, указанному при вызове <a href="glutessbeginpolygon.md"><strong>глутессбегинполигон</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-151">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="355e2-152">Прототип функции для этого обратного вызова: <strong>void</strong> <strong>еджефлагдата</strong> (<strong></strong> <em>флаг</em>глбулеан, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="355e2-152">The function prototype for this callback is: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="355e2-153">GLU_TESS_VERTEX</span><span class="sxs-lookup"><span data-stu-id="355e2-153">GLU_TESS_VERTEX</span></span></td>
<td><span data-ttu-id="355e2-154">Обратный вызов GLU_TESS_VERTEX вызывается между обратными вызовами Begin и End.</span><span class="sxs-lookup"><span data-stu-id="355e2-154">The GLU_TESS_VERTEX callback is invoked between the begin and end callbacks.</span></span> <span data-ttu-id="355e2-155">Он аналогичен Глвертекс и определяет вершины треугольников, созданных процессом тесселяции.</span><span class="sxs-lookup"><span data-stu-id="355e2-155">It is similar to glVertex , and it defines the vertexes of the triangles created by the tessellation process.</span></span> <span data-ttu-id="355e2-156">Функция принимает указатель в качестве единственного аргумента.</span><span class="sxs-lookup"><span data-stu-id="355e2-156">The function takes a pointer as its only argument.</span></span> <span data-ttu-id="355e2-157">Этот указатель идентичен непрозрачному указателю, указанному при определении вершины (см. <a href="glutessvertex.md"><strong>глутессвертекс</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="355e2-157">This pointer is identical to the opaque pointer that you provided when you defined the vertex (see <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span></span> <span data-ttu-id="355e2-158">Прототип функции для этого обратного вызова: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span><span class="sxs-lookup"><span data-stu-id="355e2-158">The function prototype for this callback is: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="355e2-159">GLU_TESS_VERTEX_DATA</span><span class="sxs-lookup"><span data-stu-id="355e2-159">GLU_TESS_VERTEX_DATA</span></span></td>
<td><span data-ttu-id="355e2-160">GLU_TESS_VERTEX_DATA совпадает с обратным вызовом GLU_TESS_VERTEX, за исключением того, что он принимает дополнительный аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="355e2-160">The GLU_TESS_VERTEX_DATA is the same as the GLU_TESS_VERTEX callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="355e2-161">Этот указатель идентичен непрозрачному указателю, указанному при вызове <a href="glutessbeginpolygon.md"><strong>глутессбегинполигон</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-161">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="355e2-162">Прототип функции для этого обратного вызова: <strong>void</strong>  <strong>вертексдата</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="355e2-162">The function prototype for this callback is: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="355e2-163">GLU_TESS_END</span><span class="sxs-lookup"><span data-stu-id="355e2-163">GLU_TESS_END</span></span></td>
<td><span data-ttu-id="355e2-164">Обратный вызов GLU_TESS_END выполняет ту же цель, что и <a href="glend.md"><strong>гленд</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-164">The GLU_TESS_END callback serves the same purpose as <a href="glend.md"><strong>glEnd</strong></a>.</span></span> <span data-ttu-id="355e2-165">Указывает конец примитива и не принимает аргументов.</span><span class="sxs-lookup"><span data-stu-id="355e2-165">It indicates the end of a primitive, and it takes no arguments.</span></span> <span data-ttu-id="355e2-166">Прототип функции для этого обратного вызова: <strong>void</strong> <strong>End</strong> (<strong>void</strong>);</span><span class="sxs-lookup"><span data-stu-id="355e2-166">The function prototype for this callback is: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="355e2-167">GLU_TESS_END_DATA</span><span class="sxs-lookup"><span data-stu-id="355e2-167">GLU_TESS_END_DATA</span></span></td>
<td><span data-ttu-id="355e2-168">Обратный вызов GLU_TESS_END_DATA совпадает с обратным вызовом GLU_TESS_END, за исключением того, что он принимает дополнительный аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="355e2-168">The GLU_TESS_END_DATA callback is the same as the GLU_TESS_END callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="355e2-169">Этот указатель идентичен непрозрачному указателю, указанному при вызове <a href="glutessbeginpolygon.md"><strong>глутессбегинполигон</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-169">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="355e2-170">Прототип функции для этого обратного вызова: <strong>void</strong> <strong>енддата</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="355e2-170">The function prototype for this callback is: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="355e2-171">GLU_TESS_COMBINE</span><span class="sxs-lookup"><span data-stu-id="355e2-171">GLU_TESS_COMBINE</span></span></td>
<td><span data-ttu-id="355e2-172">Вызовите обратный вызов GLU_TESS_COMBINE, чтобы создать новую вершину, когда тесселяция обнаружит пересечение или выполнить слияние компонентов.</span><span class="sxs-lookup"><span data-stu-id="355e2-172">Call the GLU_TESS_COMBINE callback to create a new vertex when the tessellation detects an intersection, or to merge features.</span></span> <span data-ttu-id="355e2-173">Функция принимает четыре аргумента: массив из трех элементов, каждый из которых имеет тип Глдаубле.</span><span class="sxs-lookup"><span data-stu-id="355e2-173">The function takes four arguments: An array of three elements, each of type Gldouble.</span></span><br/> <span data-ttu-id="355e2-174">Массив из четырех указателей.</span><span class="sxs-lookup"><span data-stu-id="355e2-174">An array of four pointers.</span></span><br/> <span data-ttu-id="355e2-175">Массив из четырех элементов, каждый из которых имеет тип Глфлоат.</span><span class="sxs-lookup"><span data-stu-id="355e2-175">An array of four elements, each of type GLfloat.</span></span><br/> <span data-ttu-id="355e2-176">Указатель на указатель.</span><span class="sxs-lookup"><span data-stu-id="355e2-176">A pointer to a pointer.</span></span><br/> <span data-ttu-id="355e2-177">Прототип функции для этого обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="355e2-177">The function prototype for this callback is:</span></span> <br/> <span data-ttu-id="355e2-178"><strong>void</strong> <strong>Combine</strong>(<strong>глдаубле</strong> <em>CoOrds</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>глфлоат</strong> <em>Weight</em>[4], <strong>void</strong>  \*\* <em>Data</em>);</span><span class="sxs-lookup"><span data-stu-id="355e2-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>);</span></span><br/> <span data-ttu-id="355e2-179">Вершина определяется как линейное сочетание до четырех существующих вершин, хранимых в vertex_data.</span><span class="sxs-lookup"><span data-stu-id="355e2-179">The vertex is defined as a linear combination of up to four existing vertexes, stored in vertex_data.</span></span> <span data-ttu-id="355e2-180">Коэффициенты линейной комбинации задаются по весу. Эти весовые коэффициенты всегда суммируются до 1,0.</span><span class="sxs-lookup"><span data-stu-id="355e2-180">The coefficients of the linear combination are given by weight; these weights always sum to 1.0.</span></span> <span data-ttu-id="355e2-181">Все указатели вершин действительны, даже если некоторые из весов равны нулю.</span><span class="sxs-lookup"><span data-stu-id="355e2-181">All vertex pointers are valid even when some of the weights are zero.</span></span> <span data-ttu-id="355e2-182">Параметр CoOrds задает расположение новой вершины.</span><span class="sxs-lookup"><span data-stu-id="355e2-182">The coords parameter gives the location of the new vertex.</span></span><br/> <span data-ttu-id="355e2-183">Выделение другой вершины, интерполяция параметров с помощью vertex_data и веса и возврат нового указателя вершины в данных.</span><span class="sxs-lookup"><span data-stu-id="355e2-183">Allocate another vertex, interpolate parameters using vertex_data and weight, and return the new vertex pointer in outData.</span></span> <span data-ttu-id="355e2-184">Этот маркер предоставляется во время обратных вызовов отрисовки.</span><span class="sxs-lookup"><span data-stu-id="355e2-184">This handle is supplied during rendering callbacks.</span></span> <span data-ttu-id="355e2-185">Освободите память некоторое время после вызова <a href="glutessendpolygon.md"><strong>глутессендполигон</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-185">Free the memory sometime after calling <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span></span><br/> <span data-ttu-id="355e2-186">Например, если Многоугольник располагается в произвольной плоскости в трехмерном пространстве и вы связываете цвет с каждой вершиной, то обратный вызов GLU_TESS_COMBINE может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="355e2-186">For example, if the polygon lies in an arbitrary plane in three-dimensional space, and you associate a color with each vertex, the GLU_TESS_COMBINE callback might look like the following:</span></span><br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
<span data-ttu-id="355e2-187">Когда тесселяция обнаруживает пересечение, должен быть определен обратный вызов GLU_TESS_COMBINE или GLU_TESS_COMBINE_DATA (см. ниже), который должен записывать в данные указатель, отличный от<strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="355e2-187">When the tessellation detects an intersection, the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback (see below) must be defined, and must write a non-<strong>NULL</strong> pointer into dataOut.</span></span> <span data-ttu-id="355e2-188">В противном случае возникает ошибка GLU_TESS_NEED_COMBINE_CALLBACK, и выходные данные не создаются.</span><span class="sxs-lookup"><span data-stu-id="355e2-188">Otherwise the GLU_TESS_NEED_COMBINE_CALLBACK error occurs, and no output is generated.</span></span> <span data-ttu-id="355e2-189">(Это единственная ошибка, которая может возникнуть во время тесселяции и отрисовки.)</span><span class="sxs-lookup"><span data-stu-id="355e2-189">(This is the only error that can occur during tessellation and rendering.)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="355e2-190">GLU_TESS_COMBINE_DATA</span><span class="sxs-lookup"><span data-stu-id="355e2-190">GLU_TESS_COMBINE_DATA</span></span></td>
<td><span data-ttu-id="355e2-191">Обратный вызов GLU_TESS_COMBINE_DATA совпадает с обратным вызовом GLU_TESS_COMBINE, за исключением того, что он принимает дополнительный аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="355e2-191">The GLU_TESS_COMBINE_DATA callback is the same as the GLU_TESS_COMBINE callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="355e2-192">Этот указатель идентичен непрозрачному указателю, указанному при вызове <a href="glutessbeginpolygon.md"><strong>глутессбегинполигон</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-192">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="355e2-193">Прототип функции для этого обратного вызова: <strong>void</strong> <strong>комбинедата</strong> (<strong>глдаубле</strong> <em>CoOrds</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>глфлоат</strong> <em>Weight</em>[4], <strong>void</strong>  \*\* <em>Data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="355e2-193">The function prototype for this callback is: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="355e2-194">GLU_TESS_ERROR</span><span class="sxs-lookup"><span data-stu-id="355e2-194">GLU_TESS_ERROR</span></span></td>
<td><span data-ttu-id="355e2-195">Обратный вызов GLU_TESS_ERROR вызывается при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="355e2-195">The GLU_TESS_ERROR callback is called when an error is encountered.</span></span> <span data-ttu-id="355e2-196">Один аргумент имеет тип <strong>гленум</strong>; указывает конкретную ошибку, которая была вызвана, и для нее задано одно из следующих: GLU_TESS_MISSING_BEGIN_POLYGON</span><span class="sxs-lookup"><span data-stu-id="355e2-196">The one argument is of type <strong>GLenum</strong>; it indicates the specific error that occurred and is set to one of the following: GLU_TESS_MISSING_BEGIN_POLYGON</span></span><br/> <span data-ttu-id="355e2-197">GLU_TESS_MISSING_END_POLYGON</span><span class="sxs-lookup"><span data-stu-id="355e2-197">GLU_TESS_MISSING_END_POLYGON</span></span><br/> <span data-ttu-id="355e2-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="355e2-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span></span><br/> <span data-ttu-id="355e2-199">GLU_TESS_MISSING_END_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="355e2-199">GLU_TESS_MISSING_END_CONTOUR</span></span><br/> <span data-ttu-id="355e2-200">GLU_TESS_COORD_TOO_LARGE</span><span class="sxs-lookup"><span data-stu-id="355e2-200">GLU_TESS_COORD_TOO_LARGE</span></span><br/> <span data-ttu-id="355e2-201">GLU_TESS_NEED_COMBINE_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="355e2-201">GLU_TESS_NEED_COMBINE_CALLBACK</span></span><br/> <span data-ttu-id="355e2-202">Вызовите Глуеррорстринг, чтобы получить символьные строки, описывающие эти ошибки.</span><span class="sxs-lookup"><span data-stu-id="355e2-202">Call gluErrorString to retrieve character strings describing these errors.</span></span> <span data-ttu-id="355e2-203">Прототип функции для этого обратного вызова выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="355e2-203">The function prototype for this callback is as follows:</span></span><br/> <span data-ttu-id="355e2-204"><strong></strong> <strong>Ошибка</strong> void (<strong>гленум</strong> <em>);</em></span><span class="sxs-lookup"><span data-stu-id="355e2-204"><strong>void</strong> <strong>error</strong> (<strong>GLenum</strong> <em>errno</em>);</span></span><br/> <span data-ttu-id="355e2-205">Библиотека GLU восстанавливает из первых четырех ошибок, вставляя недостающий вызов или вызовы.</span><span class="sxs-lookup"><span data-stu-id="355e2-205">The GLU library recovers from the first four errors by inserting the missing call or calls.</span></span> <span data-ttu-id="355e2-206">GLU_TESS_COORD_TOO_LARGE указывает, что в некоторых координатах вершины превышена предопределенная константа GLU_TESS_MAX_COORD в абсолютном значении и что значение было обработано.</span><span class="sxs-lookup"><span data-stu-id="355e2-206">GLU_TESS_COORD_TOO_LARGE indicates that some vertex coordinate exceeded the predefined constant GLU_TESS_MAX_COORD in absolute value, and that the value has been clamped.</span></span> <span data-ttu-id="355e2-207">(Значения координат должны быть достаточно малыми, чтобы два из них можно было умножить без переполнения.) GLU_TESS_NEED_COMBINE_CALLBACK указывает, что тесселяция обнаружила пересечение между двумя краями во входных данных, а обратный вызов GLU_TESS_COMBINE или GLU_TESS_COMBINE_DATA не был предоставлен.</span><span class="sxs-lookup"><span data-stu-id="355e2-207">(Coordinate values must be small enough that two can be multiplied together without overflow.) GLU_TESS_NEED_COMBINE_CALLBACK indicates that the tessellation detected an intersection between two edges in the input data, and the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback was not provided.</span></span> <span data-ttu-id="355e2-208">Выходные данные создаваться не будут.</span><span class="sxs-lookup"><span data-stu-id="355e2-208">No output will be generated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="355e2-209">GLU_TESS_ERROR_DATA</span><span class="sxs-lookup"><span data-stu-id="355e2-209">GLU_TESS_ERROR_DATA</span></span></td>
<td><span data-ttu-id="355e2-210">Обратный вызов GLU_TESS_ERROR_DATA совпадает с обратным вызовом GLU_TESS_ERROR, за исключением того, что он принимает дополнительный аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="355e2-210">The GLU_TESS_ERROR_DATA callback is the same as the GLU_TESS_ERROR callback, except that it takes an additional pointer argument.</span></span> <span data-ttu-id="355e2-211">Этот указатель идентичен непрозрачному указателю, указанному при вызове <a href="glutessbeginpolygon.md"><strong>глутессбегинполигон</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="355e2-211">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="355e2-212">Прототип функции для этого обратного вызова имеет <strong>следующий тип: void</strong> <strong>errorData</strong> (<strong>гленум</strong> <em>No</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="355e2-212">The function prototype for this callback is: <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="355e2-213">Требования</span><span class="sxs-lookup"><span data-stu-id="355e2-213">Requirements</span></span>



| <span data-ttu-id="355e2-214">Требование</span><span class="sxs-lookup"><span data-stu-id="355e2-214">Requirement</span></span> | <span data-ttu-id="355e2-215">Значение</span><span class="sxs-lookup"><span data-stu-id="355e2-215">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="355e2-216">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="355e2-216">Minimum supported client</span></span><br/> | <span data-ttu-id="355e2-217">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="355e2-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="355e2-218">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="355e2-218">Minimum supported server</span></span><br/> | <span data-ttu-id="355e2-219">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="355e2-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="355e2-220">Заголовок</span><span class="sxs-lookup"><span data-stu-id="355e2-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="355e2-221"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="355e2-221"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="355e2-222">Библиотека</span><span class="sxs-lookup"><span data-stu-id="355e2-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="355e2-223"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="355e2-223"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="355e2-224">DLL</span><span class="sxs-lookup"><span data-stu-id="355e2-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="355e2-225"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="355e2-225"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="355e2-226">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="355e2-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="355e2-227">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="355e2-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="355e2-228">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="355e2-228">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="355e2-229">**гленд**</span><span class="sxs-lookup"><span data-stu-id="355e2-229">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="355e2-230">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="355e2-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> <dt>

[<span data-ttu-id="355e2-231">**глуделететесс**</span><span class="sxs-lookup"><span data-stu-id="355e2-231">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="355e2-232">**глуеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="355e2-232">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="355e2-233">**глуневтесс**</span><span class="sxs-lookup"><span data-stu-id="355e2-233">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="355e2-234">**глутессбегинполигон**</span><span class="sxs-lookup"><span data-stu-id="355e2-234">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="355e2-235">**глутессендполигон**</span><span class="sxs-lookup"><span data-stu-id="355e2-235">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="355e2-236">**глутессвертекс**</span><span class="sxs-lookup"><span data-stu-id="355e2-236">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





