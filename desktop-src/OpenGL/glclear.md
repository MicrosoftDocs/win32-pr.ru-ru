---
title: Функция Глклеар (GL. h)
description: Функция Глклеар очищает буферы до предустановленных значений.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- Функция Глклеар OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672691"
---
# <a name="glclear-function"></a><span data-ttu-id="a6edf-104">Функция Глклеар</span><span class="sxs-lookup"><span data-stu-id="a6edf-104">glClear function</span></span>

<span data-ttu-id="a6edf-105">Функция **глклеар** очищает буферы до предустановленных значений.</span><span class="sxs-lookup"><span data-stu-id="a6edf-105">The **glClear** function clears buffers to preset values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6edf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6edf-106">Syntax</span></span>


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="a6edf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6edf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6edf-108">*виде*</span><span class="sxs-lookup"><span data-stu-id="a6edf-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="a6edf-109">Побитовые операторы или для масок, которые указывают буферы для очистки.</span><span class="sxs-lookup"><span data-stu-id="a6edf-109">Bitwise OR operators of masks that indicate the buffers to be cleared.</span></span> <span data-ttu-id="a6edf-110">Ниже приведены четыре маски.</span><span class="sxs-lookup"><span data-stu-id="a6edf-110">The four masks are as follows.</span></span>



| <span data-ttu-id="a6edf-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a6edf-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="a6edf-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a6edf-112">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <span data-ttu-id="a6edf-113"><dt>**\_ \_ бит буфера цвета \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-113"><dt>**GL\_COLOR\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="a6edf-114">Буферы, в настоящее время включенные для записи цвета.</span><span class="sxs-lookup"><span data-stu-id="a6edf-114">The buffers currently enabled for color writing.</span></span><br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <span data-ttu-id="a6edf-115"><dt>**\_ \_ бит буфера глубины \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-115"><dt>**GL\_DEPTH\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="a6edf-116">Буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="a6edf-116">The depth buffer.</span></span><br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <span data-ttu-id="a6edf-117"><dt>**\_бит накопленного \_ буфера GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-117"><dt>**GL\_ACCUM\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="a6edf-118">Буфер накопления.</span><span class="sxs-lookup"><span data-stu-id="a6edf-118">The accumulation buffer.</span></span><br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <span data-ttu-id="a6edf-119"><dt>**\_ \_ бит буфера шаблона \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-119"><dt>**GL\_STENCIL\_BUFFER\_BIT**</dt></span></span> </dl> | <span data-ttu-id="a6edf-120">Буфер шаблона.</span><span class="sxs-lookup"><span data-stu-id="a6edf-120">The stencil buffer.</span></span><br/>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6edf-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6edf-121">Return value</span></span>

<span data-ttu-id="a6edf-122">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a6edf-122">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a6edf-123">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a6edf-123">Error codes</span></span>

<span data-ttu-id="a6edf-124">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="a6edf-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a6edf-125">Имя</span><span class="sxs-lookup"><span data-stu-id="a6edf-125">Name</span></span>                                                                                                  | <span data-ttu-id="a6edf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a6edf-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6edf-127"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-127"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a6edf-128">В *маске* задается любой бит, отличный от четырех заданных битов.</span><span class="sxs-lookup"><span data-stu-id="a6edf-128">Any bit other than the four defined bits was set in *mask*.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a6edf-129"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a6edf-130">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a6edf-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a6edf-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6edf-131">Remarks</span></span>

<span data-ttu-id="a6edf-132">Функция **глклеар** задает для области битплане в окне значения, ранее выбранные с помощью [**глклеарколор**](glclearcolor.md), [**глклеариндекс**](glclearindex.md), [**глклеардепс**](glcleardepth.md), [**глклеарстенЦил**](glclearstencil.md)и [**глклеараккум**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="a6edf-132">The **glClear** function sets the bitplane area of the window to values previously selected by [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), and [**glClearAccum**](glclearaccum.md).</span></span> <span data-ttu-id="a6edf-133">Можно очистить несколько цветовых буферов одновременно, выбрав более одного буфера за раз с помощью [**глдравбуффер**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a6edf-133">You can clear multiple color buffers simultaneously by selecting more than one buffer at a time using [**glDrawBuffer**](gldrawbuffer.md).</span></span>

<span data-ttu-id="a6edf-134">Тест «точка-владение», «ножницы», «дизеринг» и «buffer вритемаскс» влияют на работу **глклеар**.</span><span class="sxs-lookup"><span data-stu-id="a6edf-134">The pixel-ownership test, the scissor test, dithering, and the buffer writemasks affect the operation of **glClear**.</span></span> <span data-ttu-id="a6edf-135">Ножница развязывается к снятой области.</span><span class="sxs-lookup"><span data-stu-id="a6edf-135">The scissor box bounds the cleared region.</span></span> <span data-ttu-id="a6edf-136">Функция **глклеар** пропускает альфа-функцию, функцию Blend, логическую операцию, набор элементов, сопоставление текстур и буфер *z*.</span><span class="sxs-lookup"><span data-stu-id="a6edf-136">The **glClear** function ignores the alpha function, blend function, logical operation, stenciling, texture mapping, and *z*-buffering.</span></span>

<span data-ttu-id="a6edf-137">Функция **глклеар** принимает один аргумент (*Mask*), который является побитовым или из нескольких значений, указывающих, какой буфер нужно очистить.</span><span class="sxs-lookup"><span data-stu-id="a6edf-137">The **glClear** function takes a single argument (*mask*) that is the bitwise OR of several values indicating which buffer is to be cleared.</span></span>

<span data-ttu-id="a6edf-138">Значение, на которое очищается каждый буфер, зависит от значения Clear для этого буфера.</span><span class="sxs-lookup"><span data-stu-id="a6edf-138">The value to which each buffer is cleared depends on the setting of the clear value for that buffer.</span></span>

<span data-ttu-id="a6edf-139">Если буфер отсутствует, вызов **глклеар** , направленный в этот буфер, не действует.</span><span class="sxs-lookup"><span data-stu-id="a6edf-139">If a buffer is not present, a **glClear** call directed at that buffer has no effect.</span></span>

<span data-ttu-id="a6edf-140">Следующие функции извлекают сведения, относящиеся к **глклеар**:</span><span class="sxs-lookup"><span data-stu-id="a6edf-140">The following functions retrieve information related to **glClear**:</span></span>

<span data-ttu-id="a6edf-141">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ « \_ Удаление накопленной \_ стоимости GL»</span><span class="sxs-lookup"><span data-stu-id="a6edf-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="a6edf-142">**глжет** с аргументом \_ " \_ Очистка \_ значения глубины GL"</span><span class="sxs-lookup"><span data-stu-id="a6edf-142">**glGet** with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

<span data-ttu-id="a6edf-143">**глжет** с аргументом \_ " \_ очистить \_ значение индекса GL"</span><span class="sxs-lookup"><span data-stu-id="a6edf-143">**glGet** with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="a6edf-144">**глжет** с аргументом \_ " \_ очистить \_ значение цвета GL"</span><span class="sxs-lookup"><span data-stu-id="a6edf-144">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

<span data-ttu-id="a6edf-145">**глжет** с аргументом \_ " \_ очистить значение трафарета GL" \_</span><span class="sxs-lookup"><span data-stu-id="a6edf-145">**glGet** with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="a6edf-146">Требования</span><span class="sxs-lookup"><span data-stu-id="a6edf-146">Requirements</span></span>



| <span data-ttu-id="a6edf-147">Требование</span><span class="sxs-lookup"><span data-stu-id="a6edf-147">Requirement</span></span> | <span data-ttu-id="a6edf-148">Значение</span><span class="sxs-lookup"><span data-stu-id="a6edf-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6edf-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6edf-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a6edf-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a6edf-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a6edf-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6edf-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a6edf-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a6edf-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a6edf-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a6edf-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6edf-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a6edf-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a6edf-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6edf-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a6edf-157">DLL</span><span class="sxs-lookup"><span data-stu-id="a6edf-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6edf-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6edf-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6edf-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6edf-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6edf-160">**глклеараккум**</span><span class="sxs-lookup"><span data-stu-id="a6edf-160">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="a6edf-161">**глклеарколор**</span><span class="sxs-lookup"><span data-stu-id="a6edf-161">**glClearColor**</span></span>](glclearcolor.md)
</dt> <dt>

[<span data-ttu-id="a6edf-162">**глклеардепс**</span><span class="sxs-lookup"><span data-stu-id="a6edf-162">**glClearDepth**</span></span>](glcleardepth.md)
</dt> <dt>

[<span data-ttu-id="a6edf-163">**глклеариндекс**</span><span class="sxs-lookup"><span data-stu-id="a6edf-163">**glClearIndex**</span></span>](glclearindex.md)
</dt> <dt>

[<span data-ttu-id="a6edf-164">**глклеарстенЦил**</span><span class="sxs-lookup"><span data-stu-id="a6edf-164">**glClearStencil**</span></span>](glclearstencil.md)
</dt> <dt>

[<span data-ttu-id="a6edf-165">**глдравбуффер**</span><span class="sxs-lookup"><span data-stu-id="a6edf-165">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="a6edf-166">**глжет**</span><span class="sxs-lookup"><span data-stu-id="a6edf-166">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="a6edf-167">**глсЦиссор**</span><span class="sxs-lookup"><span data-stu-id="a6edf-167">**glScissor**</span></span>](glscissor.md)
</dt> </dl>

 

 





