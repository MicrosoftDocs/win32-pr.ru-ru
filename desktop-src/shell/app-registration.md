---
description: В этом разделе описывается, как приложения могут предоставлять сведения о себе, необходимые для реализации определенных сценариев.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Регистрация приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990964"
---
# <a name="application-registration"></a><span data-ttu-id="7b44d-103">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="7b44d-103">Application Registration</span></span>

<span data-ttu-id="7b44d-104">В этом разделе описывается, как приложения могут предоставлять сведения о себе, необходимые для реализации определенных сценариев.</span><span class="sxs-lookup"><span data-stu-id="7b44d-104">This topic discusses how applications can expose information about themselves necessary to enable certain scenarios.</span></span> <span data-ttu-id="7b44d-105">Сюда входят сведения, необходимые для размещения приложения, команды, поддерживаемые приложением, а также типы файлов, которые может выполнять приложение.</span><span class="sxs-lookup"><span data-stu-id="7b44d-105">This includes information needed to locate the application, the verbs that the application supports and the types of files that an application can handle.</span></span>

<span data-ttu-id="7b44d-106">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7b44d-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7b44d-107">Поиск исполняемого файла приложения</span><span class="sxs-lookup"><span data-stu-id="7b44d-107">Finding an Application Executable</span></span>](#finding-an-application-executable)
-   [<span data-ttu-id="7b44d-108">Регистрация приложений</span><span class="sxs-lookup"><span data-stu-id="7b44d-108">Registering Applications</span></span>](#registering-applications)
    -   [<span data-ttu-id="7b44d-109">Использование подраздела путей к приложению</span><span class="sxs-lookup"><span data-stu-id="7b44d-109">Using the App Paths Subkey</span></span>](#using-the-app-paths-subkey)
    -   [<span data-ttu-id="7b44d-110">Использование подраздела приложений</span><span class="sxs-lookup"><span data-stu-id="7b44d-110">Using the Applications Subkey</span></span>](#using-the-applications-subkey)
-   [<span data-ttu-id="7b44d-111">Регистрация команд и других сведений о сопоставлении файлов</span><span class="sxs-lookup"><span data-stu-id="7b44d-111">Registering Verbs and Other File Association Information</span></span>](#registering-verbs-and-other-file-association-information)
-   [<span data-ttu-id="7b44d-112">Регистрация воспринимаемого типа</span><span class="sxs-lookup"><span data-stu-id="7b44d-112">Registering a Perceived Type</span></span>](#registering-a-perceived-type)
-   [<span data-ttu-id="7b44d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="7b44d-113">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="7b44d-114">Приложения также можно зарегистрировать в окне Настройка доступа к программам и параметров по умолчанию (SPAD) и задать приложения панели управления программы по умолчанию (SYDP).</span><span class="sxs-lookup"><span data-stu-id="7b44d-114">Applications can also be registered in the Set Program Access and Computer Defaults (SPAD) and Set Your Default Programs (SYDP) control panel applications.</span></span> <span data-ttu-id="7b44d-115">Сведения о регистрации приложений в SPAD и SYDP см. в разделе [рекомендации по сопоставлению файлов и программам по умолчанию](appguide-fa-defpro.md), [настройке доступа к программам и по умолчанию для компьютеров (SPAD)](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="7b44d-115">For information about SPAD and SYDP application registration, see [Guidelines for File Associations and Default Programs](appguide-fa-defpro.md), and [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md).</span></span>

 

## <a name="finding-an-application-executable"></a><span data-ttu-id="7b44d-116">Поиск исполняемого файла приложения</span><span class="sxs-lookup"><span data-stu-id="7b44d-116">Finding an Application Executable</span></span>

<span data-ttu-id="7b44d-117">При вызове функции [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) с именем исполняемого файла в его параметре *лпфиле* существует несколько мест, где функция ищет файл.</span><span class="sxs-lookup"><span data-stu-id="7b44d-117">When the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called with the name of an executable file in its *lpFile* parameter, there are several places where the function looks for the file.</span></span> <span data-ttu-id="7b44d-118">Мы рекомендуем зарегистрировать приложение в подразделе реестра **app paths** .</span><span class="sxs-lookup"><span data-stu-id="7b44d-118">We recommend registering your application in the **App Paths** registry subkey.</span></span> <span data-ttu-id="7b44d-119">Это позволяет избежать необходимости изменять переменную среды системного пути в приложениях.</span><span class="sxs-lookup"><span data-stu-id="7b44d-119">Doing so avoids the need for applications to modify the system PATH environment variable.</span></span>

<span data-ttu-id="7b44d-120">Файл ищется в следующих расположениях:</span><span class="sxs-lookup"><span data-stu-id="7b44d-120">The file is sought in the following locations:</span></span>

-   <span data-ttu-id="7b44d-121">текущий рабочий каталог.</span><span class="sxs-lookup"><span data-stu-id="7b44d-121">The current working directory.</span></span>
-   <span data-ttu-id="7b44d-122">Только каталог **Windows** (Поиск подкаталогов не выполняется).</span><span class="sxs-lookup"><span data-stu-id="7b44d-122">The **Windows** directory only (no subdirectories are searched).</span></span>
-   <span data-ttu-id="7b44d-123">Каталог **Windows \\ system32** .</span><span class="sxs-lookup"><span data-stu-id="7b44d-123">The **Windows\\System32** directory.</span></span>
-   <span data-ttu-id="7b44d-124">Каталоги, перечисленные в переменной среды PATH.</span><span class="sxs-lookup"><span data-stu-id="7b44d-124">Directories listed in the PATH environment variable.</span></span>
-   <span data-ttu-id="7b44d-125">Рекомендуется: **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app paths**</span><span class="sxs-lookup"><span data-stu-id="7b44d-125">Recommended: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**</span></span>

## <a name="registering-applications"></a><span data-ttu-id="7b44d-126">Регистрация приложений</span><span class="sxs-lookup"><span data-stu-id="7b44d-126">Registering Applications</span></span>

<span data-ttu-id="7b44d-127">Подразделы реестра " **пути приложений** " и " **приложения** " используются для регистрации и управления поведением системы от имени приложений.</span><span class="sxs-lookup"><span data-stu-id="7b44d-127">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="7b44d-128">Подраздел **app paths** является предпочтительным расположением.</span><span class="sxs-lookup"><span data-stu-id="7b44d-128">The **App Paths** subkey is the preferred location.</span></span>

### <a name="using-the-app-paths-subkey"></a><span data-ttu-id="7b44d-129">Использование подраздела путей к приложению</span><span class="sxs-lookup"><span data-stu-id="7b44d-129">Using the App Paths Subkey</span></span>

<span data-ttu-id="7b44d-130">В Windows 7 и более поздних версиях настоятельно рекомендуется устанавливать приложения для каждого пользователя, а не для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="7b44d-130">In Windows 7 and later, we strongly recommend you install applications per user rather than per machine.</span></span> <span data-ttu-id="7b44d-131">Приложение, установленное для каждого пользователя, может быть зарегистрировано в разделе **hKey \_ текущее \_ пользовательское** \\ **программное обеспечение** \\  \\  \\  \\ **пути к приложению** Microsoft Windows CurrentVersion.</span><span class="sxs-lookup"><span data-stu-id="7b44d-131">An application that is installed for per user can be registered under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span> <span data-ttu-id="7b44d-132">Приложение, установленное для всех пользователей компьютера, может быть зарегистрировано в папке **hKey \_ Локальное \_** \\ **программное обеспечение** \\  \\  \\  \\ **пути приложения** Microsoft Windows CurrentVersion.</span><span class="sxs-lookup"><span data-stu-id="7b44d-132">An application that is installed for all users of the computer can be registered under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span>

<span data-ttu-id="7b44d-133">Записи, найденные в разделе **пути к приложениям** , используются в основном для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="7b44d-133">The entries found under **App Paths** are used primarily for the following purposes:</span></span>

-   <span data-ttu-id="7b44d-134">Для преобразования имени исполняемого файла приложения в полный путь к этому файлу.</span><span class="sxs-lookup"><span data-stu-id="7b44d-134">To map an application's executable file name to that file's fully qualified path.</span></span>
-   <span data-ttu-id="7b44d-135">Значение, чтобы предварительно доложить данные в переменную среды PATH для каждого приложения, отдельно для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="7b44d-135">To pre-pend information to the PATH environment variable on a per-application, per-process basis.</span></span>

<span data-ttu-id="7b44d-136">Если имя подраздела **путей к приложению** совпадает с именем файла, оболочка выполняет два действия:</span><span class="sxs-lookup"><span data-stu-id="7b44d-136">If the name of a subkey of **App Paths** matches the file name, the Shell performs two actions:</span></span>

-   <span data-ttu-id="7b44d-137">Запись (по умолчанию) используется в качестве полного пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="7b44d-137">The (Default) entry is used as the file's fully qualified path.</span></span>
-   <span data-ttu-id="7b44d-138">Запись пути для этого подраздела предваряется переменной среды PATH этого процесса.</span><span class="sxs-lookup"><span data-stu-id="7b44d-138">The Path entry for that subkey is pre-pended to the PATH environment variable of that process.</span></span> <span data-ttu-id="7b44d-139">Если это не требуется, можно опустить значение пути.</span><span class="sxs-lookup"><span data-stu-id="7b44d-139">If this is not required, the Path value can be omitted.</span></span>

<span data-ttu-id="7b44d-140">Возможны следующие проблемы, которые следует учитывать:</span><span class="sxs-lookup"><span data-stu-id="7b44d-140">Potential issues to be aware of include:</span></span>

-   <span data-ttu-id="7b44d-141">Оболочка ограничивает длину командной строки МАКСИМАЛЬным числом символов, равным \_ \* 2.</span><span class="sxs-lookup"><span data-stu-id="7b44d-141">The Shell limits the length of a command line to MAX\_PATH \* 2 characters.</span></span> <span data-ttu-id="7b44d-142">Если имеется много файлов, перечисленных в качестве записей реестра, или их пути слишком длинные, имена файлов, приведенные ниже в списке, могут быть потеряны, так как Командная строка усекается.</span><span class="sxs-lookup"><span data-stu-id="7b44d-142">If there are many files listed as registry entries or their paths are long, file names later in the list could be lost as the command line is truncated.</span></span>
-   <span data-ttu-id="7b44d-143">Некоторые приложения не принимают несколько имен файлов в командной строке.</span><span class="sxs-lookup"><span data-stu-id="7b44d-143">Some applications do not accept multiple file names in a command line.</span></span>
-   <span data-ttu-id="7b44d-144">Некоторые приложения, принимающие несколько имен файлов, не распознают формат, в котором они предоставляются оболочкой.</span><span class="sxs-lookup"><span data-stu-id="7b44d-144">Some applications that accept multiple file names do not recognize the format in which the Shell provides them.</span></span> <span data-ttu-id="7b44d-145">Оболочка предоставляет список параметров в виде строки в кавычках, но некоторым приложениям могут потребоваться строки без кавычек.</span><span class="sxs-lookup"><span data-stu-id="7b44d-145">The Shell provides the parameter list as a quoted string, but some applications might require strings without quotes.</span></span>
-   <span data-ttu-id="7b44d-146">Не все элементы, которые можно перетаскивать, являются частью файловой системы; Например, «принтеры».</span><span class="sxs-lookup"><span data-stu-id="7b44d-146">Not all items that can be dragged are part of the file system; for example, printers.</span></span> <span data-ttu-id="7b44d-147">Эти элементы не имеют стандартного пути Win32, поэтому нет способа предоставить осмысленное значение *лппараметерс* для [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="7b44d-147">These items do not have a standard Win32 path, so there is no way to provide a meaningful *lpParameters* value to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="7b44d-148">Использование записи Дроптаржет позволяет избежать этих потенциальных проблем, предоставляя доступ ко всем форматам буфера обмена, включая [кфстр \_ шеллидлист](clipboard.md) (для длинных списков файлов) и [кфстр \_ филеконтентс](clipboard.md) (для объектов, не являющихся объектами файловой системы).</span><span class="sxs-lookup"><span data-stu-id="7b44d-148">Using the DropTarget entry avoids these potential issues by providing access to all of the clipboard formats, including [CFSTR\_SHELLIDLIST](clipboard.md) (for long file lists) and [CFSTR\_FILECONTENTS](clipboard.md) (for non-file-system objects).</span></span>

<span data-ttu-id="7b44d-149">**Для регистрации и управления поведением приложений с помощью подраздела путей приложений**:</span><span class="sxs-lookup"><span data-stu-id="7b44d-149">**To register and control the behavior of your applications with the App Paths subkey**:</span></span>

1.  <span data-ttu-id="7b44d-150">Добавьте подраздел с тем же именем, что и у исполняемого файла, в подраздел **пути к приложению** , как показано в следующей записи реестра.</span><span class="sxs-lookup"><span data-stu-id="7b44d-150">Add a subkey with the same name as your executable file to the **App Paths** subkey, as shown in the following registry entry.</span></span>

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  <span data-ttu-id="7b44d-151">Сведения о записях подраздела **пути приложения** см. в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7b44d-151">See the following table for details of the **App Paths** subkey entries.</span></span> 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="7b44d-152">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="7b44d-152">Registry entry</span></span></th>
    <th><span data-ttu-id="7b44d-153">Сведения</span><span class="sxs-lookup"><span data-stu-id="7b44d-153">Details</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="7b44d-154">(по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b44d-154">(Default)</span></span></td>
    <td><span data-ttu-id="7b44d-155">Полный путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="7b44d-155">Is the fully qualified path to the application.</span></span> <span data-ttu-id="7b44d-156">Имя приложения, указанное в записи (по умолчанию), может быть указано с расширением exe или без него.</span><span class="sxs-lookup"><span data-stu-id="7b44d-156">The application name provided in the (Default) entry can be stated with or without its .exe extension.</span></span> <span data-ttu-id="7b44d-157">При необходимости функция <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> добавляет расширение при поиске подраздела <strong>пути к приложению</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b44d-157">If necessary, the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function adds the extension when searching <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="7b44d-158">Запись относится к типу <strong>REG_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b44d-158">The entry is of the <strong>REG_SZ</strong> type.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="7b44d-159">донтуседесктопчанжераутер</span><span class="sxs-lookup"><span data-stu-id="7b44d-159">DontUseDesktopChangeRouter</span></span></td>
    <td><span data-ttu-id="7b44d-160">Является обязательным для приложений отладчика, чтобы избежать взаимоблокировок диалогового окна файлов при отладке процесса проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="7b44d-160">Is mandatory for debugger applications to avoid file dialog deadlocks when debugging the Windows Explorer process.</span></span> <span data-ttu-id="7b44d-161">Однако установка записи Донтуседесктопчанжераутер значительно менее эффективно обрабатывает уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="7b44d-161">Setting the DontUseDesktopChangeRouter entry produces a slightly less efficient handling of the change notifications, however.</span></span> <span data-ttu-id="7b44d-162">Запись относится к типу <strong>REG_DWORD</strong> , а значение — 0x1.</span><span class="sxs-lookup"><span data-stu-id="7b44d-162">The entry is of the <strong>REG_DWORD</strong> type and the value is 0x1.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="7b44d-163">DropTarget</span><span class="sxs-lookup"><span data-stu-id="7b44d-163">DropTarget</span></span></td>
    <td><span data-ttu-id="7b44d-164">— Это идентификатор класса (CLSID).</span><span class="sxs-lookup"><span data-stu-id="7b44d-164">Is a class identifier (CLSID).</span></span> <span data-ttu-id="7b44d-165">Запись Дроптаржет содержит идентификатор CLSID объекта (обычно это локальный сервер, а не внутрипроцессный сервер), который реализует <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>интерфейс IDropTarget</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b44d-165">The DropTarget entry contains the CLSID of an object (usually a local server rather than an in-process server) that implements <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span></span> <span data-ttu-id="7b44d-166">По умолчанию, когда цель перетаскивания является исполняемым файлом и не указано значение Дроптаржет, оболочка преобразует список удаленных файлов в параметр командной строки и передает его в <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> через <em>лппараметерс</em>.</span><span class="sxs-lookup"><span data-stu-id="7b44d-166">By default, when the drop target is an executable file, and no DropTarget value is provided, the Shell converts the list of dropped files into a command-line parameter and passes it to <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> through <em>lpParameters</em>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="7b44d-167">Путь</span><span class="sxs-lookup"><span data-stu-id="7b44d-167">Path</span></span></td>
    <td><span data-ttu-id="7b44d-168">Предоставляет строку (в виде разделенного точкой с запятой списка каталогов) для добавления к переменной среды PATH при запуске приложения путем вызова <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b44d-168">Supplies a string (in the form of a semicolon-separated list of directories) to append to the PATH environment variable when an application is launched by calling <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span> <span data-ttu-id="7b44d-169">Это полный путь к EXE-файлу.</span><span class="sxs-lookup"><span data-stu-id="7b44d-169">It is the fully qualified path to the .exe.</span></span> <span data-ttu-id="7b44d-170">Это <strong>REG_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="7b44d-170">It is of <strong>REG_SZ</strong>.</span></span> <span data-ttu-id="7b44d-171">В <strong>Windows 7 и более поздних версиях</strong>тип может быть <strong>REG_EXPAND_SZ</strong>и обычно <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="7b44d-171">In <strong>Windows 7 and later</strong>, the type can be <strong>REG_EXPAND_SZ</strong>, and is commonly <strong>REG_EXPAND_SZ</strong> %ProgramFiles%.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="7b44d-172">Помимо записей (по умолчанию), пути и Дроптаржет, распознаваемых оболочкой, приложение может также добавлять пользовательские значения в подраздел <strong>пути приложения</strong> в исполняемом файле.</span><span class="sxs-lookup"><span data-stu-id="7b44d-172">In addition to the (Default), Path, and DropTarget entries recognized by the Shell, an application can also add custom values to its executable file's <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="7b44d-173">Мы рекомендуем разработчикам приложений использовать подраздел <strong>пути к приложению</strong> , чтобы указать специфический для приложения путь вместо добавления к глобальному системному пути.</span><span class="sxs-lookup"><span data-stu-id="7b44d-173">We encourage application developers to use the <strong>App Paths</strong> subkey to provide an application-specific path instead of making additions to the global system path.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="7b44d-174">SupportedProtocols</span><span class="sxs-lookup"><span data-stu-id="7b44d-174">SupportedProtocols</span></span></td>
    <td><span data-ttu-id="7b44d-175">Создает строку, содержащую схемы протокола URL для данного ключа.</span><span class="sxs-lookup"><span data-stu-id="7b44d-175">Creates a string that contains the URL protocol schemes for a given key.</span></span> <span data-ttu-id="7b44d-176">Это может содержать несколько значений реестра для указания поддерживаемых схем.</span><span class="sxs-lookup"><span data-stu-id="7b44d-176">This can contain multiple registry values to indicate which schemes are supported.</span></span> <span data-ttu-id="7b44d-177">Эта строка соответствует формату <strong>scheme1: scheme2</strong>.</span><span class="sxs-lookup"><span data-stu-id="7b44d-177">This string follows the format of <strong>scheme1:scheme2</strong>.</span></span> <span data-ttu-id="7b44d-178">Если этот список не пуст, в строку будет добавлен <strong>файл:</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b44d-178">If this list is not empty, <strong>file:</strong> will be added to the string.</span></span> <span data-ttu-id="7b44d-179">Этот протокол неявно поддерживается, если определен <em>суппортедпротоколс</em> .</span><span class="sxs-lookup"><span data-stu-id="7b44d-179">This protocol is implicitly supported when <em>SupportedProtocols</em> is defined.</span></span> <br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="7b44d-180">UseUrl</span><span class="sxs-lookup"><span data-stu-id="7b44d-180">UseUrl</span></span></td>
    <td><span data-ttu-id="7b44d-181">Указывает, что приложение может принять URL-адрес (вместо имени файла) в командной строке.</span><span class="sxs-lookup"><span data-stu-id="7b44d-181">Indicates that your application can accept a URL (instead of a file name) on the command line.</span></span> <span data-ttu-id="7b44d-182">Эта запись должна быть задана приложениями, которые могут открывать документы непосредственно из Интернета, например веб-браузеры и проигрыватели мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7b44d-182">Applications that can open documents directly from the internet, like web browsers and media players, should set this entry.</span></span> <br/> <span data-ttu-id="7b44d-183">Когда функция <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> запускает приложение, а значение усеурл = 1 не задано, <strong>ShellExecuteEx</strong> скачивает документ в локальный файл и вызывает обработчик для локальной копии.</span><span class="sxs-lookup"><span data-stu-id="7b44d-183">When the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function starts an application and the UseUrl=1 value is not set, <strong>ShellExecuteEx</strong> downloads the document to a local file and invokes the handler on the local copy.</span></span><br/> <span data-ttu-id="7b44d-184">Например, если в приложении есть этот набор записей и пользователь щелкнул правой кнопкой мыши файл, хранящийся на веб-сервере, команда Открыть станет доступной.</span><span class="sxs-lookup"><span data-stu-id="7b44d-184">For example, if the application has this entry set and a user right-clicks on a file stored on a web server, the Open verb will be made available.</span></span> <span data-ttu-id="7b44d-185">В противном случае пользователю потребуется загрузить файл и открыть локальную копию.</span><span class="sxs-lookup"><span data-stu-id="7b44d-185">If not, the user will have to download the file and open the local copy.</span></span> <br/> <span data-ttu-id="7b44d-186">Запись Усеурл имеет тип <strong>REG_DWORD</strong> , а значение — 0x1.</span><span class="sxs-lookup"><span data-stu-id="7b44d-186">The UseUrl entry is of <strong>REG_DWORD</strong> type, and the value is 0x1.</span></span><br/> <span data-ttu-id="7b44d-187">В Windows Vista и более ранних версиях эта запись указывала на то, что URL-адрес должен быть передан в приложение вместе с локальным именем файла при вызове через ShellExecuteEx.</span><span class="sxs-lookup"><span data-stu-id="7b44d-187">In Windows Vista and earlier, this entry indicated that the URL should be passed to the application along with a local file name, when called via ShellExecuteEx.</span></span> <span data-ttu-id="7b44d-188">В Windows 7 это означает, что приложение может распознать любой переданный ему URL-адрес HTTP или HTTPS без необходимости указывать имя файла кэша.</span><span class="sxs-lookup"><span data-stu-id="7b44d-188">In Windows 7, it indicates that the application can understand any http or https url that is passed to it, without having to supply the cache file name as well.</span></span> <span data-ttu-id="7b44d-189">Этот раздел реестра связан с ключом <em>суппортедпротоколс</em> .</span><span class="sxs-lookup"><span data-stu-id="7b44d-189">This registry key is associated with the <em>SupportedProtocols</em> key.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a><span data-ttu-id="7b44d-190">Использование подраздела приложений</span><span class="sxs-lookup"><span data-stu-id="7b44d-190">Using the Applications Subkey</span></span>

<span data-ttu-id="7b44d-191">С помощью записей реестра, перечисленных в разделе **\_ \_ корневые приложения для классов hKey** \\  \\ *ApplicationName.exe* , приложения могут предоставлять сведения, относящиеся к приложению, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7b44d-191">Through the inclusion of registry entries under the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey, applications can provide the application-specific information shown in the following table.</span></span>



| <span data-ttu-id="7b44d-192">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="7b44d-192">Registry entry</span></span>                   | <span data-ttu-id="7b44d-193">Описание</span><span class="sxs-lookup"><span data-stu-id="7b44d-193">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b44d-194">\\команда оболочки</span><span class="sxs-lookup"><span data-stu-id="7b44d-194">shell\\verb</span></span>                      | <span data-ttu-id="7b44d-195">Предоставляет метод Verb для вызова приложения из Опенвис.</span><span class="sxs-lookup"><span data-stu-id="7b44d-195">Provides the verb method for calling the application from OpenWith.</span></span> <span data-ttu-id="7b44d-196">Если определение глагола не указано, система предполагает, что приложение поддерживает [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), и передает имя файла в командной строке.</span><span class="sxs-lookup"><span data-stu-id="7b44d-196">Without a verb definition specified here, the system assumes that the application supports [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), and passes the file name on the command line.</span></span> <span data-ttu-id="7b44d-197">Эта функция применяется ко всем методам команд, включая Дроптаржет, ExecuteCommand и платформа динамических данных Exchange (DDE).</span><span class="sxs-lookup"><span data-stu-id="7b44d-197">This functionality applies to all the verb methods, including DropTarget, ExecuteCommand, and Dynamic Data Exchange (DDE).</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7b44d-198">дефаултикон</span><span class="sxs-lookup"><span data-stu-id="7b44d-198">DefaultIcon</span></span>                      | <span data-ttu-id="7b44d-199">Позволяет приложению указать конкретный значок для представления приложения вместо первого значка, хранящегося в exe-файле.</span><span class="sxs-lookup"><span data-stu-id="7b44d-199">Enables an application to provide a specific icon to represent the application instead of the first icon stored in the .exe file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7b44d-200">фриендляппнаме</span><span class="sxs-lookup"><span data-stu-id="7b44d-200">FriendlyAppName</span></span>                  | <span data-ttu-id="7b44d-201">Предоставляет способ получения локализуемого имени, отображаемого для приложения, а не только сведений о версии, которые могут быть не подлежат локализации.</span><span class="sxs-lookup"><span data-stu-id="7b44d-201">Provides a way to get a localizable name to display for an application instead of just the version information appearing, which may not be localizable.</span></span> <span data-ttu-id="7b44d-202">[**Ассокстр**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) запроса на сопоставление считывает это значение записи реестра и возвращается к использованию имени филедескриптион в сведениях о версии.</span><span class="sxs-lookup"><span data-stu-id="7b44d-202">The association query [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) reads this registry entry value and falls back to use the FileDescription name in the version information.</span></span> <span data-ttu-id="7b44d-203">Если это имя отсутствует, запрос ассоциации по умолчанию имеет отображаемое имя файла.</span><span class="sxs-lookup"><span data-stu-id="7b44d-203">If that name is missing, the association query defaults to the display name of the file.</span></span> <span data-ttu-id="7b44d-204">Приложения должны использовать **ассокстр \_ фриендляппнаме** для получения этих сведений, чтобы получить правильное поведение.</span><span class="sxs-lookup"><span data-stu-id="7b44d-204">Applications should use **ASSOCSTR\_FRIENDLYAPPNAME** to retrieve this information to obtain the proper behavior.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="7b44d-205">суппортедтипес</span><span class="sxs-lookup"><span data-stu-id="7b44d-205">SupportedTypes</span></span>                   | <span data-ttu-id="7b44d-206">Список типов файлов, поддерживаемых приложением.</span><span class="sxs-lookup"><span data-stu-id="7b44d-206">Lists the file types that the application supports.</span></span> <span data-ttu-id="7b44d-207">Это позволит включить приложение в список каскадного меню диалогового окна **Открыть с помощью** .</span><span class="sxs-lookup"><span data-stu-id="7b44d-207">Doing so enables the application to be listed in the cascade menu of the **Open with** dialog box.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7b44d-208">нупенвис</span><span class="sxs-lookup"><span data-stu-id="7b44d-208">NoOpenWith</span></span>                       | <span data-ttu-id="7b44d-209">Указывает, что для открытия этого типа файлов не указано ни одно приложение.</span><span class="sxs-lookup"><span data-stu-id="7b44d-209">Indicates that no application is specified for opening this file type.</span></span> <span data-ttu-id="7b44d-210">Имейте в виду, что если подключ Опенвиспрогидс был задан для приложения по типу файла, а сам подраздел ProgID не имеет записи Нупенвис, это приложение появится в списке рекомендуемых или доступных приложений, даже если в нем указана запись Нупенвис.</span><span class="sxs-lookup"><span data-stu-id="7b44d-210">Be aware that if an OpenWithProgIDs subkey has been set for an application by file type, and the ProgID subkey itself does not also have a NoOpenWith entry, that application will appear in the list of recommended or available applications even if it has specified the NoOpenWith entry.</span></span> <span data-ttu-id="7b44d-211">Дополнительные сведения см. в разделе как [включить приложение в диалоговое окно "Открыть с помощью](how-to-include-an-application-on-the-open-with-dialog-box.md) " и [как исключить приложение из диалогового окна "Открыть с помощью"](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="7b44d-211">For more information, see [How to How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) and [How to exclude an Application from the Open with Dialog Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span></span><br/> |
| <span data-ttu-id="7b44d-212">ишостапп</span><span class="sxs-lookup"><span data-stu-id="7b44d-212">IsHostApp</span></span>                        | <span data-ttu-id="7b44d-213">Указывает, что процесс является ведущим процессом, например Rundll32.exe или Dllhost.exe, и не должен учитываться при закреплении в меню **запуска** или включении в список наиболее часто используемых (часто используемые).</span><span class="sxs-lookup"><span data-stu-id="7b44d-213">Indicates that the process is a host process, such as Rundll32.exe or Dllhost.exe, and should not be considered for **Start** menu pinning or inclusion in the Most Frequently Used (MFU) list.</span></span> <span data-ttu-id="7b44d-214">При запуске с ярлыком, содержащим список аргументов, не равный null, или явные [идентификаторы модели пользователя приложения (аппусермоделидс)](appids.md), процесс можно закрепить (как это сочетание клавиш).</span><span class="sxs-lookup"><span data-stu-id="7b44d-214">When launched with a shortcut that contains a non-null argument list or an explicit [Application User Model IDs (AppUserModelIDs)](appids.md), the process can be pinned (as that shortcut).</span></span> <span data-ttu-id="7b44d-215">Такие сочетания клавиш являются кандидатами для включения в список наиболее часто используемых.</span><span class="sxs-lookup"><span data-stu-id="7b44d-215">Such shortcuts are candidates for inclusion in the MFU list.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7b44d-216">OnStartPage</span><span class="sxs-lookup"><span data-stu-id="7b44d-216">NoStartPage</span></span>                      | <span data-ttu-id="7b44d-217">Указывает, что исполняемый файл и ярлыки приложения следует исключить из меню **Пуск** , а также закреплять или включать в список наиболее часто используемых программ.</span><span class="sxs-lookup"><span data-stu-id="7b44d-217">Indicates that the application executable and shortcuts should be excluded from the **Start** menu and from pinning or inclusion in the MFU list.</span></span> <span data-ttu-id="7b44d-218">Эта запись обычно используется для исключения системных средств, установщиков и программ-установщиков и файлов readme.</span><span class="sxs-lookup"><span data-stu-id="7b44d-218">This entry is typically used to exclude system tools, installers and uninstallers, and readme files.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7b44d-219">усиксекутаблефортаскбарграупикон</span><span class="sxs-lookup"><span data-stu-id="7b44d-219">UseExecutableForTaskbarGroupIcon</span></span> | <span data-ttu-id="7b44d-220">Заставляет панель задач использовать значок этого исполняемого файла по умолчанию, если для этого приложения нет ярлыка также прикрепляемые, а вместо значка окна, которое было впервые обнаружено.</span><span class="sxs-lookup"><span data-stu-id="7b44d-220">Causes the taskbar to use the default icon of this executable if there is no pinnable shortcut for this application, and instead of the icon of the window that was first encountered.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7b44d-221">таскбарграупикон</span><span class="sxs-lookup"><span data-stu-id="7b44d-221">TaskbarGroupIcon</span></span>                 | <span data-ttu-id="7b44d-222">Задает значок, используемый для переопределения значка панели задач.</span><span class="sxs-lookup"><span data-stu-id="7b44d-222">Specifies the icon used to override the taskbar icon.</span></span> <span data-ttu-id="7b44d-223">Обычно для панели задач используется значок окна.</span><span class="sxs-lookup"><span data-stu-id="7b44d-223">The window icon is normally used for the taskbar.</span></span> <span data-ttu-id="7b44d-224">Установка записи Таскбарграупикон приводит к тому, что система использует значок из EXE приложения.</span><span class="sxs-lookup"><span data-stu-id="7b44d-224">Setting the TaskbarGroupIcon entry causes the system to use the icon from the .exe for the application instead.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="7b44d-225">Примеры</span><span class="sxs-lookup"><span data-stu-id="7b44d-225">Examples</span></span>

<span data-ttu-id="7b44d-226">Ниже приведены некоторые примеры регистраций приложений с **помощью \_ \_ корневых** \\ **приложений** \\ *ApplicationName.exe* подраздел "классы hKey".</span><span class="sxs-lookup"><span data-stu-id="7b44d-226">Some examples of application registrations through the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey are as follows.</span></span> <span data-ttu-id="7b44d-227">Все значения записей реестра имеют тип **reg \_ SZ** , за исключением **дефаултикон** , который имеет тип **\_ раскрытия reg Expand \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="7b44d-227">All registry entry values are of **REG\_SZ** type, with the exception of **DefaultIcon** which is of **REG\_EXPAND\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a><span data-ttu-id="7b44d-228">Регистрация команд и других сведений о сопоставлении файлов</span><span class="sxs-lookup"><span data-stu-id="7b44d-228">Registering Verbs and Other File Association Information</span></span>

<span data-ttu-id="7b44d-229">Подразделы, зарегистрированные в разделе **\_ классы hKey \_ root** \\ **системфилеассоЦиатионс** , позволяют оболочке определять поведение по умолчанию атрибутов для типов файлов и включать общие сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="7b44d-229">Subkeys registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** enable the Shell to define the default behavior of attributes for file types and enable shared file associations.</span></span> <span data-ttu-id="7b44d-230">Когда пользователь изменяет приложение по умолчанию для типа файлов, идентификатор ProgID нового приложения по умолчанию имеет приоритет в предоставлении команд и других сведений о сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="7b44d-230">When users change the default application for a file type, the ProgID of the new default application has priority in providing verbs and other association information.</span></span> <span data-ttu-id="7b44d-231">Этот приоритет обусловлен тем, что он является первой записью в массиве ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="7b44d-231">This priority is due to it being the first entry in the association array.</span></span> <span data-ttu-id="7b44d-232">Если программа по умолчанию изменена, сведения в предыдущем ProgID больше не будут доступны.</span><span class="sxs-lookup"><span data-stu-id="7b44d-232">If the default program is changed, the information under the previous ProgID is no longer available.</span></span>

<span data-ttu-id="7b44d-233">Чтобы заранее решить последствия изменения программ по умолчанию, можно использовать **\_ классы hKey \_ root** \\ **системфилеассоЦиатионс** для регистрации команд и других сведений о сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="7b44d-233">To deal proactively with the consequences of a change to default programs, you can use **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** to register verbs and other association information.</span></span> <span data-ttu-id="7b44d-234">Из-за их расположения после идентификатора ProgID в массиве ассоциаций эти регистрации имеют более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="7b44d-234">Due to their location after the ProgID in the association array, these registrations are lower priority.</span></span> <span data-ttu-id="7b44d-235">Эти СистемфилеассоЦиатионсрегистратионс стабильны, даже если пользователи меняют программы по умолчанию и предоставляют расположение для регистрации вторичных команд, которые всегда будут доступны для конкретного типа файлов.</span><span class="sxs-lookup"><span data-stu-id="7b44d-235">These SystemFileAssociationsregistrations are stable even when users change the default programs, and provide a location to register secondary verbs that will always be available for a particular file type.</span></span> <span data-ttu-id="7b44d-236">Пример реестра см. в подразделе [Регистрация наблюдаемого типа](#registering-a-perceived-type) далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="7b44d-236">For a registry example, see [Registering a Perceived Type](#registering-a-perceived-type) later in this topic.</span></span>

<span data-ttu-id="7b44d-237">В следующем примере реестра показано, что происходит, когда пользователь запускает элемент **программы по умолчанию** на панели управления, чтобы изменить файлы по умолчанию для MP3-файлов на App2ProgID.</span><span class="sxs-lookup"><span data-stu-id="7b44d-237">The following registry example shows what happens when the user runs the **Default Programs** item in Control Panel to change the default for .mp3 files to App2ProgID.</span></span> <span data-ttu-id="7b44d-238">После изменения значения по умолчанию Verb1 больше не доступно, а Verb2 становится значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b44d-238">After changing the default, Verb1 is no longer available, and Verb2 becomes the default.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a><span data-ttu-id="7b44d-239">Регистрация воспринимаемого типа</span><span class="sxs-lookup"><span data-stu-id="7b44d-239">Registering a Perceived Type</span></span>

<span data-ttu-id="7b44d-240">Значения реестра для наблюдаемых типов определяются как подразделы подраздела реестра **hKey \_ \_ root** \\ **системфилеассоЦиатионс** .</span><span class="sxs-lookup"><span data-stu-id="7b44d-240">Registry values for perceived types are defined as subkeys of the **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey.</span></span> <span data-ttu-id="7b44d-241">Например, **текст** распознанного типа регистрируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7b44d-241">For example, the perceived type **text** is registered as follows:</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

<span data-ttu-id="7b44d-242">Распознанный тип файла обозначается путем включения значения PerceivedType в подраздел типа файла.</span><span class="sxs-lookup"><span data-stu-id="7b44d-242">A file type's perceived type is indicated by including a PerceivedType value in the file type's subkey.</span></span> <span data-ttu-id="7b44d-243">Для значения PerceivedType задается имя воспринимаемого типа, зарегистрированного в подразделе реестра **hKey \_ \_ root** \\ **системфилеассоЦиатионс** , как показано в предыдущем примере реестра.</span><span class="sxs-lookup"><span data-stu-id="7b44d-243">The PerceivedType value is set to the name of the perceived type registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey, as shown in the previous registry example.</span></span> <span data-ttu-id="7b44d-244">Например, чтобы объявить cpp Files как воспринимаемый тип "текст", добавьте следующую запись реестра:</span><span class="sxs-lookup"><span data-stu-id="7b44d-244">To declare .cpp files as being of perceived type "text", for example, add the following registry entry:</span></span>

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a><span data-ttu-id="7b44d-245">См. также</span><span class="sxs-lookup"><span data-stu-id="7b44d-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b44d-246">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="7b44d-246">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="7b44d-247">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="7b44d-247">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="7b44d-248">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="7b44d-248">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="7b44d-249">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="7b44d-249">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="7b44d-250">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="7b44d-250">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="7b44d-251">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="7b44d-251">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="7b44d-252">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="7b44d-252">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="7b44d-253">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="7b44d-253">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

