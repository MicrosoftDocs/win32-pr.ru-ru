---
title: Функция Глматериалфв (GL. h)
description: Функция Глматериалфв задает параметры материала для модели освещения.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- Функция Глматериалфв OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44b200abe0588a657f770902a9a897329e1942a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414717"
---
# <a name="glmaterialfv-function"></a><span data-ttu-id="6b778-104">Функция Глматериалфв</span><span class="sxs-lookup"><span data-stu-id="6b778-104">glMaterialfv function</span></span>

<span data-ttu-id="6b778-105">Функция **глматериалфв** задает параметры материала для модели освещения.</span><span class="sxs-lookup"><span data-stu-id="6b778-105">The **glMaterialfv** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b778-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b778-106">Syntax</span></span>


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="6b778-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b778-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b778-108">*личным*</span><span class="sxs-lookup"><span data-stu-id="6b778-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="6b778-109">Лицо или грани, которые обновляются.</span><span class="sxs-lookup"><span data-stu-id="6b778-109">The face or faces that are being updated.</span></span> <span data-ttu-id="6b778-110">Должен быть одним из следующих: GL \_ спереди, GL \_ или GL \_ спереди и ГК \_ .</span><span class="sxs-lookup"><span data-stu-id="6b778-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="6b778-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="6b778-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="6b778-112">Параметр Material для обновляемого лица или граней.</span><span class="sxs-lookup"><span data-stu-id="6b778-112">The material parameter of the face or faces being updated.</span></span> <span data-ttu-id="6b778-113">Ниже приведены параметры, которые можно указать с помощью **глматериалфв** и их интерпретации в уравнении освещения.</span><span class="sxs-lookup"><span data-stu-id="6b778-113">The parameters that can be specified using **glMaterialfv**, and their interpretations by the lighting equation, are as follows.</span></span>



| <span data-ttu-id="6b778-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6b778-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="6b778-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6b778-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="6b778-116"><dt>**\_окружение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-116"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                                       | <span data-ttu-id="6b778-117">Параметр params содержит четыре значения с плавающей запятой, которые определяют внешний тип RGBA, отражающий материал.</span><span class="sxs-lookup"><span data-stu-id="6b778-117">The params parameter contains four floating-point values that specify the ambient RGBA reflectance of the material.</span></span> <span data-ttu-id="6b778-118">Целочисленные значения сопоставляются линейно, так что наиболее положительное значение, представленное в результате, сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="6b778-118">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="6b778-119">Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="6b778-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="6b778-120">Ни целое число, ни значения с плавающей запятой не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="6b778-120">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="6b778-121">Окружение по умолчанию для внешних и фоновых материалов имеет значение (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="6b778-121">The default ambient reflectance for both front-facing and back-facing materials is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="6b778-122"><dt>**Рассеивание GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-122"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="6b778-123">Параметр params содержит четыре значения с плавающей запятой, которые указывают, что рассеянный RGBA отражает материал.</span><span class="sxs-lookup"><span data-stu-id="6b778-123">The params parameter contains four floating-point values that specify the diffuse RGBA reflectance of the material.</span></span> <span data-ttu-id="6b778-124">Целочисленные значения сопоставляются линейно, так что наиболее положительное значение, представленное в результате, сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="6b778-124">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="6b778-125">Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="6b778-125">Floating-point values are mapped directly.</span></span> <span data-ttu-id="6b778-126">Ни целое число, ни значения с плавающей запятой не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="6b778-126">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="6b778-127">По умолчанию рассеяние отразится как для внешних, так и для внутренних материалов (0,8, 0,8, 0,8, 1,0).</span><span class="sxs-lookup"><span data-stu-id="6b778-127">The default diffuse reflectance for both front-facing and back-facing materials is (0.8, 0.8, 0.8, 1.0).</span></span> <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="6b778-128"><dt>**\_отражающий GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-128"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                                    | <span data-ttu-id="6b778-129">Параметр params содержит четыре значения с плавающей запятой, которые определяют отражающий RGBA для отражения материала.</span><span class="sxs-lookup"><span data-stu-id="6b778-129">The params parameter contains four floating-point values that specify the specular RGBA reflectance of the material.</span></span> <span data-ttu-id="6b778-130">Целочисленные значения сопоставляются линейно, так что наиболее положительное значение, представленное в результате, сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="6b778-130">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="6b778-131">Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="6b778-131">Floating-point values are mapped directly.</span></span> <span data-ttu-id="6b778-132">Ни целое число, ни значения с плавающей запятой не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="6b778-132">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="6b778-133">Зеркальное отражение по умолчанию для материалов с внешним и резервным доступом имеет значение (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="6b778-133">The default specular reflectance for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="6b778-134"><dt>**\_эмиссия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-134"><dt>**GL\_EMISSION**</dt></span></span> </dl>                                    | <span data-ttu-id="6b778-135">Параметр params содержит четыре значения с плавающей запятой, которые указывают на RGBA, порожденную светлой интенсивностью материала.</span><span class="sxs-lookup"><span data-stu-id="6b778-135">The params parameter contains four floating-point values that specify the RGBA emitted light intensity of the material.</span></span> <span data-ttu-id="6b778-136">Целочисленные значения сопоставляются линейно, так что наиболее положительное значение, представленное в результате, сопоставляется с 1,0, а наиболее отрицательное значение — в-1,0.</span><span class="sxs-lookup"><span data-stu-id="6b778-136">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="6b778-137">Значения с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="6b778-137">Floating-point values are mapped directly.</span></span> <span data-ttu-id="6b778-138">Ни целое число, ни значения с плавающей запятой не обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="6b778-138">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="6b778-139">Интенсивность выбросов по умолчанию для материалов с внешним и резервным доступом имеет значение (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="6b778-139">The default emission intensity for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="6b778-140"><dt>**\_коэффициента БЛЕСКА GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-140"><dt>**GL\_SHININESS**</dt></span></span> </dl>                                 | <span data-ttu-id="6b778-141">Параметр *param* — это одно целое значение, которое указывает экспоненту RGBA для вещества.</span><span class="sxs-lookup"><span data-stu-id="6b778-141">The *param* parameter is a single integer value that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="6b778-142">Целочисленные значения сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="6b778-142">Integer values are mapped directly.</span></span> <span data-ttu-id="6b778-143">Принимаются только значения в диапазоне \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="6b778-143">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="6b778-144">По умолчанию отраженный экспонента для материалов с внешним и резервным интерфейсом — 0.</span><span class="sxs-lookup"><span data-stu-id="6b778-144">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <span data-ttu-id="6b778-145"><dt>**\_внешняя \_ и \_ РАССЕЯНная среды GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-145"><dt>**GL\_AMBIENT\_AND\_DIFFUSE**</dt></span></span> </dl> | <span data-ttu-id="6b778-146">Эквивалентно вызову [**глматериал**](glmaterial-functions.md) дважды с одними и теми же значениями параметров, один раз с окружающей назначением GL \_ и один раз с \_ диффузией GL.</span><span class="sxs-lookup"><span data-stu-id="6b778-146">Equivalent to calling [**glMaterial**](glmaterial-functions.md) twice with the same parameter values, once with GL\_AMBIENT and once with GL\_DIFFUSE.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="6b778-147"><dt>**\_ \_ индексы цвета GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-147"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl>                    | <span data-ttu-id="6b778-148">Параметр params содержит три значения с плавающей запятой, указывающие цветовые индексы для внешних, рассеянных и отраженных освещения.</span><span class="sxs-lookup"><span data-stu-id="6b778-148">The params parameter contains three floating-point values specifying the color indexes for ambient, diffuse, and specular lighting.</span></span> <span data-ttu-id="6b778-149">Эти три значения и коэффициента блеска GL \_ — это единственные значения материала, используемые в уравнении режима цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="6b778-149">These three values, and GL\_SHININESS, are the only material values used by the color-index mode lighting equation.</span></span> <span data-ttu-id="6b778-150">Обсуждение освещения цветового индекса см. в [**гллигхтмодел**](gllightmodel-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="6b778-150">Refer to [**glLightModel**](gllightmodel-functions.md) for a discussion of color-index lighting.</span></span><br/>                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="6b778-151">*params*</span><span class="sxs-lookup"><span data-stu-id="6b778-151">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="6b778-152">Значение, для которого \_ будет задан параметр GL коэффициента блеска.</span><span class="sxs-lookup"><span data-stu-id="6b778-152">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b778-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b778-153">Return value</span></span>

<span data-ttu-id="6b778-154">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6b778-154">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b778-155">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6b778-155">Error codes</span></span>

<span data-ttu-id="6b778-156">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="6b778-156">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6b778-157">Имя</span><span class="sxs-lookup"><span data-stu-id="6b778-157">Name</span></span>                                                                                              | <span data-ttu-id="6b778-158">Значение</span><span class="sxs-lookup"><span data-stu-id="6b778-158">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b778-159"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-159"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="6b778-160">Pname  не является  допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="6b778-160">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="6b778-161"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-161"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="6b778-162">Указана отражающая Экспонента за пределами диапазона \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="6b778-162">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6b778-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b778-163">Remarks</span></span>

<span data-ttu-id="6b778-164">Функция [**глматериалфв**](glmaterialf.md) присваивает значения материальным параметрам.</span><span class="sxs-lookup"><span data-stu-id="6b778-164">The [**glMaterialfv**](glmaterialf.md) function assigns values to material parameters.</span></span> <span data-ttu-id="6b778-165">Существует два соответствующих набора параметров материала.</span><span class="sxs-lookup"><span data-stu-id="6b778-165">There are two matched sets of material parameters.</span></span> <span data-ttu-id="6b778-166">Первый, *внешний* набор, используется для затенения точек, линий, точечных рисунков и всех многоугольников (если двустороннее освещение отключено) или только для внешних многоугольников (если включено двустороннее освещение).</span><span class="sxs-lookup"><span data-stu-id="6b778-166">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="6b778-167">Другой набор, с *обратным переходом*, используется для затенения задних многоугольников только при включении двустороннего освещения.</span><span class="sxs-lookup"><span data-stu-id="6b778-167">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="6b778-168">Дополнительные сведения об односторонним и двустороннем вычислениях освещения см. в разделе [**гллигхтмодел**](gllightmodel-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="6b778-168">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="6b778-169">Функция [**глматериалфв**](glmaterialf.md) принимает три аргумента.</span><span class="sxs-lookup"><span data-stu-id="6b778-169">The [**glMaterialfv**](glmaterialf.md) function takes three arguments.</span></span> <span data-ttu-id="6b778-170">Первый, *лицевой стороной* указывает, будут ли изменены изначальные материалы, первоначальные \_ \_ \_ \_ и \_ задние плановые материалы GL.</span><span class="sxs-lookup"><span data-stu-id="6b778-170">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="6b778-171">Второй параметр, *pname*, указывает, какое из нескольких параметров в одном или обоих наборах будет изменено.</span><span class="sxs-lookup"><span data-stu-id="6b778-171">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="6b778-172">Третья, *param*, указывает, какое значение будет присвоено указанному параметру.</span><span class="sxs-lookup"><span data-stu-id="6b778-172">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="6b778-173">Параметры материала используются в уравнении освещения, которое при необходимости применяется к каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="6b778-173">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="6b778-174">Уравнение рассматривается в [**гллигхтмодел**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6b778-174">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="6b778-175">Параметры материала можно обновить в любое время.</span><span class="sxs-lookup"><span data-stu-id="6b778-175">The material parameters can be updated at any time.</span></span> <span data-ttu-id="6b778-176">В частности, [**глматериалфв**](glmaterialf.md) можно вызывать между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6b778-176">In particular, [**glMaterialfv**](glmaterialf.md) can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="6b778-177">Если для каждой вершины необходимо изменить только один параметр материала, [**глколорматериал**](glcolormaterial.md) является предпочтительным по сравнению с **глматериалфв**.</span><span class="sxs-lookup"><span data-stu-id="6b778-177">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialfv**.</span></span>

<span data-ttu-id="6b778-178">Следующая функция получает сведения, связанные с [**глматериалфв**](glmaterialf.md):</span><span class="sxs-lookup"><span data-stu-id="6b778-178">The following function retrieves information related to [**glMaterialfv**](glmaterialf.md):</span></span>

[<span data-ttu-id="6b778-179">**глжетматериал**</span><span class="sxs-lookup"><span data-stu-id="6b778-179">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="6b778-180">Требования</span><span class="sxs-lookup"><span data-stu-id="6b778-180">Requirements</span></span>



| <span data-ttu-id="6b778-181">Требование</span><span class="sxs-lookup"><span data-stu-id="6b778-181">Requirement</span></span> | <span data-ttu-id="6b778-182">Значение</span><span class="sxs-lookup"><span data-stu-id="6b778-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b778-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b778-183">Minimum supported client</span></span><br/> | <span data-ttu-id="6b778-184">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b778-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6b778-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b778-185">Minimum supported server</span></span><br/> | <span data-ttu-id="6b778-186">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b778-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b778-187">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b778-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b778-188"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-188"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6b778-189">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b778-189">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b778-190"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-190"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b778-191">DLL</span><span class="sxs-lookup"><span data-stu-id="6b778-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b778-192"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b778-192"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b778-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b778-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b778-194">**глколорматериал**</span><span class="sxs-lookup"><span data-stu-id="6b778-194">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="6b778-195">**гллигхт**</span><span class="sxs-lookup"><span data-stu-id="6b778-195">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="6b778-196">**гллигхтмодел**</span><span class="sxs-lookup"><span data-stu-id="6b778-196">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





