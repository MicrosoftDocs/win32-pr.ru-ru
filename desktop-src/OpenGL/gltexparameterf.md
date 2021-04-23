---
title: Функция Глтекспараметерф (GL. h)
description: Задает параметры текстуры. | Функция Глтекспараметерф (GL. h)
ms.assetid: 20b9f2d5-66e1-41cd-9571-8caa38ef033d
keywords:
- Функция Глтекспараметерф OpenGL
topic_type:
- apiref
api_name:
- glTexParameterf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f749513757ee32f6fe468dadbe968b8657a06f3d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684888"
---
# <a name="gltexparameterf-function"></a><span data-ttu-id="878f3-105">Функция Глтекспараметерф</span><span class="sxs-lookup"><span data-stu-id="878f3-105">glTexParameterf function</span></span>

<span data-ttu-id="878f3-106">Задает параметры текстуры.</span><span class="sxs-lookup"><span data-stu-id="878f3-106">Sets texture parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="878f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="878f3-107">Syntax</span></span>


```C++
void WINAPI glTexParameterf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="878f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="878f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="878f3-109">*target*</span><span class="sxs-lookup"><span data-stu-id="878f3-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="878f3-110">Целевая текстура, которая должна быть либо \_ 2D-текстурой \_ 1d, либо \_ плоской текстурой GL \_ .</span><span class="sxs-lookup"><span data-stu-id="878f3-110">The target texture, which must be either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="878f3-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="878f3-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="878f3-112">Символическое имя параметра текстуры с одним значением.</span><span class="sxs-lookup"><span data-stu-id="878f3-112">The symbolic name of a single valued texture parameter.</span></span> <span data-ttu-id="878f3-113">Следующие символы принимаются в *pname*.</span><span class="sxs-lookup"><span data-stu-id="878f3-113">The following symbols are accepted in *pname*.</span></span>



| <span data-ttu-id="878f3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="878f3-114">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="878f3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="878f3-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="878f3-116"><dt>**\_ \_ Фильтр min текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-116"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="878f3-117">Функция текстуры Минификация используется каждый раз, когда пиксел, на который выполняется текстурирование, сопоставляется с областью больше одного элемента текстуры.</span><span class="sxs-lookup"><span data-stu-id="878f3-117">The texture minifying function is used whenever the pixel being textured maps to an area greater than one texture element.</span></span> <span data-ttu-id="878f3-118">Существует шесть определенных функций Минификация.</span><span class="sxs-lookup"><span data-stu-id="878f3-118">There are six defined minifying functions.</span></span> <span data-ttu-id="878f3-119">Два из них используют ближайший один или ближайшие четыре элемента текстуры для расчета значения текстуры.</span><span class="sxs-lookup"><span data-stu-id="878f3-119">Two of them use the nearest one or nearest four texture elements to compute the texture value.</span></span> <span data-ttu-id="878f3-120">Другие четыре MIP-карты использования.</span><span class="sxs-lookup"><span data-stu-id="878f3-120">The other four use mipmaps.</span></span><br/> <span data-ttu-id="878f3-121">Mipmap — это упорядоченный набор массивов, представляющий одно и то же изображение при постепенном понижении разрешений.</span><span class="sxs-lookup"><span data-stu-id="878f3-121">A mipmap is an ordered set of arrays representing the same image at progressively lower resolutions.</span></span> <span data-ttu-id="878f3-122">Если текстура имеет измерения 2nx2<sup>m</sup> , то есть максимум (n, m) + 1 MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="878f3-122">If the texture has dimensions 2nx2<sup>m</sup> there are max(n, m) + 1 mipmaps.</span></span> <span data-ttu-id="878f3-123">Первый mipmap — исходная текстура с измерениями 2nx2<sup>m</sup>.</span><span class="sxs-lookup"><span data-stu-id="878f3-123">The first mipmap is the original texture, with dimensions 2nx2<sup>m</sup>.</span></span> <span data-ttu-id="878f3-124">Каждый последующий mipmap имеет измерения 2<sup>k</sup>1 экземпляр 2<sup>l</sup>1, где 2<sup>k</sup>x2<sup>l</sup> — это размеры предыдущего mipmap, до тех пор, пока k = 0 или l = 0.</span><span class="sxs-lookup"><span data-stu-id="878f3-124">Each subsequent mipmap has dimensions 2<sup>k</sup>1x2<sup>l</sup>1 where 2<sup>k</sup>x2<sup>l</sup> are the dimensions of the previous mipmap, until either k = 0 or l = 0.</span></span> <span data-ttu-id="878f3-125">В этот момент последующие MIP-карты имеют измерение 1 экземпляр 2<sup>l</sup>1 или 2<sup>k</sup>1x1 до окончательного mipmap, который имеет 1x1 измерения.</span><span class="sxs-lookup"><span data-stu-id="878f3-125">At that point, subsequent mipmaps have dimension 1x2<sup>l</sup>1 or 2<sup>k</sup>1x1 until the final mipmap, which has dimension 1x1.</span></span> <span data-ttu-id="878f3-126">MIP-карты определяются с помощью [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md) с аргументом уровня детализации, указывающим порядок MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="878f3-126">Mipmaps are defined using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md) with the level-of-detail argument indicating the order of the mipmaps.</span></span> <span data-ttu-id="878f3-127">Уровень 0 является исходной текстурой; полужирный максимальный уровень (n, m) является окончательным 1x1 mipmap.</span><span class="sxs-lookup"><span data-stu-id="878f3-127">Level 0 is the original texture; level bold max(n, m) is the final 1x1 mipmap.</span></span><br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="878f3-128"><dt>**\_ \_ Фильтр MAG текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-128"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="878f3-129">Функция увеличения текстуры используется, когда пиксел, на который выполняется текстурирование, соответствует области, меньшей или равной одному элементу текстуры.</span><span class="sxs-lookup"><span data-stu-id="878f3-129">The texture magnification function is used when the pixel being textured maps to an area less than or equal to one texture element.</span></span> <span data-ttu-id="878f3-130">Он задает для функции увеличения текстуры значение " \_ Ближайшая к главной или" \_ линейная.</span><span class="sxs-lookup"><span data-stu-id="878f3-130">It sets the texture magnification function to either GL\_NEAREST or GL\_LINEAR.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="878f3-131"><dt>**\_Перенос текстуры в ГК \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-131"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>             | <span data-ttu-id="878f3-132">Задает параметр переноса для координаты текстуры s в значение GL \_ или GL \_ .</span><span class="sxs-lookup"><span data-stu-id="878f3-132">Sets the wrap parameter for texture coordinate s to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="878f3-133">\_Срез GL приводит к тому, что координаты s заменяются на диапазон \[ 0, 1 \] и удобно использовать для предотвращения упаковки артефактов при сопоставлении одного изображения с объектом.</span><span class="sxs-lookup"><span data-stu-id="878f3-133">GL\_CLAMP causes s coordinates to be clamped to the range \[0,1\] and is useful for preventing wrapping artifacts when mapping a single image onto an object.</span></span> <span data-ttu-id="878f3-134">При выполнении операции ГК \_ Repeat целая часть координаты s не учитывается. OpenGL использует только дробную часть, тем самым создавая Повторяющийся шаблон.</span><span class="sxs-lookup"><span data-stu-id="878f3-134">GL\_REPEAT causes the integer part of the s coordinate to be ignored; OpenGL uses only the fractional part, thereby creating a repeating pattern.</span></span> <span data-ttu-id="878f3-135">Доступ к элементам текстур границ осуществляется только в том случае, если для переноса задано значение «GL \_ ».</span><span class="sxs-lookup"><span data-stu-id="878f3-135">Border texture elements are accessed only if wrapping is set to GL\_CLAMP.</span></span> <span data-ttu-id="878f3-136">Изначально \_ \_ для параметра "создать оболочку текстуры GL" \_ задано значение GL \_ Repeat.</span><span class="sxs-lookup"><span data-stu-id="878f3-136">Initially, GL\_TEXTURE\_WRAP\_S is set to GL\_REPEAT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="878f3-137"><dt>**\_Обтекание текстуры GL \_ \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-137"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>             | <span data-ttu-id="878f3-138">Устанавливает параметр переноса для координаты текстуры t в значение GL \_ или GL \_ .</span><span class="sxs-lookup"><span data-stu-id="878f3-138">Sets the wrap parameter for texture coordinate t to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="878f3-139">См. обсуждение в разделе \_ Перенос текстуры в ГК \_ \_ S.</span><span class="sxs-lookup"><span data-stu-id="878f3-139">See the discussion under GL\_TEXTURE\_WRAP\_S.</span></span> <span data-ttu-id="878f3-140">Изначально \_ \_ \_ для параметра T текстуры GL задано значение GL \_ Repeat.</span><span class="sxs-lookup"><span data-stu-id="878f3-140">Initially, GL\_TEXTURE\_WRAP\_T is set to GL\_REPEAT</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="878f3-141">*param*</span><span class="sxs-lookup"><span data-stu-id="878f3-141">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="878f3-142">Значение *pname*.</span><span class="sxs-lookup"><span data-stu-id="878f3-142">The value of *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="878f3-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="878f3-143">Return value</span></span>

<span data-ttu-id="878f3-144">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="878f3-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="878f3-145">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="878f3-145">Error codes</span></span>

<span data-ttu-id="878f3-146">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="878f3-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="878f3-147">Имя</span><span class="sxs-lookup"><span data-stu-id="878f3-147">Name</span></span>                                                                                                  | <span data-ttu-id="878f3-148">Значение</span><span class="sxs-lookup"><span data-stu-id="878f3-148">Meaning</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="878f3-149"><dt>**GL \_ НЕДОПУСТИМое \_ перечисление**</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-149"><dt>**GL\_INVALID\_ENUM** </dt></span></span> </dl>     | <span data-ttu-id="878f3-150">*Target* или *pname* не является одним из принятых значений, или если *параметр param* должен иметь определенное константное значение (на основе значения *pname*) и не было.</span><span class="sxs-lookup"><span data-stu-id="878f3-150">*target* or *pname* was not one of the accepted defined values, or when *param* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="878f3-151"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="878f3-152">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="878f3-152">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="878f3-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="878f3-153">Remarks</span></span>

<span data-ttu-id="878f3-154">Сопоставление текстур — это метод, который применяет изображение к поверхности объекта, как если бы изображение было декал или целлофане сжимать.</span><span class="sxs-lookup"><span data-stu-id="878f3-154">Texture mapping is a technique that applies an image onto an object's surface as if the image were a decal or cellophane shrink-wrap.</span></span> <span data-ttu-id="878f3-155">Изображение создается в пространстве текстуры с помощью системы координат (*s*, *t*).</span><span class="sxs-lookup"><span data-stu-id="878f3-155">The image is created in texture space, with an (*s*, *t*) coordinate system.</span></span> <span data-ttu-id="878f3-156">Текстура — это одно-или двухмерный изображение и набор параметров, определяющих, как выводятся образцы из изображения.</span><span class="sxs-lookup"><span data-stu-id="878f3-156">A texture is a one- or two-dimensional image and a set of parameters that determine how samples are derived from the image.</span></span>

<span data-ttu-id="878f3-157">Функция **глтекспараметер** присваивает значение или значения в параметрах текстуры указанному в качестве pname.</span><span class="sxs-lookup"><span data-stu-id="878f3-157">The **glTexParameter** function assigns the value or values in params to the texture parameter specified as pname.</span></span> <span data-ttu-id="878f3-158">Целевой параметр определяет целевую текстуру, либо \_ 2D-текстура \_ 1d, либо \_ ДВУХМЕРНАЯ текстура GL \_ .</span><span class="sxs-lookup"><span data-stu-id="878f3-158">The target parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="878f3-159">По мере того как в процессе минификации будет вычислено больше элементов текстуры, будут очевидны и менее артефакты для присвоения псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="878f3-159">As more texture elements are sampled in the minification process, fewer aliasing artifacts will be apparent.</span></span> <span data-ttu-id="878f3-160">Хотя функции, \_ присоединяемые к главной и главной \_ линейной минификации, могут быть быстрее, чем остальные четыре, они задают только один или четыре элемента текстуры для определения значения текстуры отображаемого пикселя и могут формировать моире или неоднородные переходы.</span><span class="sxs-lookup"><span data-stu-id="878f3-160">While the GL\_NEAREST and GL\_LINEAR minification functions can be faster than the other four, they sample only one or four texture elements to determine the texture value of the pixel being rendered and can produce moire patterns or ragged transitions.</span></span> <span data-ttu-id="878f3-161">Значение по умолчанию для \_ фильтра min для текстуры GL \_ \_ — это \_ Ближайшая к \_ mipmap \_ Линейная шкала.</span><span class="sxs-lookup"><span data-stu-id="878f3-161">The default value of GL\_TEXTURE\_MIN\_FILTER is GL\_NEAREST\_MIPMAP\_LINEAR.</span></span>

<span data-ttu-id="878f3-162">Предположим, что текстурирование включено (путем вызова [**гленабле**](glenable.md) с аргументом GL \_ текстуры \_ 1d или \_ двухмерной текстурой GL \_ ), а \_ для фильтра "min текстур ГК \_ \_ " задана одна из функций, требующих mipmap.</span><span class="sxs-lookup"><span data-stu-id="878f3-162">Suppose that texturing is enabled (by calling [**glEnable**](glenable.md) with argument GL\_TEXTURE\_1D or GL\_TEXTURE\_2D) and GL\_TEXTURE\_MIN\_FILTER is set to one of the functions that requires a mipmap.</span></span> <span data-ttu-id="878f3-163">Если размеры изображений текстуры, определенных в данный момент (с предыдущими вызовами [**glTexImage1D**](glteximage1d.md) или [**glTexImage2D**](glteximage2d.md)), не соответствуют правильной последовательности для MIP-карты или меньше изображений текстуры, чем требуется, или набор изображений текстуры имеет разное количество компонентов текстуры, то это так, как если бы сопоставление текстур было отключено.</span><span class="sxs-lookup"><span data-stu-id="878f3-163">If either the dimensions of the texture images currently defined (with previous calls to [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md)) do not follow the proper sequence for mipmaps, or there are fewer texture images defined than are needed, or the set of texture images have differing numbers of texture components, then it is as if texture mapping were disabled.</span></span> <span data-ttu-id="878f3-164">Линейная фильтрация обращается к четырем ближайшим элементам текстуры только в двумерной текстуре.</span><span class="sxs-lookup"><span data-stu-id="878f3-164">Linear filtering accesses the four nearest texture elements only in 2-D textures.</span></span> <span data-ttu-id="878f3-165">В 1-D текстурах Линейная фильтрация обращается к двум ближайшим элементам текстуры.</span><span class="sxs-lookup"><span data-stu-id="878f3-165">In 1-D textures, linear filtering accesses the two nearest texture elements.</span></span> <span data-ttu-id="878f3-166">Следующая функция получает сведения, связанные с **глтекспараметерф**, **глтекспараметери**, **глтекспараметерфв** и **глтекспараметерив**.</span><span class="sxs-lookup"><span data-stu-id="878f3-166">The following function retrieves information related to **glTexParameterf**, **glTexParameteri**, **glTexParameterfv**, and **glTexParameteriv**.</span></span>

## <a name="requirements"></a><span data-ttu-id="878f3-167">Требования</span><span class="sxs-lookup"><span data-stu-id="878f3-167">Requirements</span></span>



| <span data-ttu-id="878f3-168">Требование</span><span class="sxs-lookup"><span data-stu-id="878f3-168">Requirement</span></span> | <span data-ttu-id="878f3-169">Значение</span><span class="sxs-lookup"><span data-stu-id="878f3-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="878f3-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="878f3-170">Minimum supported client</span></span><br/> | <span data-ttu-id="878f3-171">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="878f3-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="878f3-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="878f3-172">Minimum supported server</span></span><br/> | <span data-ttu-id="878f3-173">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="878f3-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="878f3-174">Заголовок</span><span class="sxs-lookup"><span data-stu-id="878f3-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="878f3-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="878f3-176">Библиотека</span><span class="sxs-lookup"><span data-stu-id="878f3-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="878f3-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="878f3-178">DLL</span><span class="sxs-lookup"><span data-stu-id="878f3-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="878f3-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="878f3-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="878f3-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="878f3-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="878f3-181">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="878f3-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="878f3-182">**глбиндтекстуре**</span><span class="sxs-lookup"><span data-stu-id="878f3-182">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="878f3-183">**глкопипикселс**</span><span class="sxs-lookup"><span data-stu-id="878f3-183">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="878f3-184">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="878f3-184">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="878f3-185">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="878f3-185">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="878f3-186">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="878f3-186">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="878f3-187">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="878f3-187">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="878f3-188">**гленд**</span><span class="sxs-lookup"><span data-stu-id="878f3-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="878f3-189">**глжеттекспараметер**</span><span class="sxs-lookup"><span data-stu-id="878f3-189">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="878f3-190">**глпикселсторе**</span><span class="sxs-lookup"><span data-stu-id="878f3-190">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="878f3-191">**глпикселтрансфер**</span><span class="sxs-lookup"><span data-stu-id="878f3-191">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="878f3-192">**глприоритизетекстурес**</span><span class="sxs-lookup"><span data-stu-id="878f3-192">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="878f3-193">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="878f3-193">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="878f3-194">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="878f3-194">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="878f3-195">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="878f3-195">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="878f3-196">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="878f3-196">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="878f3-197">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="878f3-197">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="878f3-198">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="878f3-198">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





