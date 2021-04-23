---
title: Функция Глжеттексимаже (GL. h)
description: Функция Глжеттексимаже возвращает изображение текстуры.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- Функция Глжеттексимаже OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661977"
---
# <a name="glgetteximage-function"></a><span data-ttu-id="74eda-104">Функция Глжеттексимаже</span><span class="sxs-lookup"><span data-stu-id="74eda-104">glGetTexImage function</span></span>

<span data-ttu-id="74eda-105">Функция **глжеттексимаже** возвращает изображение текстуры.</span><span class="sxs-lookup"><span data-stu-id="74eda-105">The **glGetTexImage** function returns a texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="74eda-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74eda-106">Syntax</span></span>


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="74eda-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="74eda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74eda-108">*target*</span><span class="sxs-lookup"><span data-stu-id="74eda-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="74eda-109">Указывает, какая текстура должна быть получена.</span><span class="sxs-lookup"><span data-stu-id="74eda-109">Specifies which texture is to be obtained.</span></span> <span data-ttu-id="74eda-110">\_ \_ Принимаются текстуры GL 1d \_ и \_ 2D текстуры GL.</span><span class="sxs-lookup"><span data-stu-id="74eda-110">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="74eda-111">*level*</span><span class="sxs-lookup"><span data-stu-id="74eda-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="74eda-112">Номер уровня детализации требуемого изображения.</span><span class="sxs-lookup"><span data-stu-id="74eda-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="74eda-113">Уровень 0 является базовым уровнем образа.</span><span class="sxs-lookup"><span data-stu-id="74eda-113">Level 0 is the base image level.</span></span> <span data-ttu-id="74eda-114">Уровень *n* — это *n*-ое изображение для сокращения mipmap.</span><span class="sxs-lookup"><span data-stu-id="74eda-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="74eda-115">*format*</span><span class="sxs-lookup"><span data-stu-id="74eda-115">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="74eda-116">Формат пикселей для возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="74eda-116">A pixel format for the returned data.</span></span> <span data-ttu-id="74eda-117">Поддерживаются форматы "красный", "Зеленая", "зеленый", "синий", "Красная", "GL", "GL", "красное", "GL", "GL", "BGR", "Расш \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="74eda-117">The supported formats are GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_LUMINANCE, GL\_BGR\_EXT, GL\_BGRA\_EXT, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="74eda-118">*type*</span><span class="sxs-lookup"><span data-stu-id="74eda-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="74eda-119">Тип пикселя для возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="74eda-119">A pixel type for the returned data.</span></span> <span data-ttu-id="74eda-120">Поддерживаются следующие типы: \_ Byte без знака \_ , байт ГК \_ , формат GL \_ без знака \_ Short, ГК \_ Short, GL \_ без знака \_ типа int, GL \_ и тип \_ float.</span><span class="sxs-lookup"><span data-stu-id="74eda-120">The supported types are GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="74eda-121">*зависим*</span><span class="sxs-lookup"><span data-stu-id="74eda-121">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="74eda-122">Возвращает изображение текстуры.</span><span class="sxs-lookup"><span data-stu-id="74eda-122">Returns the texture image.</span></span> <span data-ttu-id="74eda-123">Должен быть указателем на массив типа, указанного в *типе*.</span><span class="sxs-lookup"><span data-stu-id="74eda-123">Should be a pointer to an array of the type specified by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74eda-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74eda-124">Return value</span></span>

<span data-ttu-id="74eda-125">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="74eda-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74eda-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="74eda-126">Error codes</span></span>

<span data-ttu-id="74eda-127">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="74eda-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="74eda-128">Имя</span><span class="sxs-lookup"><span data-stu-id="74eda-128">Name</span></span>                                                                                                  | <span data-ttu-id="74eda-129">Значение</span><span class="sxs-lookup"><span data-stu-id="74eda-129">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74eda-130"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="74eda-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="74eda-131">*целевой объект*, *Формат* или *тип* не являются допустимыми значениями.</span><span class="sxs-lookup"><span data-stu-id="74eda-131">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="74eda-132"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="74eda-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="74eda-133">*уровень* меньше нуля или больше, чем *log* 2 (*Max*), где *Max* — это возвращаемое значение для \_ максимального \_ размера текстуры GL \_ .</span><span class="sxs-lookup"><span data-stu-id="74eda-133">*level* is less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="74eda-134"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="74eda-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="74eda-135">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="74eda-135">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) .</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="74eda-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74eda-136">Remarks</span></span>

<span data-ttu-id="74eda-137">Функция **глжеттексимаже** возвращает изображение текстуры в *Пиксели*.</span><span class="sxs-lookup"><span data-stu-id="74eda-137">The **glGetTexImage** function returns a texture image into *pixels*.</span></span> <span data-ttu-id="74eda-138">Параметр *Target* указывает, является ли требуемое изображение текстуры единицей, заданным [**glTexImage1D**](glteximage1d.md)**(** \_ \_ плоская текстура 1d **)** или [**glTexImage2D**](glteximage2d.md)**(** \_ 2D-текстура GL \_ **)**.</span><span class="sxs-lookup"><span data-stu-id="74eda-138">The *target* parameter specifies whether the desired texture image is one specified by [**glTexImage1D**](glteximage1d.md)**(** GL\_TEXTURE\_1D **)** or by [**glTexImage2D**](glteximage2d.md)**(** GL\_TEXTURE\_2D **)**.</span></span> <span data-ttu-id="74eda-139">Параметр *Level* задает номер уровня детализации требуемого изображения.</span><span class="sxs-lookup"><span data-stu-id="74eda-139">The *level* parameter specifies the level-of-detail number of the desired image.</span></span> <span data-ttu-id="74eda-140">Параметры *Format* и *Type* определяют формат и тип нужного массива изображений.</span><span class="sxs-lookup"><span data-stu-id="74eda-140">The *format* and *type* parameters specify the format and type of the desired image array.</span></span> <span data-ttu-id="74eda-141">Описание допустимых значений параметров *Format* и *Type* соответственно см. в разделе **glTexImage1D** and [**глдравпикселс**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="74eda-141">For a description of the acceptable values for the *format* and *type* parameters, respectively, see **glTexImage1D** and [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="74eda-142">Операция **глжеттексимаже** лучше понять, учитывая, что выбранный внутренний рисунок с четырьмя компонентами является буфером цвета RGBA, размером изображения.</span><span class="sxs-lookup"><span data-stu-id="74eda-142">Operation of **glGetTexImage** is best understood by considering the selected internal four-component texture image to be an RGBA color buffer the size of the image.</span></span> <span data-ttu-id="74eda-143">Семантика **глжеттексимаже** затем идентична методу [**глреадпикселс**](glreadpixels.md) , вызываемому с тем же *форматом* и *типом*, если для *x* и *y* установлено нулевое значение, *Ширина* устанавливается в ширину изображения текстуры (включая границу, если она была указана), а *Высота* — на одну для одномерного изображения или на высоту изображения текстуры (включая границу, если она была указана) для 2-d изображений.</span><span class="sxs-lookup"><span data-stu-id="74eda-143">The semantics of **glGetTexImage** are then identical to those of [**glReadPixels**](glreadpixels.md) called with the same *format* and *type*, with *x* and *y* set to zero, *width* set to the width of the texture image (including border if one was specified), and *height* set to one for 1-D images, or to the height of the texture image (including border, if one was specified) for 2-D images.</span></span>

<span data-ttu-id="74eda-144">Так как внутреннее изображение текстуры является изображением RGBA, форматы пикселей, индекс \_ цвета GL \_ , \_ индекс трафарета GL \_ и \_ компонент глубины GL не \_ принимаются, а \_ точечный рисунок GL не принимается.</span><span class="sxs-lookup"><span data-stu-id="74eda-144">Because the internal texture image is an RGBA image, pixel formats GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, and GL\_DEPTH\_COMPONENT are not accepted, and pixel type GL\_BITMAP is not accepted.</span></span>

<span data-ttu-id="74eda-145">Если выбранное изображение текстуры не содержит четырех компонентов, применяются следующие сопоставления.</span><span class="sxs-lookup"><span data-stu-id="74eda-145">If the selected texture image does not contain four components, the following mappings are applied.</span></span> <span data-ttu-id="74eda-146">Текстуры с одним компонентом обрабатываются как буферы RGBA, для которых красный цвет установлен в значение одного компонента, а зеленый, синий и альфа-канал устанавливается в ноль.</span><span class="sxs-lookup"><span data-stu-id="74eda-146">Single-component textures are treated as RGBA buffers with red set to the single-component value, and green, blue, and alpha set to zero.</span></span>

<span data-ttu-id="74eda-147">Текстуры двух компонентов обрабатываются как буферы RGBA, при этом красным параметрам присвоено значение 0, альфа-каналу — значение первого компонента, а зеленому и синему — нуль.</span><span class="sxs-lookup"><span data-stu-id="74eda-147">Two-component textures are treated as RGBA buffers, with red set to the value of component zero, alpha set to the value of component one, and green and blue set to zero.</span></span> <span data-ttu-id="74eda-148">Наконец, текстуры с тремя компонентами обрабатываются как буферы RGBA, для которых Red установлено значение 0, зеленый — на компонент, синий — на компонент 2, а альфа-канал — нуль.</span><span class="sxs-lookup"><span data-stu-id="74eda-148">Finally, three-component textures are treated as RGBA buffers with red set to component zero, green set to component one, blue set to component two, and alpha set to zero.</span></span>

<span data-ttu-id="74eda-149">Чтобы определить требуемый размер *пикселей*, используйте [**глжеттекслевелпараметер**](glgettexlevelparameter.md) для определения размеров изображения внутренней текстуры, а затем увеличьте требуемое количество пикселей по объему хранилища, требуемого для каждого пикселя, в зависимости от *формата* и *типа*.</span><span class="sxs-lookup"><span data-stu-id="74eda-149">To determine the required size of *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) to ascertain the dimensions of the internal texture image, and then scale the required number of pixels by the storage required for each pixel, based on *format* and *type*.</span></span> <span data-ttu-id="74eda-150">Не забудьте принять в учетную запись параметры хранения пикселов, особенно \_ Выравнивание по пакету GL \_ .</span><span class="sxs-lookup"><span data-stu-id="74eda-150">Be sure to take the pixel-storage parameters into account, especially GL\_PACK\_ALIGNMENT.</span></span>

<span data-ttu-id="74eda-151">Если возникает ошибка, содержимое *пикселей* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="74eda-151">If an error is generated, no change is made to the contents of *pixels*.</span></span>

<span data-ttu-id="74eda-152">Следующие функции извлекают сведения, относящиеся к **глжеттексимаже**:</span><span class="sxs-lookup"><span data-stu-id="74eda-152">The following functions retrieve information related to **glGetTexImage**:</span></span>

<span data-ttu-id="74eda-153">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ Выравнивание по пакету GL \_ и другие</span><span class="sxs-lookup"><span data-stu-id="74eda-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PACK\_ALIGNMENT and others</span></span>

<span data-ttu-id="74eda-154">[**глжеттекслевелпараметер**](glgettexlevelparameter.md) с аргументом \_ Ширина текстуры GL \_</span><span class="sxs-lookup"><span data-stu-id="74eda-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) with argument GL\_TEXTURE\_WIDTH</span></span>

<span data-ttu-id="74eda-155">**глжеттекслевелпараметер** с аргументом " \_ Высота текстуры GL" \_</span><span class="sxs-lookup"><span data-stu-id="74eda-155">**glGetTexLevelParameter** with argument GL\_TEXTURE\_HEIGHT</span></span>

<span data-ttu-id="74eda-156">**глжеттекслевелпараметер** с аргументом \_ border текстуры GL \_</span><span class="sxs-lookup"><span data-stu-id="74eda-156">**glGetTexLevelParameter** with argument GL\_TEXTURE\_BORDER</span></span>

<span data-ttu-id="74eda-157">**глжеттекслевелпараметер** с аргументом " \_ компоненты текстуры GL" \_</span><span class="sxs-lookup"><span data-stu-id="74eda-157">**glGetTexLevelParameter** with argument GL\_TEXTURE\_COMPONENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="74eda-158">Требования</span><span class="sxs-lookup"><span data-stu-id="74eda-158">Requirements</span></span>



| <span data-ttu-id="74eda-159">Требование</span><span class="sxs-lookup"><span data-stu-id="74eda-159">Requirement</span></span> | <span data-ttu-id="74eda-160">Значение</span><span class="sxs-lookup"><span data-stu-id="74eda-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74eda-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74eda-161">Minimum supported client</span></span><br/> | <span data-ttu-id="74eda-162">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74eda-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="74eda-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74eda-163">Minimum supported server</span></span><br/> | <span data-ttu-id="74eda-164">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74eda-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74eda-165">Заголовок</span><span class="sxs-lookup"><span data-stu-id="74eda-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="74eda-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="74eda-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="74eda-167">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74eda-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="74eda-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74eda-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="74eda-169">DLL</span><span class="sxs-lookup"><span data-stu-id="74eda-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74eda-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74eda-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74eda-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74eda-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74eda-172">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="74eda-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="74eda-173">**глдравпикселс**</span><span class="sxs-lookup"><span data-stu-id="74eda-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="74eda-174">**гленд**</span><span class="sxs-lookup"><span data-stu-id="74eda-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="74eda-175">**глжеттекслевелпараметер**</span><span class="sxs-lookup"><span data-stu-id="74eda-175">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="74eda-176">**глреадпикселс**</span><span class="sxs-lookup"><span data-stu-id="74eda-176">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="74eda-177">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="74eda-177">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="74eda-178">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="74eda-178">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





