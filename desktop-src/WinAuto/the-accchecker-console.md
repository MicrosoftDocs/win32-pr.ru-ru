---
title: Консоль Аккчеккер
description: Консоль Аккчеккер (AccCheckConsole.exe) — это средство командной строки для проверки реализации специальных возможностей пользовательского интерфейса приложения.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Консоль Аккчеккер
- Программа командной строки Аккчеккер
- Командная строка, Аккчеккер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887792"
---
# <a name="the-accchecker-console"></a><span data-ttu-id="b0af8-106">Консоль Аккчеккер</span><span class="sxs-lookup"><span data-stu-id="b0af8-106">The AccChecker Console</span></span>

<span data-ttu-id="b0af8-107">Консоль Аккчеккер (AccCheckConsole.exe) — это средство командной строки для проверки реализации специальных возможностей пользовательского интерфейса приложения.</span><span class="sxs-lookup"><span data-stu-id="b0af8-107">AccChecker Console (AccCheckConsole.exe) is a command-line tool for verifying the accessibility implementation of your application's UI.</span></span> <span data-ttu-id="b0af8-108">Командная строка принимает различные входные данные (например, HWND, заголовок окна и подпрограммы проверки) и предоставляет код выхода, соответствующий количеству журналов ошибок.</span><span class="sxs-lookup"><span data-stu-id="b0af8-108">The command-line accepts a variety of inputs (such as HWND, window title, and verification routine) and supplies an exit code that corresponds to the error log count.</span></span>

-   [<span data-ttu-id="b0af8-109">Синтаксис командной строки</span><span class="sxs-lookup"><span data-stu-id="b0af8-109">Command-line Syntax</span></span>](#command-line-syntax)
-   [<span data-ttu-id="b0af8-110">Коды ошибок командной строки</span><span class="sxs-lookup"><span data-stu-id="b0af8-110">Command-line Error Codes</span></span>](#command-line-error-codes)
-   [<span data-ttu-id="b0af8-111">Примеры командной строки</span><span class="sxs-lookup"><span data-stu-id="b0af8-111">Command-line Examples</span></span>](#command-line-examples)
-   [<span data-ttu-id="b0af8-112">См. также</span><span class="sxs-lookup"><span data-stu-id="b0af8-112">Related topics</span></span>](#related-topics)

![средство командной строки консоли аккчеккер](images/accchecker-console.png)

## <a name="command-line-syntax"></a><span data-ttu-id="b0af8-114">Синтаксис для командной строки</span><span class="sxs-lookup"><span data-stu-id="b0af8-114">Command-line Syntax</span></span>

<span data-ttu-id="b0af8-115">Консоль Аккчеккер имеет следующий синтаксис командной строки.</span><span class="sxs-lookup"><span data-stu-id="b0af8-115">AccChecker Console has the following command-line syntax.</span></span>

<span data-ttu-id="b0af8-116">**\[Параметры аккчеккконсоле \] (-HWND <hwnd> \| -Process <name> )\[<dlls>\]**</span><span class="sxs-lookup"><span data-stu-id="b0af8-116">**AccCheckConsole \[options\] (-hwnd <hwnd> \| -process <name>) \[<dlls>\]**</span></span>

<span data-ttu-id="b0af8-117">Ниже приведены параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="b0af8-117">The command-line options are as follows.</span></span>



| <span data-ttu-id="b0af8-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0af8-118">Options</span></span>                                                                                                                                                         | <span data-ttu-id="b0af8-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b0af8-119">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0af8-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd></span><span class="sxs-lookup"><span data-stu-id="b0af8-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd></span></span><br/>                                                                     | <span data-ttu-id="b0af8-121">Проверяет окно с указанным дескриптором (HWND).</span><span class="sxs-lookup"><span data-stu-id="b0af8-121">Validates the window that has the specified handle (HWND).</span></span> <span data-ttu-id="b0af8-122">Этот маркер можно указать в шестнадцатеричном или десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="b0af8-122">The handle can be specified in hexidecimal or decimal.</span></span><br/> |
| <span data-ttu-id="b0af8-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-окно <title></span><span class="sxs-lookup"><span data-stu-id="b0af8-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window <title></span></span><br/>                                                            | <span data-ttu-id="b0af8-124">Проверяет окно с указанным заголовком.</span><span class="sxs-lookup"><span data-stu-id="b0af8-124">Validates the window that has the specified title.</span></span><br/>                                                                |
| <span data-ttu-id="b0af8-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -Process <name></span><span class="sxs-lookup"><span data-stu-id="b0af8-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process <name></span></span><br/>                       | <span data-ttu-id="b0af8-126">Проверяет главное окно процесса с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="b0af8-126">Validates the main window of the process that has the specified name.</span></span><br/>                                             |
| <span data-ttu-id="b0af8-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -List</span><span class="sxs-lookup"><span data-stu-id="b0af8-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list</span></span><br/>                                       | <span data-ttu-id="b0af8-128">Список всех доступных подпрограмм проверки.</span><span class="sxs-lookup"><span data-stu-id="b0af8-128">Lists all of the available verification routines.</span></span><br/>                                                                 |
| <span data-ttu-id="b0af8-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> — включить <name></span><span class="sxs-lookup"><span data-stu-id="b0af8-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable <name></span></span><br/>                          | <span data-ttu-id="b0af8-130">Выполняет указанную подпрограммы проверки.</span><span class="sxs-lookup"><span data-stu-id="b0af8-130">Runs the specified verification routine.</span></span> <span data-ttu-id="b0af8-131">Этот параметр можно указать более одного раза.</span><span class="sxs-lookup"><span data-stu-id="b0af8-131">This option can be specified more than once.</span></span><br/>                             |
| <span data-ttu-id="b0af8-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> — отключить <name></span><span class="sxs-lookup"><span data-stu-id="b0af8-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable <name></span></span><br/> | <span data-ttu-id="b0af8-133">Выполняет все, кроме указанной подпрограммы проверки.</span><span class="sxs-lookup"><span data-stu-id="b0af8-133">Runs all but the specified verification routine.</span></span> <span data-ttu-id="b0af8-134">Этот параметр можно указать более одного раза.</span><span class="sxs-lookup"><span data-stu-id="b0af8-134">This option can be specified more than once.</span></span><br/>                     |
| <span data-ttu-id="b0af8-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (сведения \| предупреждения об \| ошибке)</span><span class="sxs-lookup"><span data-stu-id="b0af8-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info\|warn\|err)</span></span><br/>                          | <span data-ttu-id="b0af8-136">Самая низкая оценка событий, которая будет записана в журнал.</span><span class="sxs-lookup"><span data-stu-id="b0af8-136">The lowest event rating that will be logged.</span></span><br/>                                                                      |
| <span data-ttu-id="b0af8-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -файл_журнала <file></span><span class="sxs-lookup"><span data-stu-id="b0af8-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span></span><br/>                       | <span data-ttu-id="b0af8-138">Записывает выходные данные в указанный файл журнала.</span><span class="sxs-lookup"><span data-stu-id="b0af8-138">Write the output to the specified log file.</span></span> <span data-ttu-id="b0af8-139">Этот параметр можно указать более одного раза.</span><span class="sxs-lookup"><span data-stu-id="b0af8-139">This option can be specified more than once.</span></span><br/>                          |
| <span data-ttu-id="b0af8-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>— подавлять <file></span><span class="sxs-lookup"><span data-stu-id="b0af8-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress <file></span></span><br/>                                                         | <span data-ttu-id="b0af8-141">Используйте указанный XML-файл для подавления ошибок.</span><span class="sxs-lookup"><span data-stu-id="b0af8-141">Use the specified XML file to suppress errors.</span></span> <br/>                                                                   |
| <span data-ttu-id="b0af8-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span><span class="sxs-lookup"><span data-stu-id="b0af8-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span></span><br/>                                                                                             | <span data-ttu-id="b0af8-143">Не записывайте выходные данные ведения журнала в stdout.</span><span class="sxs-lookup"><span data-stu-id="b0af8-143">Do not write logging output to stdout.</span></span><br/>                                                                            |
| <span data-ttu-id="b0af8-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-Справка</span><span class="sxs-lookup"><span data-stu-id="b0af8-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help</span></span> <br/>                           | <span data-ttu-id="b0af8-145">Отображает краткую справку.</span><span class="sxs-lookup"><span data-stu-id="b0af8-145">Displays quick help.</span></span> <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a><span data-ttu-id="b0af8-146">Коды ошибок командной строки</span><span class="sxs-lookup"><span data-stu-id="b0af8-146">Command-line Error Codes</span></span>

<span data-ttu-id="b0af8-147">Ниже приведены коды ошибок, возвращаемые из Аккчеккконсоле при использовании "Echo% ERRORLEVEL%".</span><span class="sxs-lookup"><span data-stu-id="b0af8-147">Following are error codes returned from AccCheckConsole when using "echo %errorlevel%"</span></span>



| <span data-ttu-id="b0af8-148">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="b0af8-148">Error code</span></span>                       | <span data-ttu-id="b0af8-149">Описание</span><span class="sxs-lookup"><span data-stu-id="b0af8-149">Description</span></span>                                 |
|----------------------------------|---------------------------------------------|
| <span data-ttu-id="b0af8-150"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="b0af8-150"><span id="0"></span>0</span></span><br/> | <span data-ttu-id="b0af8-151">Нет ошибок и предупреждений.</span><span class="sxs-lookup"><span data-stu-id="b0af8-151">No errors and no warnings.</span></span><br/>       |
| <span data-ttu-id="b0af8-152"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="b0af8-152"><span id="1"></span>1</span></span><br/> | <span data-ttu-id="b0af8-153">Запрошена инструкция Usage.</span><span class="sxs-lookup"><span data-stu-id="b0af8-153">Usages statement was requested.</span></span> <br/> |
| <span data-ttu-id="b0af8-154"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="b0af8-154"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="b0af8-155">Ошибки и предупреждения отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b0af8-155">Errors and no warnings.</span></span><br/>          |
| <span data-ttu-id="b0af8-156"><span id="3"></span>3-5</span><span class="sxs-lookup"><span data-stu-id="b0af8-156"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="b0af8-157">Ошибки и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b0af8-157">Errors and warnings.</span></span><br/>             |
| <span data-ttu-id="b0af8-158"><span id="4"></span>4</span><span class="sxs-lookup"><span data-stu-id="b0af8-158"><span id="4"></span>4</span></span><br/> | <span data-ttu-id="b0af8-159">Предупреждения, но не ошибки.</span><span class="sxs-lookup"><span data-stu-id="b0af8-159">Warnings but no errors.</span></span><br/>          |
| <span data-ttu-id="b0af8-160"><span id="5"></span>5.0</span><span class="sxs-lookup"><span data-stu-id="b0af8-160"><span id="5"></span>5</span></span><br/> | <span data-ttu-id="b0af8-161">Недопустимая командная строка.</span><span class="sxs-lookup"><span data-stu-id="b0af8-161">Invalid command line.</span></span> <br/>           |



 

## <a name="command-line-examples"></a><span data-ttu-id="b0af8-162">Примеры командной строки</span><span class="sxs-lookup"><span data-stu-id="b0af8-162">Command-line Examples</span></span>

<span data-ttu-id="b0af8-163">Ниже приведены несколько примеров командной строки консоли Аккчеккер.</span><span class="sxs-lookup"><span data-stu-id="b0af8-163">Following are several AccChecker Console command-line examples.</span></span>

-   <span data-ttu-id="b0af8-164">Выполнение всех проверок в окне с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="b0af8-164">Run all verifications on a window with a specified name.</span></span>

    <span data-ttu-id="b0af8-165">**Аккчеккконсоле-Window "без имени — Блокнот"**</span><span class="sxs-lookup"><span data-stu-id="b0af8-165">**AccCheckConsole -window "Untitled - Notepad"**</span></span>

-   <span data-ttu-id="b0af8-166">Выполните подмножество проверок для HWND, указав файл подавления.</span><span class="sxs-lookup"><span data-stu-id="b0af8-166">Run a subset of the verifications against an HWND, specifying a suppression file.</span></span>

    <span data-ttu-id="b0af8-167">**Аккчеккконсоле-HWND 0x00382f00 — включить Чекктаббинг-Enable CheckName-подавлять suppress.xml**</span><span class="sxs-lookup"><span data-stu-id="b0af8-167">**AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**</span></span>

-   <span data-ttu-id="b0af8-168">Запустите все проверки из новой DLL-библиотеки проверки.</span><span class="sxs-lookup"><span data-stu-id="b0af8-168">Run all verifications from a new verification DLL.</span></span>

    <span data-ttu-id="b0af8-169">**Аккчеккконсоле-Window "без имени — Блокнот" VerificationRoutine1.dll**</span><span class="sxs-lookup"><span data-stu-id="b0af8-169">**AccCheckConsole -window "Untitled - Notepad" VerificationRoutine1.dll**</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0af8-170">См. также</span><span class="sxs-lookup"><span data-stu-id="b0af8-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0af8-171">Средство UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="b0af8-171">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





