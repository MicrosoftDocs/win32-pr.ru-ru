---
title: Функция Глфидбаккбуффер (GL. h)
description: Функция Глфидбаккбуффер управляет режимом обратной связи.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- Функция Глфидбаккбуффер OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661939"
---
# <a name="glfeedbackbuffer-function"></a><span data-ttu-id="11e68-104">Функция Глфидбаккбуффер</span><span class="sxs-lookup"><span data-stu-id="11e68-104">glFeedbackBuffer function</span></span>

<span data-ttu-id="11e68-105">Функция **глфидбаккбуффер** управляет режимом обратной связи.</span><span class="sxs-lookup"><span data-stu-id="11e68-105">The **glFeedbackBuffer** function controls feedback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e68-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11e68-106">Syntax</span></span>


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="11e68-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="11e68-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e68-108">*size*</span><span class="sxs-lookup"><span data-stu-id="11e68-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="11e68-109">Максимальное число значений, которые могут быть записаны в *буфер*.</span><span class="sxs-lookup"><span data-stu-id="11e68-109">The maximum number of values that can be written into *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="11e68-110">*type*</span><span class="sxs-lookup"><span data-stu-id="11e68-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="11e68-111">Символьная константа, описывающая сведения, которые будут возвращаться для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="11e68-111">A symbolic constant that describes the information that will be returned for each vertex.</span></span> <span data-ttu-id="11e68-112">Допустимы следующие символьные константы: двумерные, трехмерные, трехмерные, GL, трехмерные текстуры GL \_ \_ \_ \_ \_ \_ \_ и \_ \_ цветовая \_ текстура GL 4d.</span><span class="sxs-lookup"><span data-stu-id="11e68-112">The following symbolic constants are accepted: GL\_2D, GL\_3D, GL\_3D\_COLOR, GL\_3D\_COLOR\_TEXTURE, and GL\_4D\_COLOR\_TEXTURE.</span></span>

</dd> <dt>

<span data-ttu-id="11e68-113">*двойной*</span><span class="sxs-lookup"><span data-stu-id="11e68-113">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="11e68-114">Возвращает данные обратной связи.</span><span class="sxs-lookup"><span data-stu-id="11e68-114">Returns the feedback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e68-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11e68-115">Return value</span></span>

<span data-ttu-id="11e68-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="11e68-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11e68-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="11e68-117">Error codes</span></span>

<span data-ttu-id="11e68-118">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="11e68-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="11e68-119">Имя</span><span class="sxs-lookup"><span data-stu-id="11e68-119">Name</span></span>                                                                                                  | <span data-ttu-id="11e68-120">Значение</span><span class="sxs-lookup"><span data-stu-id="11e68-120">Meaning</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11e68-121"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="11e68-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="11e68-122">*тип* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="11e68-122">*type* was not an accepted value.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="11e68-123"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="11e68-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="11e68-124">*Размер* был отрицательным.</span><span class="sxs-lookup"><span data-stu-id="11e68-124">*size* was negative.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="11e68-125"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="11e68-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="11e68-126">**глфидбаккбуффер** был вызван, когда режим рендеринга был нефинансовым \_ отзывом, или [**глрендермоде**](glrendermode.md) был вызван с аргументом \_ Feedback GL до того, как **глфидбаккбуффер** был вызван по крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="11e68-126">**glFeedbackBuffer** was called while the render mode was GL\_FEEDBACK, or [**glRenderMode**](glrendermode.md) was called with argument GL\_FEEDBACK before **glFeedbackBuffer** was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="11e68-127"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="11e68-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="11e68-128">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="11e68-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                  |



## <a name="remarks"></a><span data-ttu-id="11e68-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11e68-129">Remarks</span></span>

<span data-ttu-id="11e68-130">Функция **глфидбаккбуффер** управляет обратной связью.</span><span class="sxs-lookup"><span data-stu-id="11e68-130">The **glFeedbackBuffer** function controls feedback.</span></span> <span data-ttu-id="11e68-131">Обратная связь, как и в случае выбора, является режимом OpenGL.</span><span class="sxs-lookup"><span data-stu-id="11e68-131">Feedback, like selection, is an OpenGL mode.</span></span> <span data-ttu-id="11e68-132">Режим выбирается путем вызова [**глрендермоде**](glrendermode.md) с использованием \_ обратной связи GL.</span><span class="sxs-lookup"><span data-stu-id="11e68-132">The mode is selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="11e68-133">Когда OpenGL находится в режиме обратной связи, никакие Пиксели не создаются путем растрирования.</span><span class="sxs-lookup"><span data-stu-id="11e68-133">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="11e68-134">Вместо этого сведения о примитивах, которые были бы растровыми, отправляются обратно в приложение с помощью OpenGL.</span><span class="sxs-lookup"><span data-stu-id="11e68-134">Instead, information about primitives that would have been rasterized is fed back to the application using OpenGL.</span></span>

<span data-ttu-id="11e68-135">Функция **глфидбаккбуффер** имеет три аргумента:</span><span class="sxs-lookup"><span data-stu-id="11e68-135">The **glFeedbackBuffer** function has three arguments:</span></span>

-   <span data-ttu-id="11e68-136">*buffer* — это указатель на массив значений с плавающей запятой, в который помещаются сведения о обратной связи.</span><span class="sxs-lookup"><span data-stu-id="11e68-136">*buffer* is a pointer to an array of floating-point values into which feedback information is placed.</span></span>
-   <span data-ttu-id="11e68-137">*Размер* указывает размер массива.</span><span class="sxs-lookup"><span data-stu-id="11e68-137">*size* indicates the size of the array.</span></span>
-   <span data-ttu-id="11e68-138">*тип* — символьная константа, описывающая сведения, которые передаются обратно для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="11e68-138">*type* is a symbolic constant describing the information that is fed back for each vertex.</span></span>

<span data-ttu-id="11e68-139">Необходимо выполнить инструкцию **глфидбаккбуффер** перед включением режима обратной связи (путем вызова **глрендермоде** с аргументом \_ Feedback GL).</span><span class="sxs-lookup"><span data-stu-id="11e68-139">You must issue **glFeedbackBuffer** before feedback mode is enabled (by calling **glRenderMode** with argument GL\_FEEDBACK).</span></span> <span data-ttu-id="11e68-140">При настройке \_ обратной связи в ГК без создания буфера обратной связи или при вызове **глфидбаккбуффер** , когда OpenGL находится в режиме обратной связи, выдает ошибку.</span><span class="sxs-lookup"><span data-stu-id="11e68-140">Setting GL\_FEEDBACK without establishing the feedback buffer, or calling **glFeedbackBuffer** while OpenGL is in feedback mode, is an error.</span></span>

<span data-ttu-id="11e68-141">Переведите OpenGL из режима обратной связи, вызвав [**глрендермоде**](glrendermode.md) со значением параметра, ОТЛИЧНЫМ от GL \_ .</span><span class="sxs-lookup"><span data-stu-id="11e68-141">Take OpenGL out of feedback mode by calling [**glRenderMode**](glrendermode.md) with a parameter value other than GL\_FEEDBACK.</span></span> <span data-ttu-id="11e68-142">При этом, когда OpenGL находится в режиме обратной связи, **глрендермоде** возвращает число записей, помещенных в массив обратной связи.</span><span class="sxs-lookup"><span data-stu-id="11e68-142">When you do this while OpenGL is in feedback mode, **glRenderMode** returns the number of entries placed in the feedback array.</span></span> <span data-ttu-id="11e68-143">Возвращаемое значение никогда не превышает *Размер*.</span><span class="sxs-lookup"><span data-stu-id="11e68-143">The returned value never exceeds *size*.</span></span> <span data-ttu-id="11e68-144">Если данные обратной связи требуют больше места, чем было доступно в *буфере*, **глрендермоде** возвращает отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="11e68-144">If the feedback data required more room than was available in *buffer*, **glRenderMode** returns a negative value.</span></span>

<span data-ttu-id="11e68-145">В режиме обратной связи каждый примитив, который был бы растровым, создает блок значений, которые копируются в массив обратной связи.</span><span class="sxs-lookup"><span data-stu-id="11e68-145">While in feedback mode, each primitive that would be rasterized generates a block of values that gets copied into the feedback array.</span></span> <span data-ttu-id="11e68-146">Если это приведет к превышению максимального числа записей, **глфидбаккбуффер** частично записывает блок так, чтобы заполнить массив (если все места осталось) и устанавливает флаг переполнения.</span><span class="sxs-lookup"><span data-stu-id="11e68-146">If doing so would cause the number of entries to exceed the maximum, **glFeedbackBuffer** partially writes the block so as to fill the array (if there is any room left at all), and sets an overflow flag.</span></span> <span data-ttu-id="11e68-147">Каждый блок начинается с кода, указывающего на тип-примитив, за которым следуют значения, описывающие вершины примитива и связанные данные.</span><span class="sxs-lookup"><span data-stu-id="11e68-147">Each block begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="11e68-148">Функция **глфидбаккбуффер** также записывает записи для точечных рисунков и пиксельных прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="11e68-148">The **glFeedbackBuffer** function also writes entries for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="11e68-149">Обратная связь происходит после истечения действия многоугольника и [**глполигонмоденой**](glpolygonmode.md) интерпретации многоугольников, поэтому многоугольники, которые исключаются, не возвращаются в буфере обратной связи.</span><span class="sxs-lookup"><span data-stu-id="11e68-149">Feedback occurs after polygon culling and [**glPolygonMode**](glpolygonmode.md) interpretation of polygons has taken place, so polygons that are culled are not returned in the feedback buffer.</span></span> <span data-ttu-id="11e68-150">Это также может произойти после того, как многоугольники с более чем тремя краями разбиваются на треугольники, если реализация OpenGL визуализирует многоугольники, выполняя эту декомпозицию.</span><span class="sxs-lookup"><span data-stu-id="11e68-150">It can also occur after polygons with more than three edges are broken up into triangles, if the OpenGL implementation renders polygons by performing this decomposition.</span></span>

<span data-ttu-id="11e68-151">Вы можете вставить маркер в буфер обратной связи с помощью [**глпасссраугх**](glpassthrough.md).</span><span class="sxs-lookup"><span data-stu-id="11e68-151">You can insert a marker into the feedback buffer with [**glPassThrough**](glpassthrough.md).</span></span>

<span data-ttu-id="11e68-152">Ниже приведена грамматика для блоков значений, записанных в буфер обратной связи.</span><span class="sxs-lookup"><span data-stu-id="11e68-152">The following is the grammar for the blocks of values written into the feedback buffer.</span></span> <span data-ttu-id="11e68-153">Каждый примитив обозначается уникальным идентифицирующим значением, за которым следует некоторое количество вершин.</span><span class="sxs-lookup"><span data-stu-id="11e68-153">Each primitive is indicated with a unique identifying value followed by some number of vertices.</span></span> <span data-ttu-id="11e68-154">Записи многоугольников содержат целочисленное значение, указывающее, сколько вершин следуют за ними.</span><span class="sxs-lookup"><span data-stu-id="11e68-154">Polygon entries include an integer value indicating how many vertices follow.</span></span> <span data-ttu-id="11e68-155">Вершина возвращается в виде некоторого числа значений с плавающей запятой, как определено *типом*.</span><span class="sxs-lookup"><span data-stu-id="11e68-155">A vertex is fed back as some number of floating-point values, as determined by *type*.</span></span> <span data-ttu-id="11e68-156">Цвет возвращается в виде четырех значений в режиме RGBA и одно значение в режиме индексирования цвета.</span><span class="sxs-lookup"><span data-stu-id="11e68-156">Colors are fed back as four values in RGBA mode and one value in color-index mode.</span></span>

<span data-ttu-id="11e68-157">Фидбакклист < feedbackItem Фидбакклист \| feedbackItem</span><span class="sxs-lookup"><span data-stu-id="11e68-157">feedbackList <  feedbackItem feedbackList \| feedbackItem</span></span>

<span data-ttu-id="11e68-158">feedbackItem < точка \| lineSegment \| \| точечный рисунок Многоугольник \| пикселректангле \| пропускания</span><span class="sxs-lookup"><span data-stu-id="11e68-158">feedbackItem <  point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru</span></span>

<span data-ttu-id="11e68-159">\_ \_ вершина маркера точки < главной точки</span><span class="sxs-lookup"><span data-stu-id="11e68-159">point <  GL\_POINT\_TOKEN vertex</span></span>

<span data-ttu-id="11e68-160">lineSegment < вершина линии вершинного \_ \_ маркера строки главной вершины для \| \_ \_ \_ маркера сброса линии вершин</span><span class="sxs-lookup"><span data-stu-id="11e68-160">lineSegment <  GL\_LINE\_TOKEN vertex vertex \| GL\_LINE\_RESET\_TOKEN vertex vertex</span></span>

<span data-ttu-id="11e68-161">многоугольник < \_ маркером многоугольника GL \_ n</span><span class="sxs-lookup"><span data-stu-id="11e68-161">polygon <  GL\_POLYGON\_TOKEN n polySpec</span></span>

<span data-ttu-id="11e68-162"><ная вершина вершины вершинной вершины с коspec \|</span><span class="sxs-lookup"><span data-stu-id="11e68-162">polySpec <  polySpec vertex \| vertex vertex vertex</span></span>

<span data-ttu-id="11e68-163">Битовая карта < \_ \_ вершиной маркера точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="11e68-163">bitmap <  GL\_BITMAP\_TOKEN vertex</span></span>

<span data-ttu-id="11e68-164">Пикселректангле < GL \_ нарисовать \_ пиксельный \_ маркер вершина \| \_ Копировать \_ пиксель \_ маркер вершина</span><span class="sxs-lookup"><span data-stu-id="11e68-164">pixelRectangle <  GL\_DRAW\_PIXEL\_TOKEN vertex \| GL\_COPY\_PIXEL\_TOKEN vertex</span></span>

<span data-ttu-id="11e68-165">passThru < \_ \_ \_ значение токена GL ГК</span><span class="sxs-lookup"><span data-stu-id="11e68-165">passThru <  GL\_PASS\_THROUGH\_TOKEN value</span></span>

<span data-ttu-id="11e68-166">вершина < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture</span><span class="sxs-lookup"><span data-stu-id="11e68-166">vertex <  2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture</span></span>

<span data-ttu-id="11e68-167">значение 2D <</span><span class="sxs-lookup"><span data-stu-id="11e68-167">2d <  value value</span></span>

<span data-ttu-id="11e68-168">трехмерное < значение значения</span><span class="sxs-lookup"><span data-stu-id="11e68-168">3d <  value value value</span></span>

<span data-ttu-id="11e68-169">цвет значения значения 3dColor <</span><span class="sxs-lookup"><span data-stu-id="11e68-169">3dColor <  value value value color</span></span>

<span data-ttu-id="11e68-170">3dColorTexture < значение значения Да Color</span><span class="sxs-lookup"><span data-stu-id="11e68-170">3dColorTexture <  value value value color tex</span></span>

<span data-ttu-id="11e68-171">4dColorTexture < значение значения значение Да Color</span><span class="sxs-lookup"><span data-stu-id="11e68-171">4dColorTexture <  value value value value color tex</span></span>

<span data-ttu-id="11e68-172">цвет < \| индекс RGBA</span><span class="sxs-lookup"><span data-stu-id="11e68-172">color <  rgba \| index</span></span>

<span data-ttu-id="11e68-173">значение RGBA < значение значения</span><span class="sxs-lookup"><span data-stu-id="11e68-173">rgba <  value value value value</span></span>

<span data-ttu-id="11e68-174">значение индекса <</span><span class="sxs-lookup"><span data-stu-id="11e68-174">index <  value</span></span>

<span data-ttu-id="11e68-175">значение Да < значение значения</span><span class="sxs-lookup"><span data-stu-id="11e68-175">tex <  value value value value</span></span>

<span data-ttu-id="11e68-176">Параметр *value* — это число с плавающей запятой, а *n* — целое число с плавающей запятой, которое предоставляет количество вершин в многоугольнике.</span><span class="sxs-lookup"><span data-stu-id="11e68-176">The *value* parameter is a floating-point number, and *n* is a floating-point integer giving the number of vertices in the polygon.</span></span> <span data-ttu-id="11e68-177">Ниже приведены символьные константы с плавающей запятой \_ : \_ токен точки GL, \_ маркер строки GL \_ , \_ маркер сброса строки GL, маркер многоугольника GL, маркер Bitmap в ГК, маркер рисования пикселей в формате GL, маркер копирования пикселей в формате GL \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ и \_ \_ токен передачи по ГК \_ .</span><span class="sxs-lookup"><span data-stu-id="11e68-177">The following are symbolic floating-point constants: GL\_POINT\_TOKEN, GL\_LINE\_TOKEN, GL\_LINE\_RESET\_TOKEN, GL\_POLYGON\_TOKEN, GL\_BITMAP\_TOKEN, GL\_DRAW\_PIXEL\_TOKEN, GL\_COPY\_PIXEL\_TOKEN, and GL\_PASS\_THROUGH\_TOKEN.</span></span> <span data-ttu-id="11e68-178">\_ \_ Маркер сброса строки GL \_ возвращается при каждом сбросе шаблона стиппле строки.</span><span class="sxs-lookup"><span data-stu-id="11e68-178">GL\_LINE\_RESET\_TOKEN is returned whenever the line stipple pattern is reset.</span></span> <span data-ttu-id="11e68-179">Данные, возвращаемые в виде вершины, зависят от *типа* обратной связи.</span><span class="sxs-lookup"><span data-stu-id="11e68-179">The data returned as a vertex depends on the feedback *type*.</span></span>

<span data-ttu-id="11e68-180">В следующей таблице передается соответствие между *типом* и числом значений на вершину. *k* — 1 в режиме индексирования цвета и 4 в режиме RGBA.</span><span class="sxs-lookup"><span data-stu-id="11e68-180">The following table gives the correspondence between *type* and the number of values per vertex; *k* is 1 in color-index mode and 4 in RGBA mode.</span></span>



| <span data-ttu-id="11e68-181">Тип</span><span class="sxs-lookup"><span data-stu-id="11e68-181">Type</span></span>                   | <span data-ttu-id="11e68-182">Координаты</span><span class="sxs-lookup"><span data-stu-id="11e68-182">Coordinates</span></span>        | <span data-ttu-id="11e68-183">Цвет</span><span class="sxs-lookup"><span data-stu-id="11e68-183">Color</span></span> | <span data-ttu-id="11e68-184">Текстура</span><span class="sxs-lookup"><span data-stu-id="11e68-184">Texture</span></span> | <span data-ttu-id="11e68-185">Общее число значений</span><span class="sxs-lookup"><span data-stu-id="11e68-185">Total number of values</span></span> |
|------------------------|--------------------|-------|---------|------------------------|
| <span data-ttu-id="11e68-186">\_2D GL</span><span class="sxs-lookup"><span data-stu-id="11e68-186">GL\_2D</span></span>                 | <span data-ttu-id="11e68-187">*x*, *y*</span><span class="sxs-lookup"><span data-stu-id="11e68-187">*x*, *y*</span></span>           |       |         | <span data-ttu-id="11e68-188">2</span><span class="sxs-lookup"><span data-stu-id="11e68-188">2</span></span>                      |
| <span data-ttu-id="11e68-189">\_Трехмерная GL</span><span class="sxs-lookup"><span data-stu-id="11e68-189">GL\_3D</span></span>                 | <span data-ttu-id="11e68-190">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="11e68-190">*x*, *y*, *z*</span></span>      |       |         | <span data-ttu-id="11e68-191">3</span><span class="sxs-lookup"><span data-stu-id="11e68-191">3</span></span>                      |
| <span data-ttu-id="11e68-192">\_Трехмерный \_ Цвет GL</span><span class="sxs-lookup"><span data-stu-id="11e68-192">GL\_3D\_COLOR</span></span>          | <span data-ttu-id="11e68-193">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="11e68-193">*x*, *y*, *z*</span></span>      | <span data-ttu-id="11e68-194">*занят*</span><span class="sxs-lookup"><span data-stu-id="11e68-194">*k*</span></span>   |         | <span data-ttu-id="11e68-195">3 + *k*</span><span class="sxs-lookup"><span data-stu-id="11e68-195">3 + *k*</span></span>                |
| <span data-ttu-id="11e68-196">\_ \_ Текстура трехмерного цвета GL \_</span><span class="sxs-lookup"><span data-stu-id="11e68-196">GL\_3D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="11e68-197">*x*, *y*, *z*,</span><span class="sxs-lookup"><span data-stu-id="11e68-197">*x*, *y*, *z*,</span></span>     | <span data-ttu-id="11e68-198">*занят*</span><span class="sxs-lookup"><span data-stu-id="11e68-198">*k*</span></span>   | <span data-ttu-id="11e68-199">4</span><span class="sxs-lookup"><span data-stu-id="11e68-199">4</span></span>       | <span data-ttu-id="11e68-200">7 + *k*</span><span class="sxs-lookup"><span data-stu-id="11e68-200">7 + *k*</span></span>                |
| <span data-ttu-id="11e68-201">\_ \_ Цветовая \_ текстура GL 4D</span><span class="sxs-lookup"><span data-stu-id="11e68-201">GL\_4D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="11e68-202">*x*, *y*, *z*, *w*</span><span class="sxs-lookup"><span data-stu-id="11e68-202">*x*, *y*, *z*, *w*</span></span> | <span data-ttu-id="11e68-203">*занят*</span><span class="sxs-lookup"><span data-stu-id="11e68-203">*k*</span></span>   | <span data-ttu-id="11e68-204">4</span><span class="sxs-lookup"><span data-stu-id="11e68-204">4</span></span>       | <span data-ttu-id="11e68-205">8 + *k*</span><span class="sxs-lookup"><span data-stu-id="11e68-205">8 + *k*</span></span>                |



 

<span data-ttu-id="11e68-206">Координаты вершины обратной связи находятся в координатах окна, кроме *w*, которые находятся в координатах клипов.</span><span class="sxs-lookup"><span data-stu-id="11e68-206">Feedback vertex coordinates are in window coordinates, except *w*, which is in clip coordinates.</span></span> <span data-ttu-id="11e68-207">Цвета обратной связи освещены, если освещение включено.</span><span class="sxs-lookup"><span data-stu-id="11e68-207">Feedback colors are lighted, if lighting is enabled.</span></span> <span data-ttu-id="11e68-208">Координаты текстуры отклика создаются, если включено создание координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="11e68-208">Feedback texture coordinates are generated, if texture coordinate generation is enabled.</span></span> <span data-ttu-id="11e68-209">Они всегда преобразуются в матрицу текстуры.</span><span class="sxs-lookup"><span data-stu-id="11e68-209">They are always transformed by the texture matrix.</span></span>

<span data-ttu-id="11e68-210">Функция **глфидбаккбуффер** , используемая в списке вывода, не компилируется в список просмотра, а выполняется немедленно.</span><span class="sxs-lookup"><span data-stu-id="11e68-210">The **glFeedbackBuffer** function, when used in a display list, is not compiled into the display list but rather is executed immediately.</span></span>

<span data-ttu-id="11e68-211">Следующая функция получает сведения, связанные с **глфидбаккбуффер**:</span><span class="sxs-lookup"><span data-stu-id="11e68-211">The following function retrieves information related to **glFeedbackBuffer**:</span></span>

<span data-ttu-id="11e68-212">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ режим рендеринга GL \_</span><span class="sxs-lookup"><span data-stu-id="11e68-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="11e68-213">Требования</span><span class="sxs-lookup"><span data-stu-id="11e68-213">Requirements</span></span>



| <span data-ttu-id="11e68-214">Требование</span><span class="sxs-lookup"><span data-stu-id="11e68-214">Requirement</span></span> | <span data-ttu-id="11e68-215">Значение</span><span class="sxs-lookup"><span data-stu-id="11e68-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11e68-216">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11e68-216">Minimum supported client</span></span><br/> | <span data-ttu-id="11e68-217">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11e68-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="11e68-218">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11e68-218">Minimum supported server</span></span><br/> | <span data-ttu-id="11e68-219">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11e68-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11e68-220">Заголовок</span><span class="sxs-lookup"><span data-stu-id="11e68-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e68-221"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e68-221"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="11e68-222">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11e68-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="11e68-223"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11e68-223"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="11e68-224">DLL</span><span class="sxs-lookup"><span data-stu-id="11e68-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11e68-225"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e68-225"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e68-226">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11e68-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e68-227">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="11e68-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="11e68-228">**гленд**</span><span class="sxs-lookup"><span data-stu-id="11e68-228">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="11e68-229">**глжет**</span><span class="sxs-lookup"><span data-stu-id="11e68-229">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="11e68-230">**гллинестиппле**</span><span class="sxs-lookup"><span data-stu-id="11e68-230">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="11e68-231">**глпасссраугх**</span><span class="sxs-lookup"><span data-stu-id="11e68-231">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="11e68-232">**глполигонмоде**</span><span class="sxs-lookup"><span data-stu-id="11e68-232">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="11e68-233">**глрендермоде**</span><span class="sxs-lookup"><span data-stu-id="11e68-233">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="11e68-234">**глселектбуффер**</span><span class="sxs-lookup"><span data-stu-id="11e68-234">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





