---
title: Функция Глбегин (GL. h)
description: Функции Глбегин и гленд разделяют вершины примитива или группы похожих примитивов. | Функция Глбегин (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- Функция Глбегин OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000184"
---
# <a name="glbegin-function"></a><span data-ttu-id="c9566-105">Функция Глбегин</span><span class="sxs-lookup"><span data-stu-id="c9566-105">glBegin function</span></span>

<span data-ttu-id="c9566-106">Функции **глбегин** и [**гленд**](glend.md) разделяют вершины примитива или группы похожих примитивов.</span><span class="sxs-lookup"><span data-stu-id="c9566-106">The **glBegin** and [**glend**](glend.md) functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9566-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9566-107">Syntax</span></span>


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="c9566-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9566-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9566-109">*mode*</span><span class="sxs-lookup"><span data-stu-id="c9566-109">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="c9566-110">Примитивы или примитивы, которые будут созданы из вершин, представленных между **глбегин** и последующими [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c9566-110">The primitive or primitives that will be created from vertices presented between **glBegin** and the subsequent [**glend**](glend.md).</span></span> <span data-ttu-id="c9566-111">Ниже приведены допустимые символьные константы и их значения.</span><span class="sxs-lookup"><span data-stu-id="c9566-111">The following are accepted symbolic constants and their meanings:</span></span>



| <span data-ttu-id="c9566-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c9566-112">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="c9566-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c9566-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <span data-ttu-id="c9566-114"><dt>**\_точки GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-114"><dt>**GL\_POINTS**</dt></span></span> </dl>                          | <span data-ttu-id="c9566-115">Обрабатывает каждую вершину как единую точку.</span><span class="sxs-lookup"><span data-stu-id="c9566-115">Treats each vertex as a single point.</span></span> <span data-ttu-id="c9566-116">Вершина *n* определяет точку *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-116">Vertex *n* defines point *n*.</span></span> <span data-ttu-id="c9566-117">Выводятся *N* точек.</span><span class="sxs-lookup"><span data-stu-id="c9566-117">*N* points are drawn.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <span data-ttu-id="c9566-118"><dt>**\_строки GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-118"><dt>**GL\_LINES**</dt></span></span> </dl>                             | <span data-ttu-id="c9566-119">Обрабатывает каждую пару вершин как отдельный сегмент линии.</span><span class="sxs-lookup"><span data-stu-id="c9566-119">Treats each pair of vertices as an independent line segment.</span></span> <span data-ttu-id="c9566-120">Вершины *2n-1* и *2N* определяют строку *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-120">Vertices *2n - 1* and *2n* define line *n*.</span></span> <span data-ttu-id="c9566-121">Рисуются линии *N/2* .</span><span class="sxs-lookup"><span data-stu-id="c9566-121">*N/2* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <span data-ttu-id="c9566-122"><dt>**\_ \_ полоса строк GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-122"><dt>**GL\_LINE\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="c9566-123">Рисует подключенную группу сегментов линии от первой вершины до последней.</span><span class="sxs-lookup"><span data-stu-id="c9566-123">Draws a connected group of line segments from the first vertex to the last.</span></span> <span data-ttu-id="c9566-124">Вершины *n* и *n + 1* определяют строку *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-124">Vertices *n* and *n+1* define line *n*.</span></span> <span data-ttu-id="c9566-125">Рисуется *N-1* строк.</span><span class="sxs-lookup"><span data-stu-id="c9566-125">*N - 1* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <span data-ttu-id="c9566-126"><dt>**\_линейный \_ цикл GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-126"><dt>**GL\_LINE\_LOOP**</dt></span></span> </dl>                | <span data-ttu-id="c9566-127">Рисует подключенную группу сегментов линии из первой вершины в последнюю, а затем обратно в первую.</span><span class="sxs-lookup"><span data-stu-id="c9566-127">Draws a connected group of line segments from the first vertex to the last, then back to the first.</span></span> <span data-ttu-id="c9566-128">Вершины *n* и *n + 1* определяют строку *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-128">Vertices *n* and *n + 1* define line *n*.</span></span> <span data-ttu-id="c9566-129">Однако последняя строка определяется вершинами *N* и *1*.</span><span class="sxs-lookup"><span data-stu-id="c9566-129">The last line, however, is defined by vertices *N* and *1*.</span></span> <span data-ttu-id="c9566-130">Выводятся *N* линий.</span><span class="sxs-lookup"><span data-stu-id="c9566-130">*N* lines are drawn.</span></span><br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <span data-ttu-id="c9566-131"><dt>**\_треугольники GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-131"><dt>**GL\_TRIANGLES**</dt></span></span> </dl>                 | <span data-ttu-id="c9566-132">Обрабатывает каждую Triplet вершин как независимый треугольник.</span><span class="sxs-lookup"><span data-stu-id="c9566-132">Treats each triplet of vertices as an independent triangle.</span></span> <span data-ttu-id="c9566-133">Вершины *3N-2*, *3n-1* и *3N* определяют треугольник *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-133">Vertices *3n - 2*, *3n - 1*, and *3n* define triangle *n*.</span></span> <span data-ttu-id="c9566-134">Рисуются треугольники в виде *N/3* .</span><span class="sxs-lookup"><span data-stu-id="c9566-134">*N/3* triangles are drawn.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <span data-ttu-id="c9566-135"><dt>**\_полоса треугольников GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-135"><dt>**GL\_TRIANGLE\_STRIP**</dt></span></span> </dl> | <span data-ttu-id="c9566-136">Рисует подключенную группу треугольников.</span><span class="sxs-lookup"><span data-stu-id="c9566-136">Draws a connected group of triangles.</span></span> <span data-ttu-id="c9566-137">Один треугольник определяется для каждой вершины, представленной после первых двух вершин.</span><span class="sxs-lookup"><span data-stu-id="c9566-137">One triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="c9566-138">Для нечетных *n*, вершин *n*, *n + 1* и *n + 2* определяют треугольник *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-138">For odd *n*, vertices *n*, *n + 1*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="c9566-139">Для даже *n* вершин *n + 1*, *n* и *n + 2* определяют треугольник *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-139">For even *n*, vertices *n + 1*, *n*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="c9566-140">Рисуются треугольники по *N-2* .</span><span class="sxs-lookup"><span data-stu-id="c9566-140">*N - 2* triangles are drawn.</span></span><br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <span data-ttu-id="c9566-141"><dt>**\_вентилятор с треугольником GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-141"><dt>**GL\_TRIANGLE\_FAN**</dt></span></span> </dl>       | <span data-ttu-id="c9566-142">Рисует подключенную группу треугольников.</span><span class="sxs-lookup"><span data-stu-id="c9566-142">Draws a connected group of triangles.</span></span> <span data-ttu-id="c9566-143">один треугольник определяется для каждой вершины, представленной после первых двух вершин.</span><span class="sxs-lookup"><span data-stu-id="c9566-143">one triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="c9566-144">Вершины *1*, *n + 1*, *n + 2* определяют треугольник *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-144">Vertices *1*, *n + 1*, *n + 2* define triangle *n*.</span></span> <span data-ttu-id="c9566-145">Рисуются треугольники по *N-2* .</span><span class="sxs-lookup"><span data-stu-id="c9566-145">*N - 2* triangles are drawn.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <span data-ttu-id="c9566-146"><dt>**четыре Нефин. \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-146"><dt>**GL\_QUADS**</dt></span></span> </dl>                             | <span data-ttu-id="c9566-147">Обрабатывает каждую группу из четырех вершин как независимые грани четырехсторонней.</span><span class="sxs-lookup"><span data-stu-id="c9566-147">Treats each group of four vertices as an independent quadrilateral.</span></span> <span data-ttu-id="c9566-148">Вершины *4n-3*, *4N-2*, *4n-1* и *4N* определяют грани четырехсторонней *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-148">Vertices *4n - 3*, *4n - 2*, *4n - 1*, and *4n* define quadrilateral *n*.</span></span> <span data-ttu-id="c9566-149">Выводятся *N/4* куадрилатералс.</span><span class="sxs-lookup"><span data-stu-id="c9566-149">*N/4* quadrilaterals are drawn.</span></span><br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <span data-ttu-id="c9566-150"><dt>**\_четыре \_ ленты GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-150"><dt>**GL\_QUAD\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="c9566-151">Рисует подключенную группу куадрилатералс.</span><span class="sxs-lookup"><span data-stu-id="c9566-151">Draws a connected group of quadrilaterals.</span></span> <span data-ttu-id="c9566-152">Один грани четырехсторонней определяется для каждой пары вершин, представленных после первой пары.</span><span class="sxs-lookup"><span data-stu-id="c9566-152">One quadrilateral is defined for each pair of vertices presented after the first pair.</span></span> <span data-ttu-id="c9566-153">Вершины *2n-1*, *2N*, *2N + 2* и *2n + 1* определяют грани четырехсторонней *n*.</span><span class="sxs-lookup"><span data-stu-id="c9566-153">Vertices *2n - 1*, *2n*, *2n + 2*, and *2n + 1* define quadrilateral *n*.</span></span> <span data-ttu-id="c9566-154">Нарисованы *N/2-1* куадрилатералс.</span><span class="sxs-lookup"><span data-stu-id="c9566-154">*N/2 - 1* quadrilaterals are drawn.</span></span> <span data-ttu-id="c9566-155">Обратите внимание, что порядок, в котором вершины используются для создания грани четырехсторонней из данных о полосках, отличается от того, который используется с независимыми данными.</span><span class="sxs-lookup"><span data-stu-id="c9566-155">Note that the order in which vertices are used to construct a quadrilateral from strip data is different from that used with independent data.</span></span><br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <span data-ttu-id="c9566-156"><dt>**\_МНОГОУГОЛЬНИК GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-156"><dt>**GL\_POLYGON**</dt></span></span> </dl>                       | <span data-ttu-id="c9566-157">Рисует один выпуклой многоугольник.</span><span class="sxs-lookup"><span data-stu-id="c9566-157">Draws a single, convex polygon.</span></span> <span data-ttu-id="c9566-158">Вершины с *1* по *N* определяют этот многоугольник.</span><span class="sxs-lookup"><span data-stu-id="c9566-158">Vertices *1* through *N* define this polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9566-159">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9566-159">Return value</span></span>

<span data-ttu-id="c9566-160">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c9566-160">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c9566-161">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c9566-161">Error codes</span></span>

<span data-ttu-id="c9566-162">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="c9566-162">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c9566-163">Имя</span><span class="sxs-lookup"><span data-stu-id="c9566-163">Name</span></span>                                                                                                  | <span data-ttu-id="c9566-164">Значение</span><span class="sxs-lookup"><span data-stu-id="c9566-164">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9566-165"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-165"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c9566-166">для *режима* задано неприемлемое значение.</span><span class="sxs-lookup"><span data-stu-id="c9566-166">*mode* was set to an unaccepted value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="c9566-167"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-167"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c9566-168">Функция, отличная от [глвертекс](glvertex-functions.md), [глколор](glcolor-functions.md), [глиндекс](glindex-functions.md), [глнормал](glnormal-functions.md), [глтекскурд](gltexcoord-functions.md), [глевалкурд](glevalcoord-functions.md), [глевалпоинт](glevalpoint.md), [глматериал](glmaterial-functions.md), [гледжефлаг](gledgeflag-functions.md), [**glCallList**](glcalllist.md)или [**glCallLists**](glcalllists.md) , была вызвана между **glBegin** и соответствующим [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c9566-168">A function other than [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md), or [**glCallLists**](glcalllists.md) was called between **glBegin** and the corresponding [**glend**](glend.md).</span></span> <span data-ttu-id="c9566-169">Функция **гленд** была вызвана до вызова соответствующего **глбегин** , или **глбегин** была вызвана в последовательности **глбегин** / **гленд** .</span><span class="sxs-lookup"><span data-stu-id="c9566-169">The function **glend** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glend** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="c9566-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9566-170">Remarks</span></span>

<span data-ttu-id="c9566-171">Функции **глбегин** и [**гленд**](glend.md) разделяют вершины, определяющие примитив или группу похожих примитивов.</span><span class="sxs-lookup"><span data-stu-id="c9566-171">The **glBegin** and [**glend**](glend.md) functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="c9566-172">Функция **глбегин** принимает один аргумент, указывающий, какой из десяти примитивов будет составлять вершины.</span><span class="sxs-lookup"><span data-stu-id="c9566-172">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="c9566-173">При отсчете *n* в виде целого числа, начиная с единицы, и *n* в качестве общего числа указанных вершин используются следующие интерпретации.</span><span class="sxs-lookup"><span data-stu-id="c9566-173">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="c9566-174">Можно использовать только подмножество функций OpenGL между **глбегин** и [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c9566-174">You can use only a subset of OpenGL functions between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="c9566-175">Вы можете использовать следующие функции:</span><span class="sxs-lookup"><span data-stu-id="c9566-175">The functions you can use are:</span></span>

    [<span data-ttu-id="c9566-176">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="c9566-176">**glVertex**</span></span>](glvertex-functions.md)

     

    [<span data-ttu-id="c9566-177">**глколор**</span><span class="sxs-lookup"><span data-stu-id="c9566-177">**glColor**</span></span>](glcolor-functions.md)

     

    [<span data-ttu-id="c9566-178">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="c9566-178">**glIndex**</span></span>](glindex-functions.md)

     

    [<span data-ttu-id="c9566-179">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="c9566-179">**glNormal**</span></span>](glnormal-functions.md)

     

    [<span data-ttu-id="c9566-180">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="c9566-180">**glTexCoord**</span></span>](gltexcoord-functions.md)

     

    [<span data-ttu-id="c9566-181">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="c9566-181">**glEvalCoord**</span></span>](glevalcoord-functions.md)

     

    [<span data-ttu-id="c9566-182">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="c9566-182">**glEvalPoint**</span></span>](glevalpoint.md)

     

    [<span data-ttu-id="c9566-183">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="c9566-183">**glMaterial**</span></span>](glmaterial-functions.md)

     

    [<span data-ttu-id="c9566-184">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="c9566-184">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="c9566-185">Можно также использовать [**глкалллист**](glcalllist.md) или [**глкалллистс**](glcalllists.md) для выполнения списков вывода, включающих только предыдущие функции.</span><span class="sxs-lookup"><span data-stu-id="c9566-185">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="c9566-186">Если между **глбегин** и [**гленд**](glend.md)вызывается любая другая функция OpenGL, устанавливается флаг ошибки и функция игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c9566-186">If any other OpenGL function is called between **glBegin** and [**glend**](glend.md), the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="c9566-187">Независимо от значения, выбранного для *режима* в **глбегин**, количество вершин, которые можно определить между **глбегин** и [**гленд**](glend.md), не ограничено.</span><span class="sxs-lookup"><span data-stu-id="c9566-187">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="c9566-188">Линии, треугольники, куадрилатералс и многоугольники, которые не были заданы, не рисуются.</span><span class="sxs-lookup"><span data-stu-id="c9566-188">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="c9566-189">Неполные результаты спецификации, если указано слишком мало вершин для указания даже одного примитива или если задано неверное кратное для вершин.</span><span class="sxs-lookup"><span data-stu-id="c9566-189">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="c9566-190">Неполный примитив не учитывается; рисуются все примитивы.</span><span class="sxs-lookup"><span data-stu-id="c9566-190">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="c9566-191">Минимальная спецификация вершин для каждого примитива:</span><span class="sxs-lookup"><span data-stu-id="c9566-191">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="c9566-192">Минимальное число вершин</span><span class="sxs-lookup"><span data-stu-id="c9566-192">Minimum number of vertices</span></span> | <span data-ttu-id="c9566-193">Тип примитива</span><span class="sxs-lookup"><span data-stu-id="c9566-193">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="c9566-194">1</span><span class="sxs-lookup"><span data-stu-id="c9566-194">1</span></span>                          | <span data-ttu-id="c9566-195">point</span><span class="sxs-lookup"><span data-stu-id="c9566-195">point</span></span>             |
    | <span data-ttu-id="c9566-196">2</span><span class="sxs-lookup"><span data-stu-id="c9566-196">2</span></span>                          | <span data-ttu-id="c9566-197">line</span><span class="sxs-lookup"><span data-stu-id="c9566-197">line</span></span>              |
    | <span data-ttu-id="c9566-198">3</span><span class="sxs-lookup"><span data-stu-id="c9566-198">3</span></span>                          | <span data-ttu-id="c9566-199">треугольник</span><span class="sxs-lookup"><span data-stu-id="c9566-199">triangle</span></span>          |
    | <span data-ttu-id="c9566-200">4</span><span class="sxs-lookup"><span data-stu-id="c9566-200">4</span></span>                          | <span data-ttu-id="c9566-201">грани четырехсторонней</span><span class="sxs-lookup"><span data-stu-id="c9566-201">quadrilateral</span></span>     |
    | <span data-ttu-id="c9566-202">3</span><span class="sxs-lookup"><span data-stu-id="c9566-202">3</span></span>                          | <span data-ttu-id="c9566-203">polygon</span><span class="sxs-lookup"><span data-stu-id="c9566-203">polygon</span></span>           |

    

     

-   <span data-ttu-id="c9566-204">Режимы, для которых требуется несколько вершин, — это \_ строки GL (2), \_ треугольники GL (3), \_ четыре четырехъядерных (4) и \_ четыре четырехъядерных \_ лент (2).</span><span class="sxs-lookup"><span data-stu-id="c9566-204">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9566-205">Требования</span><span class="sxs-lookup"><span data-stu-id="c9566-205">Requirements</span></span>



| <span data-ttu-id="c9566-206">Требование</span><span class="sxs-lookup"><span data-stu-id="c9566-206">Requirement</span></span> | <span data-ttu-id="c9566-207">Значение</span><span class="sxs-lookup"><span data-stu-id="c9566-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9566-208">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9566-208">Minimum supported client</span></span><br/> | <span data-ttu-id="c9566-209">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9566-209">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c9566-210">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9566-210">Minimum supported server</span></span><br/> | <span data-ttu-id="c9566-211">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9566-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c9566-212">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c9566-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9566-213"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-213"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c9566-214">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9566-214">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9566-215"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-215"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c9566-216">DLL</span><span class="sxs-lookup"><span data-stu-id="c9566-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9566-217"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9566-217"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9566-218">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9566-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9566-219">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="c9566-219">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="c9566-220">**глкалллистс**</span><span class="sxs-lookup"><span data-stu-id="c9566-220">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="c9566-221">**глколор**</span><span class="sxs-lookup"><span data-stu-id="c9566-221">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c9566-222">**гледжефлаг**</span><span class="sxs-lookup"><span data-stu-id="c9566-222">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="c9566-223">**гленд**</span><span class="sxs-lookup"><span data-stu-id="c9566-223">**glEnd**</span></span>](/windows/desktop/OpenGL/glend)
</dt> <dt>

[<span data-ttu-id="c9566-224">**глевалкурд**</span><span class="sxs-lookup"><span data-stu-id="c9566-224">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c9566-225">**глевалпоинт**</span><span class="sxs-lookup"><span data-stu-id="c9566-225">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="c9566-226">**глиндекс**</span><span class="sxs-lookup"><span data-stu-id="c9566-226">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c9566-227">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="c9566-227">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="c9566-228">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="c9566-228">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="c9566-229">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="c9566-229">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c9566-230">**глвертекс**</span><span class="sxs-lookup"><span data-stu-id="c9566-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

