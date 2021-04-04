---
title: Функция Глкалллистс (GL. h)
description: Функция Глкалллистс выполняет список списков вывода.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- Функция Глкалллистс OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988793"
---
# <a name="glcalllists-function"></a><span data-ttu-id="b8f97-104">Функция Глкалллистс</span><span class="sxs-lookup"><span data-stu-id="b8f97-104">glCallLists function</span></span>

<span data-ttu-id="b8f97-105">Функция **глкалллистс** выполняет список списков вывода.</span><span class="sxs-lookup"><span data-stu-id="b8f97-105">The **glCallLists** function executes a list of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f97-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8f97-106">Syntax</span></span>


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a><span data-ttu-id="b8f97-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8f97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f97-108">*n*</span><span class="sxs-lookup"><span data-stu-id="b8f97-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f97-109">Число выполняемых списков вывода.</span><span class="sxs-lookup"><span data-stu-id="b8f97-109">The number of display lists to be executed.</span></span>

</dd> <dt>

<span data-ttu-id="b8f97-110">*type*</span><span class="sxs-lookup"><span data-stu-id="b8f97-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f97-111">Тип значений в *списках*.</span><span class="sxs-lookup"><span data-stu-id="b8f97-111">The type of values in *lists*.</span></span> <span data-ttu-id="b8f97-112">Допустимы следующие символьные константы.</span><span class="sxs-lookup"><span data-stu-id="b8f97-112">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="b8f97-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b8f97-113">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="b8f97-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b8f97-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="b8f97-115"><dt>**\_байт GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-115"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="b8f97-116">Параметр *lists* обрабатывается как массив байтов со знаком, каждый из которых находится в диапазоне от-128 до 127.</span><span class="sxs-lookup"><span data-stu-id="b8f97-116">The *lists* parameter is treated as an array of signed bytes, each in the range -128 through 127.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="b8f97-117"><dt>**\_байт без знака GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-117"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="b8f97-118">Параметр *lists* обрабатывается как массив беззнаковых байтов, каждый из которых находится в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="b8f97-118">The *lists* parameter is treated as an array of unsigned bytes, each in the range 0 through 255.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="b8f97-119"><dt>**\_Краткая GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-119"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="b8f97-120">Параметр *lists* обрабатывается как массив из 2-байтных целых чисел со знаком, каждый из которых находится в диапазоне от-32768 до 32767.</span><span class="sxs-lookup"><span data-stu-id="b8f97-120">The *lists* parameter is treated as an array of signed 2-byte integers, each in the range -32768 through 32767.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="b8f97-121"><dt>**\_ \_ сокращенный формат GL без знака**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-121"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="b8f97-122">Параметр *lists* обрабатывается как массив из 2-байтных целых чисел без знака, каждый из которых находится в диапазоне от 0 до 65535.</span><span class="sxs-lookup"><span data-stu-id="b8f97-122">The *lists* parameter is treated as an array of unsigned 2-byte integers, each in the range 0 through 65535.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="b8f97-123"><dt>**тип в GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-123"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="b8f97-124">Параметр *lists* рассматривается как массив из 4-байтовых целых чисел со знаком.</span><span class="sxs-lookup"><span data-stu-id="b8f97-124">The *lists* parameter is treated as an array of signed 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="b8f97-125"><dt>**\_целое число без знака GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-125"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="b8f97-126">Параметр *lists* обрабатывается как массив из 4-байтовых целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="b8f97-126">The *lists* parameter is treated as an array of unsigned 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="b8f97-127"><dt>**с \_ плавающей запятой**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-127"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="b8f97-128">Параметр *lists* обрабатывается как массив из 4-байтовых значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b8f97-128">The *lists* parameter is treated as an array of 4-byte, floating-point values.</span></span><br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <span data-ttu-id="b8f97-129"><dt>**GL \_ 2 \_ байта**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-129"><dt>**GL\_2\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="b8f97-130">Параметр *lists* обрабатывается как массив байтов без знака.</span><span class="sxs-lookup"><span data-stu-id="b8f97-130">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="b8f97-131">Каждая пара байтов указывает одно имя списка экранов.</span><span class="sxs-lookup"><span data-stu-id="b8f97-131">Each pair of bytes specifies a single display-list name.</span></span> <span data-ttu-id="b8f97-132">Значение пары вычислено как 256 раз в секунду значение без знака для первого байта плюс неподписанное значение второго байта.</span><span class="sxs-lookup"><span data-stu-id="b8f97-132">The value of the pair is computed as 256 times the unsigned value of the first byte plus the unsigned value of the second byte.</span></span><br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <span data-ttu-id="b8f97-133"><dt>**\_3 \_ БАЙТа GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-133"><dt>**GL\_3\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="b8f97-134">Параметр *lists* обрабатывается как массив байтов без знака.</span><span class="sxs-lookup"><span data-stu-id="b8f97-134">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="b8f97-135">Каждый Triplet байт указывает одно имя списка экранов.</span><span class="sxs-lookup"><span data-stu-id="b8f97-135">Each triplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="b8f97-136">Значение Triplet вычислено как 65536 раз за число без знака первого байта, плюс 256 раз в секунду беззнаковое значение второго байта плюс неподписанное значение третьего байта.</span><span class="sxs-lookup"><span data-stu-id="b8f97-136">The value of the triplet is computed as 65536 times the unsigned value of the first byte, plus 256 times the unsigned value of the second byte, plus the unsigned value of the third byte.</span></span><br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <span data-ttu-id="b8f97-137"><dt>**GL \_ 4 \_ байта**</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-137"><dt>**GL\_4\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="b8f97-138">Параметр *lists* обрабатывается как массив байтов без знака.</span><span class="sxs-lookup"><span data-stu-id="b8f97-138">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="b8f97-139">Каждый четверный байт указывает одно имя списка экранов.</span><span class="sxs-lookup"><span data-stu-id="b8f97-139">Each quadruplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="b8f97-140">Значение четверной подсчета вычислено Как 16777216 раз в секунду в значении без знака первого байта, плюс 65536 раз в значение без знака второго байта плюс в 256 раз в третий байт плюс значение без знака для четвертого байта.</span><span class="sxs-lookup"><span data-stu-id="b8f97-140">The value of the quadruplet is computed as 16777216 times the unsigned value of the first byte, plus 65536 times the unsigned value of the second byte, plus 256 times the unsigned value of the third byte, plus the unsigned value of the fourth byte.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8f97-141">*приводит*</span><span class="sxs-lookup"><span data-stu-id="b8f97-141">*lists*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f97-142">Адрес массива смещений имен в списке вывода.</span><span class="sxs-lookup"><span data-stu-id="b8f97-142">The address of an array of name offsets in the display list.</span></span> <span data-ttu-id="b8f97-143">Тип указателя — void, так как в зависимости от значения *типа* смещения могут быть байтами, закреплением, ints или числом с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b8f97-143">The pointer type is void because the offsets can be bytes, shorts, ints, or floats, depending on the value of *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f97-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8f97-144">Return value</span></span>

<span data-ttu-id="b8f97-145">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b8f97-145">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f97-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8f97-146">Remarks</span></span>

<span data-ttu-id="b8f97-147">Функция **глкалллистс** приводит к тому, что каждый список экранов в списке имен передается как *списки* для выполнения.</span><span class="sxs-lookup"><span data-stu-id="b8f97-147">The **glCallLists** function causes each display list in the list of names passed as *lists* to be executed.</span></span> <span data-ttu-id="b8f97-148">В результате функции, сохраненные в каждом списке вывода, выполняются по порядку, так же, как если бы они были вызваны без использования списка дисплеев.</span><span class="sxs-lookup"><span data-stu-id="b8f97-148">As a result, the functions saved in each display list are executed in order, just as if they were called without using a display list.</span></span> <span data-ttu-id="b8f97-149">Имена списков вывода, которые не были определены, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b8f97-149">Names of display lists that have not been defined are ignored.</span></span>

<span data-ttu-id="b8f97-150">Функция **глкалллистс** предоставляет эффективные средства для исполнения списков вывода.</span><span class="sxs-lookup"><span data-stu-id="b8f97-150">The **glCallLists** function provides an efficient means for executing display lists.</span></span> <span data-ttu-id="b8f97-151">Параметр *n* указывает количество списков с различными форматами имен (заданные параметром *типа* ) **глкалллистс** .</span><span class="sxs-lookup"><span data-stu-id="b8f97-151">The *n* parameter specifies the number of lists with various name formats (specified by the *type* parameter) **glCallLists** executes.</span></span>

<span data-ttu-id="b8f97-152">Список имен списков вывода не завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="b8f97-152">The list of display list names is not null-terminated.</span></span> <span data-ttu-id="b8f97-153">Вместо *n* указывает, сколько имен следует взять из *списков*.</span><span class="sxs-lookup"><span data-stu-id="b8f97-153">Rather, *n* specifies how many names are to be taken from *lists*.</span></span>

<span data-ttu-id="b8f97-154">Функция [**гллистбасе**](gllistbase.md) делает дополнительный уровень косвенного обращения доступным.</span><span class="sxs-lookup"><span data-stu-id="b8f97-154">The [**glListBase**](gllistbase.md) function makes an additional level of indirection available.</span></span> <span data-ttu-id="b8f97-155">Функция **гллистбасе** задает смещение без знака, которое добавляется к каждому имени списка вывода, указанному в *списках* перед выполнением списка отображений.</span><span class="sxs-lookup"><span data-stu-id="b8f97-155">The **glListBase** function specifies an unsigned offset that is added to each display list name specified in *lists* before that display list is executed.</span></span>

<span data-ttu-id="b8f97-156">Функция **глкалллистс** может отображаться в списке отображения.</span><span class="sxs-lookup"><span data-stu-id="b8f97-156">The **glCallLists** function can appear inside a display list.</span></span> <span data-ttu-id="b8f97-157">Чтобы избежать возможности бесконечной рекурсии, полученной в результате вызова друг друга из списков вывода, на уровне вложенности списков отображаемых данных во время выполнения списка отображается ограничение.</span><span class="sxs-lookup"><span data-stu-id="b8f97-157">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display list execution.</span></span> <span data-ttu-id="b8f97-158">Это ограничение должно быть не менее 64 и зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="b8f97-158">This limit must be at least 64, and it depends on the implementation.</span></span>

<span data-ttu-id="b8f97-159">Состояние OpenGL не сохраняется и не восстанавливается в результате вызова **глкалллистс**.</span><span class="sxs-lookup"><span data-stu-id="b8f97-159">The OpenGL state is not saved and restored across a call to **glCallLists**.</span></span> <span data-ttu-id="b8f97-160">Поэтому изменения, внесенные в состояние OpenGL во время выполнения списков отображения, остаются после завершения выполнения.</span><span class="sxs-lookup"><span data-stu-id="b8f97-160">Thus, changes made to the OpenGL state during the execution of the display lists remain after execution is completed.</span></span> <span data-ttu-id="b8f97-161">Используйте [**глпушаттриб**](glpushattrib.md), [**глпопаттриб**](glpopattrib.md), [**глпушматрикс**](glpushmatrix.md)и [**глпопматрикс**](glpopmatrix.md) , чтобы сохранить состояние OpenGL во всех вызовах **глкалллистс** .</span><span class="sxs-lookup"><span data-stu-id="b8f97-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md) to preserve the OpenGL state across **glCallLists** calls.</span></span>

<span data-ttu-id="b8f97-162">Вы можете выполнять списки вывода между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md), если в списке отображаются только те функции, которые разрешены в этом интервале.</span><span class="sxs-lookup"><span data-stu-id="b8f97-162">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="b8f97-163">Следующие функции извлекают сведения, относящиеся к функции **глкалллистс** :</span><span class="sxs-lookup"><span data-stu-id="b8f97-163">The following functions retrieve information related to the **glCallLists** function:</span></span>

<span data-ttu-id="b8f97-164">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом \_ base GL List \_</span><span class="sxs-lookup"><span data-stu-id="b8f97-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIST\_BASE</span></span>

<span data-ttu-id="b8f97-165">**глжет** с аргументом \_ , \_ вложенным в параметр GL Max List \_</span><span class="sxs-lookup"><span data-stu-id="b8f97-165">**glGet** with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="b8f97-166">**глислист**</span><span class="sxs-lookup"><span data-stu-id="b8f97-166">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="b8f97-167">Требования</span><span class="sxs-lookup"><span data-stu-id="b8f97-167">Requirements</span></span>



| <span data-ttu-id="b8f97-168">Требование</span><span class="sxs-lookup"><span data-stu-id="b8f97-168">Requirement</span></span> | <span data-ttu-id="b8f97-169">Значение</span><span class="sxs-lookup"><span data-stu-id="b8f97-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f97-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8f97-170">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f97-171">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8f97-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b8f97-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8f97-172">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f97-173">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8f97-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8f97-174">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b8f97-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f97-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b8f97-176">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8f97-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8f97-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8f97-178">DLL</span><span class="sxs-lookup"><span data-stu-id="b8f97-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8f97-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8f97-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f97-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8f97-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f97-181">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="b8f97-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b8f97-182">**глкалллист**</span><span class="sxs-lookup"><span data-stu-id="b8f97-182">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="b8f97-183">**глделетелистс**</span><span class="sxs-lookup"><span data-stu-id="b8f97-183">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="b8f97-184">**гленд**</span><span class="sxs-lookup"><span data-stu-id="b8f97-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b8f97-185">**глженлистс**</span><span class="sxs-lookup"><span data-stu-id="b8f97-185">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="b8f97-186">**глжет**</span><span class="sxs-lookup"><span data-stu-id="b8f97-186">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b8f97-187">**глислист**</span><span class="sxs-lookup"><span data-stu-id="b8f97-187">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="b8f97-188">**гллистбасе**</span><span class="sxs-lookup"><span data-stu-id="b8f97-188">**glListBase**</span></span>](gllistbase.md)
</dt> <dt>

[<span data-ttu-id="b8f97-189">**глневлист**</span><span class="sxs-lookup"><span data-stu-id="b8f97-189">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="b8f97-190">**глпопаттриб**</span><span class="sxs-lookup"><span data-stu-id="b8f97-190">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="b8f97-191">**глпопматрикс**</span><span class="sxs-lookup"><span data-stu-id="b8f97-191">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="b8f97-192">**глпушаттриб**</span><span class="sxs-lookup"><span data-stu-id="b8f97-192">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="b8f97-193">**глпушматрикс**</span><span class="sxs-lookup"><span data-stu-id="b8f97-193">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





