---
description: Ограничение максимальной длины пути.
title: Ограничение максимальной длины пути
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: 4bf5050f24827a2033c1e56fd9413c04f4e59500
ms.sourcegitcommit: ece80b9b7082415b2f894b0696b6b3f0c8544d72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107899743"
---
# <a name="maximum-path-length-limitation"></a><span data-ttu-id="f83e4-103">Ограничение максимальной длины пути</span><span class="sxs-lookup"><span data-stu-id="f83e4-103">Maximum Path Length Limitation</span></span>

<span data-ttu-id="f83e4-104">В Windows API (с некоторыми исключениями, обсуждаемыми в следующих параграфах) максимальная длина пути — это **максимальный \_ путь**, который определен как 260 символов.</span><span class="sxs-lookup"><span data-stu-id="f83e4-104">In the Windows API (with some exceptions discussed in the following paragraphs), the maximum length for a path is **MAX\_PATH**, which is defined as 260 characters.</span></span> <span data-ttu-id="f83e4-105">Локальный путь структурирован в следующем порядке: буква диска, двоеточие, обратная косая черта, имена компонентов, разделенные обратной косой чертой, и завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="f83e4-105">A local path is structured in the following order: drive letter, colon, backslash, name components separated by backslashes, and a terminating null character.</span></span> <span data-ttu-id="f83e4-106">Например, максимальный путь на диске D — это "D: \\ *часть 256-символьного пути* &lt; NUL &gt; ", где " &lt; NUL &gt; " представляет невидимый завершающий нуль-символ для текущей системной кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="f83e4-106">For example, the maximum path on drive D is "D:\\*some 256-character path string*&lt;NUL&gt;" where "&lt;NUL&gt;" represents the invisible terminating null character for the current system codepage.</span></span> <span data-ttu-id="f83e4-107">(Символы < > используются для наглядности и не могут быть частью допустимой строки пути.)</span><span class="sxs-lookup"><span data-stu-id="f83e4-107">(The characters < > are used here for visual clarity and cannot be part of a valid path string.)</span></span>

<span data-ttu-id="f83e4-108">Например, это ограничение может быть достигнуто при клонировании репозитория Git с длинными именами файлов в папку с длинным именем.</span><span class="sxs-lookup"><span data-stu-id="f83e4-108">For example, you may hit this limitation if you are cloning a git repo that has long file names into a folder that itself has a long name.</span></span>


> [!Note]  
> <span data-ttu-id="f83e4-109">Функции файлового ввода-вывода в Windows API преобразуют "/" в " \\ " в процессе преобразования имени в имя в формате NT, за исключением случаев использования \\ \\ префикса "? \\ ", как описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="f83e4-109">File I/O functions in the Windows API convert "/" to "\\" as part of converting the name to an NT-style name, except when using the "\\\\?\\" prefix as detailed in the following sections.</span></span>

<span data-ttu-id="f83e4-110">В API Windows имеется множество функций, которые также имеют версии Юникода, позволяющие использовать путь расширенной длины для максимальной общей длины пути в 32 767 символов.</span><span class="sxs-lookup"><span data-stu-id="f83e4-110">The Windows API has many functions that also have Unicode versions to permit an extended-length path for a maximum total path length of 32,767 characters.</span></span> <span data-ttu-id="f83e4-111">Этот тип пути состоит из компонентов, разделенных символами обратной косой черты, до значения, возвращаемого в параметре *лпмаксимумкомпонентленгс* функции [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) (обычно это значение 255 символов).</span><span class="sxs-lookup"><span data-stu-id="f83e4-111">This type of path is composed of components separated by backslashes, each up to the value returned in the *lpMaximumComponentLength* parameter of the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function (this value is commonly 255 characters).</span></span> <span data-ttu-id="f83e4-112">Чтобы указать путь расширенной длины, используйте \\ \\ префикс "? \\ ".</span><span class="sxs-lookup"><span data-stu-id="f83e4-112">To specify an extended-length path, use the "\\\\?\\" prefix.</span></span> <span data-ttu-id="f83e4-113">Например, " \\ \\ ? \\ D: \\ *очень длинный путь*".</span><span class="sxs-lookup"><span data-stu-id="f83e4-113">For example, "\\\\?\\D:\\*very long path*".</span></span>

> [!Note]  
> <span data-ttu-id="f83e4-114">Максимальный путь в 32 767 символов приблизительный, так как префикс " \\ \\ ? \\ " может быть расширен до более длинной строки системой во время выполнения, а это расширение применяется к общей длине.</span><span class="sxs-lookup"><span data-stu-id="f83e4-114">The maximum path of 32,767 characters is approximate, because the "\\\\?\\" prefix may be expanded to a longer string by the system at run time, and this expansion applies to the total length.</span></span>

<span data-ttu-id="f83e4-115">Префикс " \\ \\ ? \\ " также можно использовать с путями, созданными в соответствии с соглашением об универсальных именах (UNC).</span><span class="sxs-lookup"><span data-stu-id="f83e4-115">The "\\\\?\\" prefix can also be used with paths constructed according to the universal naming convention (UNC).</span></span> <span data-ttu-id="f83e4-116">Чтобы указать такой путь с помощью UNC, используйте параметр " \\ \\ ? \\ UNC- \\ префикс.</span><span class="sxs-lookup"><span data-stu-id="f83e4-116">To specify such a path using UNC, use the "\\\\?\\UNC\\" prefix.</span></span> <span data-ttu-id="f83e4-117">Например, " \\ \\ ? \\ Общая \\ папка сервера UNC \\ ", где" Server "— это имя компьютера, а" Share "— имя общей папки.</span><span class="sxs-lookup"><span data-stu-id="f83e4-117">For example, "\\\\?\\UNC\\server\\share", where "server" is the name of the computer and "share" is the name of the shared folder.</span></span> <span data-ttu-id="f83e4-118">Эти префиксы не используются как часть самого пути.</span><span class="sxs-lookup"><span data-stu-id="f83e4-118">These prefixes are not used as part of the path itself.</span></span> <span data-ttu-id="f83e4-119">Они указывают, что путь должен быть передан в систему с минимальным изменением, что означает, что нельзя использовать косую черту для представления разделителей пути или точку для представления текущего каталога или двойные точки для представления родительского каталога.</span><span class="sxs-lookup"><span data-stu-id="f83e4-119">They indicate that the path should be passed to the system with minimal modification, which means that you cannot use forward slashes to represent path separators, or a period to represent the current directory, or double dots to represent the parent directory.</span></span> <span data-ttu-id="f83e4-120">Поскольку нельзя использовать \\ \\ префикс "? \\ " с относительным путем, относительные пути всегда ограничены максимальным числом символов **\_ пути** .</span><span class="sxs-lookup"><span data-stu-id="f83e4-120">Because you cannot use the "\\\\?\\" prefix with a relative path, relative paths are always limited to a total of **MAX\_PATH** characters.</span></span>

<span data-ttu-id="f83e4-121">Нет необходимости выполнять нормализацию Юникода в строках пути и имени файла для использования функциями API файлового ввода-вывода Windows, так как файловая система обрабатывает путь и имена файлов как непрозрачные последовательности **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="f83e4-121">There is no need to perform any Unicode normalization on path and file name strings for use by the Windows file I/O API functions because the file system treats path and file names as an opaque sequence of **WCHAR** s.</span></span> <span data-ttu-id="f83e4-122">Любые нормализации, которые требуются вашему приложению, должны быть выполнены с учетом внешних вызовов связанных функций API файлового ввода-вывода Windows.</span><span class="sxs-lookup"><span data-stu-id="f83e4-122">Any normalization that your application requires should be performed with this in mind, external of any calls to related Windows file I/O API functions.</span></span>

<span data-ttu-id="f83e4-123">При использовании API для создания каталога указанный путь не может быть настолько длинным, что нельзя добавить имя файла 8,3 (т. е. имя каталога не может превышать **максимальный \_ путь** минус 12).</span><span class="sxs-lookup"><span data-stu-id="f83e4-123">When using an API to create a directory, the specified path cannot be so long that you cannot append an 8.3 file name (that is, the directory name cannot exceed **MAX\_PATH** minus 12).</span></span>

<span data-ttu-id="f83e4-124">Оболочка и файловая система имеют разные требования.</span><span class="sxs-lookup"><span data-stu-id="f83e4-124">The shell and the file system have different requirements.</span></span> <span data-ttu-id="f83e4-125">Можно создать путь с помощью API Windows, который пользовательский интерфейс оболочки не может интерпретировать правильно.</span><span class="sxs-lookup"><span data-stu-id="f83e4-125">It is possible to create a path with the Windows API that the shell user interface is not able to interpret properly.</span></span>

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a><span data-ttu-id="f83e4-126">Включение длинных путей в Windows 10, версии 1607 и более поздних</span><span class="sxs-lookup"><span data-stu-id="f83e4-126">Enable Long Paths in Windows 10, Version 1607, and Later</span></span>

<span data-ttu-id="f83e4-127">Начиная с Windows 10, в версии 1607 были удалены ограничения по **максимальному \_ пути** из общих функций файлов и каталогов Win32.</span><span class="sxs-lookup"><span data-stu-id="f83e4-127">Starting in Windows 10, version 1607, **MAX\_PATH** limitations have been removed from common Win32 file and directory functions.</span></span> <span data-ttu-id="f83e4-128">Однако необходимо явно принять участие в новом поведении.</span><span class="sxs-lookup"><span data-stu-id="f83e4-128">However, you must opt-in to the new behavior.</span></span>

<span data-ttu-id="f83e4-129">Чтобы обеспечить новое поведение при полном пути, должны выполняться оба следующих условия.</span><span class="sxs-lookup"><span data-stu-id="f83e4-129">To enable the new long path behavior, both of the following conditions must be met:</span></span>

* <span data-ttu-id="f83e4-130">Раздел реестра `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` должен существовать и иметь значение 1.</span><span class="sxs-lookup"><span data-stu-id="f83e4-130">The registry key `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` must exist and be set to 1.</span></span> <span data-ttu-id="f83e4-131">Значение ключа будет кэшироваться системой (на процесс) после первого вызова затронутого файла или функции каталога Win32 (см. ниже для списка функций).</span><span class="sxs-lookup"><span data-stu-id="f83e4-131">The key's value will be cached by the system (per process) after the first call to an affected Win32 file or directory function (see below for the list of functions).</span></span> <span data-ttu-id="f83e4-132">Этот раздел реестра не будет перезагружен в течение времени существования процесса.</span><span class="sxs-lookup"><span data-stu-id="f83e4-132">The registry key will not be reloaded during the lifetime of the process.</span></span> <span data-ttu-id="f83e4-133">Чтобы все приложения в системе могли распознать значение ключа, может потребоваться перезагрузка, так как некоторые процессы могли быть запущены до установки ключа.</span><span class="sxs-lookup"><span data-stu-id="f83e4-133">In order for all apps on the system to recognize the value of the key, a reboot might be required because some processes may have started before the key was set.</span></span>

<span data-ttu-id="f83e4-134">Можно также скопировать этот код в `.reg` файл, который может задать это значение, или использовать команду PowerShell из окна терминала с повышенными привилегиями:</span><span class="sxs-lookup"><span data-stu-id="f83e4-134">You can also copy this code to a `.reg` file which can set this for you, or use the PowerShell command from a terminal window with elevated privileges:</span></span>
# <a name="cmd"></a>[<span data-ttu-id="f83e4-135">cmd</span><span class="sxs-lookup"><span data-stu-id="f83e4-135">cmd</span></span>](#tab/cmd)

```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

# <a name="powershell"></a>[<span data-ttu-id="f83e4-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f83e4-136">PowerShell</span></span>](#tab/powershell)

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force

```

---

> [!NOTE]  
> <span data-ttu-id="f83e4-137">Этот раздел реестра можно также контролировать с помощью групповая политика по адресу `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` .</span><span class="sxs-lookup"><span data-stu-id="f83e4-137">This registry key can also be controlled via Group Policy at `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths`.</span></span>

* <span data-ttu-id="f83e4-138">[Манифест приложения](../sbscs/application-manifests.md) также должен содержать `longPathAware` элемент.</span><span class="sxs-lookup"><span data-stu-id="f83e4-138">The [application manifest](../sbscs/application-manifests.md) must also include the `longPathAware` element.</span></span>

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

<span data-ttu-id="f83e4-139">Это функции управления каталогом, которые больше не имеют ограничений на **Максимальное число \_ путей** , если вы явно хотите использовать режим длинного пути: Креатедиректорив, Креатедиректорексв жеткуррентдиректорив ремоведиректорив сеткуррентдиректорив.</span><span class="sxs-lookup"><span data-stu-id="f83e4-139">These are the directory management functions that no longer have **MAX\_PATH** restrictions if you opt-in to long path behavior: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.</span></span>

<span data-ttu-id="f83e4-140">Это функции управления файлами, которые больше не имеют ограничений на **максимальную длину \_ пути** , если вы явно задействуете поведение пути: копифилев, CopyFile2, копифиликсв, креатефилев, CreateFile2, креатехардлинкв, креатесимболиклинкв, делетефилев, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW.</span><span class="sxs-lookup"><span data-stu-id="f83e4-140">These are the file management functions that no longer have **MAX\_PATH** restrictions if you opt-in to long path behavior: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW.</span></span>
