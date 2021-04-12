---
title: Функция Глдепсфунк (GL. h)
description: Функция Глдепсфунк указывает значение, используемое для сравнений в буфере глубины.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- Функция Глдепсфунк OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489735"
---
# <a name="gldepthfunc-function"></a><span data-ttu-id="fc933-104">Функция Глдепсфунк</span><span class="sxs-lookup"><span data-stu-id="fc933-104">glDepthFunc function</span></span>

<span data-ttu-id="fc933-105">Функция **глдепсфунк** указывает значение, используемое для сравнений в буфере глубины.</span><span class="sxs-lookup"><span data-stu-id="fc933-105">The **glDepthFunc** function specifies the value used for depth-buffer comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc933-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc933-106">Syntax</span></span>


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a><span data-ttu-id="fc933-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc933-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc933-108">*func*</span><span class="sxs-lookup"><span data-stu-id="fc933-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="fc933-109">Задает функцию сравнения глубины.</span><span class="sxs-lookup"><span data-stu-id="fc933-109">Specifies the depth-comparison function.</span></span> <span data-ttu-id="fc933-110">Допустимы следующие символьные константы.</span><span class="sxs-lookup"><span data-stu-id="fc933-110">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="fc933-111">Значение</span><span class="sxs-lookup"><span data-stu-id="fc933-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="fc933-112">Значение</span><span class="sxs-lookup"><span data-stu-id="fc933-112">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="fc933-113"><dt>**ГК \_ никогда**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="fc933-114">Никогда не передает.</span><span class="sxs-lookup"><span data-stu-id="fc933-114">Never passes.</span></span><br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="fc933-115"><dt>**\_меньше ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="fc933-116">Проходит, если значение входящего *z* меньше, чем сохраненное значение *z* .</span><span class="sxs-lookup"><span data-stu-id="fc933-116">Passes if the incoming *z* value is less than the stored *z* value.</span></span> <span data-ttu-id="fc933-117">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc933-117">This is the default value.</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="fc933-118"><dt>**\_ЛЕКУАЛ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-118"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="fc933-119">Проходит, если входящее значение z меньше или равно сохраненному значению z.</span><span class="sxs-lookup"><span data-stu-id="fc933-119">Passes if the incoming z value is less than or equal to the stored z value.</span></span><br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="fc933-120"><dt>**значение GL \_ равно**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-120"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="fc933-121">Проходит, если входящее значение z равно сохраненному значению z.</span><span class="sxs-lookup"><span data-stu-id="fc933-121">Passes if the incoming z value is equal to the stored z value.</span></span><br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="fc933-122"><dt>**в \_ ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-122"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="fc933-123">Проходит, если входящее значение z больше, чем сохраненное значение z.</span><span class="sxs-lookup"><span data-stu-id="fc933-123">Passes if the incoming z value is greater than the stored z value.</span></span><br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="fc933-124"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-124"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="fc933-125">Проходит, если входящее значение z не равно сохраненному значению z.</span><span class="sxs-lookup"><span data-stu-id="fc933-125">Passes if the incoming z value is not equal to the stored z value.</span></span><br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="fc933-126"><dt>**\_ЖЕКУАЛ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-126"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="fc933-127">Проходит, если входящее значение z больше или равно сохраненному значению z.</span><span class="sxs-lookup"><span data-stu-id="fc933-127">Passes if the incoming z value is greater than or equal to the stored z value.</span></span><br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="fc933-128"><dt>**GL \_ всегда**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="fc933-129">Всегда передает.</span><span class="sxs-lookup"><span data-stu-id="fc933-129">Always passes.</span></span><br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc933-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc933-130">Return value</span></span>

<span data-ttu-id="fc933-131">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fc933-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fc933-132">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fc933-132">Error codes</span></span>

<span data-ttu-id="fc933-133">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="fc933-133">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fc933-134">Имя</span><span class="sxs-lookup"><span data-stu-id="fc933-134">Name</span></span>                                                                                                  | <span data-ttu-id="fc933-135">Значение</span><span class="sxs-lookup"><span data-stu-id="fc933-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc933-136"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fc933-137">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fc933-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fc933-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc933-138">Remarks</span></span>

<span data-ttu-id="fc933-139">Функция **глдепсфунк** указывает функцию, используемую для сравнения каждого входящего значения *z* с значением *z* , присутствующее в буфере глубины.</span><span class="sxs-lookup"><span data-stu-id="fc933-139">The **glDepthFunc** function specifies the function used to compare each incoming pixel *z* value with the *z* value present in the depth buffer.</span></span> <span data-ttu-id="fc933-140">Сравнение выполняется только в том случае, если включено тестирование глубины.</span><span class="sxs-lookup"><span data-stu-id="fc933-140">The comparison is performed only if depth testing is enabled.</span></span> <span data-ttu-id="fc933-141">(См. [**гленабле**](glenable.md) с АРГУМЕНТом GL \_ \_тест глубины.)</span><span class="sxs-lookup"><span data-stu-id="fc933-141">(See [**glEnable**](glenable.md) with the argument GL\_DEPTH\_TEST.)</span></span>

<span data-ttu-id="fc933-142">Изначально тестирование глубины отключено.</span><span class="sxs-lookup"><span data-stu-id="fc933-142">Initially, depth testing is disabled.</span></span>

<span data-ttu-id="fc933-143">Следующие функции извлекают сведения, относящиеся к **глдепсфунк**:</span><span class="sxs-lookup"><span data-stu-id="fc933-143">The following functions retrieve information related to **glDepthFunc**:</span></span>

<span data-ttu-id="fc933-144">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ глубины GL \_ Func</span><span class="sxs-lookup"><span data-stu-id="fc933-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_FUNC</span></span>

<span data-ttu-id="fc933-145">[**глисенаблед**](glisenabled.md) с аргументом " \_ тест глубины GL" \_</span><span class="sxs-lookup"><span data-stu-id="fc933-145">[**glIsEnabled**](glisenabled.md) with argument GL\_DEPTH\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="fc933-146">Требования</span><span class="sxs-lookup"><span data-stu-id="fc933-146">Requirements</span></span>



| <span data-ttu-id="fc933-147">Требование</span><span class="sxs-lookup"><span data-stu-id="fc933-147">Requirement</span></span> | <span data-ttu-id="fc933-148">Значение</span><span class="sxs-lookup"><span data-stu-id="fc933-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc933-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc933-149">Minimum supported client</span></span><br/> | <span data-ttu-id="fc933-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc933-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fc933-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc933-151">Minimum supported server</span></span><br/> | <span data-ttu-id="fc933-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc933-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc933-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fc933-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc933-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fc933-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc933-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc933-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc933-157">DLL</span><span class="sxs-lookup"><span data-stu-id="fc933-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc933-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc933-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc933-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc933-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc933-160">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="fc933-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fc933-161">**глдепсранже**</span><span class="sxs-lookup"><span data-stu-id="fc933-161">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="fc933-162">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="fc933-162">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="fc933-163">**гленд**</span><span class="sxs-lookup"><span data-stu-id="fc933-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fc933-164">**глжет**</span><span class="sxs-lookup"><span data-stu-id="fc933-164">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="fc933-165">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="fc933-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





