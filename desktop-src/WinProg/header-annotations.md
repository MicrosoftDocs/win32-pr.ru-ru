---
title: Заметки заголовка
description: Заметки заголовков описывают, как функция использует свои параметры и возвращаемое значение.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- Windows API, заметки к файлам заголовков
- заметки файла заголовка
- Спекстрингс. h
- язык Standard annotation (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710336"
---
# <a name="header-annotations"></a><span data-ttu-id="ce766-117">Заметки заголовка</span><span class="sxs-lookup"><span data-stu-id="ce766-117">Header Annotations</span></span>

<span data-ttu-id="ce766-118">\[В этом разделе описываются аннотации, поддерживаемые заголовками Windows в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ce766-118">\[This topic describes the annotations supported in the Windows headers through Windows 7.</span></span> <span data-ttu-id="ce766-119">При разработке для Windows 8 следует использовать аннотации, описанные в [аннотациях SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span><span class="sxs-lookup"><span data-stu-id="ce766-119">If you are developing for Windows 8, you should use the annotations described in [SAL Annotations]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span></span>

<span data-ttu-id="ce766-120">Заметки заголовков описывают, как функция использует свои параметры и возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="ce766-120">Header annotations describe how a function uses its parameters and return value.</span></span> <span data-ttu-id="ce766-121">Эти заметки были добавлены во многие файлы заголовков Windows, чтобы обеспечить правильное обращение к API Windows.</span><span class="sxs-lookup"><span data-stu-id="ce766-121">These annotations have been added to many of the Windows header files to help you ensure that you are calling the Windows API correctly.</span></span> <span data-ttu-id="ce766-122">При включении анализа кода, который доступен начиная с Visual Studio 2005, компилятор выдает предупреждения уровня 6000, если вы не вызываете эти функции в течение использования, описанного в заметках.</span><span class="sxs-lookup"><span data-stu-id="ce766-122">If you enable code analysis, which is available starting with the Visual Studio 2005, the compiler will produce level 6000 warnings if you are not calling these functions per the usage described through the annotations.</span></span> <span data-ttu-id="ce766-123">Можно также добавить эти заметки в собственный код, чтобы убедиться, что они вызываются правильно.</span><span class="sxs-lookup"><span data-stu-id="ce766-123">You can also add these annotations in your own code to ensure that it is being called correctly.</span></span> <span data-ttu-id="ce766-124">Сведения о включении анализа кода в Visual Studio см. в документации по вашей версии Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ce766-124">To enable code analysis in Visual Studio, see the documentation for your version of Visual Studio.</span></span>

<span data-ttu-id="ce766-125">Эти заметки определены в Спекстрингс. h.</span><span class="sxs-lookup"><span data-stu-id="ce766-125">These annotations are defined in Specstrings.h.</span></span> <span data-ttu-id="ce766-126">Они основаны на примитивах, которые являются частью стандартного языка аннотации (SAL) и реализованы с помощью `_declspec("SAL_*")` .</span><span class="sxs-lookup"><span data-stu-id="ce766-126">They are built on primitives that are part of the Standard Annotation Language (SAL) and implemented using `_declspec("SAL_*")`.</span></span>

<span data-ttu-id="ce766-127">Существует два класса заметок: заметки буфера и дополнительные заметки.</span><span class="sxs-lookup"><span data-stu-id="ce766-127">There are two classes of annotations: buffer annotations and advanced annotations.</span></span>

## <a name="buffer-annotations"></a><span data-ttu-id="ce766-128">Заметки буфера</span><span class="sxs-lookup"><span data-stu-id="ce766-128">Buffer Annotations</span></span>

<span data-ttu-id="ce766-129">Заметки буфера описывают, как функции используют свои указатели и могут использоваться для обнаружения переполнений буфера.</span><span class="sxs-lookup"><span data-stu-id="ce766-129">Buffer annotations describe how functions use their pointers and can be used to detect buffer overruns.</span></span> <span data-ttu-id="ce766-130">Каждый параметр может использовать ноль или одну заметку буфера.</span><span class="sxs-lookup"><span data-stu-id="ce766-130">Each parameter may use zero or one buffer annotation.</span></span> <span data-ttu-id="ce766-131">Заметка буфера создается с помощью подчеркивания в начале и компонентов, описанных в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="ce766-131">A buffer annotation is constructed with a leading underscore and the components described in the following sections.</span></span>



| <span data-ttu-id="ce766-132">Размер буфера</span><span class="sxs-lookup"><span data-stu-id="ce766-132">Buffer size</span></span>                                                                                  | <span data-ttu-id="ce766-133">Описание</span><span class="sxs-lookup"><span data-stu-id="ce766-133">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce766-134"><span id="_size_"></span><span id="_SIZE_"></span>(*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-134"><span id="_size_"></span><span id="_SIZE_"></span>(*size*)</span></span><br/>                        | <span data-ttu-id="ce766-135">Задает общий размер буфера.</span><span class="sxs-lookup"><span data-stu-id="ce766-135">Specifies the total size of the buffer.</span></span> <span data-ttu-id="ce766-136">Используйте с \_ бкаунт и \_ екаунт; не используйте с \_ компонентом Part.</span><span class="sxs-lookup"><span data-stu-id="ce766-136">Use with \_bcount and \_ecount; do not use with \_part.</span></span> <span data-ttu-id="ce766-137">Это значение представляет собой доступное пространство; оно может быть меньше выделенного пространства.</span><span class="sxs-lookup"><span data-stu-id="ce766-137">This value is the accessible space; it may be less than the allocated space.</span></span><br/> |
| <span data-ttu-id="ce766-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)</span></span><br/> | <span data-ttu-id="ce766-139">Задает общий размер и инициализированную длину буфера.</span><span class="sxs-lookup"><span data-stu-id="ce766-139">Specifies the total size and initialized length of the buffer.</span></span> <span data-ttu-id="ce766-140">Используйте с \_ бкаунт \_ частью и \_ \_ частью екаунт.</span><span class="sxs-lookup"><span data-stu-id="ce766-140">Use with \_bcount\_part and \_ecount\_part.</span></span> <span data-ttu-id="ce766-141">Общий размер может быть меньше выделенного пространства.</span><span class="sxs-lookup"><span data-stu-id="ce766-141">The total size may be less than the allocated space.</span></span><br/>              |



 



| <span data-ttu-id="ce766-142">Единицы размера буфера</span><span class="sxs-lookup"><span data-stu-id="ce766-142">Buffer size units</span></span>                                                       | <span data-ttu-id="ce766-143">Описание</span><span class="sxs-lookup"><span data-stu-id="ce766-143">Description</span></span>                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="ce766-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_бкаунт</span><span class="sxs-lookup"><span data-stu-id="ce766-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span></span><br/> | <span data-ttu-id="ce766-145">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="ce766-145">The buffer size is in bytes.</span></span><br/>    |
| <span data-ttu-id="ce766-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_екаунт</span><span class="sxs-lookup"><span data-stu-id="ce766-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span></span><br/> | <span data-ttu-id="ce766-147">Размер буфера находится в элементах.</span><span class="sxs-lookup"><span data-stu-id="ce766-147">The buffer size is in elements.</span></span><br/> |



 



| <span data-ttu-id="ce766-148">Направление</span><span class="sxs-lookup"><span data-stu-id="ce766-148">Direction</span></span>                                                            | <span data-ttu-id="ce766-149">Описание</span><span class="sxs-lookup"><span data-stu-id="ce766-149">Description</span></span>                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce766-150"><span id="_in"></span><span id="_IN"></span>\_окне</span><span class="sxs-lookup"><span data-stu-id="ce766-150"><span id="_in"></span><span id="_IN"></span>\_in</span></span><br/>          | <span data-ttu-id="ce766-151">Функция считывает данные из буфера.</span><span class="sxs-lookup"><span data-stu-id="ce766-151">The function reads from the buffer.</span></span> <span data-ttu-id="ce766-152">Вызывающий объект предоставляет буфер и инициализирует его.</span><span class="sxs-lookup"><span data-stu-id="ce766-152">The caller provides the buffer and initializes it.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="ce766-153"><span id="_inout"></span><span id="_INOUT"></span>\_Inout</span><span class="sxs-lookup"><span data-stu-id="ce766-153"><span id="_inout"></span><span id="_INOUT"></span>\_inout</span></span><br/> | <span data-ttu-id="ce766-154">Функция выполняет чтение из буфера и запись в буфер.</span><span class="sxs-lookup"><span data-stu-id="ce766-154">The function both reads from and writes to buffer.</span></span> <span data-ttu-id="ce766-155">Вызывающий объект предоставляет буфер и инициализирует его.</span><span class="sxs-lookup"><span data-stu-id="ce766-155">The caller provides the buffer and initializes it.</span></span> <span data-ttu-id="ce766-156">При использовании с \_ DEREF буфер может быть повторно выделен функцией.</span><span class="sxs-lookup"><span data-stu-id="ce766-156">If used with \_deref, the buffer may be reallocated by the function.</span></span><br/>                                      |
| <span data-ttu-id="ce766-157"><span id="_out"></span><span id="_OUT"></span>\_заполняет</span><span class="sxs-lookup"><span data-stu-id="ce766-157"><span id="_out"></span><span id="_OUT"></span>\_out</span></span><br/>       | <span data-ttu-id="ce766-158">Функция записывает данные в буфер.</span><span class="sxs-lookup"><span data-stu-id="ce766-158">The function writes to the buffer.</span></span> <span data-ttu-id="ce766-159">Если используется в возвращаемом значении или с параметром \_ DEREF, функция предоставляет буфер и инициализирует ее.</span><span class="sxs-lookup"><span data-stu-id="ce766-159">If used on the return value or with \_deref, the function provides the buffer and initializes it.</span></span> <span data-ttu-id="ce766-160">В противном случае вызывающий объект предоставляет буфер, а функция инициализирует его.</span><span class="sxs-lookup"><span data-stu-id="ce766-160">Otherwise, the caller provides the buffer and the function initializes it.</span></span><br/> |



 



| <span data-ttu-id="ce766-161">Косвенное обращение</span><span class="sxs-lookup"><span data-stu-id="ce766-161">Indirection</span></span>                                                                       | <span data-ttu-id="ce766-162">Описание</span><span class="sxs-lookup"><span data-stu-id="ce766-162">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce766-163"><span id="_deref"></span><span id="_DEREF"></span>\_Deref</span><span class="sxs-lookup"><span data-stu-id="ce766-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span></span><br/>              | <span data-ttu-id="ce766-164">Чтобы получить указатель на буфер, необходимо выполнить разыменование параметра.</span><span class="sxs-lookup"><span data-stu-id="ce766-164">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="ce766-165">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ce766-165">This parameter may not be **NULL**.</span></span><br/> |
| <span data-ttu-id="ce766-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_Deref \_ OPT</span><span class="sxs-lookup"><span data-stu-id="ce766-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref\_opt</span></span><br/> | <span data-ttu-id="ce766-167">Чтобы получить указатель на буфер, необходимо выполнить разыменование параметра.</span><span class="sxs-lookup"><span data-stu-id="ce766-167">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="ce766-168">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ce766-168">This parameter can be **NULL**.</span></span><br/>     |



 



| <span data-ttu-id="ce766-169">Инициализация</span><span class="sxs-lookup"><span data-stu-id="ce766-169">Initialization</span></span>                                                    | <span data-ttu-id="ce766-170">Описание</span><span class="sxs-lookup"><span data-stu-id="ce766-170">Description</span></span>                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce766-171"><span id="_full"></span><span id="_FULL"></span>\_полный</span><span class="sxs-lookup"><span data-stu-id="ce766-171"><span id="_full"></span><span id="_FULL"></span>\_full</span></span><br/> | <span data-ttu-id="ce766-172">Функция инициализирует весь буфер.</span><span class="sxs-lookup"><span data-stu-id="ce766-172">The function initializes the entire buffer.</span></span> <span data-ttu-id="ce766-173">Используйте только с выходными буферами.</span><span class="sxs-lookup"><span data-stu-id="ce766-173">Use only with output buffers.</span></span><br/>                                     |
| <span data-ttu-id="ce766-174"><span id="_part"></span><span id="_PART"></span>\_блок</span><span class="sxs-lookup"><span data-stu-id="ce766-174"><span id="_part"></span><span id="_PART"></span>\_part</span></span><br/> | <span data-ttu-id="ce766-175">Функция инициализирует часть буфера и явно указывает, сколько.</span><span class="sxs-lookup"><span data-stu-id="ce766-175">The function initializes part of the buffer, and explicitly indicates how much.</span></span> <span data-ttu-id="ce766-176">Используйте только с выходными буферами.</span><span class="sxs-lookup"><span data-stu-id="ce766-176">Use only with output buffers.</span></span><br/> |



 



| <span data-ttu-id="ce766-177">Обязательный или необязательный буфер</span><span class="sxs-lookup"><span data-stu-id="ce766-177">Required or optional buffer</span></span>                                    | <span data-ttu-id="ce766-178">Описание</span><span class="sxs-lookup"><span data-stu-id="ce766-178">Description</span></span>                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="ce766-179"><span id="_opt"></span><span id="_OPT"></span>\_участие</span><span class="sxs-lookup"><span data-stu-id="ce766-179"><span id="_opt"></span><span id="_OPT"></span>\_opt</span></span><br/> | <span data-ttu-id="ce766-180">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ce766-180">This parameter can be **NULL**.</span></span><br/> |



 

<span data-ttu-id="ce766-181">В следующем примере показаны аннотации для функции **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="ce766-181">The following example shows the annotations for the **GetModuleFileName** function.</span></span> <span data-ttu-id="ce766-182">Параметр *хмодуле* является необязательным входным параметром.</span><span class="sxs-lookup"><span data-stu-id="ce766-182">The *hModule* parameter is an optional input parameter .</span></span> <span data-ttu-id="ce766-183">Параметр *лпфиленаме* является выходным параметром. его размер в символах задается параметром *нсизе* , а его длина включает символ, завершающийся **нулем**.</span><span class="sxs-lookup"><span data-stu-id="ce766-183">The *lpFilename* parameter is an output parameter; its size in characters is specified by the *nSize* parameter and its length includes the **null**-terminating character.</span></span> <span data-ttu-id="ce766-184">Параметр *нсизе* является входным параметром.</span><span class="sxs-lookup"><span data-stu-id="ce766-184">The *nSize* parameter is an input parameter.</span></span>


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



<span data-ttu-id="ce766-185">Ниже приведены аннотации, определенные в Спекстрингс. h.</span><span class="sxs-lookup"><span data-stu-id="ce766-185">The following are the annotations defined in Specstrings.h.</span></span> <span data-ttu-id="ce766-186">Используйте сведения в приведенных выше таблицах, чтобы интерпретировать их значения.</span><span class="sxs-lookup"><span data-stu-id="ce766-186">Use the information in the tables above to interpret their meaning.</span></span>

<span data-ttu-id="ce766-187">__bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-187">__bcount(*size*)</span></span>  
<span data-ttu-id="ce766-188">__bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-188">__bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-189">__deref_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-189">__deref_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-190">__deref_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-190">__deref_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-191">__deref_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-191">__deref_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-192">__deref_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-192">__deref_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-193">__deref_in</span><span class="sxs-lookup"><span data-stu-id="ce766-193">__deref_in</span></span>  
<span data-ttu-id="ce766-194">__deref_in_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-194">__deref_in_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-195">__deref_in_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-195">__deref_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-196">__deref_in_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-196">__deref_in_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-197">__deref_in_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-197">__deref_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-198">__deref_in_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-198">__deref_in_opt</span></span>  
<span data-ttu-id="ce766-199">__deref_inout</span><span class="sxs-lookup"><span data-stu-id="ce766-199">__deref_inout</span></span>  
<span data-ttu-id="ce766-200">__deref_inout_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-200">__deref_inout_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-201">__deref_inout_bcount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-201">__deref_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="ce766-202">__deref_inout_bcount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-202">__deref_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-203">__deref_inout_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-203">__deref_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-204">__deref_inout_bcount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-204">__deref_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-205">__deref_inout_bcount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-205">__deref_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-206">__deref_inout_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-206">__deref_inout_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-207">__deref_inout_ecount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-207">__deref_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="ce766-208">__deref_inout_ecount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-208">__deref_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-209">__deref_inout_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-209">__deref_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-210">__deref_inout_ecount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-210">__deref_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-211">__deref_inout_ecount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-211">__deref_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-212">__deref_inout_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-212">__deref_inout_opt</span></span>  
<span data-ttu-id="ce766-213">__deref_opt_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-213">__deref_opt_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-214">__deref_opt_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-214">__deref_opt_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-215">__deref_opt_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-215">__deref_opt_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-216">__deref_opt_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-216">__deref_opt_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-217">__deref_opt_in</span><span class="sxs-lookup"><span data-stu-id="ce766-217">__deref_opt_in</span></span>  
<span data-ttu-id="ce766-218">__deref_opt_in_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-218">__deref_opt_in_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-219">__deref_opt_in_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-219">__deref_opt_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-220">__deref_opt_in_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-220">__deref_opt_in_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-221">__deref_opt_in_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-221">__deref_opt_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-222">__deref_opt_in_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-222">__deref_opt_in_opt</span></span>  
<span data-ttu-id="ce766-223">__deref_opt_inout</span><span class="sxs-lookup"><span data-stu-id="ce766-223">__deref_opt_inout</span></span>  
<span data-ttu-id="ce766-224">__deref_opt_inout_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-224">__deref_opt_inout_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-225">__deref_opt_inout_bcount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-225">__deref_opt_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="ce766-226">__deref_opt_inout_bcount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-226">__deref_opt_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-227">__deref_opt_inout_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-227">__deref_opt_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-228">__deref_opt_inout_bcount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-228">__deref_opt_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-229">__deref_opt_inout_bcount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-229">__deref_opt_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-230">__deref_opt_inout_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-230">__deref_opt_inout_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-231">__deref_opt_inout_ecount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-231">__deref_opt_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="ce766-232">__deref_opt_inout_ecount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-232">__deref_opt_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-233">__deref_opt_inout_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-233">__deref_opt_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-234">__deref_opt_inout_ecount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-234">__deref_opt_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-235">__deref_opt_inout_ecount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-235">__deref_opt_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-236">__deref_opt_inout_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-236">__deref_opt_inout_opt</span></span>  
<span data-ttu-id="ce766-237">__deref_opt_out</span><span class="sxs-lookup"><span data-stu-id="ce766-237">__deref_opt_out</span></span>  
<span data-ttu-id="ce766-238">__deref_opt_out_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-238">__deref_opt_out_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-239">__deref_opt_out_bcount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-239">__deref_opt_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="ce766-240">__deref_opt_out_bcount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-240">__deref_opt_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-241">__deref_opt_out_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-241">__deref_opt_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-242">__deref_opt_out_bcount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-242">__deref_opt_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-243">__deref_opt_out_bcount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-243">__deref_opt_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-244">__deref_opt_out_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-244">__deref_opt_out_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-245">__deref_opt_out_ecount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-245">__deref_opt_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="ce766-246">__deref_opt_out_ecount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-246">__deref_opt_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-247">__deref_opt_out_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-247">__deref_opt_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-248">__deref_opt_out_ecount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-248">__deref_opt_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-249">__deref_opt_out_ecount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-249">__deref_opt_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-250">__deref_opt_out_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-250">__deref_opt_out_opt</span></span>  
<span data-ttu-id="ce766-251">__deref_out</span><span class="sxs-lookup"><span data-stu-id="ce766-251">__deref_out</span></span>  
<span data-ttu-id="ce766-252">__deref_out_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-252">__deref_out_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-253">__deref_out_bcount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-253">__deref_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="ce766-254">__deref_out_bcount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-254">__deref_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-255">__deref_out_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-255">__deref_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-256">__deref_out_bcount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-256">__deref_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-257">__deref_out_bcount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-257">__deref_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-258">__deref_out_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-258">__deref_out_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-259">__deref_out_ecount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-259">__deref_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="ce766-260">__deref_out_ecount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-260">__deref_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-261">__deref_out_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-261">__deref_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-262">__deref_out_ecount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-262">__deref_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-263">__deref_out_ecount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-263">__deref_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-264">__deref_out_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-264">__deref_out_opt</span></span>  
<span data-ttu-id="ce766-265">__ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-265">__ecount(*size*)</span></span>  
<span data-ttu-id="ce766-266">__ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-266">__ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-267">__in</span><span class="sxs-lookup"><span data-stu-id="ce766-267">__in</span></span>  
<span data-ttu-id="ce766-268">__in_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-268">__in_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-269">__in_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-269">__in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-270">__in_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-270">__in_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-271">__in_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-271">__in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-272">__in_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-272">__in_opt</span></span>  
<span data-ttu-id="ce766-273">__inout</span><span class="sxs-lookup"><span data-stu-id="ce766-273">__inout</span></span>  
<span data-ttu-id="ce766-274">__inout_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-274">__inout_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-275">__inout_bcount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-275">__inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="ce766-276">__inout_bcount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-276">__inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-277">__inout_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-277">__inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-278">__inout_bcount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-278">__inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-279">__inout_bcount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-279">__inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-280">__inout_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-280">__inout_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-281">__inout_ecount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-281">__inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="ce766-282">__inout_ecount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-282">__inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-283">__inout_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-283">__inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-284">__inout_ecount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-284">__inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-285">__inout_ecount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-285">__inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-286">__inout_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-286">__inout_opt</span></span>  
<span data-ttu-id="ce766-287">__out</span><span class="sxs-lookup"><span data-stu-id="ce766-287">__out</span></span>  
<span data-ttu-id="ce766-288">__out_bcount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-288">__out_bcount(*size*)</span></span>  
<span data-ttu-id="ce766-289">__out_bcount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-289">__out_bcount_full(*size*)</span></span>  
<span data-ttu-id="ce766-290">__out_bcount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-290">__out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-291">__out_bcount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-291">__out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-292">__out_bcount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-292">__out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-293">__out_bcount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-293">__out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-294">__out_ecount (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-294">__out_ecount(*size*)</span></span>  
<span data-ttu-id="ce766-295">__out_ecount_full (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-295">__out_ecount_full(*size*)</span></span>  
<span data-ttu-id="ce766-296">__out_ecount_full_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-296">__out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="ce766-297">__out_ecount_opt (*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-297">__out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="ce766-298">__out_ecount_part (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-298">__out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-299">__out_ecount_part_opt (*Размер*,*Длина*)</span><span class="sxs-lookup"><span data-stu-id="ce766-299">__out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="ce766-300">__out_opt</span><span class="sxs-lookup"><span data-stu-id="ce766-300">__out_opt</span></span>  

## <a name="advanced-annotations"></a><span data-ttu-id="ce766-301">Дополнительные заметки</span><span class="sxs-lookup"><span data-stu-id="ce766-301">Advanced Annotations</span></span>

<span data-ttu-id="ce766-302">Дополнительные заметки содержат дополнительные сведения о параметре или возвращаемом значении.</span><span class="sxs-lookup"><span data-stu-id="ce766-302">Advanced annotations provide additional information about the parameter or return value.</span></span> <span data-ttu-id="ce766-303">Каждый параметр или возвращаемое значение могут использовать одну или несколько дополнительных аннотаций.</span><span class="sxs-lookup"><span data-stu-id="ce766-303">Each parameter or return value may use zero or one advanced annotation.</span></span>



| <span data-ttu-id="ce766-304">Annotation</span><span class="sxs-lookup"><span data-stu-id="ce766-304">Annotation</span></span>                                                                                                                                               | <span data-ttu-id="ce766-305">Описание</span><span class="sxs-lookup"><span data-stu-id="ce766-305">Description</span></span>                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce766-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_Блокксон (*ресурс*)</span><span class="sxs-lookup"><span data-stu-id="ce766-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)</span></span><br/> | <span data-ttu-id="ce766-307">Функции блокируют указанный ресурс.</span><span class="sxs-lookup"><span data-stu-id="ce766-307">The functions blocks on the specified resource.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="ce766-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_обратного вызова</span><span class="sxs-lookup"><span data-stu-id="ce766-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback</span></span><br/>                                                                        | <span data-ttu-id="ce766-309">Функцию можно использовать в качестве указателя функции.</span><span class="sxs-lookup"><span data-stu-id="ce766-309">The function can be used as a function pointer.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="ce766-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_Аннотация checkReturn применяется</span><span class="sxs-lookup"><span data-stu-id="ce766-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span></span><br/>                               | <span data-ttu-id="ce766-311">Вызывающие объекты должны проверить возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="ce766-311">Callers must check the return value.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="ce766-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_\_строка формата</span><span class="sxs-lookup"><span data-stu-id="ce766-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_format\_string</span></span><br/>                                                        | <span data-ttu-id="ce766-313">Параметр представляет собой строку, содержащую маркеры типа "printf-Style%".</span><span class="sxs-lookup"><span data-stu-id="ce766-313">The parameter is a string that contains printf-style % markers.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="ce766-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_в \_ авкаунт (*expr*,*size*)</span><span class="sxs-lookup"><span data-stu-id="ce766-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in\_awcount(*expr*,*size*)</span></span><br/>                            | <span data-ttu-id="ce766-315">Если выражение имеет значение true при выходе, то размер входного буфера указывается в байтах.</span><span class="sxs-lookup"><span data-stu-id="ce766-315">If the expression is true at exit, the size of the input buffer is specified in bytes.</span></span> <span data-ttu-id="ce766-316">Если выражение имеет значение false, то размер задается в элементах.</span><span class="sxs-lookup"><span data-stu-id="ce766-316">If the expression is false, the size is specified in elements.</span></span><br/>                                                                                                                |
| <span data-ttu-id="ce766-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_нуллнуллтерминатед</span><span class="sxs-lookup"><span data-stu-id="ce766-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span></span><br/>                                          | <span data-ttu-id="ce766-318">Доступ к буферу можно получить, добавив в него первую последовательность из двух **пустых** символов или указателей.</span><span class="sxs-lookup"><span data-stu-id="ce766-318">The buffer may be accessed up to and including the first sequence of two **null** characters or pointers.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="ce766-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated</span><span class="sxs-lookup"><span data-stu-id="ce766-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated</span></span><br/>                                                      | <span data-ttu-id="ce766-320">Доступ к буферу можно получить, добавив в него первый символ или указатель **null** .</span><span class="sxs-lookup"><span data-stu-id="ce766-320">The buffer may be accessed up to and including the first **null** character or pointer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="ce766-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ авкаунт (*выражение*,*Размер*)</span><span class="sxs-lookup"><span data-stu-id="ce766-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out\_awcount(*expr*,*size*)</span></span><br/>                         | <span data-ttu-id="ce766-322">Если выражение имеет значение true при выходе, размер выходного буфера указывается в байтах.</span><span class="sxs-lookup"><span data-stu-id="ce766-322">If the expression is true at exit, the size of the output buffer is specified in bytes.</span></span> <span data-ttu-id="ce766-323">Если выражение имеет значение false, то размер задается в элементах.</span><span class="sxs-lookup"><span data-stu-id="ce766-323">If the expression is false, the size is specified in elements.</span></span> <br/>                                                                                                              |
| <span data-ttu-id="ce766-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_крывают</span><span class="sxs-lookup"><span data-stu-id="ce766-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_override</span></span><br/>                                                                        | <span data-ttu-id="ce766-325">Задает поведение переопределения в стиле C# для виртуальных методов.</span><span class="sxs-lookup"><span data-stu-id="ce766-325">Specifies C#-style override behavior for virtual methods.</span></span><br/>                                                                                                                                                                                                           |
| <span data-ttu-id="ce766-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_процессу</span><span class="sxs-lookup"><span data-stu-id="ce766-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_reserved</span></span><br/>                                                                        | <span data-ttu-id="ce766-327">Параметр зарезервирован для будущего использования и должен быть равен нулю или иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ce766-327">The parameter is reserved for future use and must be zero or **NULL**.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="ce766-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_успешное завершение (*expr*)</span><span class="sxs-lookup"><span data-stu-id="ce766-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)</span></span><br/>                                                       | <span data-ttu-id="ce766-329">Если выражение имеет значение true при выходе, вызывающий объект может полагаться на все гарантии, заданные другими заметками.</span><span class="sxs-lookup"><span data-stu-id="ce766-329">If the expression is true at exit, the caller can rely on all guarantees specified by other annotations.</span></span> <span data-ttu-id="ce766-330">Если выражение имеет значение false, вызывающий объект не может полагаться на гарантии.</span><span class="sxs-lookup"><span data-stu-id="ce766-330">If the expression is false, the caller cannot rely on the guarantees.</span></span> <span data-ttu-id="ce766-331">Эта заметка автоматически добавляется к функциям, которые возвращают значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce766-331">This annotation is automatically added to functions that return an **HRESULT** value.</span></span><br/> |
| <span data-ttu-id="ce766-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)</span><span class="sxs-lookup"><span data-stu-id="ce766-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)</span></span><br/>                                                    | <span data-ttu-id="ce766-333">Рассматривайте параметр как указанный тип, а не его объявленный тип.</span><span class="sxs-lookup"><span data-stu-id="ce766-333">Treat the parameter as the specified type rather than its declared type.</span></span><br/>                                                                                                                                                                                             |



 

<span data-ttu-id="ce766-334">В следующих примерах показаны буфер и дополнительные заметки для функций [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**фриенвиронментстрингс**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)и [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .</span><span class="sxs-lookup"><span data-stu-id="ce766-334">The following examples show the buffer and advanced annotations for the [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa), and [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) functions.</span></span>


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a><span data-ttu-id="ce766-335">См. также</span><span class="sxs-lookup"><span data-stu-id="ce766-335">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce766-336">Аннотации SAL</span><span class="sxs-lookup"><span data-stu-id="ce766-336">SAL Annotations</span></span>](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="ce766-337">Пошаговое руководство. Проверка кода C/C++ на наличие дефектов</span><span class="sxs-lookup"><span data-stu-id="ce766-337">Walkthrough: Analyzing C/C++ Code for Defects</span></span>](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

