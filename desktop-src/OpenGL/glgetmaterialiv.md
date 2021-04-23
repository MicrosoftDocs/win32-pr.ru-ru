---
title: Функция Глжетматериалив (GL. h)
description: Функции Глжетматериалфв и Глжетматериалив возвращают параметры материала. | Функция Глжетматериалив (GL. h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- Функция Глжетматериалив OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f09e1a315d4929ebb92f3b0e59ed6762a7fe4b35
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684864"
---
# <a name="glgetmaterialiv-function"></a><span data-ttu-id="b2aa8-105">Функция Глжетматериалив</span><span class="sxs-lookup"><span data-stu-id="b2aa8-105">glGetMaterialiv function</span></span>

<span data-ttu-id="b2aa8-106">Функции [**глжетматериалфв**](glgetmaterialfv.md) и **глжетматериалив** возвращают параметры материала.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-106">The [**glGetMaterialfv**](glgetmaterialfv.md) and **glGetMaterialiv** functions return material parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2aa8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2aa8-107">Syntax</span></span>


```C++
void WINAPI glGetMaterialiv(
   GLenum face,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="b2aa8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2aa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2aa8-109">*личным*</span><span class="sxs-lookup"><span data-stu-id="b2aa8-109">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="b2aa8-110">Указывает, к какому из двух материалов выполняется запрос.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-110">Specifies which of the two materials is being queried.</span></span> <span data-ttu-id="b2aa8-111">\_ \_ На начало и на задний план в ГК записываются передняя и задняя части, соответственно.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-111">GL\_FRONT or GL\_BACK are accepted, representing the front and back materials, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="b2aa8-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="b2aa8-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="b2aa8-113">Возвращаемый параметр Material.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-113">The material parameter to return.</span></span> <span data-ttu-id="b2aa8-114">Принимаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-114">The following values are accepted.</span></span>



| <span data-ttu-id="b2aa8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b2aa8-115">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="b2aa8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b2aa8-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="b2aa8-117"><dt>**\_окружение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-117"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                    | <span data-ttu-id="b2aa8-118">Параметр *params* возвращает четыре значения типа Integer или с плавающей запятой, представляющие отразить окружающую часть материала.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-118">The *params* parameter returns four integer or floating-point values representing the ambient reflectance of the material.</span></span> <span data-ttu-id="b2aa8-119">Целочисленные значения при запросе линейно сопоставляются с внутренним представлением с плавающей запятой, таким образом, 1,0 сопоставляется с наиболее положительным целочисленным значением, а-1,0 сопоставляется с наиболее отрицательным значением типа Integer.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-119">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b2aa8-120">Если внутреннее значение находится за пределами диапазона \[ -1, 1 \] , соответствующее целочисленное возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-120">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="b2aa8-121"><dt>**Рассеивание GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-121"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                    | <span data-ttu-id="b2aa8-122">Параметр *params* возвращает четыре значения типа Integer или с плавающей запятой, представляющие Рассеянное отражение материала.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-122">The *params* parameter returns four integer or floating-point values representing the diffuse reflectance of the material.</span></span> <span data-ttu-id="b2aa8-123">Целочисленные значения при запросе линейно сопоставляются с внутренним представлением с плавающей запятой, таким образом, 1,0 сопоставляется с наиболее положительным целочисленным значением, а-1,0 сопоставляется с наиболее отрицательным значением типа Integer.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-123">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b2aa8-124">Если внутреннее значение находится за пределами диапазона \[ -1, 1 \] , соответствующее целочисленное возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-124">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="b2aa8-125"><dt>**\_отражающий GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-125"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                 | <span data-ttu-id="b2aa8-126">Параметр *params* возвращает четыре значения типа Integer или с плавающей запятой, представляющих отраженное отражение материала.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-126">The *params* parameter returns four integer or floating-point values representing the specular reflectance of the material.</span></span> <span data-ttu-id="b2aa8-127">Целочисленные значения при запросе линейно сопоставляются с внутренним представлением с плавающей запятой, таким образом, 1,0 сопоставляется с наиболее положительным целочисленным значением, а-1,0 сопоставляется с наиболее отрицательным значением типа Integer.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-127">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b2aa8-128">Если внутреннее значение находится за пределами диапазона \[ -1, 1 \] , соответствующее целочисленное возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-128">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="b2aa8-129"><dt>**\_эмиссия GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-129"><dt>**GL\_EMISSION**</dt></span></span> </dl>                 | <span data-ttu-id="b2aa8-130">Параметр *params* возвращает четыре значения типа Integer или с плавающей запятой, представляющие порожденную интенсивность освещения материала.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-130">The *params* parameter returns four integer or floating-point values representing the emitted light intensity of the material.</span></span> <span data-ttu-id="b2aa8-131">Целочисленные значения при запросе линейно сопоставляются с внутренним представлением с плавающей запятой, таким образом, 1,0 сопоставляется с наиболее положительным целочисленным значением, а-1,0 сопоставляется с наиболее отрицательным значением типа Integer.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-131">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="b2aa8-132">Если внутреннее значение находится за пределами диапазона \[ -1, 1 \] , соответствующее целочисленное возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-132">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="b2aa8-133"><dt>**\_коэффициента БЛЕСКА GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-133"><dt>**GL\_SHININESS**</dt></span></span> </dl>              | <span data-ttu-id="b2aa8-134">Параметр *params* возвращает одно целое число или значение с плавающей запятой, представляющее отражающую экспоненту материала.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-134">The *params* parameter returns one integer or floating-point value representing the specular exponent of the material.</span></span> <span data-ttu-id="b2aa8-135">При запросе целочисленные значения вычисляются путем округления внутреннего значения с плавающей запятой до ближайшего целого значения.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-135">Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="b2aa8-136"><dt>**\_ \_ индексы цвета GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-136"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl> | <span data-ttu-id="b2aa8-137">Параметр *params* возвращает три целого числа или значения с плавающей запятой, представляющие внешний, рассеянный и отраженный индекс материала.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-137">The *params* parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material.</span></span> <span data-ttu-id="b2aa8-138">Используйте эти индексы только для освещения цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-138">Use these indexes only for color-index lighting.</span></span> <span data-ttu-id="b2aa8-139">(Все остальные параметры используются только для освещения RGBA.) При запросе целочисленные значения вычисляются путем округления внутренних значений с плавающей запятой до ближайших целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-139">(The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                            |



 

</dd> <dt>

<span data-ttu-id="b2aa8-140">*params*</span><span class="sxs-lookup"><span data-stu-id="b2aa8-140">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b2aa8-141">Возвращает запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-141">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2aa8-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2aa8-142">Return value</span></span>

<span data-ttu-id="b2aa8-143">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2aa8-144">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b2aa8-144">Error codes</span></span>

<span data-ttu-id="b2aa8-145">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b2aa8-146">Имя</span><span class="sxs-lookup"><span data-stu-id="b2aa8-146">Name</span></span>                                                                                                  | <span data-ttu-id="b2aa8-147">Значение</span><span class="sxs-lookup"><span data-stu-id="b2aa8-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2aa8-148"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b2aa8-149">*целевой объект* или *запрос* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-149">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="b2aa8-150"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b2aa8-151">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b2aa8-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b2aa8-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2aa8-152">Remarks</span></span>

<span data-ttu-id="b2aa8-153">Функция **глжетматериал** возвращает в *params* значение или значения параметра *pname* *материала.*</span><span class="sxs-lookup"><span data-stu-id="b2aa8-153">The **glGetMaterial** function returns in *params* the value or values of parameter *pname* of material *face*.</span></span>

<span data-ttu-id="b2aa8-154">Если возникает ошибка, содержимое *параметров* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b2aa8-154">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2aa8-155">Требования</span><span class="sxs-lookup"><span data-stu-id="b2aa8-155">Requirements</span></span>



| <span data-ttu-id="b2aa8-156">Требование</span><span class="sxs-lookup"><span data-stu-id="b2aa8-156">Requirement</span></span> | <span data-ttu-id="b2aa8-157">Значение</span><span class="sxs-lookup"><span data-stu-id="b2aa8-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2aa8-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2aa8-158">Minimum supported client</span></span><br/> | <span data-ttu-id="b2aa8-159">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2aa8-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b2aa8-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2aa8-160">Minimum supported server</span></span><br/> | <span data-ttu-id="b2aa8-161">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2aa8-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2aa8-162">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b2aa8-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2aa8-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b2aa8-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2aa8-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2aa8-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b2aa8-166">DLL</span><span class="sxs-lookup"><span data-stu-id="b2aa8-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2aa8-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2aa8-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2aa8-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2aa8-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2aa8-169">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="b2aa8-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b2aa8-170">**гленд**</span><span class="sxs-lookup"><span data-stu-id="b2aa8-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b2aa8-171">**глматериал**</span><span class="sxs-lookup"><span data-stu-id="b2aa8-171">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





