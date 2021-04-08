---
title: Функция Гллигхти (GL. h)
description: Функция Гллигхти возвращает значения светлого исходного параметра.
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- Функция Гллигхти OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52225c4db8eaa31c17d12a25590b918cf94b4c3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892093"
---
# <a name="gllighti-function"></a><span data-ttu-id="71ebe-104">Функция Гллигхти</span><span class="sxs-lookup"><span data-stu-id="71ebe-104">glLighti function</span></span>

<span data-ttu-id="71ebe-105">Функция **гллигхти** возвращает значения светлого исходного параметра.</span><span class="sxs-lookup"><span data-stu-id="71ebe-105">The **glLighti** function returns light source parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ebe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71ebe-106">Syntax</span></span>


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="71ebe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="71ebe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ebe-108">*light*</span><span class="sxs-lookup"><span data-stu-id="71ebe-108">*light*</span></span> 
</dt> <dd>

<span data-ttu-id="71ebe-109">Идентификатор источника освещения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-109">The identifier of a light.</span></span> <span data-ttu-id="71ebe-110">Количество возможных источников света зависит от реализации, но поддерживаются по крайней мере восемь источников света.</span><span class="sxs-lookup"><span data-stu-id="71ebe-110">The number of possible lights depends on the implementation, but at least eight lights are supported.</span></span> <span data-ttu-id="71ebe-111">Они определяются символами-псевдонимами в форме \_ «нелегкая *я* », где *я получаю* значение: от 0 до GL Max Lights \_ \_ -1.</span><span class="sxs-lookup"><span data-stu-id="71ebe-111">They are identified by symbolic names of the form GL\_LIGHT *i* where *i* is a value: 0 to GL\_MAX\_LIGHTS - 1.</span></span>

</dd> <dt>

<span data-ttu-id="71ebe-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="71ebe-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="71ebe-113">Однозначный параметр источника Light для *Light*.</span><span class="sxs-lookup"><span data-stu-id="71ebe-113">A single-valued light source parameter for *light*.</span></span> <span data-ttu-id="71ebe-114">Допустимы следующие символьные имена.</span><span class="sxs-lookup"><span data-stu-id="71ebe-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="71ebe-115">Значение</span><span class="sxs-lookup"><span data-stu-id="71ebe-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="71ebe-116">Значение</span><span class="sxs-lookup"><span data-stu-id="71ebe-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <span data-ttu-id="71ebe-117"><dt>**\_показатель степени для точки GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-117"><dt>**GL\_SPOT\_EXPONENT**</dt></span></span> </dl>                                                                                                                                                                             | <span data-ttu-id="71ebe-118">Параметр *param* представляет собой одно целое значение, определяющее распределение интенсивности освещения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-118">The *param* parameter is a single integer value that specifies the intensity distribution of the light.</span></span> <span data-ttu-id="71ebe-119">Значения типа Integer и с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="71ebe-119">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="71ebe-120">Принимаются только значения в диапазоне \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="71ebe-120">Only values in the range \[0, 128\] are accepted.</span></span> <br/> <span data-ttu-id="71ebe-121">Эффективная интенсивность освещения ослаблена косинусом угла между направлением освещения и направлением от светлого к вершине, возведенному в степень плашечной степени.</span><span class="sxs-lookup"><span data-stu-id="71ebe-121">Effective light intensity is attenuated by the cosine of the angle between the direction of the light and the direction from the light to the vertex being lighted, raised to the power of the spot exponent.</span></span> <span data-ttu-id="71ebe-122">Таким образом, большие точки экспоненты приводят к более специализированному источнику освещения, независимо от угла отсечения точки.</span><span class="sxs-lookup"><span data-stu-id="71ebe-122">Thus, higher spot exponents result in a more focused light source, regardless of the spot cutoff angle.</span></span> <span data-ttu-id="71ebe-123">Значением точки экспоненты по умолчанию является 0, что приводит к равномерному распределению освещения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-123">The default spot exponent is 0, resulting in uniform light distribution.</span></span><br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <span data-ttu-id="71ebe-124"><dt>**\_отсечение точки GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-124"><dt>**GL\_SPOT\_CUTOFF**</dt></span></span> </dl>                                                                                                                                                                                   | <span data-ttu-id="71ebe-125">Параметр *param* — это одно целое значение, указывающее максимальный угол распределения источника освещения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-125">The *param* parameter is a single integer value that specifies the maximum spread angle of a light source.</span></span> <span data-ttu-id="71ebe-126">Значения типа Integer и с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="71ebe-126">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="71ebe-127">Принимаются только значения в диапазоне \[ 0, 90 \] и специальное значение 180.</span><span class="sxs-lookup"><span data-stu-id="71ebe-127">Only values in the range \[0, 90\], and the special value 180, are accepted.</span></span> <br/> <span data-ttu-id="71ebe-128">Если угол между направлением освещения и направлением от светлого к вершине, который является светлой, больше, чем угол отсечения, то этот источник полностью маскируется.</span><span class="sxs-lookup"><span data-stu-id="71ebe-128">If the angle between the direction of the light and the direction from the light to the vertex being lighted is greater than the spot cutoff angle, then the light is completely masked.</span></span> <span data-ttu-id="71ebe-129">В противном случае его интенсивность определяется плашечной экспонентой и факторами затухания.</span><span class="sxs-lookup"><span data-stu-id="71ebe-129">Otherwise, its intensity is controlled by the spot exponent and the attenuation factors.</span></span> <span data-ttu-id="71ebe-130">По умолчанию точечная отсечение составляет 180, что приводит к равномерному распределению освещения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-130">The default spot cutoff is 180, resulting in uniform light distribution.</span></span><br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <span data-ttu-id="71ebe-131"><dt>**\_затухание константы GL \_ , \_ линейное \_ затухание по ГК, \_ затухание в квадратичном квадрате \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-131"><dt>**GL\_CONSTANT\_ATTENUATION, GL\_LINEAR\_ATTENUATION, GL\_QUADRATIC\_ATTENUATION**</dt></span></span> </dl> | <span data-ttu-id="71ebe-132">Параметр *param* представляет собой одно целочисленное значение, определяющее один из трех факторов затухания.</span><span class="sxs-lookup"><span data-stu-id="71ebe-132">The *param* parameter is a single integer value that specifies one of the three light attenuation factors.</span></span> <span data-ttu-id="71ebe-133">Значения типа Integer и с плавающей запятой сопоставляются напрямую.</span><span class="sxs-lookup"><span data-stu-id="71ebe-133">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="71ebe-134">Принимаются только неотрицательные значения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-134">Only nonnegative values are accepted.</span></span> <br/> <span data-ttu-id="71ebe-135">Если освещение является позиционированным, а не направленным, его интенсивность уменьшается на обратную сумму: постоянный коэффициент, линейный коэффициент, умноженный на расстояние между освещением и вершиной, а также квадратный фактор, умноженный на квадрат того же расстояния.</span><span class="sxs-lookup"><span data-stu-id="71ebe-135">If the light is positional, rather than directional, its intensity is attenuated by the reciprocal of the sum of: the constant factor, the linear factor multiplied by the distance between the light and the vertex being lighted, and the quadratic factor multiplied by the square of the same distance.</span></span> <span data-ttu-id="71ebe-136">Коэффициенты затухания по умолчанию: (1, 0, 0), что не приводит к ослаблению.</span><span class="sxs-lookup"><span data-stu-id="71ebe-136">The default attenuation factors are (1,0,0), resulting in no attenuation.</span></span><br/>                   |



 

</dd> <dt>

<span data-ttu-id="71ebe-137">*param*</span><span class="sxs-lookup"><span data-stu-id="71ebe-137">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="71ebe-138">Задает значение, для которого параметр *pname* *светлого источника освещения* будет установлен равным.</span><span class="sxs-lookup"><span data-stu-id="71ebe-138">Specifies the value that parameter *pname* of light source *light* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ebe-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71ebe-139">Return value</span></span>

<span data-ttu-id="71ebe-140">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="71ebe-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71ebe-141">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="71ebe-141">Error codes</span></span>

<span data-ttu-id="71ebe-142">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="71ebe-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71ebe-143">Имя</span><span class="sxs-lookup"><span data-stu-id="71ebe-143">Name</span></span>                                                                                                  | <span data-ttu-id="71ebe-144">Значение</span><span class="sxs-lookup"><span data-stu-id="71ebe-144">Meaning</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71ebe-145"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="71ebe-146">параметр *Light* или *pname* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="71ebe-146">*light* or *pname* was not an accepted value.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="71ebe-147"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="71ebe-148">Значение точки экспоненты, указанное за пределами диапазона \[ 0, 128 \] или точечной отсечки, было указано вне диапазона \[ 0, 90 \] (за исключением специального значения 180) или был указан отрицательный коэффициент затухания.</span><span class="sxs-lookup"><span data-stu-id="71ebe-148">A spot exponent value was specified outside the range \[0, 128\], or spot cutoff was specified outside the range \[0, 90\] (except for the special value 180), or a negative attenuation factor was specified.</span></span><br/> |
| <dl> <span data-ttu-id="71ebe-149"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71ebe-150">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="71ebe-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="71ebe-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71ebe-151">Remarks</span></span>

<span data-ttu-id="71ebe-152">Функция **гллигхти** задает значение или значения отдельных параметров источника освещения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-152">The **glLighti** function sets the value or values of individual light source parameters.</span></span> <span data-ttu-id="71ebe-153">Параметр *Light* именует источник света, а — символическое имя формы \_ «GL»*i*, где 0 = <  « \_ максимальные \_ огни».</span><span class="sxs-lookup"><span data-stu-id="71ebe-153">The *light* parameter names the light and is a symbolic name of the form GL\_LIGHT *i*, where 0 = *i* < GL\_MAX\_LIGHTS.</span></span>

<span data-ttu-id="71ebe-154">Параметр *pname* указывает один из исходных параметров источника, который опять же содержит символьное имя.</span><span class="sxs-lookup"><span data-stu-id="71ebe-154">The *pname* parameter specifies one of the light source parameters, again by symbolic name.</span></span> <span data-ttu-id="71ebe-155">Параметр *param* является либо одиночным значением, либо указателем на массив, который содержит новые значения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-155">The *param* parameter is either a single value or a pointer to an array that contains the new values.</span></span>

<span data-ttu-id="71ebe-156">Вычисление освещения включается и отключается с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом \_ освещение GL.</span><span class="sxs-lookup"><span data-stu-id="71ebe-156">Lighting calculation is enabled and disabled using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_LIGHTING.</span></span> <span data-ttu-id="71ebe-157">Если включено освещение, источники света, которые включены, вносят вклад в расчет освещения.</span><span class="sxs-lookup"><span data-stu-id="71ebe-157">When lighting is enabled, light sources that are enabled contribute to the lighting calculation.</span></span> <span data-ttu-id="71ebe-158">Источник освещения *i* включен и отключен с помощью **гленабле** и **глдисабле** с аргументом GL \_ Light *i*.</span><span class="sxs-lookup"><span data-stu-id="71ebe-158">Light source *i* is enabled and disabled using **glEnable** and **glDisable** with argument GL\_LIGHT *i*.</span></span>

<span data-ttu-id="71ebe-159">Это всегда относится к нефинансовому \_ освещению *i* = GL \_ LIGHT0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="71ebe-159">It is always the case that GL\_LIGHT *i* = GL\_LIGHT0 + *i*.</span></span>

<span data-ttu-id="71ebe-160">Следующие функции извлекают сведения, относящиеся к функции **гллигхти** :</span><span class="sxs-lookup"><span data-stu-id="71ebe-160">The following functions retrieve information related to the **glLighti** function:</span></span>

[<span data-ttu-id="71ebe-161">**глжетлигхт**</span><span class="sxs-lookup"><span data-stu-id="71ebe-161">**glGetLight**</span></span>](glgetlight.md)

<span data-ttu-id="71ebe-162">[**глисенаблед**](glisenabled.md) с аргументом \_ освещение GL</span><span class="sxs-lookup"><span data-stu-id="71ebe-162">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="71ebe-163">Требования</span><span class="sxs-lookup"><span data-stu-id="71ebe-163">Requirements</span></span>



| <span data-ttu-id="71ebe-164">Требование</span><span class="sxs-lookup"><span data-stu-id="71ebe-164">Requirement</span></span> | <span data-ttu-id="71ebe-165">Значение</span><span class="sxs-lookup"><span data-stu-id="71ebe-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71ebe-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71ebe-166">Minimum supported client</span></span><br/> | <span data-ttu-id="71ebe-167">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71ebe-167">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71ebe-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71ebe-168">Minimum supported server</span></span><br/> | <span data-ttu-id="71ebe-169">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="71ebe-169">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71ebe-170">Заголовок</span><span class="sxs-lookup"><span data-stu-id="71ebe-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="71ebe-171"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-171"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71ebe-172">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71ebe-172">Library</span></span><br/>                  | <dl> <span data-ttu-id="71ebe-173"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-173"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71ebe-174">DLL</span><span class="sxs-lookup"><span data-stu-id="71ebe-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71ebe-175"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ebe-175"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ebe-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71ebe-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ebe-177">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="71ebe-177">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71ebe-178">**глколорматериал**</span><span class="sxs-lookup"><span data-stu-id="71ebe-178">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="71ebe-179">**гленд**</span><span class="sxs-lookup"><span data-stu-id="71ebe-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71ebe-180">**гллигхтмодел**</span><span class="sxs-lookup"><span data-stu-id="71ebe-180">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="71ebe-181">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="71ebe-181">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





