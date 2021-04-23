---
title: Функция glRasterPos4f (GL. h)
description: Задает точечную точку для операций с пикселями. | Функция glRasterPos4f (GL. h)
ms.assetid: 66a349b4-bc33-466a-b64a-84b968f4422f
keywords:
- Функция glRasterPos4f OpenGL
topic_type:
- apiref
api_name:
- glRasterPos4f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ccd9c0779af0e8d508e0cfd817fde96f934ccde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352355"
---
# <a name="glrasterpos4f-function"></a><span data-ttu-id="1dd3e-105">Функция glRasterPos4f</span><span class="sxs-lookup"><span data-stu-id="1dd3e-105">glRasterPos4f function</span></span>

<span data-ttu-id="1dd3e-106">Задает точечную точку для операций с пикселями.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-106">Specifies the raster position for pixel operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd3e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dd3e-107">Syntax</span></span>


```C++
void WINAPI glRasterPos4f(
   GLfloat x,
   GLfloat y,
   GLfloat z,
   GLfloat w
);
```



## <a name="parameters"></a><span data-ttu-id="1dd3e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1dd3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd3e-109">*x*</span><span class="sxs-lookup"><span data-stu-id="1dd3e-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd3e-110">Задает координату по оси x для текущей разточечной точки.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-110">Specifies the x-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="1dd3e-111">*y*</span><span class="sxs-lookup"><span data-stu-id="1dd3e-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd3e-112">Задает координату по оси y для текущей разточечной точки.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-112">Specifies the y-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="1dd3e-113">*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="1dd3e-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd3e-114">Задает координату z для текущей разточечной точки.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-114">Specifies the z-coordinate for the current raster position.</span></span>

</dd> <dt>

<span data-ttu-id="1dd3e-115">*w*</span><span class="sxs-lookup"><span data-stu-id="1dd3e-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd3e-116">W-координата текущей разточечной точки.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-116">The w-coordinate for the current raster position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dd3e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1dd3e-117">Return value</span></span>

<span data-ttu-id="1dd3e-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd3e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1dd3e-119">Remarks</span></span>

<span data-ttu-id="1dd3e-120">OpenGL поддерживает трехмерное расположение в координатах окна.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-120">OpenGL maintains a 3-D position in window coordinates.</span></span> <span data-ttu-id="1dd3e-121">Это расположение, называемое растровой позицией, сохраняется с точностью до точки.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-121">This position, called the raster position, is maintained with subpixel accuracy.</span></span> <span data-ttu-id="1dd3e-122">Он используется для размещения операций записи пикселей и точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-122">It is used to position pixel and bitmap write operations.</span></span> <span data-ttu-id="1dd3e-123">См. раздел [**глбитмап**](glbitmap.md), [**глдравпикселс**](gldrawpixels.md)и [**глкопипикселс**](glcopypixels.md).</span><span class="sxs-lookup"><span data-stu-id="1dd3e-123">See [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md), and [**glCopyPixels**](glcopypixels.md).</span></span>

<span data-ttu-id="1dd3e-124">Текущая битовая разположение состоит из трех координат окна (*x, y, z*), координаты изображения *w* , расстояния от координат глаза, допустимого бита и связанных данных о цветах и координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-124">The current raster position consists of three window coordinates (*x, y, z*), a clip coordinate *w* value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates.</span></span> <span data-ttu-id="1dd3e-125">Координата *w* — это координата обрезки, так как *w* не проецируется на окна координат.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-125">The *w* coordinate is a clip coordinate, because *w* is not projected to window coordinates.</span></span> <span data-ttu-id="1dd3e-126">Функция [glRasterPos4](glrasterpos-functions.md) указывает, что объект координирует координаты *x, y, z* и *w* явным образом.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-126">The [glRasterPos4](glrasterpos-functions.md) function specifies object coordinates *x, y, z*, and *w* explicitly.</span></span> <span data-ttu-id="1dd3e-127">Функция glRasterPos3 указывает, что объект координирует координаты *x, y* и *z* явным образом, хотя *w* неявно имеет значение One.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-127">The glRasterPos3 function specifies object coordinates *x, y,* and *z* explicitly, while *w* is implicitly set to one.</span></span> <span data-ttu-id="1dd3e-128">Функция glRasterPos2 использует значения аргументов для *x* и *y* , при этом неявно устанавливая *z* и *w* в ноль и один.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-128">The glRasterPos2 function uses the argument values for *x* and *y* while implicitly setting *z* and *w* to zero and one.</span></span>

<span data-ttu-id="1dd3e-129">Координаты объектов, представленные [глрастерпос](glrasterpos-functions.md) , обрабатываются так же, как и команда [глвертекс](glvertex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="1dd3e-129">The object coordinates presented by [glRasterPos](glrasterpos-functions.md) are treated just like those of a [glVertex](glvertex-functions.md) command.</span></span> <span data-ttu-id="1dd3e-130">Они преобразуются в текущие матрицы моделвиев и проекции и передаются на этап обрезки.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-130">They are transformed by the current modelview and projection matrices and passed to the clipping stage.</span></span> <span data-ttu-id="1dd3e-131">Если вершина не изменяется, она проецируется и масштабируется до координат окна, что становится новой текущей позицией, и \_ \_ \_ \_ устанавливается флаг допустимой текущей координаты в главной строке.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-131">If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL\_CURRENT\_RASTER\_POSITION\_VALID flag is set.</span></span> <span data-ttu-id="1dd3e-132">Если удаляется вершина, то допустимый бит снимается, и текущая битовая разкоордината, а также соответствующие координаты цвета и текстуры не определяются.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-132">If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.</span></span>

<span data-ttu-id="1dd3e-133">Текущая растровая разкоордината также включает некоторые связанные данные цвета и координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-133">The current raster position also includes some associated color data and texture coordinates.</span></span> <span data-ttu-id="1dd3e-134">Если освещение включено, то \_ \_ для текущего растрового \_ цвета, в режиме RGBA или \_ текущего \_ растрового индекса GL \_ в режиме индексирования задается цвет, созданный вычислением освещения (см. раздел [гллигхт](gllight-functions.md), [гллигхтмодел](gllightmodel-functions.md)и [**глшадемодел**](glshademodel.md)).</span><span class="sxs-lookup"><span data-stu-id="1dd3e-134">If lighting is enabled, then GL\_CURRENT\_RASTER\_COLOR, in RGBA mode, or the GL\_CURRENT\_RASTER\_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md), and [**glShadeModel**](glshademodel.md)).</span></span> <span data-ttu-id="1dd3e-135">Если освещение отключено, текущий цвет растрового изображения используется для обновления текущего цвета (в режиме RGBA, переменной состояния с \_ текущим \_ цветом) или индекса цвета (в режиме индекса цвета, ПЕРЕМЕННАЯ состояния GL \_ текущий \_ индекс).</span><span class="sxs-lookup"><span data-stu-id="1dd3e-135">If lighting is disabled, current color (in RGBA mode, state variable GL\_CURRENT\_COLOR) or color index (in color-index mode, state variable GL\_CURRENT\_INDEX) is used to update the current raster color.</span></span>

<span data-ttu-id="1dd3e-136">Аналогично, \_ Текущая \_ растровая текстура в главной диаграмме \_ \_ обновляется как функция главной схемы \_ координат GL \_ \_ на основе матрицы текстуры и функций формирования текстуры (см. [глтексжен](gltexgen-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="1dd3e-136">Likewise, GL\_CURRENT\_RASTER\_TEXTURE\_COORDS is updated as a function of GL\_CURRENT\_TEXTURE\_COORDS, based on the texture matrix and the texture generation functions (see [glTexGen](gltexgen-functions.md)).</span></span> <span data-ttu-id="1dd3e-137">Наконец, расстояние от начала координат системы координат глаза до вершины, которое преобразуется только матрицей моделвиев, заменяет \_ текущее \_ одноточечное \_ расстояние.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-137">Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL\_CURRENT\_RASTER\_DISTANCE.</span></span>

<span data-ttu-id="1dd3e-138">Изначально текущая Битовая позиция — (0, 0, 0, 1), текущее растровое расстояние равно 0, задан допустимый бит, соответствующий цвет RGBA — (1, 1, 1, 1), связанный цветовой индекс — 1, а связанные координаты текстуры — (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="1dd3e-138">Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1).</span></span> <span data-ttu-id="1dd3e-139">В режиме RGBA \_ текущий \_ растровый \_ индекс всегда равен 1; в режиме индекса цвета текущий растровый цвет RGBA всегда сохраняет свое начальное значение.</span><span class="sxs-lookup"><span data-stu-id="1dd3e-139">In RGBA mode, GL\_CURRENT\_RASTER\_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.</span></span>

> [!Note]  
> <span data-ttu-id="1dd3e-140">Растровое расположение изменяется как [глрастерпос](glrasterpos-functions.md) , так и [**глбитмап**](glbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="1dd3e-140">The raster position is modified both by [glRasterPos](glrasterpos-functions.md) and by [**glBitmap**](glbitmap.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="1dd3e-141">Если координаты точечной точки являются недопустимыми, команды рисования, основанные на растровой положении, игнорируются (то есть они не приводят к изменениям в состоянии OpenGL).</span><span class="sxs-lookup"><span data-stu-id="1dd3e-141">When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).</span></span>

 

<span data-ttu-id="1dd3e-142">Следующие функции извлекают сведения, относящиеся к [глрастерпос](glrasterpos-functions.md):</span><span class="sxs-lookup"><span data-stu-id="1dd3e-142">The following functions retrieve information related to [glRasterPos](glrasterpos-functions.md):</span></span>

<dl>

<span data-ttu-id="1dd3e-143">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущей \_ точечной \_ позицией GL</span><span class="sxs-lookup"><span data-stu-id="1dd3e-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>  
<span data-ttu-id="1dd3e-144">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущей \_ точечной \_ позицией GL \_ допустимо</span><span class="sxs-lookup"><span data-stu-id="1dd3e-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>  
<span data-ttu-id="1dd3e-145">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ текущее \_ растровое \_ расстояние</span><span class="sxs-lookup"><span data-stu-id="1dd3e-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_DISTANCE</span></span>  
<span data-ttu-id="1dd3e-146">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ текущий \_ растровый \_ Цвет GL</span><span class="sxs-lookup"><span data-stu-id="1dd3e-146">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_COLOR</span></span>  
<span data-ttu-id="1dd3e-147">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ текущий \_ растровый \_ индекс</span><span class="sxs-lookup"><span data-stu-id="1dd3e-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_INDEX</span></span>  
<span data-ttu-id="1dd3e-148">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Текущая \_ растровая \_ текстура \_</span><span class="sxs-lookup"><span data-stu-id="1dd3e-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="1dd3e-149">Требования</span><span class="sxs-lookup"><span data-stu-id="1dd3e-149">Requirements</span></span>



| <span data-ttu-id="1dd3e-150">Требование</span><span class="sxs-lookup"><span data-stu-id="1dd3e-150">Requirement</span></span> | <span data-ttu-id="1dd3e-151">Значение</span><span class="sxs-lookup"><span data-stu-id="1dd3e-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd3e-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1dd3e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd3e-153">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1dd3e-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1dd3e-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1dd3e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd3e-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1dd3e-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1dd3e-156">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1dd3e-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dd3e-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd3e-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1dd3e-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1dd3e-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="1dd3e-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dd3e-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1dd3e-160">DLL</span><span class="sxs-lookup"><span data-stu-id="1dd3e-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dd3e-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dd3e-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dd3e-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dd3e-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd3e-163">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="1dd3e-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-164">**глбитмап**</span><span class="sxs-lookup"><span data-stu-id="1dd3e-164">**glBitmap**</span></span>](glbitmap.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-165">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="1dd3e-165">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-166">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="1dd3e-166">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-167">**гленд**</span><span class="sxs-lookup"><span data-stu-id="1dd3e-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-168">гллигхт</span><span class="sxs-lookup"><span data-stu-id="1dd3e-168">glLight</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-169">гллигхтмодел</span><span class="sxs-lookup"><span data-stu-id="1dd3e-169">glLightModel</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-170">**глшадемодел**</span><span class="sxs-lookup"><span data-stu-id="1dd3e-170">**glShadeModel**</span></span>](glshademodel.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-171">**глтекскурд**</span><span class="sxs-lookup"><span data-stu-id="1dd3e-171">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-172">глтексжен</span><span class="sxs-lookup"><span data-stu-id="1dd3e-172">glTexGen</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="1dd3e-173">глвертекс</span><span class="sxs-lookup"><span data-stu-id="1dd3e-173">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





