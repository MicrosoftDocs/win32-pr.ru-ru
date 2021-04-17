---
title: Функция Глжеттекслевелпараметерфв (GL. h)
description: Функции Глжеттекслевелпараметерфв и Глжеттекслевелпараметерив возвращают значения параметров текстуры для определенного уровня детализации. | Функция Глжеттекслевелпараметерфв (GL. h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- Функция Глжеттекслевелпараметерфв OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92f8b55b41d3538f116241a0401cedf643a5e55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664909"
---
# <a name="glgettexlevelparameterfv-function"></a><span data-ttu-id="13df5-105">Функция Глжеттекслевелпараметерфв</span><span class="sxs-lookup"><span data-stu-id="13df5-105">glGetTexLevelParameterfv function</span></span>

<span data-ttu-id="13df5-106">Функции **глжеттекслевелпараметерфв** и [**глжеттекслевелпараметерив**](glgettexlevelparameteriv.md) возвращают значения параметров текстуры для определенного уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="13df5-106">The **glGetTexLevelParameterfv** and [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="13df5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13df5-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="13df5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="13df5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13df5-109">*target*</span><span class="sxs-lookup"><span data-stu-id="13df5-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="13df5-110">Символьное имя целевой текстуры: " \_ текстура \_ 1Д, \_ 2D, двухмерная текстура, \_ плоская текстура \_ \_ \_ или \_ \_ геотекстура прокси-сервера \_ GL".</span><span class="sxs-lookup"><span data-stu-id="13df5-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="13df5-111">*level*</span><span class="sxs-lookup"><span data-stu-id="13df5-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="13df5-112">Номер уровня детализации требуемого изображения.</span><span class="sxs-lookup"><span data-stu-id="13df5-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="13df5-113">Уровень 0 является базовым уровнем образа.</span><span class="sxs-lookup"><span data-stu-id="13df5-113">Level 0 is the base image level.</span></span> <span data-ttu-id="13df5-114">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="13df5-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="13df5-115">*pname*</span><span class="sxs-lookup"><span data-stu-id="13df5-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="13df5-116">Символическое имя параметра текстуры.</span><span class="sxs-lookup"><span data-stu-id="13df5-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="13df5-117">Принимаются следующие имена параметров.</span><span class="sxs-lookup"><span data-stu-id="13df5-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="13df5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="13df5-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="13df5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="13df5-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="13df5-120"><dt>**\_Ширина текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="13df5-121">Параметр *params* возвращает одно значение, содержащее ширину изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="13df5-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="13df5-122">Это значение включает границу изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="13df5-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="13df5-123"><dt>**\_Высота текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="13df5-124">Параметр *params* возвращает одно значение, содержащее высоту изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="13df5-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="13df5-125">Это значение включает границу изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="13df5-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="13df5-126"><dt>**\_ \_ внутренний формат текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="13df5-127">Параметр *params* возвращает единственное значение, описывающее формат шаг текселя текстуры.</span><span class="sxs-lookup"><span data-stu-id="13df5-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="13df5-128"><dt>**\_граница текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="13df5-129">Параметр *params* возвращает одно значение: ширину (в пикселях) границы изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="13df5-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="13df5-130"><dt>**\_ \_ красный размер текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="13df5-131">Внутреннее разрешение хранилища для красного компонента шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="13df5-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="13df5-132">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="13df5-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="13df5-133"><dt>**\_ \_ зеленый размер текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="13df5-134">Внутреннее разрешение хранилища зеленого компонента шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="13df5-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="13df5-135">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="13df5-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="13df5-136"><dt>**\_ \_ синий размер текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="13df5-137">Внутреннее разрешение хранилища для синего компонента шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="13df5-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="13df5-138">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="13df5-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="13df5-139"><dt>**\_ \_ Размер альфа-канала текстуры GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="13df5-140">Внутреннее разрешение хранилища альфа-компонента шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="13df5-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="13df5-141">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="13df5-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="13df5-142"><dt>**\_ \_ Размер светимости текстуры GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="13df5-143">Внутреннее разрешение хранилища для компонента светимости шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="13df5-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="13df5-144">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="13df5-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="13df5-145"><dt>**\_ \_ Размер интенсивности текстуры GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="13df5-146">Внутреннее разрешение хранилища компонента интенсивности шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="13df5-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="13df5-147">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="13df5-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="13df5-148"><dt>**\_компоненты текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="13df5-149">Параметр *params* возвращает одно значение: количество компонентов в изображении текстуры.</span><span class="sxs-lookup"><span data-stu-id="13df5-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="13df5-150">*params*</span><span class="sxs-lookup"><span data-stu-id="13df5-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="13df5-151">Возвращает запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="13df5-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13df5-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13df5-152">Return value</span></span>

<span data-ttu-id="13df5-153">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="13df5-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13df5-154">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="13df5-154">Error codes</span></span>

<span data-ttu-id="13df5-155">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="13df5-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="13df5-156">Имя</span><span class="sxs-lookup"><span data-stu-id="13df5-156">Name</span></span>                                                                                                  | <span data-ttu-id="13df5-157">Значение</span><span class="sxs-lookup"><span data-stu-id="13df5-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13df5-158"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="13df5-159">значение *Target* или *pname* не было принято.</span><span class="sxs-lookup"><span data-stu-id="13df5-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="13df5-160"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="13df5-161">*уровень* меньше нуля или больше, чем *log* 2 *(max)*, где *Max* — это возвращаемое значение для \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="13df5-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="13df5-162"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="13df5-163">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="13df5-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="13df5-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13df5-164">Remarks</span></span>

<span data-ttu-id="13df5-165">Функция **глжеттекслевелпараметер** возвращает значение параметра текстуры *params* для определенного уровня детализации, указанного как *Level*.</span><span class="sxs-lookup"><span data-stu-id="13df5-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="13df5-166">*Целевой* параметр определяет целевую текстуру: "текстура 1Д, плоский, 2D, текстура, двухмерная, текстура \_ прокси-сервера GL \_ \_ \_ \_ \_ \_ или \_ двухмерная текстура прокси-сервера GL \_ \_ для указания одномерного или двумерного текстурирования.</span><span class="sxs-lookup"><span data-stu-id="13df5-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="13df5-167">Параметр *pname* указывает параметр текстуры, значение или значения которого будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="13df5-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="13df5-168">Если возникает ошибка, содержимое *параметров* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="13df5-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="13df5-169">Требования</span><span class="sxs-lookup"><span data-stu-id="13df5-169">Requirements</span></span>



| <span data-ttu-id="13df5-170">Требование</span><span class="sxs-lookup"><span data-stu-id="13df5-170">Requirement</span></span> | <span data-ttu-id="13df5-171">Значение</span><span class="sxs-lookup"><span data-stu-id="13df5-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13df5-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13df5-172">Minimum supported client</span></span><br/> | <span data-ttu-id="13df5-173">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="13df5-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="13df5-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13df5-174">Minimum supported server</span></span><br/> | <span data-ttu-id="13df5-175">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="13df5-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13df5-176">Заголовок</span><span class="sxs-lookup"><span data-stu-id="13df5-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="13df5-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="13df5-178">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13df5-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="13df5-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="13df5-180">DLL</span><span class="sxs-lookup"><span data-stu-id="13df5-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13df5-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13df5-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13df5-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13df5-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13df5-183">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="13df5-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="13df5-184">**гленд**</span><span class="sxs-lookup"><span data-stu-id="13df5-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="13df5-185">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="13df5-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="13df5-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="13df5-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="13df5-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="13df5-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="13df5-188">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="13df5-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





