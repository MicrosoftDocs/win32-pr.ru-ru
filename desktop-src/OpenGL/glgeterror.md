---
title: Функция Глжетеррор (GL. h)
description: Функция Глжетеррор возвращает сведения об ошибке.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- Функция Глжетеррор OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989210"
---
# <a name="glgeterror-function"></a><span data-ttu-id="b9227-104">Функция Глжетеррор</span><span class="sxs-lookup"><span data-stu-id="b9227-104">glGetError function</span></span>

<span data-ttu-id="b9227-105">Функция **глжетеррор** возвращает сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b9227-105">The **glGetError** function returns error information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9227-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9227-106">Syntax</span></span>


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a><span data-ttu-id="b9227-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9227-107">Parameters</span></span>

<span data-ttu-id="b9227-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="b9227-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9227-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9227-109">Return value</span></span>

<span data-ttu-id="b9227-110">Функция **глжетеррор** возвращает один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="b9227-110">The **glGetError** function returns one of the following error codes.</span></span>



| <span data-ttu-id="b9227-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b9227-111">Return code</span></span>                                                                                           | <span data-ttu-id="b9227-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b9227-112">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9227-113"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-113"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b9227-114">Для перечислимого аргумента задано неприемлемое значение.</span><span class="sxs-lookup"><span data-stu-id="b9227-114">An unacceptable value is specified for an enumerated argument.</span></span> <span data-ttu-id="b9227-115">Функция, вызвавшая ошибку, игнорируется, не имеет побочного действия, Кроме установки флага ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9227-115">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>         |
| <dl> <span data-ttu-id="b9227-116"><dt>**\_недопустимое \_ значение GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-116"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b9227-117">Числовой аргумент выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="b9227-117">A numeric argument is out of range.</span></span> <span data-ttu-id="b9227-118">Функция, вызвавшая ошибку, игнорируется, не имеет побочного действия, Кроме установки флага ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9227-118">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b9227-119"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b9227-120">Указанная операция запрещена в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="b9227-120">The specified operation is not allowed in the current state.</span></span> <span data-ttu-id="b9227-121">Функция, вызвавшая ошибку, игнорируется, не имеет побочного действия, Кроме установки флага ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9227-121">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>           |
| <dl> <span data-ttu-id="b9227-122"><dt>**\_нет \_ ошибок в ГК**</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-122"><dt>**GL\_NO\_ERROR**</dt></span></span> </dl>          | <span data-ttu-id="b9227-123">Ошибки не записаны.</span><span class="sxs-lookup"><span data-stu-id="b9227-123">No error has been recorded.</span></span> <span data-ttu-id="b9227-124">Значение этой символьной константы гарантированно равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b9227-124">The value of this symbolic constant is guaranteed to be zero.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="b9227-125"><dt>**\_переполнение стека GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-125"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="b9227-126">Эта функция вызовет переполнение стека.</span><span class="sxs-lookup"><span data-stu-id="b9227-126">This function would cause a stack overflow.</span></span> <span data-ttu-id="b9227-127">Функция, вызвавшая ошибку, игнорируется, не имеет побочного действия, Кроме установки флага ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9227-127">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                            |
| <dl> <span data-ttu-id="b9227-128"><dt>**\_ \_ потеря значимости СТЕКа GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-128"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="b9227-129">Эта функция вызовет потерю стека.</span><span class="sxs-lookup"><span data-stu-id="b9227-129">This function would cause a stack underflow.</span></span> <span data-ttu-id="b9227-130">Функция, вызвавшая ошибку, игнорируется, не имеет побочного действия, Кроме установки флага ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9227-130">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                           |
| <dl> <span data-ttu-id="b9227-131"><dt>**\_ \_ \_ неиспользуемая память в GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-131"><dt>**GL\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="b9227-132">Недостаточно памяти для выполнения функции.</span><span class="sxs-lookup"><span data-stu-id="b9227-132">There is not enough memory left to execute the function.</span></span> <span data-ttu-id="b9227-133">Состояние OpenGL не определено, за исключением состояния флагов ошибок, после записи этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9227-133">The state of OpenGL is undefined, except for the state of the error flags, after this error is recorded.</span></span><br/> |



 

<span data-ttu-id="b9227-134">Обратите внимание, что **глжетеррор** возвращает \_ недопустимую операцию GL, \_ если она вызывается между вызовом [**Глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b9227-134">Note that **glGetError** returns GL\_INVALID\_OPERATION if it is called between a call to [**glBegin**](glbegin.md) and its corresponding call to [**glEnd**](glend.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9227-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9227-135">Remarks</span></span>

<span data-ttu-id="b9227-136">Каждой обнаруживаемой ошибке присваивается числовой код и символьное имя.</span><span class="sxs-lookup"><span data-stu-id="b9227-136">Each detectable error is assigned a numeric code and symbolic name.</span></span> <span data-ttu-id="b9227-137">При возникновении ошибки флагу ошибки присваивается соответствующее значение кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9227-137">When an error occurs, the error flag is set to the appropriate error code value.</span></span> <span data-ttu-id="b9227-138">Никакие другие ошибки не записываются до вызова **глжетеррор** , возвращается код ошибки, а флаг сбрасывается в значение \_ No No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="b9227-138">No other errors are recorded until **glGetError** is called, the error code is returned, and the flag is reset to GL\_NO\_ERROR.</span></span> <span data-ttu-id="b9227-139">Если вызов **глжетеррор** возвращает значение No GL, ошибка не обнаружена \_ \_ с момента последнего вызова **Глжетеррор** или с момента инициализации OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b9227-139">If a call to **glGetError** returns GL\_NO\_ERROR, there has been no detectable error since the last call to **glGetError**, or since OpenGL was initialized.</span></span>

<span data-ttu-id="b9227-140">Для поддержки распределенных реализаций может существовать несколько флагов ошибок.</span><span class="sxs-lookup"><span data-stu-id="b9227-140">To allow for distributed implementations, there may be several error flags.</span></span> <span data-ttu-id="b9227-141">Если какой-либо из отдельных флагов ошибок записал ошибку, возвращается значение этого флага и этот флаг сбрасывается до значения GL \_ без \_ ошибок при вызове **глжетеррор** .</span><span class="sxs-lookup"><span data-stu-id="b9227-141">If any single error flag has recorded an error, the value of that flag is returned and that flag is reset to GL\_NO\_ERROR when **glGetError** is called.</span></span> <span data-ttu-id="b9227-142">Если ошибка была записана более чем одним флагом, **глжетеррор** возвращает и очищает произвольное значение флага ошибки.</span><span class="sxs-lookup"><span data-stu-id="b9227-142">If more than one flag has recorded an error, **glGetError** returns and clears an arbitrary error flag value.</span></span> <span data-ttu-id="b9227-143">Если все флаги ошибок должны быть сброшены, следует всегда вызывать **глжетеррор** в цикле до тех пор, пока не будет возвращена \_ \_ Ошибка GL.</span><span class="sxs-lookup"><span data-stu-id="b9227-143">If all error flags are to be reset, you should always call **glGetError** in a loop until it returns GL\_NO\_ERROR.</span></span>

<span data-ttu-id="b9227-144">Изначально все флаги ошибок имеют значение \_ No No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="b9227-144">Initially, all error flags are set to GL\_NO\_ERROR.</span></span>

<span data-ttu-id="b9227-145">Если установлен флаг ошибки, результаты операции OpenGL не определяются, только если \_ произошла незаполненная \_ \_ память.</span><span class="sxs-lookup"><span data-stu-id="b9227-145">When an error flag is set, results of an OpenGL operation are undefined only if GL\_OUT\_OF\_MEMORY has occurred.</span></span> <span data-ttu-id="b9227-146">Во всех остальных случаях функция, создающая ошибку, игнорируется и не влияет на содержимое состояния OpenGL или буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="b9227-146">In all other cases, the function generating the error is ignored and has no effect on the OpenGL state or framebuffer contents.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9227-147">Требования</span><span class="sxs-lookup"><span data-stu-id="b9227-147">Requirements</span></span>



| <span data-ttu-id="b9227-148">Требование</span><span class="sxs-lookup"><span data-stu-id="b9227-148">Requirement</span></span> | <span data-ttu-id="b9227-149">Значение</span><span class="sxs-lookup"><span data-stu-id="b9227-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9227-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9227-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b9227-151">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9227-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9227-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9227-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b9227-153">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9227-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9227-154">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b9227-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9227-155"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-155"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b9227-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b9227-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9227-157"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-157"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9227-158">DLL</span><span class="sxs-lookup"><span data-stu-id="b9227-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9227-159"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9227-159"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9227-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9227-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9227-161">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="b9227-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b9227-162">**гленд**</span><span class="sxs-lookup"><span data-stu-id="b9227-162">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





