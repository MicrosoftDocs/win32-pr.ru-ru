---
title: Функция Глкуллфаце (GL. h)
description: Функция Глкуллфаце указывает, можно ли исключать внешние или фоновые аспекты.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- Функция Глкуллфаце OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988306"
---
# <a name="glcullface-function"></a><span data-ttu-id="34415-104">Функция Глкуллфаце</span><span class="sxs-lookup"><span data-stu-id="34415-104">glCullFace function</span></span>

<span data-ttu-id="34415-105">Функция **глкуллфаце** указывает, можно ли исключать внешние или фоновые аспекты.</span><span class="sxs-lookup"><span data-stu-id="34415-105">The **glCullFace** function specifies whether front-facing or back-facing facets can be culled.</span></span>

## <a name="syntax"></a><span data-ttu-id="34415-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34415-106">Syntax</span></span>


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="34415-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34415-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34415-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="34415-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="34415-109">Указывает, являются ли аспекты с внешними или фоновыми серверными кандидатами для отбора.</span><span class="sxs-lookup"><span data-stu-id="34415-109">Specifies whether front-facing or back-facing facets are candidates for culling.</span></span> <span data-ttu-id="34415-110">Символьные константы GL \_ Front, GL \_ назад и GL \_ Front \_ и \_ Back принимаются.</span><span class="sxs-lookup"><span data-stu-id="34415-110">The symbolic constants GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK are accepted.</span></span> <span data-ttu-id="34415-111">Значение по умолчанию — GL \_ назад.</span><span class="sxs-lookup"><span data-stu-id="34415-111">The default value is GL\_BACK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34415-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34415-112">Return value</span></span>

<span data-ttu-id="34415-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="34415-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34415-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="34415-114">Error codes</span></span>

<span data-ttu-id="34415-115">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="34415-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="34415-116">Имя</span><span class="sxs-lookup"><span data-stu-id="34415-116">Name</span></span>                                                                                                  | <span data-ttu-id="34415-117">Значение</span><span class="sxs-lookup"><span data-stu-id="34415-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34415-118"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34415-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="34415-119">*режим* не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="34415-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="34415-120"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="34415-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="34415-121">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="34415-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="34415-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34415-122">Remarks</span></span>

<span data-ttu-id="34415-123">Функция **глкуллфаце** указывает, исключаются ли аспекты с внешним или фоновым *режимом*(как указано в режиме) при включении отбора аспектов.</span><span class="sxs-lookup"><span data-stu-id="34415-123">The **glCullFace** function specifies whether front-facing or back-facing facets are culled (as specified by *mode*) when facet culling is enabled.</span></span> <span data-ttu-id="34415-124">Вы включаете и отключаете отбор аспектов с помощью [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с аргументом «поверхность применения GL \_ \_ ».</span><span class="sxs-lookup"><span data-stu-id="34415-124">You enable and disable facet culling using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_CULL\_FACE.</span></span> <span data-ttu-id="34415-125">К аспектам относятся треугольники, куадрилатералс, многоугольники и прямоугольники.</span><span class="sxs-lookup"><span data-stu-id="34415-125">Facets include triangles, quadrilaterals, polygons, and rectangles.</span></span>

<span data-ttu-id="34415-126">Функция [**глфронтфаце**](glfrontface.md) указывает, какой из аспектов по часовой стрелке и против часовой стрелки является внешним и обратным.</span><span class="sxs-lookup"><span data-stu-id="34415-126">The [**glFrontFace**](glfrontface.md) function specifies which of the clockwise and counterclockwise facets are front-facing and back-facing.</span></span>

<span data-ttu-id="34415-127">Если *режим* — GL \_ спереди \_ и \_ назад, то никакие аспекты не рисуются, а другие примитивы, такие как точки и линии, рисуются.</span><span class="sxs-lookup"><span data-stu-id="34415-127">If *mode* is GL\_FRONT\_AND\_BACK, no facets are drawn, but other primitives, such as points and lines, are drawn.</span></span>

<span data-ttu-id="34415-128">Следующие функции извлекают сведения, относящиеся к **глкуллфаце**:</span><span class="sxs-lookup"><span data-stu-id="34415-128">The following functions retrieve information related to **glCullFace**:</span></span>

<span data-ttu-id="34415-129">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ " \_ режим отбора" для параметра GL \_</span><span class="sxs-lookup"><span data-stu-id="34415-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CULL\_FACE\_MODE</span></span>

<span data-ttu-id="34415-130">[**глисенаблед**](glisenabled.md) с аргументом " \_ отбор, \_ лицо"</span><span class="sxs-lookup"><span data-stu-id="34415-130">[**glIsEnabled**](glisenabled.md) with argument GL\_CULL\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="34415-131">Требования</span><span class="sxs-lookup"><span data-stu-id="34415-131">Requirements</span></span>



| <span data-ttu-id="34415-132">Требование</span><span class="sxs-lookup"><span data-stu-id="34415-132">Requirement</span></span> | <span data-ttu-id="34415-133">Значение</span><span class="sxs-lookup"><span data-stu-id="34415-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34415-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34415-134">Minimum supported client</span></span><br/> | <span data-ttu-id="34415-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34415-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="34415-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34415-136">Minimum supported server</span></span><br/> | <span data-ttu-id="34415-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="34415-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34415-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="34415-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="34415-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="34415-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="34415-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34415-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="34415-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34415-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="34415-142">DLL</span><span class="sxs-lookup"><span data-stu-id="34415-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34415-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34415-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34415-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34415-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34415-145">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="34415-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="34415-146">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="34415-146">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="34415-147">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="34415-147">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="34415-148">**гленд**</span><span class="sxs-lookup"><span data-stu-id="34415-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="34415-149">**глфронтфаце**</span><span class="sxs-lookup"><span data-stu-id="34415-149">**glFrontFace**</span></span>](glfrontface.md)
</dt> <dt>

[<span data-ttu-id="34415-150">**глжет**</span><span class="sxs-lookup"><span data-stu-id="34415-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="34415-151">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="34415-151">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





