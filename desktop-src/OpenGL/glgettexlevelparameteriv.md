---
title: Функция Глжеттекслевелпараметерив (GL. h)
description: Функции Глжеттекслевелпараметерфв и Глжеттекслевелпараметерив возвращают значения параметров текстуры для определенного уровня детализации. | Функция Глжеттекслевелпараметерив (GL. h)
ms.assetid: 536d7bc9-1599-47ff-8559-374f96f1d5f3
keywords:
- Функция Глжеттекслевелпараметерив OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0fa167eae842784e967538ff1539e0b43a6a2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000090"
---
# <a name="glgettexlevelparameteriv-function"></a><span data-ttu-id="8e3b0-105">Функция Глжеттекслевелпараметерив</span><span class="sxs-lookup"><span data-stu-id="8e3b0-105">glGetTexLevelParameteriv function</span></span>

<span data-ttu-id="8e3b0-106">Функции [**глжеттекслевелпараметерфв**](glgettexlevelparameterfv.md) и **глжеттекслевелпараметерив** возвращают значения параметров текстуры для определенного уровня детализации.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-106">The [**glGetTexLevelParameterfv**](glgettexlevelparameterfv.md) and **glGetTexLevelParameteriv** functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e3b0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e3b0-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameteriv(
   GLenum target,
   GLint  level,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="8e3b0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e3b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e3b0-109">*target*</span><span class="sxs-lookup"><span data-stu-id="8e3b0-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8e3b0-110">Символьное имя целевой текстуры: " \_ текстура \_ 1Д, \_ 2D, двухмерная текстура, \_ плоская текстура \_ \_ \_ или \_ \_ геотекстура прокси-сервера \_ GL".</span><span class="sxs-lookup"><span data-stu-id="8e3b0-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="8e3b0-111">*level*</span><span class="sxs-lookup"><span data-stu-id="8e3b0-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="8e3b0-112">Номер уровня детализации требуемого изображения.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="8e3b0-113">Уровень 0 является базовым уровнем образа.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-113">Level 0 is the base image level.</span></span> <span data-ttu-id="8e3b0-114">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="8e3b0-115">*pname*</span><span class="sxs-lookup"><span data-stu-id="8e3b0-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="8e3b0-116">Символическое имя параметра текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="8e3b0-117">Принимаются следующие имена параметров.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="8e3b0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8e3b0-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="8e3b0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8e3b0-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="8e3b0-120"><dt>**\_Ширина текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="8e3b0-121">Параметр *params* возвращает одно значение, содержащее ширину изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="8e3b0-122">Это значение включает границу изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="8e3b0-123"><dt>**\_Высота текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="8e3b0-124">Параметр *params* возвращает одно значение, содержащее высоту изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="8e3b0-125">Это значение включает границу изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="8e3b0-126"><dt>**\_ \_ внутренний формат текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="8e3b0-127">Параметр *params* возвращает единственное значение, описывающее формат шаг текселя текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="8e3b0-128"><dt>**\_граница текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="8e3b0-129">Параметр *params* возвращает одно значение: ширину (в пикселях) границы изображения текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="8e3b0-130"><dt>**\_ \_ красный размер текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="8e3b0-131">Внутреннее разрешение хранилища для красного компонента шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="8e3b0-132">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b0-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="8e3b0-133"><dt>**\_ \_ зеленый размер текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="8e3b0-134">Внутреннее разрешение хранилища зеленого компонента шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="8e3b0-135">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b0-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="8e3b0-136"><dt>**\_ \_ синий размер текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="8e3b0-137">Внутреннее разрешение хранилища для синего компонента шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="8e3b0-138">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b0-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="8e3b0-139"><dt>**\_ \_ Размер альфа-канала текстуры GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="8e3b0-140">Внутреннее разрешение хранилища альфа-компонента шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="8e3b0-141">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b0-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="8e3b0-142"><dt>**\_ \_ Размер светимости текстуры GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="8e3b0-143">Внутреннее разрешение хранилища для компонента светимости шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="8e3b0-144">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b0-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="8e3b0-145"><dt>**\_ \_ Размер интенсивности текстуры GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="8e3b0-146">Внутреннее разрешение хранилища компонента интенсивности шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="8e3b0-147">Решение, выбранное OpenGL, будет закрыто для разрешения, запрошенного пользователем с аргументом Component параметра [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b0-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="8e3b0-148"><dt>**\_компоненты текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="8e3b0-149">Параметр *params* возвращает одно значение: количество компонентов в изображении текстуры.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="8e3b0-150">*params*</span><span class="sxs-lookup"><span data-stu-id="8e3b0-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="8e3b0-151">Возвращает запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e3b0-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e3b0-152">Return value</span></span>

<span data-ttu-id="8e3b0-153">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8e3b0-154">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8e3b0-154">Error codes</span></span>

<span data-ttu-id="8e3b0-155">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8e3b0-156">Имя</span><span class="sxs-lookup"><span data-stu-id="8e3b0-156">Name</span></span>                                                                                                  | <span data-ttu-id="8e3b0-157">Значение</span><span class="sxs-lookup"><span data-stu-id="8e3b0-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e3b0-158"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8e3b0-159">значение *Target* или *pname* не было принято.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="8e3b0-160"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8e3b0-161">*уровень* меньше нуля или больше, чем *log* 2 *(max)*, где *Max* — это возвращаемое значение для \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="8e3b0-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="8e3b0-162"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8e3b0-163">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8e3b0-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8e3b0-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e3b0-164">Remarks</span></span>

<span data-ttu-id="8e3b0-165">Функция **глжеттекслевелпараметер** возвращает значение параметра текстуры *params* для определенного уровня детализации, указанного как *Level*.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="8e3b0-166">*Целевой* параметр определяет целевую текстуру: "текстура 1Д, плоский, 2D, текстура, двухмерная, текстура \_ прокси-сервера GL \_ \_ \_ \_ \_ \_ или \_ двухмерная текстура прокси-сервера GL \_ \_ для указания одномерного или двумерного текстурирования.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="8e3b0-167">Параметр *pname* указывает параметр текстуры, значение или значения которого будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="8e3b0-168">Если возникает ошибка, содержимое *параметров* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8e3b0-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e3b0-169">Требования</span><span class="sxs-lookup"><span data-stu-id="8e3b0-169">Requirements</span></span>



| <span data-ttu-id="8e3b0-170">Требование</span><span class="sxs-lookup"><span data-stu-id="8e3b0-170">Requirement</span></span> | <span data-ttu-id="8e3b0-171">Значение</span><span class="sxs-lookup"><span data-stu-id="8e3b0-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3b0-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e3b0-172">Minimum supported client</span></span><br/> | <span data-ttu-id="8e3b0-173">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8e3b0-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8e3b0-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e3b0-174">Minimum supported server</span></span><br/> | <span data-ttu-id="8e3b0-175">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8e3b0-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8e3b0-176">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8e3b0-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e3b0-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8e3b0-178">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e3b0-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="8e3b0-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8e3b0-180">DLL</span><span class="sxs-lookup"><span data-stu-id="8e3b0-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e3b0-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e3b0-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e3b0-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e3b0-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3b0-183">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="8e3b0-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8e3b0-184">**гленд**</span><span class="sxs-lookup"><span data-stu-id="8e3b0-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8e3b0-185">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="8e3b0-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="8e3b0-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8e3b0-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8e3b0-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8e3b0-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8e3b0-188">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="8e3b0-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





