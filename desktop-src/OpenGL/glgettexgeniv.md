---
title: Функция Глжеттексженив (GL. h)
description: Функции Глжеттексжендв, Глжеттексженфв и Глжеттексженив возвращают параметры создания координат текстуры. | Функция Глжеттексженив (GL. h)
ms.assetid: 62c481d1-4862-43bb-9319-5a282c4e47d3
keywords:
- Функция Глжеттексженив OpenGL
topic_type:
- apiref
api_name:
- glGetTexGeniv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29569c84d21dbb2cd69579c78747e844cfd23ba4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684849"
---
# <a name="glgettexgeniv-function"></a><span data-ttu-id="fb6a5-105">Функция Глжеттексженив</span><span class="sxs-lookup"><span data-stu-id="fb6a5-105">glGetTexGeniv function</span></span>

<span data-ttu-id="fb6a5-106">Функции [**глжеттексжендв**](glgettexgendv.md), [**глжеттексженфв**](glgettexgenfv.md)и **глжеттексженив** возвращают параметры создания координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-106">The [**glGetTexGendv**](glgettexgendv.md), [**glGetTexGenfv**](glgettexgenfv.md), and **glGetTexGeniv** functions return texture coordinate generation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6a5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb6a5-107">Syntax</span></span>


```C++
void WINAPI glGetTexGeniv(
   GLenum coord,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="fb6a5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb6a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb6a5-109">*курд*</span><span class="sxs-lookup"><span data-stu-id="fb6a5-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6a5-110">Координата текстуры.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-110">A texture coordinate.</span></span> <span data-ttu-id="fb6a5-111">Необходимо указать GL \_ S, GL \_ T, GL \_ R или GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-111">Must be GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="fb6a5-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="fb6a5-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6a5-113">Символическое имя возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-113">The symbolic name of the value(s) to be returned.</span></span> <span data-ttu-id="fb6a5-114">Должен быть либо \_ \_ \_ режимом формирования текстуры GL, либо именем одного из уравнений плоскости создания текстуры: \_ «плоскость объектов GL» или «плоскость «планового \_ \_ взгляда \_ ».</span><span class="sxs-lookup"><span data-stu-id="fb6a5-114">Must be either GL\_TEXTURE\_GEN\_MODE or the name of one of the texture generation plane equations: GL\_OBJECT\_PLANE or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="fb6a5-115">Ниже приведены эти значения.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-115">These values are as follows.</span></span>



| <span data-ttu-id="fb6a5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fb6a5-116">Value</span></span>                                                                                                                                                                             | <span data-ttu-id="fb6a5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fb6a5-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <span data-ttu-id="fb6a5-118"><dt>**\_ \_ режим ГЕНЕРАЦИИ текстуры \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a5-118"><dt>**GL\_TEXTURE\_GEN\_MODE**</dt></span></span> </dl> | <span data-ttu-id="fb6a5-119">Параметр *params* возвращает функцию создания текстуры с одним значением, символьную константу.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-119">The *params* parameter returns the single-valued texture generation function, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <span data-ttu-id="fb6a5-120"><dt>**\_плоскость объектов \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a5-120"><dt>**GL\_OBJECT\_PLANE**</dt></span></span> </dl>              | <span data-ttu-id="fb6a5-121">Параметр *params* возвращает четыре коэффициента уравнений плоскости, определяющие создание объектных линейных координат.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-121">The *params* parameter returns the four plane equation coefficients that specify object linear-coordinate generation.</span></span> <span data-ttu-id="fb6a5-122">При запросе целочисленные значения сопоставляются непосредственно из внутреннего представления с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-122">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <span data-ttu-id="fb6a5-123"><dt>**\_плоскость для глаз в ГК \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a5-123"><dt>**GL\_EYE\_PLANE**</dt></span></span> </dl>                       | <span data-ttu-id="fb6a5-124">Параметр *params* возвращает четыре коэффициента уравнений плоскости, которые определяют Создание линейного создания координат глаз.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-124">The *params* parameter returns the four plane equation coefficients that specify eye linear-coordinate generation.</span></span> <span data-ttu-id="fb6a5-125">При запросе целочисленные значения сопоставляются непосредственно из внутреннего представления с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-125">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span> <span data-ttu-id="fb6a5-126">Возвращаемые значения — это те, которые поддерживаются в координатах глаза.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-126">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="fb6a5-127">Они не равны значениям, заданным с помощью [**глтексжен**](gltexgen-functions.md), если только матрица моделвиев не была определена во время вызова **глтексжен** .</span><span class="sxs-lookup"><span data-stu-id="fb6a5-127">They are not equal to the values specified using [**glTexGen**](gltexgen-functions.md), unless the modelview matrix was identified at the time **glTexGen** was called.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb6a5-128">*params*</span><span class="sxs-lookup"><span data-stu-id="fb6a5-128">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fb6a5-129">Возвращает запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-129">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb6a5-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb6a5-130">Return value</span></span>

<span data-ttu-id="fb6a5-131">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb6a5-132">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fb6a5-132">Error codes</span></span>

<span data-ttu-id="fb6a5-133">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-133">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fb6a5-134">Имя</span><span class="sxs-lookup"><span data-stu-id="fb6a5-134">Name</span></span>                                                                                                  | <span data-ttu-id="fb6a5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="fb6a5-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb6a5-136"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a5-136"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fb6a5-137">*курд* или *pname* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-137">*coord* or *pname* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="fb6a5-138"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a5-138"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fb6a5-139">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fb6a5-139">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fb6a5-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb6a5-140">Remarks</span></span>

<span data-ttu-id="fb6a5-141">Функция **глжеттексжен** *возвращает в* параметрах выбранных параметров функции создания координат текстуры, указанной с помощью **глтексжен**.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-141">The **glGetTexGen** function returns in *params* selected parameters of a texture-coordinate generation function that you specified with **glTexGen**.</span></span> <span data-ttu-id="fb6a5-142">Параметр *курд* называет одно из координат текстуры (*s*, *t*, *r*, *q*), используя символьную константу GL \_ , GL \_ t, GL \_ r или GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-142">The *coord* parameter names one of the (*s*, *t*, *r*, *q*) texture coordinates, using the symbolic constant GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

<span data-ttu-id="fb6a5-143">Если возникает ошибка, содержимое *параметров* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-143">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6a5-144">Требования</span><span class="sxs-lookup"><span data-stu-id="fb6a5-144">Requirements</span></span>



| <span data-ttu-id="fb6a5-145">Требование</span><span class="sxs-lookup"><span data-stu-id="fb6a5-145">Requirement</span></span> | <span data-ttu-id="fb6a5-146">Значение</span><span class="sxs-lookup"><span data-stu-id="fb6a5-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6a5-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb6a5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="fb6a5-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb6a5-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fb6a5-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb6a5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="fb6a5-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb6a5-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb6a5-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fb6a5-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb6a5-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a5-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fb6a5-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fb6a5-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb6a5-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a5-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb6a5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="fb6a5-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb6a5-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb6a5-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6a5-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb6a5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6a5-158">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fb6a5-159">**гленд**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-159">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fb6a5-160">**глтексжен**</span><span class="sxs-lookup"><span data-stu-id="fb6a5-160">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> </dl>

 

 





