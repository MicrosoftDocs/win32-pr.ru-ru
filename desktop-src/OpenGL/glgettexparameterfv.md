---
title: Функция Глжеттекспараметерфв (GL. h)
description: Функции Глжеттекспараметерфв и Глжеттекспараметерив возвращают значения параметров текстуры. | Функция Глжеттекспараметерфв (GL. h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- Функция Глжеттекспараметерфв OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0af6e5fd91d38240dd3463b9440333b5da431d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684940"
---
# <a name="glgettexparameterfv-function"></a><span data-ttu-id="31de2-105">Функция Глжеттекспараметерфв</span><span class="sxs-lookup"><span data-stu-id="31de2-105">glGetTexParameterfv function</span></span>

<span data-ttu-id="31de2-106">Функции **глжеттекспараметерфв** и [**глжеттекспараметерив**](glgettexparameteriv.md) возвращают значения параметров текстуры.</span><span class="sxs-lookup"><span data-stu-id="31de2-106">The **glGetTexParameterfv** and [**glGetTexParameteriv**](glgettexparameteriv.md) functions return texture parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="31de2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31de2-107">Syntax</span></span>


```C++
void WINAPI glGetTexParameterfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="31de2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="31de2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31de2-109">*target*</span><span class="sxs-lookup"><span data-stu-id="31de2-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="31de2-110">Символьное имя целевой текстуры.</span><span class="sxs-lookup"><span data-stu-id="31de2-110">The symbolic name of the target texture.</span></span> <span data-ttu-id="31de2-111">\_ \_ Принимаются текстуры GL 1d \_ и \_ 2D текстуры GL.</span><span class="sxs-lookup"><span data-stu-id="31de2-111">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="31de2-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="31de2-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="31de2-113">Символическое имя параметра текстуры.</span><span class="sxs-lookup"><span data-stu-id="31de2-113">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="31de2-114">Принимаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="31de2-114">The following values are accepted.</span></span>



| <span data-ttu-id="31de2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="31de2-115">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="31de2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="31de2-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="31de2-117"><dt>**\_ \_ Фильтр MAG текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-117"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="31de2-118">Возвращает фильтр увеличения текстуры с одним значением, символьная константа.</span><span class="sxs-lookup"><span data-stu-id="31de2-118">Returns the single-valued texture magnification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="31de2-119"><dt>**\_ \_ Фильтр min текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-119"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="31de2-120">Возвращает однозначный минификацииный фильтр, символьную константу.</span><span class="sxs-lookup"><span data-stu-id="31de2-120">Returns the single-valued texture minification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="31de2-121"><dt>**\_Перенос текстуры в ГК \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-121"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="31de2-122">Возвращает функцию упаковки с одним значением для координаты текстуры *s*, символьную константу.</span><span class="sxs-lookup"><span data-stu-id="31de2-122">Returns the single-valued wrapping function for texture coordinate *s*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="31de2-123"><dt>**\_Обтекание текстуры GL \_ \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-123"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="31de2-124">Возвращает функцию упаковки с одним значением для координаты текстуры *t*, символьную константу.</span><span class="sxs-lookup"><span data-stu-id="31de2-124">Returns the single-valued wrapping function for texture coordinate *t*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="31de2-125"><dt>**\_ \_ Цвет границы текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-125"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="31de2-126">Возвращает четыре числа с плавающей запятой, которые составляют цвет RGBA границы текстуры.</span><span class="sxs-lookup"><span data-stu-id="31de2-126">Returns four integer or floating-point numbers that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="31de2-127">Значения с плавающей запятой возвращаются в диапазоне \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="31de2-127">Floating-point values are returned in the range \[0,1\].</span></span> <span data-ttu-id="31de2-128">Целочисленные значения возвращаются в виде линейного сопоставления с внутренним представлением с плавающей запятой таким образом, что 1,0 сопоставляется с самым положительным целым числом и-1,0 сопоставляется с наиболее отрицательным целым числом.</span><span class="sxs-lookup"><span data-stu-id="31de2-128">Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.</span></span><br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="31de2-129"><dt>**\_приоритет текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-129"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="31de2-130">Возвращает приоритет проживания целевой текстуры (или связанную с ним текстуру).</span><span class="sxs-lookup"><span data-stu-id="31de2-130">Returns the residence priority of the target texture (or the named texture bound to it).</span></span> <span data-ttu-id="31de2-131">Начальное значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="31de2-131">The initial value is 1.</span></span> <span data-ttu-id="31de2-132">См. [**глприоритизетекстурес**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="31de2-132">See [**glPrioritizeTextures**](glprioritizetextures.md).</span></span><br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <span data-ttu-id="31de2-133"><dt>**\_резидентная текстура GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-133"><dt>**GL\_TEXTURE\_RESIDENT**</dt></span></span> </dl>              | <span data-ttu-id="31de2-134">Возвращает состояние проживания целевой текстуры.</span><span class="sxs-lookup"><span data-stu-id="31de2-134">Returns the residence status of the target texture.</span></span> <span data-ttu-id="31de2-135">Если значение, возвращенное в параметре params, имеет значение GL \_ true, текстура накладывается в память текстуры.</span><span class="sxs-lookup"><span data-stu-id="31de2-135">If the value returned in params is GL\_TRUE, the texture is resident in texture memory.</span></span> <span data-ttu-id="31de2-136">См. [**гларетекстуресресидент**](glaretexturesresident.md).</span><span class="sxs-lookup"><span data-stu-id="31de2-136">See [**glAreTexturesResident**](glaretexturesresident.md).</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="31de2-137">*params*</span><span class="sxs-lookup"><span data-stu-id="31de2-137">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="31de2-138">Возвращает параметры текстуры.</span><span class="sxs-lookup"><span data-stu-id="31de2-138">Returns the texture parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31de2-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31de2-139">Return value</span></span>

<span data-ttu-id="31de2-140">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="31de2-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="31de2-141">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="31de2-141">Error codes</span></span>

<span data-ttu-id="31de2-142">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="31de2-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="31de2-143">Имя</span><span class="sxs-lookup"><span data-stu-id="31de2-143">Name</span></span>                                                                                                  | <span data-ttu-id="31de2-144">Значение</span><span class="sxs-lookup"><span data-stu-id="31de2-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31de2-145"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="31de2-146">Недопустимое значение *целевого объекта* или *имени* .</span><span class="sxs-lookup"><span data-stu-id="31de2-146">*target* or *name* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="31de2-147"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="31de2-148">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="31de2-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="31de2-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31de2-149">Remarks</span></span>

<span data-ttu-id="31de2-150">Функция **глжеттекспараметер** возвращает в *params* значение или значения параметра текстуры, указанного как *pname*.</span><span class="sxs-lookup"><span data-stu-id="31de2-150">The **glGetTexParameter** function returns in *params* the value or values of the texture parameter specified as *pname*.</span></span> <span data-ttu-id="31de2-151">*Целевой* параметр определяет целевую текстуру, либо \_ \_ 2D-текстура 1d, либо \_ двухмерная текстура GL \_ , чтобы указать одномерный или двухмерный текстурированный рисунок.</span><span class="sxs-lookup"><span data-stu-id="31de2-151">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="31de2-152">Параметр *pname* принимает те же символы, что и [**глтекспараметер**](gltexparameter-functions.md), с одинаковыми интерпретациями.</span><span class="sxs-lookup"><span data-stu-id="31de2-152">The *pname* parameter accepts the same symbols as [**glTexParameter**](gltexparameter-functions.md), with the same interpretations.</span></span>

<span data-ttu-id="31de2-153">Если возникает ошибка, содержимое *параметров* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="31de2-153">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="31de2-154">Требования</span><span class="sxs-lookup"><span data-stu-id="31de2-154">Requirements</span></span>



| <span data-ttu-id="31de2-155">Требование</span><span class="sxs-lookup"><span data-stu-id="31de2-155">Requirement</span></span> | <span data-ttu-id="31de2-156">Значение</span><span class="sxs-lookup"><span data-stu-id="31de2-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31de2-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31de2-157">Minimum supported client</span></span><br/> | <span data-ttu-id="31de2-158">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="31de2-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31de2-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31de2-159">Minimum supported server</span></span><br/> | <span data-ttu-id="31de2-160">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="31de2-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31de2-161">Заголовок</span><span class="sxs-lookup"><span data-stu-id="31de2-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="31de2-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="31de2-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31de2-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="31de2-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="31de2-165">DLL</span><span class="sxs-lookup"><span data-stu-id="31de2-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31de2-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31de2-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31de2-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31de2-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31de2-168">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="31de2-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="31de2-169">**гленд**</span><span class="sxs-lookup"><span data-stu-id="31de2-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="31de2-170">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="31de2-170">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





