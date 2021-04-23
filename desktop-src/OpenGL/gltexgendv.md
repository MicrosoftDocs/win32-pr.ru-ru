---
title: Функция Глтексжендв (GL. h)
description: Управляет созданием координат текстуры. | Функция Глтексжендв (GL. h)
ms.assetid: fe0e28e4-50d3-473f-a290-7745a1718618
keywords:
- Функция Глтексжендв OpenGL
topic_type:
- apiref
api_name:
- glTexGendv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccae96a6289d2172115763b6b6117bf184e2eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104567480"
---
# <a name="gltexgendv-function"></a><span data-ttu-id="ca10d-105">Функция Глтексжендв</span><span class="sxs-lookup"><span data-stu-id="ca10d-105">glTexGendv function</span></span>

<span data-ttu-id="ca10d-106">Управляет созданием координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="ca10d-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca10d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca10d-107">Syntax</span></span>


```C++
void WINAPI glTexGendv(
         GLenum   coord,
         GLenum   pname,
   const GLdouble *params
);
```



## <a name="parameters"></a><span data-ttu-id="ca10d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca10d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca10d-109">*курд*</span><span class="sxs-lookup"><span data-stu-id="ca10d-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="ca10d-110">Координата текстуры.</span><span class="sxs-lookup"><span data-stu-id="ca10d-110">A texture coordinate.</span></span> <span data-ttu-id="ca10d-111">Должно быть одним из следующих: GL \_ S, GL \_ T, GL \_ R или GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="ca10d-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="ca10d-112">**pname**</span><span class="sxs-lookup"><span data-stu-id="ca10d-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="ca10d-113">Символическое имя функции создания координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="ca10d-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="ca10d-114">*params*</span><span class="sxs-lookup"><span data-stu-id="ca10d-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="ca10d-115">Массив, содержащий коэффициенты для соответствующей функции формирования текстуры.</span><span class="sxs-lookup"><span data-stu-id="ca10d-115">An array that contains the coefficients for the corresponding texture generation function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca10d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca10d-116">Return value</span></span>

<span data-ttu-id="ca10d-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ca10d-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ca10d-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ca10d-118">Error codes</span></span>

<span data-ttu-id="ca10d-119">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="ca10d-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ca10d-120">Имя</span><span class="sxs-lookup"><span data-stu-id="ca10d-120">Name</span></span>                                                                                                  | <span data-ttu-id="ca10d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ca10d-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca10d-122"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ca10d-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ca10d-123">*курд* или *pname* не является допустимым определенным значением, или *pname* был ЗАДАН \_ режимом "текстура GL", \_ \_ а *params* не является допустимым определенным значением.</span><span class="sxs-lookup"><span data-stu-id="ca10d-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="ca10d-124"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ca10d-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ca10d-125">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ca10d-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="ca10d-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca10d-126">Remarks</span></span>

<span data-ttu-id="ca10d-127">Функция **глтексжен** выбирает функцию создания координат текстуры или предоставляет коэффициенты для одной из функций.</span><span class="sxs-lookup"><span data-stu-id="ca10d-127">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="ca10d-128">Параметр *курд* называет один из координат текстуры (s, t, r, q) и должен быть одним из следующих символов: GL \_ s, GL \_ t, GL \_ r или GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="ca10d-128">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="ca10d-129">Параметр *pname* должен быть одной из трех символьных констант: \_ \_ режим генерации текстуры GL, план \_ \_ объектов GL \_ или плоскость "GL" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ca10d-129">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="ca10d-130">Если *pname* является либо плоскостью \_ объектной \_ плоскости \_ \_ , либо плоскостью в главной области, *параметр param* содержит коэффициенты для соответствующей функции формирования текстуры.</span><span class="sxs-lookup"><span data-stu-id="ca10d-130">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="ca10d-131">Если функция формирования текстуры является \_ \_ линейной объектом GL, функция</span><span class="sxs-lookup"><span data-stu-id="ca10d-131">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="ca10d-132">! [Формула, показывающая функцию Глтексжен при GL_OBJECT_LINEAR функции формирования текстуры.]</span><span class="sxs-lookup"><span data-stu-id="ca10d-132">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="ca10d-133">используется, где g — значение, вычисленное для координаты с именем в курд; P1, P2, P3 и P4 — четыре значения, указанные в параметрах. и x?, y?, z? и w? — Это объектные координаты вершины.</span><span class="sxs-lookup"><span data-stu-id="ca10d-133">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="ca10d-134">Эту функцию можно использовать для текстуры Map ландшафта, используя уровень Sea в качестве опорной плоскости (определяемой P1, P2, P3 и P4).</span><span class="sxs-lookup"><span data-stu-id="ca10d-134">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="ca10d-135">\_ \_ Функция формирования линейной координаты объекта GL выдает высоту вершины ландшафта в качестве расстояния от уровня моря; эта высота используется для индексации изображения текстуры, чтобы отобразить белый снег на пиковые значения, а зеленый — на фусиллс, например.</span><span class="sxs-lookup"><span data-stu-id="ca10d-135">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="ca10d-136">Если функция формирования текстуры имеет \_ \_ линейный глаз, функция</span><span class="sxs-lookup"><span data-stu-id="ca10d-136">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="ca10d-137">! [Формула, показывающая функцию Глтексжен при GL_EYE_LINEAR функции формирования текстуры.]</span><span class="sxs-lookup"><span data-stu-id="ca10d-137">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="ca10d-138">используется, где</span><span class="sxs-lookup"><span data-stu-id="ca10d-138">is used, where</span></span>

![Формула, показывающая координаты глаза вершины.](images/tex03.png)

<span data-ttu-id="ca10d-140">и x?, y?, z? и w? — Это координаты вершины, P1, P2, P3 и P4 — значения, указанные в *параметре param*, а M — моделвиев матрица при **каллглтексжен**.</span><span class="sxs-lookup"><span data-stu-id="ca10d-140">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you **callglTexGen**.</span></span> <span data-ttu-id="ca10d-141">Если M имеет неплохое условие или в единственном числе, координаты текстуры, формируемые результирующей функцией, могут быть неточными или неопределенными.</span><span class="sxs-lookup"><span data-stu-id="ca10d-141">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="ca10d-142">Обратите внимание, что значения *параметра param* определяют опорную плоскость в координатах глаза.</span><span class="sxs-lookup"><span data-stu-id="ca10d-142">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="ca10d-143">Матрица моделвиев, которая применяется к ним, может отличаться от той, которая действует при преобразовании вершин многоугольников.</span><span class="sxs-lookup"><span data-stu-id="ca10d-143">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="ca10d-144">Эта функция устанавливает поле координат текстуры, которое может создавать динамические линии контура для перемещения объектов.</span><span class="sxs-lookup"><span data-stu-id="ca10d-144">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="ca10d-145">Если *pname* является главной \_ сферой \_ , а *курд* — \_ в качестве координат GL s или GL \_ t, s и t текстуры создаются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ca10d-145">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="ca10d-146">Давайте рассмотрим вектор единиц, указывающий от источника к вершине многоугольника (в координатах глаза).</span><span class="sxs-lookup"><span data-stu-id="ca10d-146">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="ca10d-147">Пусть n будет текущим нормальным, после преобразования в координаты глаз.</span><span class="sxs-lookup"><span data-stu-id="ca10d-147">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="ca10d-148">Let f = (FX () FY () ФЗ) T является вектором отражения, таким, что</span><span class="sxs-lookup"><span data-stu-id="ca10d-148">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Уравнение, показывающее Вектор отражения в виде функции вектора и текущего нормального.](images/tex05.png)

<span data-ttu-id="ca10d-150">Наконец, Let</span><span class="sxs-lookup"><span data-stu-id="ca10d-150">Finally, let</span></span>

![Уравнение, показывающее m как функцию вектора отражения.](images/tex07.png)

<span data-ttu-id="ca10d-152">Затем значения, назначенные координатам текстуры i и t, имеют значение</span><span class="sxs-lookup"><span data-stu-id="ca10d-152">Then the values assigned to the i and t texture coordinates are</span></span>

![Уравнение, показывающее значения, назначенные координатам i и t текстур.](images/tex06.png)

<span data-ttu-id="ca10d-154">Функцию создания координат текстуры можно включить или отключить с помощью [**гленабле**](glenable.md) или [**глдисабле**](gldisable.md) с одним из символьных названий текстурных координат (формирование текстур главной книги, формирование текстур главной книги в ГК, \_ \_ \_ \_ \_ \_ \_ текстура \_ Gen \_ R или \_ текстура GL \_ \_ ) в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="ca10d-154">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="ca10d-155">Если эта функция включена, то указанная Координата текстуры вычисляются в соответствии с формируемой функцией, связанной с этой координатой.</span><span class="sxs-lookup"><span data-stu-id="ca10d-155">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="ca10d-156">Если эта функция отключена, последующие вершины принимают указанную координату текстуры из текущего набора координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="ca10d-156">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="ca10d-157">Изначально все функции создания текстур установлены на \_ \_ линейный глаз и отключаются.</span><span class="sxs-lookup"><span data-stu-id="ca10d-157">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="ca10d-158">Оба уравнения плоскости: (1, 0, 0, 0); Оба уравнения плоскости t: (0, 1, 0, 0); все уравнения плоскости r и q имеют значение (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="ca10d-158">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="ca10d-159">Следующие функции извлекают сведения, относящиеся к Глтексжен:</span><span class="sxs-lookup"><span data-stu-id="ca10d-159">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="ca10d-160">**глжеттексжен**</span><span class="sxs-lookup"><span data-stu-id="ca10d-160">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="ca10d-161">[**глисенаблед**](glisenabled.md) с аргументом \_ Gen текстура GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="ca10d-161">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="ca10d-162">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстуры \_ Gen \_ T</span><span class="sxs-lookup"><span data-stu-id="ca10d-162">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="ca10d-163">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстура \_ Gen \_ R</span><span class="sxs-lookup"><span data-stu-id="ca10d-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="ca10d-164">[**глисенаблед**](glisenabled.md) с аргументом GL \_ текстура \_ Gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="ca10d-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="ca10d-165">Требования</span><span class="sxs-lookup"><span data-stu-id="ca10d-165">Requirements</span></span>



| <span data-ttu-id="ca10d-166">Требование</span><span class="sxs-lookup"><span data-stu-id="ca10d-166">Requirement</span></span> | <span data-ttu-id="ca10d-167">Значение</span><span class="sxs-lookup"><span data-stu-id="ca10d-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca10d-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca10d-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ca10d-169">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ca10d-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ca10d-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca10d-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ca10d-171">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ca10d-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca10d-172">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ca10d-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca10d-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca10d-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ca10d-174">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ca10d-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca10d-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca10d-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ca10d-176">DLL</span><span class="sxs-lookup"><span data-stu-id="ca10d-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca10d-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca10d-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca10d-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca10d-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca10d-179">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="ca10d-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ca10d-180">**гленд**</span><span class="sxs-lookup"><span data-stu-id="ca10d-180">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ca10d-181">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ca10d-181">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ca10d-182">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="ca10d-182">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="ca10d-183">**глжеттексжен**</span><span class="sxs-lookup"><span data-stu-id="ca10d-183">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="ca10d-184">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="ca10d-184">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="ca10d-185">глтексенв</span><span class="sxs-lookup"><span data-stu-id="ca10d-185">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="ca10d-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ca10d-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ca10d-187">глтекспараметер</span><span class="sxs-lookup"><span data-stu-id="ca10d-187">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="ca10d-188">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="ca10d-188">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="ca10d-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="ca10d-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





