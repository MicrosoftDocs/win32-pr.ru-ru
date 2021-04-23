---
title: Функция Гленабле (GL. h)
description: Функции Гленабле и Глдисабле включают или отключают возможности OpenGL. | Функция Гленабле (GL. h)
ms.assetid: cd4590dd-ae41-47c9-9861-10d72318840f
keywords:
- Функция Гленабле OpenGL
topic_type:
- apiref
api_name:
- glEnable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bc2d13233afec956c798805295c44c96df45d04
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664923"
---
# <a name="glenable-function"></a><span data-ttu-id="22d04-105">Функция Гленабле</span><span class="sxs-lookup"><span data-stu-id="22d04-105">glEnable function</span></span>

<span data-ttu-id="22d04-106">Функции **гленабле** и [**глдисабле**](gldisable.md) включают или отключают возможности OpenGL.</span><span class="sxs-lookup"><span data-stu-id="22d04-106">The **glEnable** and [**glDisable**](gldisable.md) functions enable or disable OpenGL capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d04-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22d04-107">Syntax</span></span>


```C++
void WINAPI glEnable(
   GLenum cap
);
```



## <a name="parameters"></a><span data-ttu-id="22d04-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="22d04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22d04-109">*конец*</span><span class="sxs-lookup"><span data-stu-id="22d04-109">*cap*</span></span> 
</dt> <dd>

<span data-ttu-id="22d04-110">Символьная константа, указывающая на возможность OpenGL.</span><span class="sxs-lookup"><span data-stu-id="22d04-110">A symbolic constant indicating an OpenGL capability.</span></span>

<span data-ttu-id="22d04-111">Сведения о том, что может занять *ограничение* значений, см. в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="22d04-111">For discussion of the values *cap* can take, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22d04-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22d04-112">Return value</span></span>

<span data-ttu-id="22d04-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="22d04-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="22d04-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="22d04-114">Error codes</span></span>

<span data-ttu-id="22d04-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="22d04-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="22d04-116">Имя</span><span class="sxs-lookup"><span data-stu-id="22d04-116">Name</span></span>                                                                                                  | <span data-ttu-id="22d04-117">Значение</span><span class="sxs-lookup"><span data-stu-id="22d04-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22d04-118"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="22d04-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="22d04-119">*ограничение* не было одним из значений, перечисленных в предыдущем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="22d04-119">*cap* was not one of the values listed in the preceding Remarks section.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="22d04-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="22d04-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="22d04-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="22d04-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22d04-122">Remarks</span></span>

<span data-ttu-id="22d04-123">Функции **гленабле** и **глдисабле** включают и отключают различные графические возможности OpenGL.</span><span class="sxs-lookup"><span data-stu-id="22d04-123">The **glEnable** and **glDisable** functions enable and disable various OpenGL graphics capabilities.</span></span> <span data-ttu-id="22d04-124">Чтобы определить текущее значение любой возможности, используйте [**глисенаблед**](glisenabled.md) или [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="22d04-124">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="22d04-125">И **гленабле** , и **глдисабле** принимают один аргумент ( *Cap*), который может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="22d04-125">Both **glEnable** and **glDisable** take a single argument, *cap*, which can assume one of the following values:</span></span>



| <span data-ttu-id="22d04-126">Значение</span><span class="sxs-lookup"><span data-stu-id="22d04-126">Value</span></span>                       | <span data-ttu-id="22d04-127">Значение</span><span class="sxs-lookup"><span data-stu-id="22d04-127">Meaning</span></span>                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d04-128">\_альфа- \_ тест GL</span><span class="sxs-lookup"><span data-stu-id="22d04-128">GL\_ALPHA\_TEST</span></span>             | <span data-ttu-id="22d04-129">Если этот флажок включен, выполните тестирование альфа-версии.</span><span class="sxs-lookup"><span data-stu-id="22d04-129">If enabled, do alpha testing.</span></span> <span data-ttu-id="22d04-130">См. [**глалфафунк**](glalphafunc.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-130">See [**glAlphaFunc**](glalphafunc.md).</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="22d04-131">Автоматический режим "GL" \_ \_</span><span class="sxs-lookup"><span data-stu-id="22d04-131">GL\_AUTO\_NORMAL</span></span>            | <span data-ttu-id="22d04-132">Если этот режим включен, обычные векторы области вычислений изменяются в том случае, если вершины GL \_ MAP2 \_ вершина \_ 3 или GL \_ MAP2 \_ вершины \_ 4 созданы.</span><span class="sxs-lookup"><span data-stu-id="22d04-132">If enabled, compute surface normal vectors analytically when either GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4 has generated vertices.</span></span> <span data-ttu-id="22d04-133">См. [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-133">See [**glMap2**](glmap2.md).</span></span>                                                                                        |
| <span data-ttu-id="22d04-134">ГК \_ Blend</span><span class="sxs-lookup"><span data-stu-id="22d04-134">GL\_BLEND</span></span>                   | <span data-ttu-id="22d04-135">Если параметр включен, то наложение входящих значений цвета RGBA на значения в цветовых буферах.</span><span class="sxs-lookup"><span data-stu-id="22d04-135">If enabled, blend the incoming RGBA color values with the values in the color buffers.</span></span> <span data-ttu-id="22d04-136">См. [**глблендфунк**](glblendfunc.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-136">See [**glBlendFunc**](glblendfunc.md).</span></span>                                                                                                                              |
| <span data-ttu-id="22d04-137">В \_ главной \_ плоскости Clip,*i*</span><span class="sxs-lookup"><span data-stu-id="22d04-137">GL\_CLIP\_PLANE *i*</span></span>          | <span data-ttu-id="22d04-138">Если этот флажок установлен, обрезает геометрию относительно определяемой пользователем *плоскости-* отсечения.</span><span class="sxs-lookup"><span data-stu-id="22d04-138">If enabled, clip geometry against user-defined clipping plane *i*.</span></span> <span data-ttu-id="22d04-139">См. [**глклипплане**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-139">See [**glClipPlane**](glclipplane.md).</span></span>                                                                                                                                                  |
| <span data-ttu-id="22d04-140">\_ \_ Операция логики цвета GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-140">GL\_COLOR\_LOGIC\_OP</span></span>        | <span data-ttu-id="22d04-141">Если параметр включен, применяется текущая логическая операция к входящему значению цвета и цветового буфера RGBA.</span><span class="sxs-lookup"><span data-stu-id="22d04-141">If enabled, apply the current logical operation to the incoming RGBA color and color buffer values.</span></span> <span data-ttu-id="22d04-142">См. [**гллогикоп**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-142">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                     |
| <span data-ttu-id="22d04-143">\_цветовой \_ материал GL</span><span class="sxs-lookup"><span data-stu-id="22d04-143">GL\_COLOR\_MATERIAL</span></span>         | <span data-ttu-id="22d04-144">Если параметр включен, то один или несколько параметров материала отписывают текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="22d04-144">If enabled, have one or more material parameters track the current color.</span></span> <span data-ttu-id="22d04-145">См. [**глколорматериал**](glcolormaterial.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-145">See [**glColorMaterial**](glcolormaterial.md).</span></span>                                                                                                                                   |
| <span data-ttu-id="22d04-146">\_лицо для отбора GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-146">GL\_CULL\_FACE</span></span>              | <span data-ttu-id="22d04-147">При включении отбор многоугольников на основе их обмотки в координатах окна.</span><span class="sxs-lookup"><span data-stu-id="22d04-147">If enabled, cull polygons based on their winding in window coordinates.</span></span> <span data-ttu-id="22d04-148">См. [**глкуллфаце**](glcullface.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-148">See [**glCullFace**](glcullface.md).</span></span>                                                                                                                                               |
| <span data-ttu-id="22d04-149">\_тест глубины \_ GL</span><span class="sxs-lookup"><span data-stu-id="22d04-149">GL\_DEPTH\_TEST</span></span>             | <span data-ttu-id="22d04-150">Если этот параметр включен, выполняется сравнение глубин и обновление буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="22d04-150">If enabled, do depth comparisons and update the depth buffer.</span></span> <span data-ttu-id="22d04-151">См. раздел [**глдепсфунк**](gldepthfunc.md) and [**глдепсранже**](gldepthrange.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-151">See [**glDepthFunc**](gldepthfunc.md) and [**glDepthRange**](gldepthrange.md).</span></span>                                                                                                              |
| <span data-ttu-id="22d04-152">\_ДИЗЕРИНГ GL</span><span class="sxs-lookup"><span data-stu-id="22d04-152">GL\_DITHER</span></span>                  | <span data-ttu-id="22d04-153">Если параметр включен, то перед записью цветовых компонентов или индексов в буфер цвета.</span><span class="sxs-lookup"><span data-stu-id="22d04-153">If enabled, dither color components or indexes before they are written to the color buffer.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="22d04-154">\_туман GL</span><span class="sxs-lookup"><span data-stu-id="22d04-154">GL\_FOG</span></span>                     | <span data-ttu-id="22d04-155">Если параметр включен, смешивается цвет тумана в цвет после текстурирования.</span><span class="sxs-lookup"><span data-stu-id="22d04-155">If enabled, blend a fog color into the post-texturing color.</span></span> <span data-ttu-id="22d04-156">См. [**глфог**](glfog.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-156">See [**glFog**](glfog.md).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="22d04-157">\_ \_ Операция логики индекса GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-157">GL\_INDEX\_LOGIC\_OP</span></span>        | <span data-ttu-id="22d04-158">Если параметр включен, применяется текущая логическая операция к индексу входящего индекса и цветового буфера.</span><span class="sxs-lookup"><span data-stu-id="22d04-158">If enabled, apply the current logical operation to the incoming index and color buffer indices.</span></span> <span data-ttu-id="22d04-159">См. [**гллогикоп**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-159">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                         |
| <span data-ttu-id="22d04-160">\_Непростая GL</span><span class="sxs-lookup"><span data-stu-id="22d04-160">GL\_LIGHT *i*</span></span>                | <span data-ttu-id="22d04-161">Если параметр включен, включите *в оценку* уравнение освещения освещение.</span><span class="sxs-lookup"><span data-stu-id="22d04-161">If enabled, include light *i* in the evaluation of the lighting equation.</span></span> <span data-ttu-id="22d04-162">См. раздел [**гллигхтмодел**](gllightmodel-functions.md) and [**гллигхт**](gllight-functions.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-162">See [**glLightModel**](gllightmodel-functions.md) and [**glLight**](gllight-functions.md).</span></span>                                                                                      |
| <span data-ttu-id="22d04-163">освещение в ГК \_</span><span class="sxs-lookup"><span data-stu-id="22d04-163">GL\_LIGHTING</span></span>                | <span data-ttu-id="22d04-164">Если параметр включен, используйте текущие параметры освещения для расчета цвета или индекса вершин.</span><span class="sxs-lookup"><span data-stu-id="22d04-164">If enabled, use the current lighting parameters to compute the vertex color or index.</span></span> <span data-ttu-id="22d04-165">Если параметр отключен, связывает текущий цвет или индекс с каждой вершиной.</span><span class="sxs-lookup"><span data-stu-id="22d04-165">If disabled, associate the current color or index with each vertex.</span></span> <span data-ttu-id="22d04-166">См. раздел [**глматериал**](glmaterial-functions.md), **гллигхтмодел** и **гллигхт**.</span><span class="sxs-lookup"><span data-stu-id="22d04-166">See [**glMaterial**](glmaterial-functions.md), **glLightModel**, and **glLight**.</span></span>                |
| <span data-ttu-id="22d04-167">\_ \_ сглаженная линия GL</span><span class="sxs-lookup"><span data-stu-id="22d04-167">GL\_LINE\_SMOOTH</span></span>            | <span data-ttu-id="22d04-168">Если параметр включен, нарисуйте линии с правильной фильтрацией.</span><span class="sxs-lookup"><span data-stu-id="22d04-168">If enabled, draw lines with correct filtering.</span></span> <span data-ttu-id="22d04-169">При отключении нарисуйте линии с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="22d04-169">If disabled, draw aliased lines.</span></span> <span data-ttu-id="22d04-170">См. [**гллиневидс**](gllinewidth.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-170">See [**glLineWidth**](gllinewidth.md).</span></span>                                                                                                                                     |
| <span data-ttu-id="22d04-171">\_стиппле строки \_ GL</span><span class="sxs-lookup"><span data-stu-id="22d04-171">GL\_LINE\_STIPPLE</span></span>           | <span data-ttu-id="22d04-172">Если параметр включен, используйте шаблон стиппле текущей линии при рисовании линий.</span><span class="sxs-lookup"><span data-stu-id="22d04-172">If enabled, use the current line stipple pattern when drawing lines.</span></span> <span data-ttu-id="22d04-173">См. [**гллинестиппле**](gllinestipple.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-173">See [**glLineStipple**](gllinestipple.md).</span></span>                                                                                                                                            |
| <span data-ttu-id="22d04-174">\_логическая \_ Операция GL</span><span class="sxs-lookup"><span data-stu-id="22d04-174">GL\_LOGIC\_OP</span></span>               | <span data-ttu-id="22d04-175">Если параметр включен, примените выбранную в данный момент логическую операцию к индексам входящих и цветовых буферов.</span><span class="sxs-lookup"><span data-stu-id="22d04-175">If enabled, apply the currently selected logical operation to the incoming and color-buffer indexes.</span></span> <span data-ttu-id="22d04-176">См. [**гллогикоп**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-176">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                    |
| <span data-ttu-id="22d04-177">«Карта1» GL, \_ \_ Цвет \_ 4</span><span class="sxs-lookup"><span data-stu-id="22d04-177">GL\_MAP1\_COLOR\_4</span></span>          | <span data-ttu-id="22d04-178">Если этот флажок установлен, вызовы [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) создают значения RGBA.</span><span class="sxs-lookup"><span data-stu-id="22d04-178">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="22d04-179">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-179">See also [**glMap1**](glmap1.md).</span></span>                                           |
| <span data-ttu-id="22d04-180">\_Индекс «КАРТА1» \_ GL</span><span class="sxs-lookup"><span data-stu-id="22d04-180">GL\_MAP1\_INDEX</span></span>             | <span data-ttu-id="22d04-181">Если этот флажок установлен, вызовы **glEvalCoord1**, **glEvalMesh1** и **glEvalPoint1** создают цветовые индексы.</span><span class="sxs-lookup"><span data-stu-id="22d04-181">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate color indexes.</span></span> <span data-ttu-id="22d04-182">См. также **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="22d04-182">See also **glMap1**.</span></span>                                                                                                                                   |
| <span data-ttu-id="22d04-183">«Карта1» GL ( \_ \_ Обычная)</span><span class="sxs-lookup"><span data-stu-id="22d04-183">GL\_MAP1\_NORMAL</span></span>            | <span data-ttu-id="22d04-184">Если этот режим включен, вызовы [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) создают нормали.</span><span class="sxs-lookup"><span data-stu-id="22d04-184">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="22d04-185">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-185">See also [**glMap1**](glmap1.md).</span></span>                                               |
| <span data-ttu-id="22d04-186">\_«Карта1» \_ текстура GL \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="22d04-186">GL\_MAP1\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="22d04-187">Если этот флажок установлен, вызовы **glEvalCoord1**, **glEvalMesh1** и **glEvalPoint1** формируют *координаты* текстуры.</span><span class="sxs-lookup"><span data-stu-id="22d04-187">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s* texture coordinates.</span></span> <span data-ttu-id="22d04-188">См. также **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="22d04-188">See also **glMap1**.</span></span>                                                                                                                         |
| <span data-ttu-id="22d04-189">GL \_ «Карта1» \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="22d04-189">GL\_MAP1\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="22d04-190">Если этот флажок установлен, вызовы [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) формируют координаты *s* и *t* .</span><span class="sxs-lookup"><span data-stu-id="22d04-190">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="22d04-191">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-191">See also [**glMap1**](glmap1.md).</span></span>                       |
| <span data-ttu-id="22d04-192">\_«Карта1» \_ текстура GL \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="22d04-192">GL\_MAP1\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="22d04-193">Если этот флажок установлен, вызовы **glEvalCoord1**, **glEvalMesh1** и **glEvalPoint1** формируют координаты *s*, *t* и *r* .</span><span class="sxs-lookup"><span data-stu-id="22d04-193">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="22d04-194">См. также **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="22d04-194">See also **glMap1**.</span></span>                                                                                                           |
| <span data-ttu-id="22d04-195">\_«Карта1» \_ текстура GL \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="22d04-195">GL\_MAP1\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="22d04-196">Если этот флажок установлен, вызовы [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) создают координаты текстуры *s*, *t*, *r* и *q* .</span><span class="sxs-lookup"><span data-stu-id="22d04-196">If enabled, calls to [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="22d04-197">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-197">See also [**glMap1**](glmap1.md).</span></span>                    |
| <span data-ttu-id="22d04-198">GL \_ «Карта1», \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="22d04-198">GL\_MAP1\_VERTEX\_3</span></span>         | <span data-ttu-id="22d04-199">Если этот флажок установлен, вызовы **glEvalCoord1**, **glEvalMesh1** и **glEvalPoint1** создают координаты *x*, *y* и *z* .</span><span class="sxs-lookup"><span data-stu-id="22d04-199">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="22d04-200">См. также **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="22d04-200">See also **glMap1**.</span></span>                                                                                                            |
| <span data-ttu-id="22d04-201">\_«Карта1»ная \_ вершина GL \_ 4</span><span class="sxs-lookup"><span data-stu-id="22d04-201">GL\_MAP1\_VERTEX\_4</span></span>         | <span data-ttu-id="22d04-202">Если этот флажок установлен, вызовы [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) создают однородные координаты *x*, *y*, *z* и *w* вершин.</span><span class="sxs-lookup"><span data-stu-id="22d04-202">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="22d04-203">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-203">See also [**glMap1**](glmap1.md).</span></span> |
| <span data-ttu-id="22d04-204">MAP2 GL, \_ \_ Цвет \_ 4</span><span class="sxs-lookup"><span data-stu-id="22d04-204">GL\_MAP2\_COLOR\_4</span></span>          | <span data-ttu-id="22d04-205">Если этот флажок установлен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) создают значения RGBA.</span><span class="sxs-lookup"><span data-stu-id="22d04-205">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="22d04-206">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-206">See also [**glMap2**](glmap2.md).</span></span>                                           |
| <span data-ttu-id="22d04-207">\_Индекс MAP2 \_ GL</span><span class="sxs-lookup"><span data-stu-id="22d04-207">GL\_MAP2\_INDEX</span></span>             | <span data-ttu-id="22d04-208">Если этот флажок установлен, вызовы **glEvalCoord2**, **glEvalMesh2** и **glEvalPoint2** создают цветовые индексы.</span><span class="sxs-lookup"><span data-stu-id="22d04-208">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate color indexes.</span></span> <span data-ttu-id="22d04-209">См. также **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="22d04-209">See also **glMap2**.</span></span>                                                                                                                                   |
| <span data-ttu-id="22d04-210">MAP2 GL ( \_ \_ Обычная)</span><span class="sxs-lookup"><span data-stu-id="22d04-210">GL\_MAP2\_NORMAL</span></span>            | <span data-ttu-id="22d04-211">Если этот режим включен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) создают нормали.</span><span class="sxs-lookup"><span data-stu-id="22d04-211">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="22d04-212">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-212">See also [**glMap2**](glmap2.md).</span></span>                                               |
| <span data-ttu-id="22d04-213">\_MAP2 \_ текстура GL \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="22d04-213">GL\_MAP2\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="22d04-214">Если этот флажок установлен, вызовы **glEvalCoord2**, **glEvalMesh2** и **glEvalPoint2** формируют *координаты* текстуры.</span><span class="sxs-lookup"><span data-stu-id="22d04-214">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s* texture coordinates.</span></span> <span data-ttu-id="22d04-215">См. также **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="22d04-215">See also **glMap2**.</span></span>                                                                                                                         |
| <span data-ttu-id="22d04-216">GL \_ MAP2 \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="22d04-216">GL\_MAP2\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="22d04-217">Если этот флажок установлен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) формируют координаты *s* и *t* .</span><span class="sxs-lookup"><span data-stu-id="22d04-217">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="22d04-218">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-218">See also [**glMap2**](glmap2.md).</span></span>                       |
| <span data-ttu-id="22d04-219">\_MAP2 \_ текстура GL \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="22d04-219">GL\_MAP2\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="22d04-220">Если этот флажок установлен, вызовы **glEvalCoord2**, **glEvalMesh2** и **glEvalPoint2** формируют координаты *s*, *t* и *r* .</span><span class="sxs-lookup"><span data-stu-id="22d04-220">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="22d04-221">См. также **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="22d04-221">See also **glMap2**.</span></span>                                                                                                           |
| <span data-ttu-id="22d04-222">\_MAP2 \_ текстура GL \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="22d04-222">GL\_MAP2\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="22d04-223">Если этот флажок установлен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) создают координаты текстуры *s*, *t*, *r* и *q* .</span><span class="sxs-lookup"><span data-stu-id="22d04-223">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="22d04-224">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-224">See also [**glMap2**](glmap2.md).</span></span>            |
| <span data-ttu-id="22d04-225">GL \_ map2, \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="22d04-225">GL\_MAP2\_VERTEX\_3</span></span>         | <span data-ttu-id="22d04-226">Если этот флажок установлен, вызовы **glEvalCoord2**, **glEvalMesh2** и **glEvalPoint2** создают координаты *x*, *y* и *z* .</span><span class="sxs-lookup"><span data-stu-id="22d04-226">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="22d04-227">См. также **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="22d04-227">See also **glMap2**.</span></span>                                                                                                            |
| <span data-ttu-id="22d04-228">\_MAP2ная \_ вершина GL \_ 4</span><span class="sxs-lookup"><span data-stu-id="22d04-228">GL\_MAP2\_VERTEX\_4</span></span>         | <span data-ttu-id="22d04-229">Если этот флажок установлен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) создают однородные координаты *x*, *y*, *z* и *w* вершин.</span><span class="sxs-lookup"><span data-stu-id="22d04-229">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="22d04-230">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-230">See also [**glMap2**](glmap2.md).</span></span> |
| <span data-ttu-id="22d04-231">\_нормализация GL</span><span class="sxs-lookup"><span data-stu-id="22d04-231">GL\_NORMALIZE</span></span>               | <span data-ttu-id="22d04-232">Если параметр включен, обычные векторы, заданные с помощью **глнормал** , масштабируются до длины единицы после преобразования.</span><span class="sxs-lookup"><span data-stu-id="22d04-232">If enabled, normal vectors specified with **glNormal** are scaled to unit length after transformation.</span></span> <span data-ttu-id="22d04-233">См. [**глнормал**](glnormal-functions.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-233">See [**glNormal**](glnormal-functions.md).</span></span>                                                                                                          |
| <span data-ttu-id="22d04-234">\_ \_ гладкий пункт GL</span><span class="sxs-lookup"><span data-stu-id="22d04-234">GL\_POINT\_SMOOTH</span></span>           | <span data-ttu-id="22d04-235">Если параметр включен, рисуйте точки с правильной фильтрацией.</span><span class="sxs-lookup"><span data-stu-id="22d04-235">If enabled, draw points with proper filtering.</span></span> <span data-ttu-id="22d04-236">При отключении Нарисуйте точки с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="22d04-236">If disabled, draw aliased points.</span></span> <span data-ttu-id="22d04-237">См. [**глпоинтсизе**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-237">See [**glPointSize**](glpointsize.md).</span></span>                                                                                                                                    |
| <span data-ttu-id="22d04-238">\_ \_ Заливка смещения МНОГОУГОЛЬНИКа GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-238">GL\_POLYGON\_OFFSET\_FILL</span></span>   | <span data-ttu-id="22d04-239">Если параметр включен и многоугольник отображается в \_ режиме заполнения GL, то смещение добавляется к значениям глубины фрагментов многоугольника перед выполнением сравнения глубины.</span><span class="sxs-lookup"><span data-stu-id="22d04-239">If enabled, and if the polygon is rendered in GL\_FILL mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="22d04-240">См. [**глполигоноффсет**](glpolygonoffset.md)**.**</span><span class="sxs-lookup"><span data-stu-id="22d04-240">See [**glPolygonOffset**](glpolygonoffset.md)**.**</span></span>                                      |
| <span data-ttu-id="22d04-241">\_строка смещения многоугольника GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="22d04-241">GL\_POLYGON\_OFFSET\_LINE</span></span>   | <span data-ttu-id="22d04-242">Если параметр включен и многоугольник отображается в \_ режиме строки GL, то перед сравнением глубины добавляется смещение к значениям глубины фрагментов многоугольника.</span><span class="sxs-lookup"><span data-stu-id="22d04-242">If enabled, and if the polygon is rendered in GL\_LINE mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="22d04-243">См. **глполигоноффсет**.</span><span class="sxs-lookup"><span data-stu-id="22d04-243">See **glPolygonOffset**.</span></span>                                                                 |
| <span data-ttu-id="22d04-244">\_точка смещения многоугольника GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="22d04-244">GL\_POLYGON\_OFFSET\_POINT</span></span>  | <span data-ttu-id="22d04-245">Если этот параметр включен, смещение добавляется к значениям глубины фрагментов многоугольника перед выполнением сравнения с глубиной, если многоугольник отображается в \_ режиме точки GL.</span><span class="sxs-lookup"><span data-stu-id="22d04-245">If enabled, an offset is added to depth values of a polygon's fragments before the depth comparison is performed, if the polygon is rendered in GL\_POINT mode.</span></span> <span data-ttu-id="22d04-246">См. [**глполигоноффсет**](glpolygonoffset.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-246">See [**glPolygonOffset**](glpolygonoffset.md).</span></span>                                             |
| <span data-ttu-id="22d04-247">\_несглаженный МНОГОУГОЛЬНИК GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-247">GL\_POLYGON\_SMOOTH</span></span>         | <span data-ttu-id="22d04-248">Если параметр включен, нарисуйте многоугольники с правильной фильтрацией.</span><span class="sxs-lookup"><span data-stu-id="22d04-248">If enabled, draw polygons with proper filtering.</span></span> <span data-ttu-id="22d04-249">Если этот отключен, нарисуйте многоугольники с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="22d04-249">If disabled, draw aliased polygons.</span></span> <span data-ttu-id="22d04-250">См. [**глполигонмоде**](glpolygonmode.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-250">See [**glPolygonMode**](glpolygonmode.md).</span></span>                                                                                                                            |
| <span data-ttu-id="22d04-251">\_стиппле многоугольника GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-251">GL\_POLYGON\_STIPPLE</span></span>        | <span data-ttu-id="22d04-252">Если параметр включен, при отрисовке многоугольников используется шаблон стиппле с использованием текущего многоугольника.</span><span class="sxs-lookup"><span data-stu-id="22d04-252">If enabled, use the current polygon stipple pattern when rendering polygons.</span></span> <span data-ttu-id="22d04-253">См. [**глполигонстиппле**](glpolygonstipple.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-253">See [**glPolygonStipple**](glpolygonstipple.md).</span></span>                                                                                                                              |
| <span data-ttu-id="22d04-254">\_тест вырезание GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-254">GL\_SCISSOR\_TEST</span></span>           | <span data-ttu-id="22d04-255">Если параметр включен, отбросить фрагменты, расположенные за пределами прямоугольной прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="22d04-255">If enabled, discard fragments that are outside the scissor rectangle.</span></span> <span data-ttu-id="22d04-256">См. [**глсЦиссор**](glscissor.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-256">See [**glScissor**](glscissor.md).</span></span>                                                                                                                                                   |
| <span data-ttu-id="22d04-257">\_тест шаблона \_ GL</span><span class="sxs-lookup"><span data-stu-id="22d04-257">GL\_STENCIL\_TEST</span></span>           | <span data-ttu-id="22d04-258">Если параметр включен, проверка трафарета и обновление буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="22d04-258">If enabled, do stencil testing and update the stencil buffer.</span></span> <span data-ttu-id="22d04-259">См. раздел [**глстенЦилфунк**](glstencilfunc.md) and [**глстенЦилоп**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-259">See [**glStencilFunc**](glstencilfunc.md) and [**glStencilOp**](glstencilop.md).</span></span>                                                                                                            |
| <span data-ttu-id="22d04-260">\_Одномерное текстура GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-260">GL\_TEXTURE\_1D</span></span>             | <span data-ttu-id="22d04-261">Если этот флажок включен, выполняется одномерный текстурированный текстура (если одновременно не включено двухмерный текстурирование).</span><span class="sxs-lookup"><span data-stu-id="22d04-261">If enabled, one-dimensional texturing is performed (unless two-dimensional texturing is also enabled).</span></span> <span data-ttu-id="22d04-262">См. [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-262">See [**glTexImage1D**](glteximage1d.md).</span></span>                                                                                                            |
| <span data-ttu-id="22d04-263">\_2D-текстура GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-263">GL\_TEXTURE\_2D</span></span>             | <span data-ttu-id="22d04-264">Если этот флажок включен, выполняется двухмерный текстурирование.</span><span class="sxs-lookup"><span data-stu-id="22d04-264">If enabled, two-dimensional texturing is performed.</span></span> <span data-ttu-id="22d04-265">См. [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-265">See [**glTexImage2D**](glteximage2d.md).</span></span>                                                                                                                                                               |
| <span data-ttu-id="22d04-266">\_ \_ Общие вопросы о ТЕКСТУРе GL \_</span><span class="sxs-lookup"><span data-stu-id="22d04-266">GL\_TEXTURE\_GEN\_Q</span></span>         | <span data-ttu-id="22d04-267">Если параметр включен, координата текстуры *q* вычисляются с помощью функции формирования текстуры, определенной с помощью [**глтексжен**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-267">If enabled, the *q* texture coordinate is computed using the texture-generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="22d04-268">В противном случае используется текущая Координата текстуры *q* .</span><span class="sxs-lookup"><span data-stu-id="22d04-268">Otherwise, the current *q* texture coordinate is used.</span></span>                                                        |
| <span data-ttu-id="22d04-269">заполнение текстур главной книги \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="22d04-269">GL\_TEXTURE\_GEN\_R</span></span>         | <span data-ttu-id="22d04-270">Если параметр включен, координата текстуры *r* вычисляются с помощью функции формирования текстуры, определенной с помощью [**глтексжен**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-270">If enabled, the *r* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="22d04-271">Если этот параметр отключен, используется текущая Координата текстуры *r* .</span><span class="sxs-lookup"><span data-stu-id="22d04-271">If disabled, the current *r* texture coordinate is used.</span></span>                                                      |
| <span data-ttu-id="22d04-272">\_Gen текстура GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="22d04-272">GL\_TEXTURE\_GEN\_S</span></span>         | <span data-ttu-id="22d04-273">Если параметр включен, координата текстуры *s* вычисляются с помощью функции формирования текстуры, определенной с помощью **глтексжен**.</span><span class="sxs-lookup"><span data-stu-id="22d04-273">If enabled, the *s* texture coordinate is computed using the texture generation function defined with **glTexGen**.</span></span> <span data-ttu-id="22d04-274">Если этот параметр отключен, используется координата *текущей текстуры* .</span><span class="sxs-lookup"><span data-stu-id="22d04-274">If disabled, the current *s* texture coordinate is used.</span></span>                                                                                |
| <span data-ttu-id="22d04-275">\_Gen текстура GL \_ \_ T</span><span class="sxs-lookup"><span data-stu-id="22d04-275">GL\_TEXTURE\_GEN\_T</span></span>         | <span data-ttu-id="22d04-276">Если параметр включен, координата текстуры *t* вычисляются с помощью функции формирования текстуры, определенной с помощью [**глтексжен**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="22d04-276">If enabled, the *t* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="22d04-277">Если параметр отключен, используется текущая координата *t* текстура.</span><span class="sxs-lookup"><span data-stu-id="22d04-277">If disabled, the current *t* texture coordinate is used.</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="22d04-278">Требования</span><span class="sxs-lookup"><span data-stu-id="22d04-278">Requirements</span></span>



| <span data-ttu-id="22d04-279">Требование</span><span class="sxs-lookup"><span data-stu-id="22d04-279">Requirement</span></span> | <span data-ttu-id="22d04-280">Значение</span><span class="sxs-lookup"><span data-stu-id="22d04-280">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22d04-281">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22d04-281">Minimum supported client</span></span><br/> | <span data-ttu-id="22d04-282">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22d04-282">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="22d04-283">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22d04-283">Minimum supported server</span></span><br/> | <span data-ttu-id="22d04-284">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22d04-284">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22d04-285">Заголовок</span><span class="sxs-lookup"><span data-stu-id="22d04-285">Header</span></span><br/>                   | <dl> <span data-ttu-id="22d04-286"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="22d04-286"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="22d04-287">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22d04-287">Library</span></span><br/>                  | <dl> <span data-ttu-id="22d04-288"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22d04-288"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="22d04-289">DLL</span><span class="sxs-lookup"><span data-stu-id="22d04-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22d04-290"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22d04-290"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d04-291">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22d04-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d04-292">**глалфафунк**</span><span class="sxs-lookup"><span data-stu-id="22d04-292">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="22d04-293">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="22d04-293">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="22d04-294">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="22d04-294">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="22d04-295">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="22d04-295">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="22d04-296">**глклипплане**</span><span class="sxs-lookup"><span data-stu-id="22d04-296">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="22d04-297">**глколорматериал**</span><span class="sxs-lookup"><span data-stu-id="22d04-297">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="22d04-298">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="22d04-298">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="22d04-299">**глкуллфаце**</span><span class="sxs-lookup"><span data-stu-id="22d04-299">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="22d04-300">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="22d04-300">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="22d04-301">**глдепсранже**</span><span class="sxs-lookup"><span data-stu-id="22d04-301">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="22d04-302">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="22d04-302">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="22d04-303">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="22d04-303">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="22d04-304">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="22d04-304">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="22d04-305">**гленд**</span><span class="sxs-lookup"><span data-stu-id="22d04-305">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="22d04-306">**glEvalCoord1**</span><span class="sxs-lookup"><span data-stu-id="22d04-306">**glEvalCoord1**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="22d04-307">**glEvalMesh1**</span><span class="sxs-lookup"><span data-stu-id="22d04-307">**glEvalMesh1**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="22d04-308">**glEvalPoint1**</span><span class="sxs-lookup"><span data-stu-id="22d04-308">**glEvalPoint1**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="22d04-309">**глфог**</span><span class="sxs-lookup"><span data-stu-id="22d04-309">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="22d04-310">**глжет**</span><span class="sxs-lookup"><span data-stu-id="22d04-310">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="22d04-311">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="22d04-311">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="22d04-312">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="22d04-312">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="22d04-313">**гллигхт**</span><span class="sxs-lookup"><span data-stu-id="22d04-313">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="22d04-314">**гллигхтмодел**</span><span class="sxs-lookup"><span data-stu-id="22d04-314">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="22d04-315">**гллиневидс**</span><span class="sxs-lookup"><span data-stu-id="22d04-315">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="22d04-316">**гллинестиппле**</span><span class="sxs-lookup"><span data-stu-id="22d04-316">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="22d04-317">**гллогикоп**</span><span class="sxs-lookup"><span data-stu-id="22d04-317">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="22d04-318">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="22d04-318">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="22d04-319">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="22d04-319">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="22d04-320">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="22d04-320">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="22d04-321">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="22d04-321">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="22d04-322">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="22d04-322">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="22d04-323">**глпоинтсизе**</span><span class="sxs-lookup"><span data-stu-id="22d04-323">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="22d04-324">**глполигонмоде**</span><span class="sxs-lookup"><span data-stu-id="22d04-324">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="22d04-325">**глполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="22d04-325">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="22d04-326">**глсЦиссор**</span><span class="sxs-lookup"><span data-stu-id="22d04-326">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="22d04-327">**глстенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="22d04-327">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="22d04-328">**глстенЦилоп**</span><span class="sxs-lookup"><span data-stu-id="22d04-328">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="22d04-329">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="22d04-329">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="22d04-330">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="22d04-330">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="22d04-331">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="22d04-331">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="22d04-332">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="22d04-332">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





