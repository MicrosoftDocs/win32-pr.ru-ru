---
title: cpp_cmd Switch
description: '\_Параметр cmd/КПП указывает препроцессор, который КОМПИЛЯТОР MIDL использует для предварительной обработки входных файлов.'
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd параметр MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784233"
---
# <a name="cpp_cmd-switch"></a><span data-ttu-id="90543-104">/КПП \_ cmd Switch</span><span class="sxs-lookup"><span data-stu-id="90543-104">/cpp\_cmd switch</span></span>

<span data-ttu-id="90543-105">Параметр **\_ cmd/КПП** Указывает препроцессор, который компилятор MIDL использует для предварительной обработки входных файлов.</span><span class="sxs-lookup"><span data-stu-id="90543-105">The **/cpp\_cmd** switch specifies the preprocessor that the MIDL compiler uses to preprocess input files.</span></span>

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a><span data-ttu-id="90543-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="90543-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="90543-107">*\_Двоичный файл препроцессора C \_*</span><span class="sxs-lookup"><span data-stu-id="90543-107">*C\_preprocessor\_binary*</span></span> 
</dt> <dd>

<span data-ttu-id="90543-108">Указывает команду, вызывающую препроцессор.</span><span class="sxs-lookup"><span data-stu-id="90543-108">Specifies the command that invokes the preprocessor.</span></span> <span data-ttu-id="90543-109">Эта команда позволяет разработчикам переопределить препроцессор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90543-109">This command allows developers to override the default preprocessor.</span></span> <span data-ttu-id="90543-110">По умолчанию MIDL вызывает компилятор Microsoft C/C++ из среды сборки компьютера сборки.</span><span class="sxs-lookup"><span data-stu-id="90543-110">By default, MIDL invokes the Microsoft C/C++ compiler from the build machine's build environment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90543-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90543-111">Remarks</span></span>

<span data-ttu-id="90543-112">*\_ \_ Двоичный аргумент препроцессора C* для параметра может указывать полный путь; суффикс exe и кавычки являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="90543-112">The *C\_preprocessor\_binary* argument to the switch may specify the full path; the exe suffix and quotes are optional.</span></span> <span data-ttu-id="90543-113">Как правило, разработчики используют параметр, чтобы выбрать конкретную версию препроцессора Microsoft C/C++ или аналог в среде сборки.</span><span class="sxs-lookup"><span data-stu-id="90543-113">Typically, developers use the switch to choose a particular version of the Microsoft C/C++ preprocessor or equivalent in the build environment.</span></span> <span data-ttu-id="90543-114">В этом случае нет необходимости использовать параметр [**/КПП \_ OPT**](-cpp-opt.md) с **/КПП \_ cmd**.</span><span class="sxs-lookup"><span data-stu-id="90543-114">In this case, it is not necessary to use the [**/cpp\_opt**](-cpp-opt.md) switch with **/cpp\_cmd**.</span></span>

<span data-ttu-id="90543-115">При использовании препроцессора, не относящегося к Майкрософт, особенно если указанный препроцессор не направляет выходные данные в stdout, необходимо указать параметр компилятора C, который перенаправляет выходные данные в stdout в рамках компилятора MIDL, [**/КПП параметр \_ OPT**](-cpp-opt.md) .</span><span class="sxs-lookup"><span data-stu-id="90543-115">When using a non-Microsoft preprocessor, especially when the specified preprocessor does not direct its output to stdout, the C compiler switch that redirects output to stdout as part of the MIDL compiler [**/cpp\_opt**](-cpp-opt.md) switch must be specified.</span></span> <span data-ttu-id="90543-116">Дополнительные сведения см. [в разделе Требования к препроцессору для MIDL](c-preprocessor-requirements-for-midl.md) .</span><span class="sxs-lookup"><span data-stu-id="90543-116">See [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for details</span></span>

<span data-ttu-id="90543-117">Препроцессор вызывается строкой команды, сформированной из информации, предоставленной компилятором MIDL с помощью **/КПП \_ cmd**, [**/КПП \_ OPT**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)и [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="90543-117">The preprocessor is invoked by a command string that is formed from the information provided to the MIDL compiler by **/cpp\_cmd**, [**/cpp\_opt**](-cpp-opt.md), [**/D**](-d.md), [**/I**](-i.md), and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="90543-118">В следующей таблице приведена сводка по построению командной строки для каждого сочетания **/КПП \_ cmd** и параметров **/КПП \_ OPT** .</span><span class="sxs-lookup"><span data-stu-id="90543-118">The following table summarizes how the command string is constructed for each combination of **/cpp\_cmd** and **/cpp\_opt** switches.</span></span>

<span data-ttu-id="90543-119">Если параметр **\_ cmd/КПП** не указан, компилятор MIDL вызывает компилятор Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="90543-119">When the **/cpp\_cmd** switch is not specified, the MIDL compiler invokes the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="90543-120">MIDL использует Cl.exe двоичный файл, находящийся в среде сборки.</span><span class="sxs-lookup"><span data-stu-id="90543-120">MIDL uses a Cl.exe binary found in the build environment.</span></span>

<span data-ttu-id="90543-121">Если параметр [**/КПП \_ OPT**](-cpp-opt.md) отсутствует, компилятор MIDL объединяет строку, указанную параметром **/КПП \_ cmd** , со сведениями, указанными в параметрах MIDL [**/i**](-i.md), [**/d**](-d.md) и [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="90543-121">When the [**/cpp\_opt**](-cpp-opt.md) switch is not present, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the information specified by the MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) options.</span></span> <span data-ttu-id="90543-122">Строка/E также объединяется в строку вызова C-компилятора, чтобы указать, что компилятор C/C++ должен выполнять только предварительную обработку.</span><span class="sxs-lookup"><span data-stu-id="90543-122">The string /E is also concatenated to the C-compiler invocation string to indicate that the C/C++ compiler should perform preprocessing only.</span></span> <span data-ttu-id="90543-123">Для подавления заголовка компилятора C/C++ добавляется параметр [**/nologo**](-nologo.md) .</span><span class="sxs-lookup"><span data-stu-id="90543-123">The [**/nologo**](-nologo.md) switch is added to suppress the C/C++ compiler banner.</span></span> <span data-ttu-id="90543-124">Компилятор MIDL использует объединенную строку для вызова препроцессора C для IDL верхнего уровня, а также импортированных IDL-файлов, а также для всех имеющихся, соответствующих файлов ACF.</span><span class="sxs-lookup"><span data-stu-id="90543-124">The MIDL compiler uses the concatenated string to invoke the C preprocessor for top-level IDL as well as imported IDL files, and also for any present, corresponding ACF files.</span></span>

<span data-ttu-id="90543-125">Если имеется переключатель [**/КПП \_ OPT**](-cpp-opt.md) , который является редким случаем для текущих 32-разрядных и 64-разрядных платформ, компилятор MIDL объединяет строку, указанную параметром **/КПП \_ cmd** , со строкой, заданной параметром **\_ OPT/КПП** .</span><span class="sxs-lookup"><span data-stu-id="90543-125">When the [**/cpp\_opt**](-cpp-opt.md) switch is present, which should be a rare case for the current 32-bit and 64-bit platforms, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the string specified by the **/cpp\_opt** switch.</span></span> <span data-ttu-id="90543-126">Компилятор MIDL использует объединенную строку для вызова указанного двоичного файла препроцессора вместо препроцессора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90543-126">The MIDL compiler uses the concatenated string to invoke the indicated preprocessor binary in place of the default preprocessor.</span></span> <span data-ttu-id="90543-127">Если указан **параметр/КПП \_ OPT** , ни параметры компилятора MIDL, заданные с помощью ключей [**/I**](-i.md), [**/d**](-d.md)и [**/u**](-u.md) , ни параметр компилятора C не соединены со строкой.</span><span class="sxs-lookup"><span data-stu-id="90543-127">When the **/cpp\_opt** switch is present, neither the MIDL compiler options specified by the [**/I**](-i.md), [**/D**](-d.md), and [**/U**](-u.md) switches nor the C compiler switch /E is concatenated with the string.</span></span> <span data-ttu-id="90543-128">Необходимо указать параметр/E или его эквивалент в составе строки.</span><span class="sxs-lookup"><span data-stu-id="90543-128">You must supply the /E option, or equivalent, as part of the string.</span></span>



| <span data-ttu-id="90543-129">/КПП \_ cmd?</span><span class="sxs-lookup"><span data-stu-id="90543-129">/cpp\_cmd present?</span></span> | <span data-ttu-id="90543-130">/КПП \_ OPT?</span><span class="sxs-lookup"><span data-stu-id="90543-130">/cpp\_opt present?</span></span> | <span data-ttu-id="90543-131">Описание</span><span class="sxs-lookup"><span data-stu-id="90543-131">Description</span></span>                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90543-132">Нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90543-132">No (default)</span></span>       | <span data-ttu-id="90543-133">Нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90543-133">No (default)</span></span>       | <span data-ttu-id="90543-134">Вызывает компилятор Microsoft C/C++ по умолчанию с параметрами, полученными из ключей MIDL [**/i**](-i.md), [**/d**](-d.md) и [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="90543-134">Invokes the default Microsoft C/C++ compiler with settings obtained from MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="90543-135">Добавляет параметры препроцессора/E и [**/nologo**](-nologo.md).</span><span class="sxs-lookup"><span data-stu-id="90543-135">Adds the preprocessor switches /E and [**/nologo**](-nologo.md).</span></span> |
| <span data-ttu-id="90543-136">Да</span><span class="sxs-lookup"><span data-stu-id="90543-136">Yes</span></span>                | <span data-ttu-id="90543-137">Нет</span><span class="sxs-lookup"><span data-stu-id="90543-137">No</span></span>                 | <span data-ttu-id="90543-138">Вызывает указанный двоичный файл препроцессора с теми же параметрами, что и выше.</span><span class="sxs-lookup"><span data-stu-id="90543-138">Invokes the indicated preprocessor binary with the same switches as above.</span></span>                                                                                                                                        |
| <span data-ttu-id="90543-139">Нет</span><span class="sxs-lookup"><span data-stu-id="90543-139">No</span></span>                 | <span data-ttu-id="90543-140">Да</span><span class="sxs-lookup"><span data-stu-id="90543-140">Yes</span></span>                | <span data-ttu-id="90543-141">Вызывает компилятор Microsoft C с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="90543-141">Invokes the Microsoft C compiler with specified options.</span></span> <span data-ttu-id="90543-142">Не использует параметры MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="90543-142">Does not use MIDL [**/I**](-i.md), [**/D**](-d.md), [**/U**](-u.md) options.</span></span> <span data-ttu-id="90543-143">Необходимо указать/E в качестве части [**/КПП \_ OPT**](-cpp-opt.md).</span><span class="sxs-lookup"><span data-stu-id="90543-143">You must supply /E as part of [**/cpp\_opt**](-cpp-opt.md).</span></span>             |
| <span data-ttu-id="90543-144">Да</span><span class="sxs-lookup"><span data-stu-id="90543-144">Yes</span></span>                | <span data-ttu-id="90543-145">Да</span><span class="sxs-lookup"><span data-stu-id="90543-145">Yes</span></span>                | <span data-ttu-id="90543-146">Вызывает указанный двоичный файл препроцессора только с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="90543-146">Invokes the specified preprocessor binary with specified options only.</span></span> <span data-ttu-id="90543-147">Необходимо использовать кавычки.</span><span class="sxs-lookup"><span data-stu-id="90543-147">You must use quotes.</span></span>                                                                                                                       |



 

## <a name="examples"></a><span data-ttu-id="90543-148">Примеры</span><span class="sxs-lookup"><span data-stu-id="90543-148">Examples</span></span>

<span data-ttu-id="90543-149">**MIDL/КПП \_ cmd d: \\ NT \\ tools \\ ia64 \\cl.exe/дфлаг = true/ИК: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="90543-149">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="90543-150">**MIDL/КПП \_ cmd "микпп"/дфлаг = true/ИК: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="90543-150">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="90543-151">**MIDL/КПП \_ OPT "/E/дфлаг = true/ИК: \\ Inc" имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="90543-151">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="90543-152">**MIDL/КПП \_ cmd "CL"/КПП \_ OPT "/e/ДФЛАГ = true/ИК: \\ Inc" имя_файла. idl**</span><span class="sxs-lookup"><span data-stu-id="90543-152">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="90543-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90543-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90543-154">**/савепп**</span><span class="sxs-lookup"><span data-stu-id="90543-154">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="90543-155">**/КПП \_ OPT**</span><span class="sxs-lookup"><span data-stu-id="90543-155">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="90543-156">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="90543-156">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="90543-157">**/но \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="90543-157">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="90543-158">Требования к препроцессору C-препроцессор для MIDL</span><span class="sxs-lookup"><span data-stu-id="90543-158">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




