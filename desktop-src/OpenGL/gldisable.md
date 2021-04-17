---
title: Функция Глдисабле (GL. h)
description: Функции Гленабле и Глдисабле включают или отключают возможности OpenGL. | Функция Глдисабле (GL. h)
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- Функция Глдисабле OpenGL
topic_type:
- apiref
api_name:
- glDisable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff5c12e53eb060777f75ad537bed265401a7a26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684952"
---
# <a name="gldisable-function"></a><span data-ttu-id="28599-105">Функция Глдисабле</span><span class="sxs-lookup"><span data-stu-id="28599-105">glDisable function</span></span>

<span data-ttu-id="28599-106">Функции [**гленабле**](glenable.md) и **глдисабле** включают или отключают возможности OpenGL.</span><span class="sxs-lookup"><span data-stu-id="28599-106">The [**glEnable**](glenable.md) and **glDisable** functions enable or disable OpenGL capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="28599-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28599-107">Syntax</span></span>


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a><span data-ttu-id="28599-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="28599-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28599-109">*конец*</span><span class="sxs-lookup"><span data-stu-id="28599-109">*cap*</span></span> 
</dt> <dd>

<span data-ttu-id="28599-110">Символьная константа, указывающая на возможность OpenGL.</span><span class="sxs-lookup"><span data-stu-id="28599-110">A symbolic constant indicating an OpenGL capability.</span></span>

<span data-ttu-id="28599-111">Сведения о том, что может занять *ограничение* значений, см. в следующем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="28599-111">For discussion of the values *cap* can take, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28599-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28599-112">Return value</span></span>

<span data-ttu-id="28599-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="28599-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="28599-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="28599-114">Error codes</span></span>

<span data-ttu-id="28599-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="28599-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="28599-116">Имя</span><span class="sxs-lookup"><span data-stu-id="28599-116">Name</span></span>                                                                                                  | <span data-ttu-id="28599-117">Значение</span><span class="sxs-lookup"><span data-stu-id="28599-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28599-118"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="28599-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="28599-119">*ограничение* не было одним из значений, перечисленных в предыдущем разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="28599-119">*cap* was not one of the values listed in the preceding Remarks section.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="28599-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="28599-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="28599-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="28599-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="28599-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28599-122">Remarks</span></span>

<span data-ttu-id="28599-123">Функции [**гленабле**](glenable.md) и **глдисабле** включают и отключают различные графические возможности OpenGL.</span><span class="sxs-lookup"><span data-stu-id="28599-123">The [**glEnable**](glenable.md) and **glDisable** functions enable and disable various OpenGL graphics capabilities.</span></span> <span data-ttu-id="28599-124">Чтобы определить текущее значение любой возможности, используйте [**глисенаблед**](glisenabled.md) или [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="28599-124">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="28599-125">И [**гленабле**](glenable.md) , и **глдисабле** принимают один аргумент ( *Cap*), который может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="28599-125">Both [**glEnable**](glenable.md) and **glDisable** take a single argument, *cap*, which can assume one of the following values:</span></span>



| <span data-ttu-id="28599-126">Значение</span><span class="sxs-lookup"><span data-stu-id="28599-126">Value</span></span>                       | <span data-ttu-id="28599-127">Значение</span><span class="sxs-lookup"><span data-stu-id="28599-127">Meaning</span></span>                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28599-128">\_альфа- \_ тест GL</span><span class="sxs-lookup"><span data-stu-id="28599-128">GL\_ALPHA\_TEST</span></span>             | <span data-ttu-id="28599-129">Если этот флажок включен, выполните тестирование альфа-версии.</span><span class="sxs-lookup"><span data-stu-id="28599-129">If enabled, do alpha testing.</span></span> <span data-ttu-id="28599-130">См. [**глалфафунк**](glalphafunc.md).</span><span class="sxs-lookup"><span data-stu-id="28599-130">See [**glAlphaFunc**](glalphafunc.md).</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="28599-131">Автоматический режим "GL" \_ \_</span><span class="sxs-lookup"><span data-stu-id="28599-131">GL\_AUTO\_NORMAL</span></span>            | <span data-ttu-id="28599-132">Если этот режим включен, обычные векторы области вычислений изменяются в том случае, если вершины GL \_ MAP2 \_ вершина \_ 3 или GL \_ MAP2 \_ вершины \_ 4 созданы.</span><span class="sxs-lookup"><span data-stu-id="28599-132">If enabled, compute surface normal vectors analytically when either GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4 has generated vertices.</span></span> <span data-ttu-id="28599-133">См. [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="28599-133">See [**glMap2**](glmap2.md).</span></span>                                                                                        |
| <span data-ttu-id="28599-134">ГК \_ Blend</span><span class="sxs-lookup"><span data-stu-id="28599-134">GL\_BLEND</span></span>                   | <span data-ttu-id="28599-135">Если параметр включен, то наложение входящих значений цвета RGBA на значения в цветовых буферах.</span><span class="sxs-lookup"><span data-stu-id="28599-135">If enabled, blend the incoming RGBA color values with the values in the color buffers.</span></span> <span data-ttu-id="28599-136">См. [**глблендфунк**](glblendfunc.md).</span><span class="sxs-lookup"><span data-stu-id="28599-136">See [**glBlendFunc**](glblendfunc.md).</span></span>                                                                                                                              |
| <span data-ttu-id="28599-137">В \_ главной \_ плоскости Clip,*i*</span><span class="sxs-lookup"><span data-stu-id="28599-137">GL\_CLIP\_PLANE *i*</span></span>          | <span data-ttu-id="28599-138">Если этот флажок установлен, обрезает геометрию относительно определяемой пользователем *плоскости-* отсечения.</span><span class="sxs-lookup"><span data-stu-id="28599-138">If enabled, clip geometry against user-defined clipping plane *i*.</span></span> <span data-ttu-id="28599-139">См. [**глклипплане**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="28599-139">See [**glClipPlane**](glclipplane.md).</span></span>                                                                                                                                                  |
| <span data-ttu-id="28599-140">\_ \_ Операция логики цвета GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-140">GL\_COLOR\_LOGIC\_OP</span></span>        | <span data-ttu-id="28599-141">Если параметр включен, применяется текущая логическая операция к входящему значению цвета и цветового буфера RGBA.</span><span class="sxs-lookup"><span data-stu-id="28599-141">If enabled, apply the current logical operation to the incoming RGBA color and color buffer values.</span></span> <span data-ttu-id="28599-142">См. [**гллогикоп**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="28599-142">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                     |
| <span data-ttu-id="28599-143">\_цветовой \_ материал GL</span><span class="sxs-lookup"><span data-stu-id="28599-143">GL\_COLOR\_MATERIAL</span></span>         | <span data-ttu-id="28599-144">Если параметр включен, то один или несколько параметров материала отписывают текущий цвет.</span><span class="sxs-lookup"><span data-stu-id="28599-144">If enabled, have one or more material parameters track the current color.</span></span> <span data-ttu-id="28599-145">См. [**глколорматериал**](glcolormaterial.md).</span><span class="sxs-lookup"><span data-stu-id="28599-145">See [**glColorMaterial**](glcolormaterial.md).</span></span>                                                                                                                                   |
| <span data-ttu-id="28599-146">\_лицо для отбора GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-146">GL\_CULL\_FACE</span></span>              | <span data-ttu-id="28599-147">При включении отбор многоугольников на основе их обмотки в координатах окна.</span><span class="sxs-lookup"><span data-stu-id="28599-147">If enabled, cull polygons based on their winding in window coordinates.</span></span> <span data-ttu-id="28599-148">См. [**глкуллфаце**](glcullface.md).</span><span class="sxs-lookup"><span data-stu-id="28599-148">See [**glCullFace**](glcullface.md).</span></span>                                                                                                                                               |
| <span data-ttu-id="28599-149">\_тест глубины \_ GL</span><span class="sxs-lookup"><span data-stu-id="28599-149">GL\_DEPTH\_TEST</span></span>             | <span data-ttu-id="28599-150">Если этот параметр включен, выполняется сравнение глубин и обновление буфера глубины.</span><span class="sxs-lookup"><span data-stu-id="28599-150">If enabled, do depth comparisons and update the depth buffer.</span></span> <span data-ttu-id="28599-151">См. раздел [**глдепсфунк**](gldepthfunc.md) and [**глдепсранже**](gldepthrange.md).</span><span class="sxs-lookup"><span data-stu-id="28599-151">See [**glDepthFunc**](gldepthfunc.md) and [**glDepthRange**](gldepthrange.md).</span></span>                                                                                                              |
| <span data-ttu-id="28599-152">\_ДИЗЕРИНГ GL</span><span class="sxs-lookup"><span data-stu-id="28599-152">GL\_DITHER</span></span>                  | <span data-ttu-id="28599-153">Если параметр включен, то перед записью цветовых компонентов или индексов в буфер цвета.</span><span class="sxs-lookup"><span data-stu-id="28599-153">If enabled, dither color components or indexes before they are written to the color buffer.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="28599-154">\_туман GL</span><span class="sxs-lookup"><span data-stu-id="28599-154">GL\_FOG</span></span>                     | <span data-ttu-id="28599-155">Если параметр включен, смешивается цвет тумана в цвет после текстурирования.</span><span class="sxs-lookup"><span data-stu-id="28599-155">If enabled, blend a fog color into the post-texturing color.</span></span> <span data-ttu-id="28599-156">См. [**глфог**](glfog.md).</span><span class="sxs-lookup"><span data-stu-id="28599-156">See [**glFog**](glfog.md).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="28599-157">\_ \_ Операция логики индекса GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-157">GL\_INDEX\_LOGIC\_OP</span></span>        | <span data-ttu-id="28599-158">Если параметр включен, применяется текущая логическая операция к индексу входящего индекса и цветового буфера.</span><span class="sxs-lookup"><span data-stu-id="28599-158">If enabled, apply the current logical operation to the incoming index and color buffer indices.</span></span> <span data-ttu-id="28599-159">См. [**гллогикоп**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="28599-159">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                         |
| <span data-ttu-id="28599-160">\_Непростая GL</span><span class="sxs-lookup"><span data-stu-id="28599-160">GL\_LIGHT *i*</span></span>                | <span data-ttu-id="28599-161">Если параметр включен, включите *в оценку* уравнение освещения освещение.</span><span class="sxs-lookup"><span data-stu-id="28599-161">If enabled, include light *i* in the evaluation of the lighting equation.</span></span> <span data-ttu-id="28599-162">См. раздел [**гллигхтмодел**](gllightmodel-functions.md) and [**гллигхт**](gllight-functions.md).</span><span class="sxs-lookup"><span data-stu-id="28599-162">See [**glLightModel**](gllightmodel-functions.md) and [**glLight**](gllight-functions.md).</span></span>                                                                                      |
| <span data-ttu-id="28599-163">освещение в ГК \_</span><span class="sxs-lookup"><span data-stu-id="28599-163">GL\_LIGHTING</span></span>                | <span data-ttu-id="28599-164">Если параметр включен, используйте текущие параметры освещения для расчета цвета или индекса вершин.</span><span class="sxs-lookup"><span data-stu-id="28599-164">If enabled, use the current lighting parameters to compute the vertex color or index.</span></span> <span data-ttu-id="28599-165">Если параметр отключен, связывает текущий цвет или индекс с каждой вершиной.</span><span class="sxs-lookup"><span data-stu-id="28599-165">If disabled, associate the current color or index with each vertex.</span></span> <span data-ttu-id="28599-166">См. раздел [**глматериал**](glmaterial-functions.md), **гллигхтмодел** и **гллигхт**.</span><span class="sxs-lookup"><span data-stu-id="28599-166">See [**glMaterial**](glmaterial-functions.md), **glLightModel**, and **glLight**.</span></span>                |
| <span data-ttu-id="28599-167">\_ \_ сглаженная линия GL</span><span class="sxs-lookup"><span data-stu-id="28599-167">GL\_LINE\_SMOOTH</span></span>            | <span data-ttu-id="28599-168">Если параметр включен, нарисуйте линии с правильной фильтрацией.</span><span class="sxs-lookup"><span data-stu-id="28599-168">If enabled, draw lines with correct filtering.</span></span> <span data-ttu-id="28599-169">При отключении нарисуйте линии с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="28599-169">If disabled, draw aliased lines.</span></span> <span data-ttu-id="28599-170">См. [**гллиневидс**](gllinewidth.md).</span><span class="sxs-lookup"><span data-stu-id="28599-170">See [**glLineWidth**](gllinewidth.md).</span></span>                                                                                                                                     |
| <span data-ttu-id="28599-171">\_стиппле строки \_ GL</span><span class="sxs-lookup"><span data-stu-id="28599-171">GL\_LINE\_STIPPLE</span></span>           | <span data-ttu-id="28599-172">Если параметр включен, используйте шаблон стиппле текущей линии при рисовании линий.</span><span class="sxs-lookup"><span data-stu-id="28599-172">If enabled, use the current line stipple pattern when drawing lines.</span></span> <span data-ttu-id="28599-173">См. [**гллинестиппле**](gllinestipple.md).</span><span class="sxs-lookup"><span data-stu-id="28599-173">See [**glLineStipple**](gllinestipple.md).</span></span>                                                                                                                                            |
| <span data-ttu-id="28599-174">\_логическая \_ Операция GL</span><span class="sxs-lookup"><span data-stu-id="28599-174">GL\_LOGIC\_OP</span></span>               | <span data-ttu-id="28599-175">Если параметр включен, примените выбранную в данный момент логическую операцию к индексам входящих и цветовых буферов.</span><span class="sxs-lookup"><span data-stu-id="28599-175">If enabled, apply the currently selected logical operation to the incoming and color-buffer indexes.</span></span> <span data-ttu-id="28599-176">См. [**гллогикоп**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="28599-176">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                    |
| <span data-ttu-id="28599-177">«Карта1» GL, \_ \_ Цвет \_ 4</span><span class="sxs-lookup"><span data-stu-id="28599-177">GL\_MAP1\_COLOR\_4</span></span>          | <span data-ttu-id="28599-178">Если этот флажок установлен, вызовы [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) создают значения RGBA.</span><span class="sxs-lookup"><span data-stu-id="28599-178">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="28599-179">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="28599-179">See also [**glMap1**](glmap1.md).</span></span>                                           |
| <span data-ttu-id="28599-180">\_Индекс «КАРТА1» \_ GL</span><span class="sxs-lookup"><span data-stu-id="28599-180">GL\_MAP1\_INDEX</span></span>             | <span data-ttu-id="28599-181">Если этот флажок установлен, вызовы **glEvalCoord1**, **glEvalMesh1** и **glEvalPoint1** создают цветовые индексы.</span><span class="sxs-lookup"><span data-stu-id="28599-181">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate color indexes.</span></span> <span data-ttu-id="28599-182">См. также **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="28599-182">See also **glMap1**.</span></span>                                                                                                                                   |
| <span data-ttu-id="28599-183">«Карта1» GL ( \_ \_ Обычная)</span><span class="sxs-lookup"><span data-stu-id="28599-183">GL\_MAP1\_NORMAL</span></span>            | <span data-ttu-id="28599-184">Если этот режим включен, вызовы [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) создают нормали.</span><span class="sxs-lookup"><span data-stu-id="28599-184">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="28599-185">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="28599-185">See also [**glMap1**](glmap1.md).</span></span>                                               |
| <span data-ttu-id="28599-186">\_«Карта1» \_ текстура GL \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="28599-186">GL\_MAP1\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="28599-187">Если этот флажок установлен, вызовы **glEvalCoord1**, **glEvalMesh1** и **glEvalPoint1** формируют *координаты* текстуры.</span><span class="sxs-lookup"><span data-stu-id="28599-187">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s* texture coordinates.</span></span> <span data-ttu-id="28599-188">См. также **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="28599-188">See also **glMap1**.</span></span>                                                                                                                         |
| <span data-ttu-id="28599-189">GL \_ «Карта1» \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="28599-189">GL\_MAP1\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="28599-190">Если этот флажок установлен, вызовы [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) формируют координаты *s* и *t* .</span><span class="sxs-lookup"><span data-stu-id="28599-190">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="28599-191">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="28599-191">See also [**glMap1**](glmap1.md).</span></span>                       |
| <span data-ttu-id="28599-192">\_«Карта1» \_ текстура GL \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="28599-192">GL\_MAP1\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="28599-193">Если этот флажок установлен, вызовы **glEvalCoord1**, **glEvalMesh1** и **glEvalPoint1** формируют координаты *s*, *t* и *r* .</span><span class="sxs-lookup"><span data-stu-id="28599-193">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="28599-194">См. также **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="28599-194">See also **glMap1**.</span></span>                                                                                                           |
| <span data-ttu-id="28599-195">\_«Карта1» \_ текстура GL \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="28599-195">GL\_MAP1\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="28599-196">Если этот флажок установлен, вызовы [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) создают координаты текстуры *s*, *t*, *r* и *q* .</span><span class="sxs-lookup"><span data-stu-id="28599-196">If enabled, calls to [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="28599-197">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="28599-197">See also [**glMap1**](glmap1.md).</span></span>                    |
| <span data-ttu-id="28599-198">GL \_ «Карта1», \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="28599-198">GL\_MAP1\_VERTEX\_3</span></span>         | <span data-ttu-id="28599-199">Если этот флажок установлен, вызовы **glEvalCoord1**, **glEvalMesh1** и **glEvalPoint1** создают координаты *x*, *y* и *z* .</span><span class="sxs-lookup"><span data-stu-id="28599-199">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="28599-200">См. также **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="28599-200">See also **glMap1**.</span></span>                                                                                                            |
| <span data-ttu-id="28599-201">\_«Карта1»ная \_ вершина GL \_ 4</span><span class="sxs-lookup"><span data-stu-id="28599-201">GL\_MAP1\_VERTEX\_4</span></span>         | <span data-ttu-id="28599-202">Если этот флажок установлен, вызовы [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)и [**glEvalPoint1**](glevalpoint.md) создают однородные координаты *x*, *y*, *z* и *w* вершин.</span><span class="sxs-lookup"><span data-stu-id="28599-202">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="28599-203">См. также [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="28599-203">See also [**glMap1**](glmap1.md).</span></span> |
| <span data-ttu-id="28599-204">MAP2 GL, \_ \_ Цвет \_ 4</span><span class="sxs-lookup"><span data-stu-id="28599-204">GL\_MAP2\_COLOR\_4</span></span>          | <span data-ttu-id="28599-205">Если этот флажок установлен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) создают значения RGBA.</span><span class="sxs-lookup"><span data-stu-id="28599-205">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="28599-206">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="28599-206">See also [**glMap2**](glmap2.md).</span></span>                                           |
| <span data-ttu-id="28599-207">\_Индекс MAP2 \_ GL</span><span class="sxs-lookup"><span data-stu-id="28599-207">GL\_MAP2\_INDEX</span></span>             | <span data-ttu-id="28599-208">Если этот флажок установлен, вызовы **glEvalCoord2**, **glEvalMesh2** и **glEvalPoint2** создают цветовые индексы.</span><span class="sxs-lookup"><span data-stu-id="28599-208">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate color indexes.</span></span> <span data-ttu-id="28599-209">См. также **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="28599-209">See also **glMap2**.</span></span>                                                                                                                                   |
| <span data-ttu-id="28599-210">MAP2 GL ( \_ \_ Обычная)</span><span class="sxs-lookup"><span data-stu-id="28599-210">GL\_MAP2\_NORMAL</span></span>            | <span data-ttu-id="28599-211">Если этот режим включен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) создают нормали.</span><span class="sxs-lookup"><span data-stu-id="28599-211">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="28599-212">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="28599-212">See also [**glMap2**](glmap2.md).</span></span>                                               |
| <span data-ttu-id="28599-213">\_MAP2 \_ текстура GL \_ курд \_ 1</span><span class="sxs-lookup"><span data-stu-id="28599-213">GL\_MAP2\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="28599-214">Если этот флажок установлен, вызовы **glEvalCoord2**, **glEvalMesh2** и **glEvalPoint2** формируют *координаты* текстуры.</span><span class="sxs-lookup"><span data-stu-id="28599-214">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s* texture coordinates.</span></span> <span data-ttu-id="28599-215">См. также **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="28599-215">See also **glMap2**.</span></span>                                                                                                                         |
| <span data-ttu-id="28599-216">GL \_ MAP2 \_ текстура \_ курд \_ 2</span><span class="sxs-lookup"><span data-stu-id="28599-216">GL\_MAP2\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="28599-217">Если этот флажок установлен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) формируют координаты *s* и *t* .</span><span class="sxs-lookup"><span data-stu-id="28599-217">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="28599-218">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="28599-218">See also [**glMap2**](glmap2.md).</span></span>                       |
| <span data-ttu-id="28599-219">\_MAP2 \_ текстура GL \_ курд \_ 3</span><span class="sxs-lookup"><span data-stu-id="28599-219">GL\_MAP2\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="28599-220">Если этот флажок установлен, вызовы **glEvalCoord2**, **glEvalMesh2** и **glEvalPoint2** формируют координаты *s*, *t* и *r* .</span><span class="sxs-lookup"><span data-stu-id="28599-220">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="28599-221">См. также **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="28599-221">See also **glMap2**.</span></span>                                                                                                           |
| <span data-ttu-id="28599-222">\_MAP2 \_ текстура GL \_ курд \_ 4</span><span class="sxs-lookup"><span data-stu-id="28599-222">GL\_MAP2\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="28599-223">Если этот флажок установлен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) создают координаты текстуры *s*, *t*, *r* и *q* .</span><span class="sxs-lookup"><span data-stu-id="28599-223">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="28599-224">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="28599-224">See also [**glMap2**](glmap2.md).</span></span>            |
| <span data-ttu-id="28599-225">GL \_ map2, \_ вершина \_ 3</span><span class="sxs-lookup"><span data-stu-id="28599-225">GL\_MAP2\_VERTEX\_3</span></span>         | <span data-ttu-id="28599-226">Если этот флажок установлен, вызовы **glEvalCoord2**, **glEvalMesh2** и **glEvalPoint2** создают координаты *x*, *y* и *z* .</span><span class="sxs-lookup"><span data-stu-id="28599-226">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="28599-227">См. также **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="28599-227">See also **glMap2**.</span></span>                                                                                                            |
| <span data-ttu-id="28599-228">\_MAP2ная \_ вершина GL \_ 4</span><span class="sxs-lookup"><span data-stu-id="28599-228">GL\_MAP2\_VERTEX\_4</span></span>         | <span data-ttu-id="28599-229">Если этот флажок установлен, вызовы [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)и [**glEvalPoint2**](glevalpoint.md) создают однородные координаты *x*, *y*, *z* и *w* вершин.</span><span class="sxs-lookup"><span data-stu-id="28599-229">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="28599-230">См. также [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="28599-230">See also [**glMap2**](glmap2.md).</span></span> |
| <span data-ttu-id="28599-231">\_нормализация GL</span><span class="sxs-lookup"><span data-stu-id="28599-231">GL\_NORMALIZE</span></span>               | <span data-ttu-id="28599-232">Если параметр включен, обычные векторы, заданные с помощью **глнормал** , масштабируются до длины единицы после преобразования.</span><span class="sxs-lookup"><span data-stu-id="28599-232">If enabled, normal vectors specified with **glNormal** are scaled to unit length after transformation.</span></span> <span data-ttu-id="28599-233">См. [**глнормал**](glnormal-functions.md).</span><span class="sxs-lookup"><span data-stu-id="28599-233">See [**glNormal**](glnormal-functions.md).</span></span>                                                                                                          |
| <span data-ttu-id="28599-234">\_ \_ гладкий пункт GL</span><span class="sxs-lookup"><span data-stu-id="28599-234">GL\_POINT\_SMOOTH</span></span>           | <span data-ttu-id="28599-235">Если параметр включен, рисуйте точки с правильной фильтрацией.</span><span class="sxs-lookup"><span data-stu-id="28599-235">If enabled, draw points with proper filtering.</span></span> <span data-ttu-id="28599-236">При отключении Нарисуйте точки с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="28599-236">If disabled, draw aliased points.</span></span> <span data-ttu-id="28599-237">См. [**глпоинтсизе**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="28599-237">See [**glPointSize**](glpointsize.md).</span></span>                                                                                                                                    |
| <span data-ttu-id="28599-238">\_ \_ Заливка смещения МНОГОУГОЛЬНИКа GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-238">GL\_POLYGON\_OFFSET\_FILL</span></span>   | <span data-ttu-id="28599-239">Если параметр включен и многоугольник отображается в \_ режиме заполнения GL, то смещение добавляется к значениям глубины фрагментов многоугольника перед выполнением сравнения глубины.</span><span class="sxs-lookup"><span data-stu-id="28599-239">If enabled, and if the polygon is rendered in GL\_FILL mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="28599-240">См. [**глполигоноффсет**](glpolygonoffset.md)**.**</span><span class="sxs-lookup"><span data-stu-id="28599-240">See [**glPolygonOffset**](glpolygonoffset.md)**.**</span></span>                                      |
| <span data-ttu-id="28599-241">\_строка смещения многоугольника GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="28599-241">GL\_POLYGON\_OFFSET\_LINE</span></span>   | <span data-ttu-id="28599-242">Если параметр включен и многоугольник отображается в \_ режиме строки GL, то перед сравнением глубины добавляется смещение к значениям глубины фрагментов многоугольника.</span><span class="sxs-lookup"><span data-stu-id="28599-242">If enabled, and if the polygon is rendered in GL\_LINE mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="28599-243">См. **глполигоноффсет**.</span><span class="sxs-lookup"><span data-stu-id="28599-243">See **glPolygonOffset**.</span></span>                                                                 |
| <span data-ttu-id="28599-244">\_точка смещения многоугольника GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="28599-244">GL\_POLYGON\_OFFSET\_POINT</span></span>  | <span data-ttu-id="28599-245">Если этот параметр включен, смещение добавляется к значениям глубины фрагментов многоугольника перед выполнением сравнения с глубиной, если многоугольник отображается в \_ режиме точки GL.</span><span class="sxs-lookup"><span data-stu-id="28599-245">If enabled, an offset is added to depth values of a polygon's fragments before the depth comparison is performed, if the polygon is rendered in GL\_POINT mode.</span></span> <span data-ttu-id="28599-246">См. [**глполигоноффсет**](glpolygonoffset.md).</span><span class="sxs-lookup"><span data-stu-id="28599-246">See [**glPolygonOffset**](glpolygonoffset.md).</span></span>                                             |
| <span data-ttu-id="28599-247">\_несглаженный МНОГОУГОЛЬНИК GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-247">GL\_POLYGON\_SMOOTH</span></span>         | <span data-ttu-id="28599-248">Если параметр включен, нарисуйте многоугольники с правильной фильтрацией.</span><span class="sxs-lookup"><span data-stu-id="28599-248">If enabled, draw polygons with proper filtering.</span></span> <span data-ttu-id="28599-249">Если этот отключен, нарисуйте многоугольники с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="28599-249">If disabled, draw aliased polygons.</span></span> <span data-ttu-id="28599-250">См. [**глполигонмоде**](glpolygonmode.md).</span><span class="sxs-lookup"><span data-stu-id="28599-250">See [**glPolygonMode**](glpolygonmode.md).</span></span>                                                                                                                            |
| <span data-ttu-id="28599-251">\_стиппле многоугольника GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-251">GL\_POLYGON\_STIPPLE</span></span>        | <span data-ttu-id="28599-252">Если параметр включен, при отрисовке многоугольников используется шаблон стиппле с использованием текущего многоугольника.</span><span class="sxs-lookup"><span data-stu-id="28599-252">If enabled, use the current polygon stipple pattern when rendering polygons.</span></span> <span data-ttu-id="28599-253">См. [**глполигонстиппле**](glpolygonstipple.md).</span><span class="sxs-lookup"><span data-stu-id="28599-253">See [**glPolygonStipple**](glpolygonstipple.md).</span></span>                                                                                                                              |
| <span data-ttu-id="28599-254">\_тест вырезание GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-254">GL\_SCISSOR\_TEST</span></span>           | <span data-ttu-id="28599-255">Если параметр включен, отбросить фрагменты, расположенные за пределами прямоугольной прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="28599-255">If enabled, discard fragments that are outside the scissor rectangle.</span></span> <span data-ttu-id="28599-256">См. [**глсЦиссор**](glscissor.md).</span><span class="sxs-lookup"><span data-stu-id="28599-256">See [**glScissor**](glscissor.md).</span></span>                                                                                                                                                   |
| <span data-ttu-id="28599-257">\_тест шаблона \_ GL</span><span class="sxs-lookup"><span data-stu-id="28599-257">GL\_STENCIL\_TEST</span></span>           | <span data-ttu-id="28599-258">Если параметр включен, проверка трафарета и обновление буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="28599-258">If enabled, do stencil testing and update the stencil buffer.</span></span> <span data-ttu-id="28599-259">См. раздел [**глстенЦилфунк**](glstencilfunc.md) and [**глстенЦилоп**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="28599-259">See [**glStencilFunc**](glstencilfunc.md) and [**glStencilOp**](glstencilop.md).</span></span>                                                                                                            |
| <span data-ttu-id="28599-260">\_Одномерное текстура GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-260">GL\_TEXTURE\_1D</span></span>             | <span data-ttu-id="28599-261">Если этот флажок включен, выполняется одномерный текстурированный текстура (если одновременно не включено двухмерный текстурирование).</span><span class="sxs-lookup"><span data-stu-id="28599-261">If enabled, one-dimensional texturing is performed (unless two-dimensional texturing is also enabled).</span></span> <span data-ttu-id="28599-262">См. [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="28599-262">See [**glTexImage1D**](glteximage1d.md).</span></span>                                                                                                            |
| <span data-ttu-id="28599-263">\_2D-текстура GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-263">GL\_TEXTURE\_2D</span></span>             | <span data-ttu-id="28599-264">Если этот флажок включен, выполняется двухмерный текстурирование.</span><span class="sxs-lookup"><span data-stu-id="28599-264">If enabled, two-dimensional texturing is performed.</span></span> <span data-ttu-id="28599-265">См. [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="28599-265">See [**glTexImage2D**](glteximage2d.md).</span></span>                                                                                                                                                               |
| <span data-ttu-id="28599-266">\_ \_ Общие вопросы о ТЕКСТУРе GL \_</span><span class="sxs-lookup"><span data-stu-id="28599-266">GL\_TEXTURE\_GEN\_Q</span></span>         | <span data-ttu-id="28599-267">Если параметр включен, координата текстуры *q* вычисляются с помощью функции формирования текстуры, определенной с помощью [**глтексжен**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="28599-267">If enabled, the *q* texture coordinate is computed using the texture-generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="28599-268">В противном случае используется текущая Координата текстуры *q* .</span><span class="sxs-lookup"><span data-stu-id="28599-268">Otherwise, the current *q* texture coordinate is used.</span></span>                                                        |
| <span data-ttu-id="28599-269">заполнение текстур главной книги \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="28599-269">GL\_TEXTURE\_GEN\_R</span></span>         | <span data-ttu-id="28599-270">Если параметр включен, координата текстуры *r* вычисляются с помощью функции формирования текстуры, определенной с помощью [**глтексжен**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="28599-270">If enabled, the *r* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="28599-271">Если этот параметр отключен, используется текущая Координата текстуры *r* .</span><span class="sxs-lookup"><span data-stu-id="28599-271">If disabled, the current *r* texture coordinate is used.</span></span>                                                      |
| <span data-ttu-id="28599-272">\_Gen текстура GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="28599-272">GL\_TEXTURE\_GEN\_S</span></span>         | <span data-ttu-id="28599-273">Если параметр включен, координата текстуры *s* вычисляются с помощью функции формирования текстуры, определенной с помощью **глтексжен**.</span><span class="sxs-lookup"><span data-stu-id="28599-273">If enabled, the *s* texture coordinate is computed using the texture generation function defined with **glTexGen**.</span></span> <span data-ttu-id="28599-274">Если этот параметр отключен, используется координата *текущей текстуры* .</span><span class="sxs-lookup"><span data-stu-id="28599-274">If disabled, the current *s* texture coordinate is used.</span></span>                                                                                |
| <span data-ttu-id="28599-275">\_Gen текстура GL \_ \_ T</span><span class="sxs-lookup"><span data-stu-id="28599-275">GL\_TEXTURE\_GEN\_T</span></span>         | <span data-ttu-id="28599-276">Если параметр включен, координата текстуры *t* вычисляются с помощью функции формирования текстуры, определенной с помощью [**глтексжен**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="28599-276">If enabled, the *t* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="28599-277">Если параметр отключен, используется текущая координата *t* текстура.</span><span class="sxs-lookup"><span data-stu-id="28599-277">If disabled, the current *t* texture coordinate is used.</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="28599-278">Требования</span><span class="sxs-lookup"><span data-stu-id="28599-278">Requirements</span></span>



| <span data-ttu-id="28599-279">Требование</span><span class="sxs-lookup"><span data-stu-id="28599-279">Requirement</span></span> | <span data-ttu-id="28599-280">Значение</span><span class="sxs-lookup"><span data-stu-id="28599-280">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28599-281">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28599-281">Minimum supported client</span></span><br/> | <span data-ttu-id="28599-282">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28599-282">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="28599-283">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28599-283">Minimum supported server</span></span><br/> | <span data-ttu-id="28599-284">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28599-284">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28599-285">Заголовок</span><span class="sxs-lookup"><span data-stu-id="28599-285">Header</span></span><br/>                   | <dl> <span data-ttu-id="28599-286"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="28599-286"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="28599-287">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28599-287">Library</span></span><br/>                  | <dl> <span data-ttu-id="28599-288"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28599-288"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="28599-289">DLL</span><span class="sxs-lookup"><span data-stu-id="28599-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28599-290"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28599-290"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28599-291">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28599-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28599-292">**глалфафунк**</span><span class="sxs-lookup"><span data-stu-id="28599-292">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="28599-293">**гларрайелемент**</span><span class="sxs-lookup"><span data-stu-id="28599-293">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="28599-294">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="28599-294">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="28599-295">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="28599-295">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="28599-296">**глклипплане**</span><span class="sxs-lookup"><span data-stu-id="28599-296">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="28599-297">**глколорматериал**</span><span class="sxs-lookup"><span data-stu-id="28599-297">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="28599-298">**глколорпоинтер**</span><span class="sxs-lookup"><span data-stu-id="28599-298">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="28599-299">**глкуллфаце**</span><span class="sxs-lookup"><span data-stu-id="28599-299">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="28599-300">**глдепсфунк**</span><span class="sxs-lookup"><span data-stu-id="28599-300">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="28599-301">**глдепсранже**</span><span class="sxs-lookup"><span data-stu-id="28599-301">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="28599-302">**глдраваррайс**</span><span class="sxs-lookup"><span data-stu-id="28599-302">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="28599-303">**гледжефлагпоинтер**</span><span class="sxs-lookup"><span data-stu-id="28599-303">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="28599-304">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="28599-304">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="28599-305">**гленд**</span><span class="sxs-lookup"><span data-stu-id="28599-305">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="28599-306">**glEvalCoord1**</span><span class="sxs-lookup"><span data-stu-id="28599-306">**glEvalCoord1**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="28599-307">**glEvalMesh1**</span><span class="sxs-lookup"><span data-stu-id="28599-307">**glEvalMesh1**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="28599-308">**glEvalPoint1**</span><span class="sxs-lookup"><span data-stu-id="28599-308">**glEvalPoint1**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="28599-309">**глфог**</span><span class="sxs-lookup"><span data-stu-id="28599-309">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="28599-310">**глжет**</span><span class="sxs-lookup"><span data-stu-id="28599-310">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="28599-311">**глиндекспоинтер**</span><span class="sxs-lookup"><span data-stu-id="28599-311">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="28599-312">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="28599-312">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="28599-313">**гллигхт**</span><span class="sxs-lookup"><span data-stu-id="28599-313">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="28599-314">**гллигхтмодел**</span><span class="sxs-lookup"><span data-stu-id="28599-314">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="28599-315">**гллиневидс**</span><span class="sxs-lookup"><span data-stu-id="28599-315">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="28599-316">**гллинестиппле**</span><span class="sxs-lookup"><span data-stu-id="28599-316">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="28599-317">**гллогикоп**</span><span class="sxs-lookup"><span data-stu-id="28599-317">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="28599-318">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="28599-318">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="28599-319">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="28599-319">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="28599-320">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="28599-320">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="28599-321">**глнормал**</span><span class="sxs-lookup"><span data-stu-id="28599-321">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="28599-322">**глнормалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="28599-322">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="28599-323">**глпоинтсизе**</span><span class="sxs-lookup"><span data-stu-id="28599-323">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="28599-324">**глполигонмоде**</span><span class="sxs-lookup"><span data-stu-id="28599-324">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="28599-325">**глполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="28599-325">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="28599-326">**глсЦиссор**</span><span class="sxs-lookup"><span data-stu-id="28599-326">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="28599-327">**глстенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="28599-327">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="28599-328">**глстенЦилоп**</span><span class="sxs-lookup"><span data-stu-id="28599-328">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="28599-329">**глтекскурдпоинтер**</span><span class="sxs-lookup"><span data-stu-id="28599-329">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="28599-330">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="28599-330">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="28599-331">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="28599-331">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="28599-332">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="28599-332">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





