---
title: Функция glRasterPos2i (GL. h)
description: Задает точечную точку для операций с пикселями. | Функция glRasterPos2i (GL. h)
ms.assetid: 2ab3b66a-e6e7-43ed-ab4b-c897c3d19561
keywords:
- Функция glRasterPos2i OpenGL
topic_type:
- apiref
api_name:
- glRasterPos2i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae95cf1e3e375531559726eee520f829d03a1261
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914564"
---
# <a name="glrasterpos2i-function"></a><span data-ttu-id="96538-105">Функция glRasterPos2i</span><span class="sxs-lookup"><span data-stu-id="96538-105">glRasterPos2i function</span></span>

<span data-ttu-id="96538-106">Задает точечную точку для операций с пикселями.</span><span class="sxs-lookup"><span data-stu-id="96538-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="96538-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96538-107">Syntax</span></span>


```C++
void WINAPI glRasterPos2i(
   GLint x,
   GLint y
);
```



## <a name="parameters"></a><span data-ttu-id="96538-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96538-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96538-109">*x*</span><span class="sxs-lookup"><span data-stu-id="96538-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="96538-110">Задает координату по оси x для текущей разточечной точки.</span><span class="sxs-lookup"><span data-stu-id="96538-110">Specifies the x-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="96538-111">*y*</span><span class="sxs-lookup"><span data-stu-id="96538-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="96538-112">Задает координату по оси y для текущей разточечной точки.</span><span class="sxs-lookup"><span data-stu-id="96538-112">Specifies the y-coordinate for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96538-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96538-113">Return value</span></span>

<span data-ttu-id="96538-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="96538-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96538-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96538-115">Remarks</span></span>

<span data-ttu-id="96538-116">OpenGL поддерживает трехмерное расположение в координатах окна.</span><span class="sxs-lookup"><span data-stu-id="96538-116">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="96538-117">Это расположение, называемое растровой позицией, сохраняется с точностью до точки.</span><span class="sxs-lookup"><span data-stu-id="96538-117">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="96538-118">Он используется для размещения операций записи пикселей и точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="96538-118">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="96538-119">См. раздел [**глбитмап**](glbitmap.md), [**глдравпикселс**](gldrawpixels.md)и [**глкопипикселс**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="96538-119">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="96538-120">Текущая битовая разположение состоит из трех координат окна (*x, y, z*), координаты изображения *w* , расстояния от координат глаза, допустимого бита и связанных данных о цветах и координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="96538-120">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="96538-121">Координата *w* — это координата обрезки, так как *w* не проецируется на окна координат.</span><span class="sxs-lookup"><span data-stu-id="96538-121">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="96538-122">Функция [glRasterPos4](glrasterpos-functions.md) указывает, что объект координирует координаты *x, y, z* и *w* явным образом.</span><span class="sxs-lookup"><span data-stu-id="96538-122">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="96538-123">Функция glRasterPos3 указывает, что объект координирует координаты *x, y* и *z* явным образом, хотя *w* неявно имеет значение One.</span><span class="sxs-lookup"><span data-stu-id="96538-123">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="96538-124">Функция glRasterPos2 использует значения аргументов для *x* и *y* , при этом неявно устанавливая *z* и *w* в ноль и один.</span><span class="sxs-lookup"><span data-stu-id="96538-124">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="96538-125">Координаты объектов, представленные [глрастерпос](glrasterpos-functions.md) , обрабатываются так же, как и команда [глвертекс](glvertex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="96538-125">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="96538-126">Они преобразуются в текущие матрицы моделвиев и проекции и передаются на этап обрезки.</span><span class="sxs-lookup"><span data-stu-id="96538-126">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="96538-127">Если вершина не изменяется, она проецируется и масштабируется до координат окна, что становится новой текущей позицией, и \_ \_ \_ \_ устанавливается флаг допустимой текущей координаты в главной строке.</span><span class="sxs-lookup"><span data-stu-id="96538-127">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="96538-128">Если удаляется вершина, то допустимый бит снимается, и текущая битовая разкоордината, а также соответствующие координаты цвета и текстуры не определяются.</span><span class="sxs-lookup"><span data-stu-id="96538-128">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="96538-129">Текущая растровая разкоордината также включает некоторые связанные данные цвета и координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="96538-129">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="96538-130">Если освещение включено, то \_ \_ для текущего растрового \_ цвета, в режиме RGBA или \_ текущего \_ растрового индекса GL \_ в режиме индексирования задается цвет, созданный вычислением освещения (см. раздел [гллигхт](gllight-functions.md), [гллигхтмодел](gllightmodel-functions.md)и [**глшадемодел**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="96538-130">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="96538-131">Если освещение отключено, текущий цвет растрового изображения используется для обновления текущего цвета (в режиме RGBA, переменной состояния с \_ текущим \_ цветом) или индекса цвета (в режиме индекса цвета, ПЕРЕМЕННАЯ состояния GL \_ текущий \_ индекс).</span><span class="sxs-lookup"><span data-stu-id="96538-131">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="96538-132">Аналогично, \_ Текущая \_ растровая текстура в главной диаграмме \_ \_ обновляется как функция главной схемы \_ координат GL \_ \_ на основе матрицы текстуры и функций формирования текстуры (см. [глтексжен](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="96538-132">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="96538-133">Наконец, расстояние от начала координат системы координат глаза до вершины, которое преобразуется только матрицей моделвиев, заменяет \_ текущее \_ одноточечное \_ расстояние.</span><span class="sxs-lookup"><span data-stu-id="96538-133">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="96538-134">Изначально текущая Битовая позиция — (0, 0, 0, 1), текущее растровое расстояние равно 0, задан допустимый бит, соответствующий цвет RGBA — (1, 1, 1, 1), связанный цветовой индекс — 1, а связанные координаты текстуры — (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="96538-134">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="96538-135">В режиме RGBA \_ текущий \_ растровый \_ индекс всегда равен 1; в режиме индекса цвета текущий растровый цвет RGBA всегда сохраняет свое начальное значение.</span><span class="sxs-lookup"><span data-stu-id="96538-135">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="96538-136">Растровое расположение изменяется как [глрастерпос](glrasterpos-functions.md) , так и [**глбитмап**](glbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="96538-136">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="96538-137">Если координаты точечной точки являются недопустимыми, команды рисования, основанные на растровой положении, игнорируются (то есть они не приводят к изменениям в состоянии OpenGL).</span><span class="sxs-lookup"><span data-stu-id="96538-137">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="96538-138">Следующие функции извлекают сведения, относящиеся к [глрастерпос](glrasterpos-functions.md):</span><span class="sxs-lookup"><span data-stu-id="96538-138">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="96538-139">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущей \_ точечной \_ позицией GL</span><span class="sxs-lookup"><span data-stu-id="96538-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="96538-140">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущей \_ точечной \_ позицией GL \_ допустимо</span><span class="sxs-lookup"><span data-stu-id="96538-140">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="96538-141">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ текущее \_ растровое \_ расстояние</span><span class="sxs-lookup"><span data-stu-id="96538-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="96538-142">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущий \_ растровый \_ Цвет GL</span><span class="sxs-lookup"><span data-stu-id="96538-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="96538-143">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ текущий \_ растровый \_ индекс</span><span class="sxs-lookup"><span data-stu-id="96538-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="96538-144">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Текущая \_ растровая \_ текстура \_</span><span class="sxs-lookup"><span data-stu-id="96538-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="96538-145">Требования</span><span class="sxs-lookup"><span data-stu-id="96538-145">Requirements</span></span>



| <span data-ttu-id="96538-146">Требование</span><span class="sxs-lookup"><span data-stu-id="96538-146">Requirement</span></span> | <span data-ttu-id="96538-147">Значение</span><span class="sxs-lookup"><span data-stu-id="96538-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96538-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96538-148">Minimum supported client</span></span><br/> | <span data-ttu-id="96538-149">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96538-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="96538-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96538-150">Minimum supported server</span></span><br/> | <span data-ttu-id="96538-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96538-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96538-152">Заголовок</span><span class="sxs-lookup"><span data-stu-id="96538-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="96538-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="96538-153"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="96538-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96538-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="96538-155"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96538-155"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="96538-156">DLL</span><span class="sxs-lookup"><span data-stu-id="96538-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96538-157"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96538-157"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96538-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96538-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96538-159">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="96538-159">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="96538-160">**глбитмап**</span><span class="sxs-lookup"><span data-stu-id="96538-160">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="96538-161">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="96538-161">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="96538-162">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="96538-162">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="96538-163">**гленд**</span><span class="sxs-lookup"><span data-stu-id="96538-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="96538-164">гллигхт</span><span class="sxs-lookup"><span data-stu-id="96538-164">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="96538-165">гллигхтмодел</span><span class="sxs-lookup"><span data-stu-id="96538-165">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="96538-166">**глшадемодел**</span><span class="sxs-lookup"><span data-stu-id="96538-166">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="96538-167">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="96538-167">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="96538-168">глтексжен</span><span class="sxs-lookup"><span data-stu-id="96538-168">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="96538-169">глвертекс</span><span class="sxs-lookup"><span data-stu-id="96538-169">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





