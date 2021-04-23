---
title: Функция Гллигхтмоделф (GL. h)
description: Функция Гллигхтмоделф задает параметры модели освещения.
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- Функция Гллигхтмоделф OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2c17f7dc82080544a9055805cf62726227c200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071146"
---
# <a name="gllightmodelf-function"></a><span data-ttu-id="4592f-104">Функция Гллигхтмоделф</span><span class="sxs-lookup"><span data-stu-id="4592f-104">glLightModelf function</span></span>

<span data-ttu-id="4592f-105">Функция **гллигхтмоделф** задает параметры модели освещения.</span><span class="sxs-lookup"><span data-stu-id="4592f-105">The **glLightModelf** function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4592f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4592f-106">Syntax</span></span>


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a><span data-ttu-id="4592f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4592f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4592f-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="4592f-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="4592f-109">Параметр модели освещения с одним значением.</span><span class="sxs-lookup"><span data-stu-id="4592f-109">A single-valued lighting model parameter.</span></span> <span data-ttu-id="4592f-110">Принимаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="4592f-110">The following values are accepted.</span></span>



| <span data-ttu-id="4592f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4592f-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="4592f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4592f-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="4592f-113"><dt>**\_ \_ \_ Локальное \_ средство просмотра модели освещения GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4592f-113"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="4592f-114">Параметр *param* представляет собой одиночное значение с плавающей запятой, которое указывает, как вычисляются углы отраженного отражения.</span><span class="sxs-lookup"><span data-stu-id="4592f-114">The *param* parameter is a single floating-point value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="4592f-115">Если *параметр param* равен 0 (или 0,0), углы отраженного отражения принимают направление представления параллельно с и в направлении оси *z* , независимо от расположения вершины в координатах глаз.</span><span class="sxs-lookup"><span data-stu-id="4592f-115">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="4592f-116">В противном случае отраженные отражения вычисляются из источника системы координат глаза.</span><span class="sxs-lookup"><span data-stu-id="4592f-116">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="4592f-117">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="4592f-117">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="4592f-118"><dt>**\_простая модель GL на \_ \_ две \_ стороны**</dt></span><span class="sxs-lookup"><span data-stu-id="4592f-118"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="4592f-119">Параметр *param* представляет собой одно значение с плавающей запятой, которое указывает, выполняются ли для многоугольников односторонние или двусторонние вычисления освещения.</span><span class="sxs-lookup"><span data-stu-id="4592f-119">The *param* parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="4592f-120">Он не влияет на вычисления освещения для точек, линий или точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="4592f-120">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="4592f-121">Если *параметр param* равен 0 (или 0,0), то будет указано односторонняя освещение, а в уравнении освещения используются только параметры первого материала.</span><span class="sxs-lookup"><span data-stu-id="4592f-121">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="4592f-122">В противном случае будет указано двустороннее освещение.</span><span class="sxs-lookup"><span data-stu-id="4592f-122">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="4592f-123">В этом случае вершины задних многоугольников освещены с помощью параметров обратного материала, и их нормали отменяются перед вычислением уравнения освещения.</span><span class="sxs-lookup"><span data-stu-id="4592f-123">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="4592f-124">Вершины внешних многоугольников всегда освещены с помощью параметров внешнего материала, без изменения их нормальных элементов.</span><span class="sxs-lookup"><span data-stu-id="4592f-124">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="4592f-125">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="4592f-125">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4592f-126">*param*</span><span class="sxs-lookup"><span data-stu-id="4592f-126">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="4592f-127">Значение, в которое будет задан *параметр param* .</span><span class="sxs-lookup"><span data-stu-id="4592f-127">The value to which *param* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4592f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4592f-128">Return value</span></span>

<span data-ttu-id="4592f-129">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4592f-129">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4592f-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4592f-130">Error codes</span></span>

<span data-ttu-id="4592f-131">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="4592f-131">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4592f-132">Имя</span><span class="sxs-lookup"><span data-stu-id="4592f-132">Name</span></span>                                                                                                  | <span data-ttu-id="4592f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4592f-133">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4592f-134"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4592f-134"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4592f-135">*pname* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="4592f-135">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="4592f-136"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4592f-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4592f-137">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4592f-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4592f-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4592f-138">Remarks</span></span>

<span data-ttu-id="4592f-139">Функция **гллигхтмоделф** задает параметр модели освещения.</span><span class="sxs-lookup"><span data-stu-id="4592f-139">The **glLightModelf** function sets lighting model parameter.</span></span> <span data-ttu-id="4592f-140">Параметр *pname* содержит имя параметра, а *param* — новое значение. значение или значения отдельных параметров источника освещения.</span><span class="sxs-lookup"><span data-stu-id="4592f-140">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="4592f-141">В режиме RGBA неяркий цвет вершины представляет собой сумму интенсивности выбросов материала, произведение отражения окружающей среды материала и интенсивность окружающей среды с полным монтажом модели освещения и вклад каждого включенного источника света.</span><span class="sxs-lookup"><span data-stu-id="4592f-141">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="4592f-142">Каждый источник света вносит в сумму три условия: внешние, диффузные и блики.</span><span class="sxs-lookup"><span data-stu-id="4592f-142">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="4592f-143">Вклад источника «внешнее освещение» — это произведение отражения окружающей среды материала и интенсивность окружающей среды освещения.</span><span class="sxs-lookup"><span data-stu-id="4592f-143">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="4592f-144">Макет «диффузный источник света» — это произведение отражения «рассеянный свет», интенсивность рассеянного света и скалярное произведение нормали вершины с нормализованным вектором от вершины к источнику света.</span><span class="sxs-lookup"><span data-stu-id="4592f-144">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="4592f-145">Вклад источника отраженного освещения — это произведение отраженного отражения материала, интенсивность освещения источника и скалярного произведения нормализованных векторов и вершин на светлой основе, возведенное в степень коэффициента блескаи материала.</span><span class="sxs-lookup"><span data-stu-id="4592f-145">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="4592f-146">Все три вклада источника освещения загораются одинаково в зависимости от расстояния от вершины до источника освещения, а также от направления источника освещения, степени плотности распределения и угла отсечения.</span><span class="sxs-lookup"><span data-stu-id="4592f-146">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="4592f-147">Все точки с точками заменяются нулем, если они имеют отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="4592f-147">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="4592f-148">Альфа-компонент полученного светлого цвета задается равным значению альфа для отражения материалов рассеяния.</span><span class="sxs-lookup"><span data-stu-id="4592f-148">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="4592f-149">В режиме индекса цвета значение нетемного индекса диапазонов вершин от окружающей среды к отраженным значениям, передаваемым в [**глматериал**](glmaterial-functions.md) с помощью \_ \_ индексов цвета GL.</span><span class="sxs-lookup"><span data-stu-id="4592f-149">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="4592f-150">Рассеянные и бликовые коэффициенты, вычисленные с помощью (. 30,. 59, .11) взвешивания цветов источника света, коэффициента блеска материала и тех же уравнений отражения и затухания, что и в случае RGBA, определяют, насколько выше окружающая среда получает результирующий индекс.</span><span class="sxs-lookup"><span data-stu-id="4592f-150">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="4592f-151">Следующие функции извлекают сведения, относящиеся к функции **гллигхтмоделф** :</span><span class="sxs-lookup"><span data-stu-id="4592f-151">The following functions retrieve information related to the **glLightModelf** function:</span></span>

<span data-ttu-id="4592f-152">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом " \_ нелегкая модель", \_ \_ Локальное \_ средство просмотра</span><span class="sxs-lookup"><span data-stu-id="4592f-152">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="4592f-153">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом главной модели GL, \_ \_ \_ две \_ стороны</span><span class="sxs-lookup"><span data-stu-id="4592f-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="4592f-154">[**глисенаблед**](glisenabled.md) с аргументом \_ освещение GL</span><span class="sxs-lookup"><span data-stu-id="4592f-154">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="4592f-155">Требования</span><span class="sxs-lookup"><span data-stu-id="4592f-155">Requirements</span></span>



| <span data-ttu-id="4592f-156">Требование</span><span class="sxs-lookup"><span data-stu-id="4592f-156">Requirement</span></span> | <span data-ttu-id="4592f-157">Значение</span><span class="sxs-lookup"><span data-stu-id="4592f-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4592f-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4592f-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4592f-159">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4592f-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4592f-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4592f-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4592f-161">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4592f-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4592f-162">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4592f-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="4592f-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4592f-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4592f-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4592f-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="4592f-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4592f-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4592f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="4592f-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4592f-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4592f-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4592f-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4592f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4592f-169">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="4592f-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4592f-170">**гленд**</span><span class="sxs-lookup"><span data-stu-id="4592f-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4592f-171">**гллигхт**</span><span class="sxs-lookup"><span data-stu-id="4592f-171">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="4592f-172">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="4592f-172">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





