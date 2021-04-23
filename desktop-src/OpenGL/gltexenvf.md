---
title: Функция Глтексенвф (GL. h)
description: Функция Глтексенвф задает параметр среды текстуры.
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- Функция Глтексенвф OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1566378b6dcd2f91a2e2cd445f0ec39c0f6f6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801996"
---
# <a name="gltexenvf-function"></a><span data-ttu-id="47978-104">Функция Глтексенвф</span><span class="sxs-lookup"><span data-stu-id="47978-104">glTexEnvf function</span></span>

<span data-ttu-id="47978-105">Функция **глтексенвф** задает параметр среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="47978-105">The **glTexEnvf** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="47978-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47978-106">Syntax</span></span>


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="47978-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="47978-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47978-108">*target*</span><span class="sxs-lookup"><span data-stu-id="47978-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="47978-109">Среда текстуры.</span><span class="sxs-lookup"><span data-stu-id="47978-109">A texture environment.</span></span> <span data-ttu-id="47978-110">Должна быть текстура GL в виде \_ \_ env.</span><span class="sxs-lookup"><span data-stu-id="47978-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="47978-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="47978-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="47978-112">Символьное имя однозначного параметра среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="47978-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="47978-113">Необходимо использовать \_ режим GL текстуры \_ env \_ .</span><span class="sxs-lookup"><span data-stu-id="47978-113">Must be GL\_TEXTURE\_ENV\_MODE.</span></span>

</dd> <dt>

<span data-ttu-id="47978-114">*param*</span><span class="sxs-lookup"><span data-stu-id="47978-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="47978-115">Одна символьная константа, одна из них: GL, GL \_ \_ ДЕКАЛ, GL \_ Blend или GL \_ .</span><span class="sxs-lookup"><span data-stu-id="47978-115">A single symbolic constant, one of GL\_MODULATE, GL\_DECAL, GL\_BLEND, or GL\_REPLACE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47978-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47978-116">Return value</span></span>

<span data-ttu-id="47978-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="47978-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="47978-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="47978-118">Error codes</span></span>

<span data-ttu-id="47978-119">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="47978-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="47978-120">Имя</span><span class="sxs-lookup"><span data-stu-id="47978-120">Name</span></span>                                                                                                  | <span data-ttu-id="47978-121">Значение</span><span class="sxs-lookup"><span data-stu-id="47978-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47978-122"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="47978-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="47978-123">*Target* или *pname* не является одним из принятых значений, или если *Параметры* должны иметь определенное константное значение (на основе значения *pname*) и не было.</span><span class="sxs-lookup"><span data-stu-id="47978-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="47978-124"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="47978-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="47978-125">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="47978-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="47978-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47978-126">Remarks</span></span>

<span data-ttu-id="47978-127">В среде текстуры указывается способ интерпретации значений текстур при текстурировании фрагмента.</span><span class="sxs-lookup"><span data-stu-id="47978-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="47978-128">*Целевой* параметр должен иметь значение GL \_ текстуры \_ env.</span><span class="sxs-lookup"><span data-stu-id="47978-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="47978-129">Параметр *pname* имеет режим GL \_ текстуры \_ env \_ .</span><span class="sxs-lookup"><span data-stu-id="47978-129">The *pname* parameter is GL\_TEXTURE\_ENV\_MODE.</span></span> <span data-ttu-id="47978-130">Определены три функции текстуры: GL для \_ модуляции, GL \_ ДЕКАЛ и GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="47978-130">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="47978-131">Функция текстуры работает с фрагментом, используя значение изображения текстуры, которое применяется к фрагменту (см. [**глтекспараметер**](gltexparameter-functions.md)) и создает для этого фрагмента цвет RGBA.</span><span class="sxs-lookup"><span data-stu-id="47978-131">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="47978-132">В следующей таблице показано, как создается цвет RGBA для каждой из трех функций текстуры, которые можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="47978-132">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="47978-133">*C* — это тройной цвет значений (RGB), *а —* связанное альфа-значение.</span><span class="sxs-lookup"><span data-stu-id="47978-133">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="47978-134">Значения RGBA, извлеченные из изображения текстуры, находятся в диапазоне \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="47978-134">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="47978-135">Индекс *f* относится к входящему фрагменту, индексу *t* к изображению текстуры, индексу *c* на цветовую среду текстуры, а индекс *v* — значению, созданному функцией текстуры.</span><span class="sxs-lookup"><span data-stu-id="47978-135">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="47978-136">Изображение текстуры может содержать до четырех компонентов на элемент текстуры (см. раздел [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="47978-136">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="47978-137">В образе с одним компонентом lt указывает на один компонент.</span><span class="sxs-lookup"><span data-stu-id="47978-137">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="47978-138">В образе с двумя компонентами используется *L?*</span><span class="sxs-lookup"><span data-stu-id="47978-138">A two-component image uses *L?*</span></span>  <span data-ttu-id="47978-139">и *?*</span><span class="sxs-lookup"><span data-stu-id="47978-139">and *A?*</span></span> <span data-ttu-id="47978-140">.</span><span class="sxs-lookup"><span data-stu-id="47978-140">.</span></span> <span data-ttu-id="47978-141">Изображение из трех компонентов имеет только значение цвета, *C?*</span><span class="sxs-lookup"><span data-stu-id="47978-141">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="47978-142">.</span><span class="sxs-lookup"><span data-stu-id="47978-142">.</span></span> <span data-ttu-id="47978-143">Образ из четырех компонентов имеет значение цвета *C?*</span><span class="sxs-lookup"><span data-stu-id="47978-143">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="47978-144">и альфа-значение *A?*</span><span class="sxs-lookup"><span data-stu-id="47978-144">and an alpha value *A?*</span></span> <span data-ttu-id="47978-145">.</span><span class="sxs-lookup"><span data-stu-id="47978-145">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="47978-146">Число компонентов</span><span class="sxs-lookup"><span data-stu-id="47978-146">Number of components</span></span></th>
<th><span data-ttu-id="47978-147">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="47978-147">GL_MODULATE</span></span></th>
<th><span data-ttu-id="47978-148">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="47978-148">GL_DECAL</span></span></th>
<th><span data-ttu-id="47978-149">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="47978-149">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="47978-150">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="47978-150">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="47978-151"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="47978-151"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="47978-152"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="47978-152"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="47978-153">не определено $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="47978-153">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="47978-154"><em>C</em> <em><sub>v</sub></em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="47978-154"><em>C</em> <em><sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="47978-155"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="47978-155"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="47978-156"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="47978-156"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47978-157"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="47978-157"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="47978-158"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="47978-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="47978-159">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="47978-159">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="47978-160"><em>C<sub>v</sub> </em>  =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="47978-160"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="47978-161"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="47978-161"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="47978-162">не определено $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="47978-162">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="47978-163"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="47978-163"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="47978-164"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="47978-164"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="47978-165"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="47978-165"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47978-166"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="47978-166"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="47978-167"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="47978-167"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="47978-168">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="47978-168">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="47978-169"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="47978-169"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="47978-170"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="47978-170"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="47978-171"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="47978-171"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="47978-172">не определено $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="47978-172">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="47978-173"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="47978-173"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="47978-174"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="47978-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="47978-175">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="47978-175">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="47978-176"><em>C<sub>v</sub> </em>  =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="47978-176"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="47978-177"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="47978-177"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="47978-178"><em>C<sub>v</sub> </em> = (1- <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="47978-178"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="47978-179"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="47978-179"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="47978-180"><em>Ц?</em></span><span class="sxs-lookup"><span data-stu-id="47978-180"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="47978-181">не определено $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="47978-181">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="47978-182"><em>A<sub>v</sub> </em>  =  <em>А?</em></span><span class="sxs-lookup"><span data-stu-id="47978-182"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="47978-183"><em>A<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="47978-183"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="47978-184"><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="47978-184"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="47978-185">\_Режим текстуры в GL \_ \_ по умолчанию имеет значение GL \_ модуляции.</span><span class="sxs-lookup"><span data-stu-id="47978-185">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE.</span></span>

<span data-ttu-id="47978-186">Следующая функция получает сведения, связанные с **глтексенвф**:</span><span class="sxs-lookup"><span data-stu-id="47978-186">The following function retrieves information related to **glTexEnvf**:</span></span>

[<span data-ttu-id="47978-187">**глтексжетенвфв**</span><span class="sxs-lookup"><span data-stu-id="47978-187">**glTexGetEnvfv**</span></span>](glgettexenvfv.md)

## <a name="requirements"></a><span data-ttu-id="47978-188">Требования</span><span class="sxs-lookup"><span data-stu-id="47978-188">Requirements</span></span>



| <span data-ttu-id="47978-189">Требование</span><span class="sxs-lookup"><span data-stu-id="47978-189">Requirement</span></span> | <span data-ttu-id="47978-190">Значение</span><span class="sxs-lookup"><span data-stu-id="47978-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47978-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="47978-191">Minimum supported client</span></span><br/> | <span data-ttu-id="47978-192">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47978-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="47978-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="47978-193">Minimum supported server</span></span><br/> | <span data-ttu-id="47978-194">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="47978-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47978-195">Заголовок</span><span class="sxs-lookup"><span data-stu-id="47978-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="47978-196"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="47978-196"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="47978-197">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47978-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="47978-198"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47978-198"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="47978-199">DLL</span><span class="sxs-lookup"><span data-stu-id="47978-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47978-200"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47978-200"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47978-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47978-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47978-202">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="47978-202">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="47978-203">**гленд**</span><span class="sxs-lookup"><span data-stu-id="47978-203">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="47978-204">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="47978-204">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="47978-205">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="47978-205">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="47978-206">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="47978-206">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





