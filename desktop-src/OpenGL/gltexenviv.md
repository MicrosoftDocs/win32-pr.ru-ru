---
title: Функция Глтексенвив (GL. h)
description: Функция Глтексенвив задает параметр среды текстуры.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- Функция Глтексенвив OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ec232f559e8d4af10369ebe98dd0aea71e36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892741"
---
# <a name="gltexenviv-function"></a><span data-ttu-id="94bde-104">Функция Глтексенвив</span><span class="sxs-lookup"><span data-stu-id="94bde-104">glTexEnviv function</span></span>

<span data-ttu-id="94bde-105">Функция **глтексенвив** задает параметр среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="94bde-105">The **glTexEnviv** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="94bde-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94bde-106">Syntax</span></span>


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="94bde-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="94bde-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94bde-108">*target*</span><span class="sxs-lookup"><span data-stu-id="94bde-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="94bde-109">Среда текстуры.</span><span class="sxs-lookup"><span data-stu-id="94bde-109">A texture environment.</span></span> <span data-ttu-id="94bde-110">Должна быть текстура GL в виде \_ \_ env.</span><span class="sxs-lookup"><span data-stu-id="94bde-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="94bde-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="94bde-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="94bde-112">Символьное имя однозначного параметра среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="94bde-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="94bde-113">Допустимые значения: \_ режим текстуры в главной \_ \_ и \_ цветовой текстуре GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="94bde-113">Accepted values are GL\_TEXTURE\_ENV\_MODE and GL\_TEXTURE\_ENV\_COLOR.</span></span>

</dd> <dt>

<span data-ttu-id="94bde-114">*params*</span><span class="sxs-lookup"><span data-stu-id="94bde-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="94bde-115">Указатель на массив параметров: либо одну символьную константу, либо цвет RGBA.</span><span class="sxs-lookup"><span data-stu-id="94bde-115">A pointer to an array of parameters: either a single symbolic constant or an RGBA color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94bde-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94bde-116">Return value</span></span>

<span data-ttu-id="94bde-117">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="94bde-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="94bde-118">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="94bde-118">Error codes</span></span>

<span data-ttu-id="94bde-119">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="94bde-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="94bde-120">Имя</span><span class="sxs-lookup"><span data-stu-id="94bde-120">Name</span></span>                                                                                                  | <span data-ttu-id="94bde-121">Значение</span><span class="sxs-lookup"><span data-stu-id="94bde-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94bde-122"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="94bde-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="94bde-123">*Target* или *pname* не является одним из принятых значений, или если *Параметры* должны иметь определенное константное значение (на основе значения *pname*) и не было.</span><span class="sxs-lookup"><span data-stu-id="94bde-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="94bde-124"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="94bde-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="94bde-125">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="94bde-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="94bde-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94bde-126">Remarks</span></span>

<span data-ttu-id="94bde-127">В среде текстуры указывается способ интерпретации значений текстур при текстурировании фрагмента.</span><span class="sxs-lookup"><span data-stu-id="94bde-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="94bde-128">*Целевой* параметр должен иметь значение GL \_ текстуры \_ env.</span><span class="sxs-lookup"><span data-stu-id="94bde-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="94bde-129">Параметр *pname* может быть либо \_ \_ режимом GL текстуры env \_ , либо \_ цветом главной текстуры GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="94bde-129">The *pname* parameter can be either GL\_TEXTURE\_ENV\_MODE or GL\_TEXTURE\_ENV\_COLOR.</span></span>

<span data-ttu-id="94bde-130">Если *pname* имеет \_ режим GL текстуры \_ env \_ , то *params* имеет значение (или указывает на) символическое имя функции текстуры.</span><span class="sxs-lookup"><span data-stu-id="94bde-130">If *pname* is GL\_TEXTURE\_ENV\_MODE, then *params* is (or points to) the symbolic name of a texture function.</span></span> <span data-ttu-id="94bde-131">Определены три функции текстуры: GL для \_ модуляции, GL \_ ДЕКАЛ и GL \_ Blend.</span><span class="sxs-lookup"><span data-stu-id="94bde-131">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="94bde-132">Функция текстуры работает с фрагментом, используя значение изображения текстуры, которое применяется к фрагменту (см. [**глтекспараметер**](gltexparameter-functions.md)) и создает для этого фрагмента цвет RGBA.</span><span class="sxs-lookup"><span data-stu-id="94bde-132">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="94bde-133">В следующей таблице показано, как создается цвет RGBA для каждой из трех функций текстуры, которые можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="94bde-133">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="94bde-134">*C* — это тройной цвет значений (RGB), *а —* связанное альфа-значение.</span><span class="sxs-lookup"><span data-stu-id="94bde-134">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="94bde-135">Значения RGBA, извлеченные из изображения текстуры, находятся в диапазоне \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="94bde-135">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="94bde-136">Индекс *f* относится к входящему фрагменту, индексу *t* к изображению текстуры, индексу *c* на цветовую среду текстуры, а индекс *v* — значению, созданному функцией текстуры.</span><span class="sxs-lookup"><span data-stu-id="94bde-136">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="94bde-137">Изображение текстуры может содержать до четырех компонентов на элемент текстуры (см. раздел [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="94bde-137">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="94bde-138">В образе с одним компонентом lt указывает на один компонент.</span><span class="sxs-lookup"><span data-stu-id="94bde-138">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="94bde-139">В образе с двумя компонентами используется *L?*</span><span class="sxs-lookup"><span data-stu-id="94bde-139">A two-component image uses *L?*</span></span>  <span data-ttu-id="94bde-140">и *?*</span><span class="sxs-lookup"><span data-stu-id="94bde-140">and *A?*</span></span> <span data-ttu-id="94bde-141">.</span><span class="sxs-lookup"><span data-stu-id="94bde-141">.</span></span> <span data-ttu-id="94bde-142">Изображение из трех компонентов имеет только значение цвета, *C?*</span><span class="sxs-lookup"><span data-stu-id="94bde-142">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="94bde-143">.</span><span class="sxs-lookup"><span data-stu-id="94bde-143">.</span></span> <span data-ttu-id="94bde-144">Образ из четырех компонентов имеет значение цвета *C?*</span><span class="sxs-lookup"><span data-stu-id="94bde-144">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="94bde-145">и альфа-значение *A?*</span><span class="sxs-lookup"><span data-stu-id="94bde-145">and an alpha value *A?*</span></span> <span data-ttu-id="94bde-146">.</span><span class="sxs-lookup"><span data-stu-id="94bde-146">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="94bde-147">Число компонентов</span><span class="sxs-lookup"><span data-stu-id="94bde-147">Number of components</span></span></th>
<th><span data-ttu-id="94bde-148">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="94bde-148">GL_MODULATE</span></span></th>
<th><span data-ttu-id="94bde-149">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="94bde-149">GL_DECAL</span></span></th>
<th><span data-ttu-id="94bde-150">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="94bde-150">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="94bde-151">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="94bde-151">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94bde-152"><em>C<sub>v</sub> </em>   =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-152"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="94bde-153"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="94bde-153"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="94bde-154">не определено $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="94bde-154">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94bde-155"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-155"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="94bde-156"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-156"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="94bde-157"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="94bde-157"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94bde-158"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="94bde-158"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="94bde-159"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="94bde-159"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="94bde-160">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="94bde-160">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94bde-161"><em>C<sub>v</sub> </em>   =  <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-161"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="94bde-162"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="94bde-162"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="94bde-163">не определено $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="94bde-163">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94bde-164"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-164"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="94bde-165"><em>) C<sub>f</sub> </em> + <em>L?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-165"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="94bde-166"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="94bde-166"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94bde-167"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="94bde-167"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="94bde-168"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="94bde-168"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="94bde-169">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="94bde-169">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94bde-170"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-170"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="94bde-171"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="94bde-171"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="94bde-172"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-172"><em>C<sub>v</sub></em>  = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="94bde-173">не определено $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="94bde-173">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="94bde-174"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="94bde-174"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="94bde-175"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="94bde-175"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="94bde-176">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="94bde-176">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="94bde-177"><em>C<sub>v</sub> </em>   =  <em>C?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-177"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="94bde-178"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="94bde-178"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="94bde-179"><em>C<sub>v</sub> </em> = (1- <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-179"><em>C<sub>v</sub></em>  = (1 - <em>A?</em></span></span> <span data-ttu-id="94bde-180"><em>) C<sub>f</sub> </em> + <em>A?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-180"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="94bde-181"><em>Ц?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-181"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="94bde-182">не определено $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="94bde-182">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="94bde-183"><em>A<sub>v</sub> </em>   =  <em>А?</em></span><span class="sxs-lookup"><span data-stu-id="94bde-183"><em>A<sub>v</sub></em>  = <em>A?</em></span></span> <span data-ttu-id="94bde-184"><em>A<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="94bde-184"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="94bde-185"><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="94bde-185"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="94bde-186">Если pname имеет \_ Цвет главной текстуры GL \_ \_ , то *params* является указателем на массив, который содержит цвет RGBA, состоящий из четырех значений.</span><span class="sxs-lookup"><span data-stu-id="94bde-186">If pname is GL\_TEXTURE\_ENV\_COLOR, *params* is a pointer to an array that holds an RGBA color consisting of four values.</span></span> <span data-ttu-id="94bde-187">Целочисленные компоненты цвета обрабатываются линейно таким, что наиболее положительное целое число сопоставляется с 1,0, а наиболее отрицательное целочисленное сопоставляется с-1,0.</span><span class="sxs-lookup"><span data-stu-id="94bde-187">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to -1.0.</span></span> <span data-ttu-id="94bde-188">Значения записываются в диапазон \[ 0, 1, \] если они указаны.</span><span class="sxs-lookup"><span data-stu-id="94bde-188">The values are clamped to the range \[0, 1\] when they are specified.</span></span> <span data-ttu-id="94bde-189">*C <sub>c</sub>* принимает следующие четыре значения.</span><span class="sxs-lookup"><span data-stu-id="94bde-189">*C<sub>c</sub>* takes these four values.</span></span>

<span data-ttu-id="94bde-190">\_Режим текстуры в GL \_ \_ по умолчанию имеет значение GL \_ модуляции, а в \_ \_ качестве цвета текстуры GL \_ по умолчанию используется значение (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="94bde-190">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE and GL\_TEXTURE\_ENV\_COLOR defaults to (0, 0, 0, 0).</span></span>

<span data-ttu-id="94bde-191">Следующая функция получает сведения, связанные с **глтексенвив**:</span><span class="sxs-lookup"><span data-stu-id="94bde-191">The following function retrieves information related to **glTexEnviv**:</span></span>

[<span data-ttu-id="94bde-192">**глтексжетенвив**</span><span class="sxs-lookup"><span data-stu-id="94bde-192">**glTexGetEnviv**</span></span>](glgettexenviv.md)

## <a name="requirements"></a><span data-ttu-id="94bde-193">Требования</span><span class="sxs-lookup"><span data-stu-id="94bde-193">Requirements</span></span>



| <span data-ttu-id="94bde-194">Требование</span><span class="sxs-lookup"><span data-stu-id="94bde-194">Requirement</span></span> | <span data-ttu-id="94bde-195">Значение</span><span class="sxs-lookup"><span data-stu-id="94bde-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94bde-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94bde-196">Minimum supported client</span></span><br/> | <span data-ttu-id="94bde-197">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94bde-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94bde-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94bde-198">Minimum supported server</span></span><br/> | <span data-ttu-id="94bde-199">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94bde-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94bde-200">Заголовок</span><span class="sxs-lookup"><span data-stu-id="94bde-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="94bde-201"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="94bde-201"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="94bde-202">Библиотека</span><span class="sxs-lookup"><span data-stu-id="94bde-202">Library</span></span><br/>                  | <dl> <span data-ttu-id="94bde-203"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94bde-203"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94bde-204">DLL</span><span class="sxs-lookup"><span data-stu-id="94bde-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94bde-205"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94bde-205"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94bde-206">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94bde-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94bde-207">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="94bde-207">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="94bde-208">**гленд**</span><span class="sxs-lookup"><span data-stu-id="94bde-208">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="94bde-209">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="94bde-209">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="94bde-210">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="94bde-210">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="94bde-211">**глтекспараметер**</span><span class="sxs-lookup"><span data-stu-id="94bde-211">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





