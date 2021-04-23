---
title: Функция Глжеттексенвив (GL. h)
description: Функции Глжеттексенвфв и Глжеттексенвив возвращают параметры среды текстуры. | Функция Глжеттексенвив (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- Функция Глжеттексенвив OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664883"
---
# <a name="glgettexenviv-function"></a><span data-ttu-id="c6876-105">Функция Глжеттексенвив</span><span class="sxs-lookup"><span data-stu-id="c6876-105">glGetTexEnviv function</span></span>

<span data-ttu-id="c6876-106">Функции [**глжеттексенвфв**](glgettexenvfv.md) и **глжеттексенвив** возвращают параметры среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="c6876-106">The [**glGetTexEnvfv**](glgettexenvfv.md) and **glGetTexEnviv** functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6876-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6876-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="c6876-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6876-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6876-109">*target*</span><span class="sxs-lookup"><span data-stu-id="c6876-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c6876-110">Среда текстуры.</span><span class="sxs-lookup"><span data-stu-id="c6876-110">A texture environment.</span></span> <span data-ttu-id="c6876-111">Должна быть текстура GL в виде \_ \_ env.</span><span class="sxs-lookup"><span data-stu-id="c6876-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="c6876-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="c6876-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c6876-113">Символьное имя параметра среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="c6876-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="c6876-114">Принимаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c6876-114">The following values are accepted.</span></span>



| <span data-ttu-id="c6876-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c6876-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="c6876-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c6876-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="c6876-117"><dt>**\_режим текстуры \_ в главной модели \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6876-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="c6876-118">Параметр *params* возвращает однозначный режим текстуры в виде символьной константы.</span><span class="sxs-lookup"><span data-stu-id="c6876-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="c6876-119"><dt>**\_Цвет текстуры в главной \_ env \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6876-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="c6876-120">Параметр *params* возвращает четыре значения типа Integer или с плавающей запятой, которые являются цветом среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="c6876-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="c6876-121">Целочисленные значения при запросе линейно сопоставляются с внутренним представлением с плавающей запятой, таким образом, 1,0 сопоставляется с наиболее положительным целым числом, а-1,0 сопоставляется с наиболее отрицательным целым числом.</span><span class="sxs-lookup"><span data-stu-id="c6876-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c6876-122">*params*</span><span class="sxs-lookup"><span data-stu-id="c6876-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="c6876-123">Возвращает запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="c6876-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6876-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6876-124">Return value</span></span>

<span data-ttu-id="c6876-125">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c6876-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c6876-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c6876-126">Error codes</span></span>

<span data-ttu-id="c6876-127">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="c6876-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c6876-128">Имя</span><span class="sxs-lookup"><span data-stu-id="c6876-128">Name</span></span>                                                                                                  | <span data-ttu-id="c6876-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c6876-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6876-130"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c6876-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c6876-131">значение *Target* или *pname* не было принято.</span><span class="sxs-lookup"><span data-stu-id="c6876-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="c6876-132"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c6876-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c6876-133">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c6876-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c6876-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6876-134">Remarks</span></span>

<span data-ttu-id="c6876-135">Функция **глжеттексенв** возвращает в *параметре params* выбранные значения для среды текстуры, которая была указана с помощью [**глтексенв**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c6876-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="c6876-136">*Целевой* параметр указывает среду текстуры.</span><span class="sxs-lookup"><span data-stu-id="c6876-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="c6876-137">В настоящее время определена и поддерживается только одна Текстурная среда: текстура GL в виде \_ \_ env.</span><span class="sxs-lookup"><span data-stu-id="c6876-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="c6876-138">Параметр *pname* присваивает имя конкретному параметру среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="c6876-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="c6876-139">Если возникает ошибка, содержимое *параметров* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="c6876-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6876-140">Требования</span><span class="sxs-lookup"><span data-stu-id="c6876-140">Requirements</span></span>



| <span data-ttu-id="c6876-141">Требование</span><span class="sxs-lookup"><span data-stu-id="c6876-141">Requirement</span></span> | <span data-ttu-id="c6876-142">Значение</span><span class="sxs-lookup"><span data-stu-id="c6876-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6876-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6876-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c6876-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c6876-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c6876-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6876-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c6876-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c6876-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6876-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c6876-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6876-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6876-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c6876-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c6876-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6876-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6876-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6876-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c6876-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6876-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6876-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6876-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6876-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6876-154">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="c6876-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c6876-155">**гленд**</span><span class="sxs-lookup"><span data-stu-id="c6876-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c6876-156">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="c6876-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





