---
title: Функция Гллигхтмоделив (GL. h)
description: Функция Гллигхтмоделив задает параметры модели освещения.
ms.assetid: 5998bb7e-d97a-47a0-b612-e6b0046aa5d2
keywords:
- Функция Гллигхтмоделив OpenGL
topic_type:
- apiref
api_name:
- glLightModeliv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de61d53d3f4ceb9805ca5560c864379b18c65b3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803485"
---
# <a name="gllightmodeliv-function"></a><span data-ttu-id="050f5-104">Функция Гллигхтмоделив</span><span class="sxs-lookup"><span data-stu-id="050f5-104">glLightModeliv function</span></span>

<span data-ttu-id="050f5-105">Функция [**гллигхтмоделив**](gllightiv.md) задает параметры модели освещения.</span><span class="sxs-lookup"><span data-stu-id="050f5-105">The [**glLightModeliv**](gllightiv.md) function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="050f5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="050f5-106">Syntax</span></span>


```C++
void WINAPI glLightModeliv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="050f5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="050f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="050f5-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="050f5-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="050f5-109">Параметр модели освещения.</span><span class="sxs-lookup"><span data-stu-id="050f5-109">A lighting model parameter.</span></span> <span data-ttu-id="050f5-110">Принимаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="050f5-110">The following values are accepted.</span></span>



| <span data-ttu-id="050f5-111">Значение</span><span class="sxs-lookup"><span data-stu-id="050f5-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="050f5-112">Значение</span><span class="sxs-lookup"><span data-stu-id="050f5-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <span data-ttu-id="050f5-113"><dt>**\_ \_ Наружная модель освещения GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="050f5-113"><dt>**GL\_LIGHT\_MODEL\_AMBIENT**</dt></span></span> </dl>                 | <span data-ttu-id="050f5-114">Параметр *params* содержит четыре целочисленных значения, которые задают интенсивность окружающих RGBA всей сцены.</span><span class="sxs-lookup"><span data-stu-id="050f5-114">The *params* parameter contains four integer values that specify the ambient RGBA intensity of the entire scene.</span></span> <span data-ttu-id="050f5-115">Целочисленные значения сопоставляются линейно, так что наиболее положительное значение, представленное в результате, сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="050f5-115">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="050f5-116">Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="050f5-116">Floating-point values are mapped directly.</span></span> <span data-ttu-id="050f5-117">Ни целое число, ни значения с плавающей запятой не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="050f5-117">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="050f5-118">Интенсивность окружающей сцены по умолчанию — (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="050f5-118">The default ambient scene intensity is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="050f5-119"><dt>**\_ \_ \_ Локальное \_ средство просмотра модели освещения GL**</dt></span><span class="sxs-lookup"><span data-stu-id="050f5-119"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="050f5-120">Параметр *params* — это одно целое значение, указывающее, как вычисляются углы отраженного отражения.</span><span class="sxs-lookup"><span data-stu-id="050f5-120">The *params* parameter is a single integer value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="050f5-121">Если *параметр param* равен 0 (или 0,0), углы отраженного отражения принимают направление представления параллельно с и в направлении оси *z* , независимо от расположения вершины в координатах глаз.</span><span class="sxs-lookup"><span data-stu-id="050f5-121">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="050f5-122">В противном случае отраженные отражения вычисляются из источника системы координат глаза.</span><span class="sxs-lookup"><span data-stu-id="050f5-122">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="050f5-123">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="050f5-123">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="050f5-124"><dt>**\_простая модель GL на \_ \_ две \_ стороны**</dt></span><span class="sxs-lookup"><span data-stu-id="050f5-124"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="050f5-125">Параметр *params* — это одно целое значение, указывающее, выполняются ли для многоугольников односторонние или двусторонние вычисления освещения.</span><span class="sxs-lookup"><span data-stu-id="050f5-125">The *params* parameter is a single integer value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="050f5-126">Он не влияет на вычисления освещения для точек, линий или точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="050f5-126">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="050f5-127">Если *параметр param* равен 0 (или 0,0), то будет указано односторонняя освещение, а в уравнении освещения используются только параметры первого материала.</span><span class="sxs-lookup"><span data-stu-id="050f5-127">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="050f5-128">В противном случае будет указано двустороннее освещение.</span><span class="sxs-lookup"><span data-stu-id="050f5-128">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="050f5-129">В этом случае вершины задних многоугольников освещены с помощью параметров обратного материала, и их нормали отменяются перед вычислением уравнения освещения.</span><span class="sxs-lookup"><span data-stu-id="050f5-129">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="050f5-130">Вершины внешних многоугольников всегда освещены с помощью параметров внешнего материала, без изменения их нормальных элементов.</span><span class="sxs-lookup"><span data-stu-id="050f5-130">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="050f5-131">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="050f5-131">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="050f5-132">*params*</span><span class="sxs-lookup"><span data-stu-id="050f5-132">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="050f5-133">Указатель на значение или значения, которым будут заданы *Параметры* .</span><span class="sxs-lookup"><span data-stu-id="050f5-133">A pointer to the value or values to which *params* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="050f5-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="050f5-134">Return value</span></span>

<span data-ttu-id="050f5-135">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="050f5-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="050f5-136">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="050f5-136">Error codes</span></span>

<span data-ttu-id="050f5-137">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="050f5-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="050f5-138">Имя</span><span class="sxs-lookup"><span data-stu-id="050f5-138">Name</span></span>                                                                                                  | <span data-ttu-id="050f5-139">Значение</span><span class="sxs-lookup"><span data-stu-id="050f5-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="050f5-140"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="050f5-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="050f5-141">*pname* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="050f5-141">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="050f5-142"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="050f5-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="050f5-143">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="050f5-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="050f5-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="050f5-144">Remarks</span></span>

<span data-ttu-id="050f5-145">Функция **гллигхтмоделив** задает параметр модели освещения.</span><span class="sxs-lookup"><span data-stu-id="050f5-145">The **glLightModeliv** function sets lighting model parameter.</span></span> <span data-ttu-id="050f5-146">Параметр *pname* содержит имя параметра, а *param* — новое значение. значение или значения отдельных параметров источника освещения.</span><span class="sxs-lookup"><span data-stu-id="050f5-146">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="050f5-147">В режиме RGBA неяркий цвет вершины представляет собой сумму интенсивности выбросов материала, произведение отражения окружающей среды материала и интенсивность окружающей среды с полным монтажом модели освещения и вклад каждого включенного источника света.</span><span class="sxs-lookup"><span data-stu-id="050f5-147">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="050f5-148">Каждый источник света вносит в сумму три условия: внешние, диффузные и блики.</span><span class="sxs-lookup"><span data-stu-id="050f5-148">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="050f5-149">Вклад источника «внешнее освещение» — это произведение отражения окружающей среды материала и интенсивность окружающей среды освещения.</span><span class="sxs-lookup"><span data-stu-id="050f5-149">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="050f5-150">Макет «диффузный источник света» — это произведение отражения «рассеянный свет», интенсивность рассеянного света и скалярное произведение нормали вершины с нормализованным вектором от вершины к источнику света.</span><span class="sxs-lookup"><span data-stu-id="050f5-150">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="050f5-151">Вклад источника отраженного освещения — это произведение отраженного отражения материала, интенсивность освещения источника и скалярного произведения нормализованных векторов и вершин на светлой основе, возведенное в степень коэффициента блескаи материала.</span><span class="sxs-lookup"><span data-stu-id="050f5-151">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="050f5-152">Все три вклада источника освещения загораются одинаково в зависимости от расстояния от вершины до источника освещения, а также от направления источника освещения, степени плотности распределения и угла отсечения.</span><span class="sxs-lookup"><span data-stu-id="050f5-152">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="050f5-153">Все точки с точками заменяются нулем, если они имеют отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="050f5-153">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="050f5-154">Альфа-компонент полученного светлого цвета задается равным значению альфа для отражения материалов рассеяния.</span><span class="sxs-lookup"><span data-stu-id="050f5-154">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="050f5-155">В режиме индекса цвета значение нетемного индекса диапазонов вершин от окружающей среды к отраженным значениям, передаваемым в [**глматериал**](glmaterial-functions.md) с помощью \_ \_ индексов цвета GL.</span><span class="sxs-lookup"><span data-stu-id="050f5-155">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="050f5-156">Рассеянные и бликовые коэффициенты, вычисленные с помощью (. 30,. 59, .11) взвешивания цветов источника света, коэффициента блеска материала и тех же уравнений отражения и затухания, что и в случае RGBA, определяют, насколько выше окружающая среда получает результирующий индекс.</span><span class="sxs-lookup"><span data-stu-id="050f5-156">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="050f5-157">Следующие функции извлекают сведения, относящиеся к функции **гллигхтмоделив** :</span><span class="sxs-lookup"><span data-stu-id="050f5-157">The following functions retrieve information related to the **glLightModeliv** function:</span></span>

<span data-ttu-id="050f5-158">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом " \_ нелегкая модель", \_ \_ Локальное \_ средство просмотра</span><span class="sxs-lookup"><span data-stu-id="050f5-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="050f5-159">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом главной модели GL, \_ \_ \_ две \_ стороны</span><span class="sxs-lookup"><span data-stu-id="050f5-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="050f5-160">[**глисенаблед**](glisenabled.md) с аргументом \_ освещение GL</span><span class="sxs-lookup"><span data-stu-id="050f5-160">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="050f5-161">Требования</span><span class="sxs-lookup"><span data-stu-id="050f5-161">Requirements</span></span>



| <span data-ttu-id="050f5-162">Требование</span><span class="sxs-lookup"><span data-stu-id="050f5-162">Requirement</span></span> | <span data-ttu-id="050f5-163">Значение</span><span class="sxs-lookup"><span data-stu-id="050f5-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="050f5-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="050f5-164">Minimum supported client</span></span><br/> | <span data-ttu-id="050f5-165">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="050f5-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="050f5-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="050f5-166">Minimum supported server</span></span><br/> | <span data-ttu-id="050f5-167">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="050f5-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="050f5-168">Заголовок</span><span class="sxs-lookup"><span data-stu-id="050f5-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="050f5-169"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="050f5-169"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="050f5-170">Библиотека</span><span class="sxs-lookup"><span data-stu-id="050f5-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="050f5-171"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="050f5-171"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="050f5-172">DLL</span><span class="sxs-lookup"><span data-stu-id="050f5-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="050f5-173"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="050f5-173"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="050f5-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="050f5-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050f5-175">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="050f5-175">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="050f5-176">**гленд**</span><span class="sxs-lookup"><span data-stu-id="050f5-176">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="050f5-177">**гллигхт**</span><span class="sxs-lookup"><span data-stu-id="050f5-177">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="050f5-178">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="050f5-178">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





