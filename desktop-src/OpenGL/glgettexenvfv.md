---
title: Функция Глжеттексенвфв (GL. h)
description: Функции Глжеттексенвфв и Глжеттексенвив возвращают параметры среды текстуры. | Функция Глжеттексенвфв (GL. h)
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- Функция Глжеттексенвфв OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnvfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d542461b05a824c78bbad82d843735289f2fb4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664884"
---
# <a name="glgettexenvfv-function"></a><span data-ttu-id="7f71f-105">Функция Глжеттексенвфв</span><span class="sxs-lookup"><span data-stu-id="7f71f-105">glGetTexEnvfv function</span></span>

<span data-ttu-id="7f71f-106">Функции **глжеттексенвфв** и [**глжеттексенвив**](glgettexenviv.md) возвращают параметры среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="7f71f-106">The **glGetTexEnvfv** and [**glGetTexEnviv**](glgettexenviv.md) functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f71f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f71f-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnvfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="7f71f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f71f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f71f-109">*target*</span><span class="sxs-lookup"><span data-stu-id="7f71f-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="7f71f-110">Среда текстуры.</span><span class="sxs-lookup"><span data-stu-id="7f71f-110">A texture environment.</span></span> <span data-ttu-id="7f71f-111">Должна быть текстура GL в виде \_ \_ env.</span><span class="sxs-lookup"><span data-stu-id="7f71f-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="7f71f-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="7f71f-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="7f71f-113">Символьное имя параметра среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="7f71f-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="7f71f-114">Принимаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7f71f-114">The following values are accepted.</span></span>



| <span data-ttu-id="7f71f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7f71f-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="7f71f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7f71f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="7f71f-117"><dt>**\_режим текстуры \_ в главной модели \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f71f-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="7f71f-118">Параметр *params* возвращает однозначный режим текстуры в виде символьной константы.</span><span class="sxs-lookup"><span data-stu-id="7f71f-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="7f71f-119"><dt>**\_Цвет текстуры в главной \_ env \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f71f-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="7f71f-120">Параметр *params* возвращает четыре значения типа Integer или с плавающей запятой, которые являются цветом среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="7f71f-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="7f71f-121">Целочисленные значения при запросе линейно сопоставляются с внутренним представлением с плавающей запятой, таким образом, 1,0 сопоставляется с наиболее положительным целым числом, а-1,0 сопоставляется с наиболее отрицательным целым числом.</span><span class="sxs-lookup"><span data-stu-id="7f71f-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7f71f-122">*params*</span><span class="sxs-lookup"><span data-stu-id="7f71f-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="7f71f-123">Возвращает запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="7f71f-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f71f-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f71f-124">Return value</span></span>

<span data-ttu-id="7f71f-125">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7f71f-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f71f-126">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7f71f-126">Error codes</span></span>

<span data-ttu-id="7f71f-127">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="7f71f-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7f71f-128">Имя</span><span class="sxs-lookup"><span data-stu-id="7f71f-128">Name</span></span>                                                                                                  | <span data-ttu-id="7f71f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7f71f-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f71f-130"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f71f-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7f71f-131">значение *Target* или *pname* не было принято.</span><span class="sxs-lookup"><span data-stu-id="7f71f-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="7f71f-132"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7f71f-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7f71f-133">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7f71f-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7f71f-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f71f-134">Remarks</span></span>

<span data-ttu-id="7f71f-135">Функция **глжеттексенв** возвращает в *параметре params* выбранные значения для среды текстуры, которая была указана с помощью [**глтексенв**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7f71f-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="7f71f-136">*Целевой* параметр указывает среду текстуры.</span><span class="sxs-lookup"><span data-stu-id="7f71f-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="7f71f-137">В настоящее время определена и поддерживается только одна Текстурная среда: текстура GL в виде \_ \_ env.</span><span class="sxs-lookup"><span data-stu-id="7f71f-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="7f71f-138">Параметр *pname* присваивает имя конкретному параметру среды текстуры.</span><span class="sxs-lookup"><span data-stu-id="7f71f-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="7f71f-139">Если возникает ошибка, содержимое *параметров* не изменяется.</span><span class="sxs-lookup"><span data-stu-id="7f71f-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f71f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="7f71f-140">Requirements</span></span>



| <span data-ttu-id="7f71f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="7f71f-141">Requirement</span></span> | <span data-ttu-id="7f71f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="7f71f-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f71f-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f71f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7f71f-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f71f-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7f71f-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f71f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7f71f-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f71f-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f71f-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7f71f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f71f-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f71f-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7f71f-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f71f-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f71f-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f71f-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7f71f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7f71f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f71f-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f71f-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f71f-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f71f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f71f-154">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="7f71f-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7f71f-155">**гленд**</span><span class="sxs-lookup"><span data-stu-id="7f71f-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7f71f-156">**глтексенв**</span><span class="sxs-lookup"><span data-stu-id="7f71f-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





