---
title: Анализ аварийного дампа
description: В этой технической статье содержатся сведения о том, как создавать и использовать Малый дамп.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7558e47d08cb0183b8d9cefa5f22f0750fd1c598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070257"
---
# <a name="crash-dump-analysis"></a><span data-ttu-id="220c0-103">Анализ аварийного дампа</span><span class="sxs-lookup"><span data-stu-id="220c0-103">Crash Dump Analysis</span></span>

<span data-ttu-id="220c0-104">Не все ошибки можно найти до выпуска, что означает, что не все ошибки, которые вызывают исключения, можно найти до выпуска.</span><span class="sxs-lookup"><span data-stu-id="220c0-104">Not all bugs can be found prior to release, which means not all bugs that throw exceptions can be found before release.</span></span> <span data-ttu-id="220c0-105">К счастью, корпорация Майкрософт включила в пакет Platform SDK функцию для помощи разработчикам в собрании информации об исключениях, обнаруженных пользователями.</span><span class="sxs-lookup"><span data-stu-id="220c0-105">Fortunately, Microsoft has included in the Platform SDK a function to help developers collect information on exceptions that are discovered by users.</span></span> <span data-ttu-id="220c0-106">Функция [**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) записывает необходимые данные аварийного дампа в файл без сохранения всего пространства процесса.</span><span class="sxs-lookup"><span data-stu-id="220c0-106">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function writes the necessary crash dump information to a file without saving the whole process space.</span></span> <span data-ttu-id="220c0-107">Этот информационный файл аварийного дампа называется мини-дампом.</span><span class="sxs-lookup"><span data-stu-id="220c0-107">This crash dump information file is called a minidump.</span></span> <span data-ttu-id="220c0-108">В этой технической статье содержатся сведения о том, как создавать и использовать Малый дамп.</span><span class="sxs-lookup"><span data-stu-id="220c0-108">This technical article provides info about how to write and use a minidump.</span></span>

-   [<span data-ttu-id="220c0-109">Запись минидампа</span><span class="sxs-lookup"><span data-stu-id="220c0-109">Writing a Minidump</span></span>](#writing-a-minidump)
-   [<span data-ttu-id="220c0-110">Безопасность потоков</span><span class="sxs-lookup"><span data-stu-id="220c0-110">Thread safety</span></span>](#thread-safety)
-   [<span data-ttu-id="220c0-111">Создание минидампа с помощью кода</span><span class="sxs-lookup"><span data-stu-id="220c0-111">Writing a Minidump with Code</span></span>](#writing-a-minidump-with-code)
-   [<span data-ttu-id="220c0-112">Использование Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="220c0-112">Using Dumpchk.exe</span></span>](#using-dumpchkexe)
-   [<span data-ttu-id="220c0-113">Анализ минидампа</span><span class="sxs-lookup"><span data-stu-id="220c0-113">Analyzing a Minidump</span></span>](#analyzing-a-minidump)
    -   [<span data-ttu-id="220c0-114">Использование общедоступного сервера символов Майкрософт</span><span class="sxs-lookup"><span data-stu-id="220c0-114">Using the Microsoft Public Symbol Server</span></span>](#using-the-microsoft-public-symbol-server)
    -   [<span data-ttu-id="220c0-115">Отладка минидампа с помощью WinDbg</span><span class="sxs-lookup"><span data-stu-id="220c0-115">Debugging a Minidump with WinDbg</span></span>](#debugging-a-minidump-with-windbg)
    -   [<span data-ttu-id="220c0-116">Использование средств Copy-Protection с мини минидампа</span><span class="sxs-lookup"><span data-stu-id="220c0-116">Using Copy-Protection Tools with Minidumps</span></span>](#using-copy-protection-tools-with-minidumps)
-   [<span data-ttu-id="220c0-117">Сводка</span><span class="sxs-lookup"><span data-stu-id="220c0-117">Summary</span></span>](#summary)

## <a name="writing-a-minidump"></a><span data-ttu-id="220c0-118">Запись минидампа</span><span class="sxs-lookup"><span data-stu-id="220c0-118">Writing a Minidump</span></span>

<span data-ttu-id="220c0-119">Ниже приведены основные параметры для записи минидампа.</span><span class="sxs-lookup"><span data-stu-id="220c0-119">The basic options for writing a minidump are as follows:</span></span>

-   <span data-ttu-id="220c0-120">Не делать ничего.</span><span class="sxs-lookup"><span data-stu-id="220c0-120">Do nothing.</span></span> <span data-ttu-id="220c0-121">Windows автоматически создает малый дамп всякий раз, когда программа создает необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="220c0-121">Windows automatically generates a minidump whenever a program throws an unhandled exception.</span></span> <span data-ttu-id="220c0-122">Автоматическое создание минидампа доступно с момента выпуска Windows XP.</span><span class="sxs-lookup"><span data-stu-id="220c0-122">Automatic generation of a minidump is available since Windows XP.</span></span> <span data-ttu-id="220c0-123">Если пользователь допускает его, мини-дамп будет отправлен в корпорацию Майкрософт, а не к разработчику с помощью отчеты об ошибках Windows (WER).</span><span class="sxs-lookup"><span data-stu-id="220c0-123">If the user allows it, the minidump will be sent to Microsoft, and not to the developer, through Windows Error Reporting (WER).</span></span> <span data-ttu-id="220c0-124">Разработчики могут получить доступ к этим мини-дампам с помощью [классического приложения Windows](../appxpkg/windows-desktop-application-program.md).</span><span class="sxs-lookup"><span data-stu-id="220c0-124">Developers can gain access to these minidumps through the [Windows Desktop Application Program](../appxpkg/windows-desktop-application-program.md).</span></span>

    <span data-ttu-id="220c0-125">Для использования WER требуется:</span><span class="sxs-lookup"><span data-stu-id="220c0-125">Use of WER requires:</span></span>

    -   <span data-ttu-id="220c0-126">Разработчики могут подписывать свои приложения с помощью Authenticode</span><span class="sxs-lookup"><span data-stu-id="220c0-126">Developers to sign their applications using Authenticode</span></span>
    -   <span data-ttu-id="220c0-127">Приложения имеют допустимый ресурс VERSIONINFO в каждом исполняемом файле и библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="220c0-127">Applications have valid VERSIONINFO resource in every executable and DLL</span></span>

    <span data-ttu-id="220c0-128">При реализации пользовательской подпрограммы для необработанных исключений вы настоятельно законодателей использовать функцию [**репортфаулт**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) в обработчике исключений, чтобы также отправить автоматизированный Малый дамп в WER.</span><span class="sxs-lookup"><span data-stu-id="220c0-128">If you implement a custom routine for unhandled exceptions, you are strongly urged to use the [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) function in the exception handler to also send an automated minidump to WER.</span></span> <span data-ttu-id="220c0-129">Функция **репортфаулт** обрабатывает все проблемы, связанные с подключением и отправкой МИНИДАМПА в WER.</span><span class="sxs-lookup"><span data-stu-id="220c0-129">The **ReportFault** function handles all of the issues of connecting to and sending the minidump to WER.</span></span> <span data-ttu-id="220c0-130">Не отправка минидампа в WER нарушает требования игр для Windows.</span><span class="sxs-lookup"><span data-stu-id="220c0-130">Not sending minidumps to WER violates the requirements of Games for Windows.</span></span>

    <span data-ttu-id="220c0-131">Дополнительные сведения о принципах работы WER см. в разделе [как работает отчеты об ошибках Windows](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span><span class="sxs-lookup"><span data-stu-id="220c0-131">For more information on how WER works, see [How Windows Error Reporting Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span></span> <span data-ttu-id="220c0-132">Описание сведений о регистрации см. в статье [введение отчеты об ошибках Windows](https://msdn.microsoft.com/) в [зону ISV](https://msdn.microsoft.com/)MSDN.</span><span class="sxs-lookup"><span data-stu-id="220c0-132">For an explanation of registration details, see [Introducing Windows Error Reporting](https://msdn.microsoft.com/) on MSDN's [ISV Zone](https://msdn.microsoft.com/).</span></span>

-   <span data-ttu-id="220c0-133">Используйте продукт из Microsoft Visual Studio Team System.</span><span class="sxs-lookup"><span data-stu-id="220c0-133">Use a product from the Microsoft Visual Studio Team System.</span></span> <span data-ttu-id="220c0-134">В меню **Отладка** выберите команду **сохранить дамп как** , чтобы сохранить копию дампа.</span><span class="sxs-lookup"><span data-stu-id="220c0-134">On the **Debug** menu, click **Save Dump As** to save a copy of a dump.</span></span> <span data-ttu-id="220c0-135">Использование локально сохраненного дампа является только параметром для внутреннего тестирования и отладки.</span><span class="sxs-lookup"><span data-stu-id="220c0-135">Use of a locally saved dump is only an option for in-house testing and debugging.</span></span>
-   <span data-ttu-id="220c0-136">Добавьте код в проект.</span><span class="sxs-lookup"><span data-stu-id="220c0-136">Add code to your project.</span></span> <span data-ttu-id="220c0-137">Добавьте функцию [**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) и соответствующий код обработки исключений, чтобы сохранить и отправить Малый дамп непосредственно разработчику.</span><span class="sxs-lookup"><span data-stu-id="220c0-137">Add the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function and the appropriate exception handling code to save and send a minidump directly to the developer.</span></span> <span data-ttu-id="220c0-138">В этой статье показано, как реализовать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="220c0-138">This article demonstrates how to implement this option.</span></span> <span data-ttu-id="220c0-139">Однако обратите внимание, что в настоящее время **минидумпвритедумп** не работает с управляемым кодом и доступен только в Windows XP, Windows Vista, Windows 7.</span><span class="sxs-lookup"><span data-stu-id="220c0-139">However, note that **MiniDumpWriteDump** does not currently work with managed code and is only available on Windows XP, Windows Vista, Windows 7.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="220c0-140">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="220c0-140">Thread safety</span></span>

<span data-ttu-id="220c0-141">[**Минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) является частью библиотеки dbghelp.</span><span class="sxs-lookup"><span data-stu-id="220c0-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) is part of the DBGHELP library.</span></span> <span data-ttu-id="220c0-142">Эта библиотека не является потокобезопасной, поэтому любая программа, использующая **минидумпвритедумп** , должна синхронизировать все потоки, прежде чем пытаться вызвать **минидумпвритедумп**.</span><span class="sxs-lookup"><span data-stu-id="220c0-142">This library is not thread-safe, so any program that uses **MiniDumpWriteDump** should synchronize all threads before attempting to call **MiniDumpWriteDump**.</span></span>

## <a name="writing-a-minidump-with-code"></a><span data-ttu-id="220c0-143">Создание минидампа с помощью кода</span><span class="sxs-lookup"><span data-stu-id="220c0-143">Writing a Minidump with Code</span></span>

<span data-ttu-id="220c0-144">Фактическая реализация проста.</span><span class="sxs-lookup"><span data-stu-id="220c0-144">The actual implementation is straightforward.</span></span> <span data-ttu-id="220c0-145">Ниже приведен простой пример использования [**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="220c0-145">The following is a simple example of how to use [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



<span data-ttu-id="220c0-146">Этот пример демонстрирует базовое использование [**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) и минимальную информацию, необходимую для ее вызова.</span><span class="sxs-lookup"><span data-stu-id="220c0-146">This example demonstrates the basic usage of [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) and the minimum information necessary to call it.</span></span> <span data-ttu-id="220c0-147">Имя файла дампа является разработчиком; Однако, чтобы избежать конфликтов имен файлов, рекомендуется создать имя файла из имени и номера версии приложения, идентификатора процесса и потока, а также даты и времени.</span><span class="sxs-lookup"><span data-stu-id="220c0-147">The name of the dump file is up to the developer; however, to avoid file name collisions, it is advisable to generate the file name from the application's name and version number, the process and thread IDs, and the date and time.</span></span> <span data-ttu-id="220c0-148">Это также поможет защитить малые дампы, сгруппированные по приложениям и версиям.</span><span class="sxs-lookup"><span data-stu-id="220c0-148">This will also help to keep the minidumps grouped by application and version.</span></span> <span data-ttu-id="220c0-149">Разработчик может решить, какой объем информации используется для различения имен файлов минидампа.</span><span class="sxs-lookup"><span data-stu-id="220c0-149">It is up to the developer to decide how much information is used to differentiate minidump file names.</span></span>

<span data-ttu-id="220c0-150">Следует отметить, что имя пути в предыдущем примере было создано путем вызова функции [**жеттемппас**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) для получения пути к каталогу, назначенному для временных файлов.</span><span class="sxs-lookup"><span data-stu-id="220c0-150">It should be noted that the path name in the preceding example was generated by calling the [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files.</span></span> <span data-ttu-id="220c0-151">Использование этого каталога работает даже с учетными записями пользователей с минимальными правами доступа, и это также предотвращает загрузку дискового пространства с жесткого диска после того, как он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="220c0-151">Use of this directory works even with least-privileged user accounts, and it also prevents the minidump from taking up hard drive space after it is no longer needed.</span></span>

<span data-ttu-id="220c0-152">Если вы архивируете продукт во время ежедневного процесса сборки, также обязательно включите символы для сборки, чтобы при необходимости можно было выполнить отладку старой версии продукта.</span><span class="sxs-lookup"><span data-stu-id="220c0-152">If you archive the product during your daily build process, also be sure to include symbols for the build so that you can debug an old version of the product, if necessary.</span></span> <span data-ttu-id="220c0-153">Кроме того, необходимо выполнить действия по поддержке полной оптимизации компилятора при создании символов.</span><span class="sxs-lookup"><span data-stu-id="220c0-153">You also need to take steps to maintain full compiler optimizations while generating symbols.</span></span> <span data-ttu-id="220c0-154">Это можно сделать, открыв свойства проекта в среде разработки, а для конфигурации выпуска выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="220c0-154">This can be done by opening your project's properties in the development environment and, for the release configuration, doing the following:</span></span>

1.  <span data-ttu-id="220c0-155">В левой части страницы свойств проекта щелкните C/C++.</span><span class="sxs-lookup"><span data-stu-id="220c0-155">On the left side of the project's property page, click C/C++.</span></span> <span data-ttu-id="220c0-156">По умолчанию отображаются **Общие** параметры.</span><span class="sxs-lookup"><span data-stu-id="220c0-156">By default, this displays **General** settings.</span></span> <span data-ttu-id="220c0-157">В правой части страницы свойств проекта задайте для параметра **Формат отладочной информации** значение **база данных программы (/Zi)**.</span><span class="sxs-lookup"><span data-stu-id="220c0-157">On the right side of the project's property page, set **Debug Information Format** to **Program Database (/Zi)**.</span></span>
2.  <span data-ttu-id="220c0-158">В левой части страницы свойств разверните узел **Компоновщик**, а затем щелкните **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="220c0-158">On the left side of the property page, expand **Linker**, and then click **Debugging**.</span></span> <span data-ttu-id="220c0-159">В правой части страницы свойств задайте для параметра **создать отладочную информацию** значение **Да (/Debug)**.</span><span class="sxs-lookup"><span data-stu-id="220c0-159">On the right side of the property page, set **Generate Debug Info** to **Yes (/DEBUG)**.</span></span>
3.  <span data-ttu-id="220c0-160">Щелкните **Оптимизация** и задайте **ссылки** на **лиминате данные без ссылок (/OPT: REF)**.</span><span class="sxs-lookup"><span data-stu-id="220c0-160">Click **Optimization**, and set **References** to E **liminate Unreferenced Data (/OPT:REF)**.</span></span>
4.  <span data-ttu-id="220c0-161">Установите **флажок Включить сворачивание записей COMDAT** , чтобы **удалить избыточные COMDAT (/OPT: ICF)**.</span><span class="sxs-lookup"><span data-stu-id="220c0-161">Set **Enable COMDAT Folding** to **Remove Redundant COMDATs (/OPT:ICF)**.</span></span>

<span data-ttu-id="220c0-162">В MSDN содержится более подробная информация о [**структуре \_ \_ сведений об исключениях минидампа**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) и функции [**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .</span><span class="sxs-lookup"><span data-stu-id="220c0-162">MSDN has more detailed information on the [**MINIDUMP\_EXCEPTION\_INFORMATION**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) structure and the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function.</span></span>

## <a name="using-dumpchkexe"></a><span data-ttu-id="220c0-163">Использование Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="220c0-163">Using Dumpchk.exe</span></span>

<span data-ttu-id="220c0-164">Dumpchk.exe — это служебная программа командной строки, которую можно использовать для проверки правильности создания файла дампа.</span><span class="sxs-lookup"><span data-stu-id="220c0-164">Dumpchk.exe is a command-line utility that can be used to verify that a dump file was created correctly.</span></span> <span data-ttu-id="220c0-165">Если Dumpchk.exe создает ошибку, файл дампа поврежден и не может быть проанализирован.</span><span class="sxs-lookup"><span data-stu-id="220c0-165">If Dumpchk.exe generates an error, then the dump file is corrupt and cannot be analyzed.</span></span> <span data-ttu-id="220c0-166">Сведения об использовании Dumpchk.exe см. в разделе [использование Dumpchk.exe для проверки файла дампа памяти](https://support.microsoft.com/kb/315271/).</span><span class="sxs-lookup"><span data-stu-id="220c0-166">For information on using Dumpchk.exe, see [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).</span></span>

<span data-ttu-id="220c0-167">Dumpchk.exe входит в состав компакт-диска Windows XP, и его можно установить на системные \\ файлы программы \\ поддержки \\ , запустив Setup.exe в \\ папке средства поддержки \\ на компакт-диске Windows XP.</span><span class="sxs-lookup"><span data-stu-id="220c0-167">Dumpchk.exe is included on the Windows XP product CD and can be installed to System Drive\\Program Files\\Support Tools\\ by running Setup.exe in the Support\\Tools\\ folder on the Windows XP product CD.</span></span> <span data-ttu-id="220c0-168">Вы также можете получить последнюю версию Dumpchk.exe, загрузив и установив средства отладки, доступные в [средствах отладки Windows](https://www.microsoft.com/whdc/devtools/debugging/) в [центре разработчиков оборудования Windows](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="220c0-168">You can also get the latest version of Dumpchk.exe by download and installing the debugging tools available from [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

## <a name="analyzing-a-minidump"></a><span data-ttu-id="220c0-169">Анализ минидампа</span><span class="sxs-lookup"><span data-stu-id="220c0-169">Analyzing a Minidump</span></span>

<span data-ttu-id="220c0-170">Открытие минидампа для анализа — это так же просто, как создание такого дампа.</span><span class="sxs-lookup"><span data-stu-id="220c0-170">Opening a minidump for analysis is as easy as creating one.</span></span>

<span data-ttu-id="220c0-171">**Анализ минидампа**</span><span class="sxs-lookup"><span data-stu-id="220c0-171">**To analyze a minidump**</span></span>

1.  <span data-ttu-id="220c0-172">Запустите Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="220c0-172">Open Visual Studio.</span></span>
2.  <span data-ttu-id="220c0-173">В меню **файл** выберите команду **Открыть проект**.</span><span class="sxs-lookup"><span data-stu-id="220c0-173">On the **File** menu, click **Open Project**.</span></span>
3.  <span data-ttu-id="220c0-174">Задайте **файлы типа** для **дампа файлов**, перейдите к файлу дампа, выберите его и нажмите кнопку **Открыть.**</span><span class="sxs-lookup"><span data-stu-id="220c0-174">Set **Files of type** to **Dump Files**, navigate to the dump file, select it, and click **Open.**</span></span>
4.  <span data-ttu-id="220c0-175">Запустите отладчик.</span><span class="sxs-lookup"><span data-stu-id="220c0-175">Run the debugger.</span></span>

<span data-ttu-id="220c0-176">Отладчик создаст имитацию процесса.</span><span class="sxs-lookup"><span data-stu-id="220c0-176">The debugger will create a simulated process.</span></span> <span data-ttu-id="220c0-177">Имитация процесса будет остановлена в инструкции, вызвавшей сбой.</span><span class="sxs-lookup"><span data-stu-id="220c0-177">The simulated process will be halted at the instruction that caused the crash.</span></span>

### <a name="using-the-microsoft-public-symbol-server"></a><span data-ttu-id="220c0-178">Использование общедоступного сервера символов Майкрософт</span><span class="sxs-lookup"><span data-stu-id="220c0-178">Using the Microsoft Public Symbol Server</span></span>

<span data-ttu-id="220c0-179">Чтобы получить стек для сбоев драйвера или системного уровня, может потребоваться настроить Visual Studio для указания на общедоступный сервер символов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="220c0-179">To get the stack for driver- or system-level crashes, it might be necessary to configure Visual Studio to point to the Microsoft public symbol server.</span></span>

<span data-ttu-id="220c0-180">**Установка пути к серверу символов Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="220c0-180">**To set a path to the Microsoft symbol server**</span></span>

1.  <span data-ttu-id="220c0-181">В меню **Отладка** выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="220c0-181">On the **Debug** menu, click **Options**.</span></span>
2.  <span data-ttu-id="220c0-182">В диалоговом окне **Параметры** откройте узел **Отладка** и щелкните **символы**.</span><span class="sxs-lookup"><span data-stu-id="220c0-182">In the **Options** dialog box, open the **Debugging** node, and click **Symbols**.</span></span>
3.  <span data-ttu-id="220c0-183">Убедитесь, что **Поиск в указанных выше расположениях выполняется, только если символы загружаются вручную** , если не требуется загружать символы вручную при отладке.</span><span class="sxs-lookup"><span data-stu-id="220c0-183">Make sure **Search the above locations only when symbols are loaded manually** is not selected, unless you want to load symbols manually when you debug.</span></span>
4.  <span data-ttu-id="220c0-184">Если вы используете символы на удаленном сервере символов, можно повысить производительность, указав локальный каталог, в который могут быть скопированы символы.</span><span class="sxs-lookup"><span data-stu-id="220c0-184">If you are using symbols on a remote symbol server, you can improve performance by specifying a local directory that symbols can be copied to.</span></span> <span data-ttu-id="220c0-185">Для этого введите путь для **кэширования символов с сервера символов в этот каталог**.</span><span class="sxs-lookup"><span data-stu-id="220c0-185">To do this, enter a path for **Cache symbols from symbol server to this directory**.</span></span> <span data-ttu-id="220c0-186">Чтобы подключиться к общедоступному серверу символов Майкрософт, необходимо включить этот параметр.</span><span class="sxs-lookup"><span data-stu-id="220c0-186">To connect to the Microsoft public symbol server, you need to enable this setting.</span></span> <span data-ttu-id="220c0-187">Обратите внимание, что при отладке программы на удаленном компьютере каталог кэша ссылается на каталог на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="220c0-187">Note that if you are debugging a program on a remote computer, the cache directory refers to a directory on the remote computer.</span></span>
5.  <span data-ttu-id="220c0-188">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="220c0-188">Click **OK**.</span></span>
6.  <span data-ttu-id="220c0-189">Поскольку используется общедоступный сервер символов Майкрософт, появляется диалоговое окно с лицензионным соглашением.</span><span class="sxs-lookup"><span data-stu-id="220c0-189">Because you are using the Microsoft public symbol server, an End User License Agreement dialog box appears.</span></span> <span data-ttu-id="220c0-190">Нажмите кнопку **Да** , чтобы принять условия соглашения и скачать символы в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="220c0-190">Click **Yes** to accept the agreement and download symbols to your local cache.</span></span>

### <a name="debugging-a-minidump-with-windbg"></a><span data-ttu-id="220c0-191">Отладка минидампа с помощью WinDbg</span><span class="sxs-lookup"><span data-stu-id="220c0-191">Debugging a Minidump with WinDbg</span></span>

<span data-ttu-id="220c0-192">Вы также можете использовать WinDbg, отладчик, который является частью средств отладки Windows, для отладки минидампа.</span><span class="sxs-lookup"><span data-stu-id="220c0-192">You can also use WinDbg, a debugger that is part of the Windows Debugging Tools, to debug a minidump.</span></span> <span data-ttu-id="220c0-193">WinDbg позволяет выполнять отладку без использования Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="220c0-193">WinDbg allows you to debug without having to use Visual Studio.</span></span> <span data-ttu-id="220c0-194">Сведения о загрузке средств отладки Windows см. в разделе [средства отладки Windows](https://www.microsoft.com/whdc/devtools/debugging/) в [центре разработчиков оборудования для Windows](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="220c0-194">To download Windows Debugging Tools, see [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

<span data-ttu-id="220c0-195">После установки средств отладки Windows необходимо ввести путь к символам в WinDbg.</span><span class="sxs-lookup"><span data-stu-id="220c0-195">After installing Windows Debugging Tools, you must enter the symbol path in WinDbg.</span></span>

<span data-ttu-id="220c0-196">**Ввод пути к символам в WinDbg**</span><span class="sxs-lookup"><span data-stu-id="220c0-196">**To enter a symbol path in WinDbg**</span></span>

1.  <span data-ttu-id="220c0-197">В меню **файл** выберите пункт **путь к символам**.</span><span class="sxs-lookup"><span data-stu-id="220c0-197">On the **File** menu, click **Symbol Path**.</span></span>
2.  <span data-ttu-id="220c0-198">В окне **путь поиска символов** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="220c0-198">In the **Symbol Search Path** window, enter the following:</span></span>

    <span data-ttu-id="220c0-199">SRV \* c: \\ кэш \* https://msdl.microsoft.com/download/symbols ;</span><span class="sxs-lookup"><span data-stu-id="220c0-199">"srv\*c:\\cache\*https://msdl.microsoft.com/download/symbols;"</span></span>

### <a name="using-copy-protection-tools-with-minidumps"></a><span data-ttu-id="220c0-200">Использование средств Copy-Protection с мини минидампа</span><span class="sxs-lookup"><span data-stu-id="220c0-200">Using Copy-Protection Tools with Minidumps</span></span>

<span data-ttu-id="220c0-201">Разработчикам также необходимо знать, как схема защиты от копирования может повлиять на малый дамп.</span><span class="sxs-lookup"><span data-stu-id="220c0-201">Developers also need to be aware of how their copy-protection scheme might affect the minidump.</span></span> <span data-ttu-id="220c0-202">Большинство схем защиты от копирования имеют собственные средства дешифрования, и разработчик может научиться использовать эти средства с [**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="220c0-202">Most copy-protection schemes have their own descramble tools, and it is up to the developer to learn how to use those tools with [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>

## <a name="summary"></a><span data-ttu-id="220c0-203">Сводка</span><span class="sxs-lookup"><span data-stu-id="220c0-203">Summary</span></span>

<span data-ttu-id="220c0-204">Функция [**минидумпвритедумп**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) может быть чрезвычайно полезной инструментом для сбора и устранения ошибок после выпуска продукта.</span><span class="sxs-lookup"><span data-stu-id="220c0-204">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function can be an extremely useful tool in collecting and solving bugs after the product has been released.</span></span> <span data-ttu-id="220c0-205">Написание пользовательского обработчика исключений, использующего **минидумпвритедумп** , позволяет разработчику настраивать сбор информации и улучшать процесс отладки.</span><span class="sxs-lookup"><span data-stu-id="220c0-205">Writing a custom exception handler that uses **MiniDumpWriteDump** allows the developer to customize the information collection and improve the debugging process.</span></span> <span data-ttu-id="220c0-206">Функция достаточно гибка для использования в любом проекте на основе C++ и должна рассматриваться как часть процесса стабильности любого проекта.</span><span class="sxs-lookup"><span data-stu-id="220c0-206">The function is flexible enough to be used in any C++-based project and should be considered part of any project's stability process.</span></span>

 

 