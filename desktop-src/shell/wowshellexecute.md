---
description: Выполняет операцию с указанным файлом.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: Функция Вовшеллексекуте
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: ae50ad570211303cdfb7aa8e86908593ab48537d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187805"
---
# <a name="wowshellexecute-function"></a><span data-ttu-id="15a6e-103">Функция Вовшеллексекуте</span><span class="sxs-lookup"><span data-stu-id="15a6e-103">WOWShellExecute function</span></span>

<span data-ttu-id="15a6e-104">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="15a6e-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="15a6e-105">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="15a6e-106">Выполняет операцию с указанным файлом.</span><span class="sxs-lookup"><span data-stu-id="15a6e-106">Performs an operation on a specified file.</span></span> <span data-ttu-id="15a6e-107">**Вовшеллексекуте** существует только для использования с виртуальным компьютером DOS Microsoft Windows NT (Ntvdm.exe), который позволяет запускать дисковую операционную систему (DOS) и 16-разрядное программное обеспечение в системе Windows и не должно использоваться другими людьми.</span><span class="sxs-lookup"><span data-stu-id="15a6e-107">**WOWShellExecute** exists only for use with the Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe), which allows disk operating system (DOS) and 16-bit software to run on a Windows system, and should not be used by anyone else.</span></span> <span data-ttu-id="15a6e-108">Вместо этого используйте [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="15a6e-108">Use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a6e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15a6e-109">Syntax</span></span>


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a><span data-ttu-id="15a6e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="15a6e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a6e-111">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a6e-112">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="15a6e-112">Type: **HWND**</span></span>

<span data-ttu-id="15a6e-113">Маркер окна владельца, используемый для отображения пользовательского интерфейса или сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="15a6e-113">A handle to the owner window used for displaying a UI or error messages.</span></span> <span data-ttu-id="15a6e-114">Это значение может быть **равно NULL** , если операция не связана с окном.</span><span class="sxs-lookup"><span data-stu-id="15a6e-114">This value can be **NULL** if the operation is not associated with a window.</span></span>

</dd> <dt>

<span data-ttu-id="15a6e-115">*лпоператион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-115">*lpOperation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a6e-116">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="15a6e-116">Type: **LPCTSTR**</span></span>

<span data-ttu-id="15a6e-117">Указатель на строку, **завершающуюся нулем,** которая в данном случае называется *глаголом*, которая указывает выполняемое действие.</span><span class="sxs-lookup"><span data-stu-id="15a6e-117">A pointer to a **null**-terminated string, referred to in this case as a *verb*, that specifies the action to be performed.</span></span> <span data-ttu-id="15a6e-118">Набор доступных команд зависит от конкретного файла или папки.</span><span class="sxs-lookup"><span data-stu-id="15a6e-118">The set of available verbs depends on the particular file or folder.</span></span> <span data-ttu-id="15a6e-119">Как правило, действия, доступные в контекстном меню объекта, являются доступными командами.</span><span class="sxs-lookup"><span data-stu-id="15a6e-119">Generally, the actions available from an object's shortcut menu are available verbs.</span></span> <span data-ttu-id="15a6e-120">Дополнительные сведения о командах и их доступности см. в разделе " *команды объектов* " раздела [Запуск приложений](launch.md).</span><span class="sxs-lookup"><span data-stu-id="15a6e-120">For more information about verbs and their availability, see the *Object Verbs* section of [Launching Applications](launch.md).</span></span> <span data-ttu-id="15a6e-121">Дополнительные сведения о контекстных меню см. в разделе [расширение контекстных меню](context.md) .</span><span class="sxs-lookup"><span data-stu-id="15a6e-121">See [Extending Shortcut Menus](context.md) for further discussion of shortcut menus.</span></span> <span data-ttu-id="15a6e-122">Обычно используются следующие команды.</span><span class="sxs-lookup"><span data-stu-id="15a6e-122">The following verbs are commonly used.</span></span>

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span data-ttu-id="15a6e-123"><span id="edit"></span><span id="EDIT"></span>**Редактор**</span><span class="sxs-lookup"><span data-stu-id="15a6e-123"><span id="edit"></span><span id="EDIT"></span>**edit**</span></span>


</dt> <dd>

<span data-ttu-id="15a6e-124">Запускает редактор и открывает документ для редактирования.</span><span class="sxs-lookup"><span data-stu-id="15a6e-124">Launches an editor and opens the document for editing.</span></span> <span data-ttu-id="15a6e-125">Если *лпфиле* не является файлом документа, функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="15a6e-125">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span data-ttu-id="15a6e-126"><span id="explore"></span><span id="EXPLORE"></span>**просматриваем**</span><span class="sxs-lookup"><span data-stu-id="15a6e-126"><span id="explore"></span><span id="EXPLORE"></span>**explore**</span></span>


</dt> <dd>

<span data-ttu-id="15a6e-127">Изучает папку, указанную параметром *лпфиле*.</span><span class="sxs-lookup"><span data-stu-id="15a6e-127">Explores the folder specified by *lpFile*.</span></span>

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span data-ttu-id="15a6e-128"><span id="find"></span><span id="FIND"></span>**Найдено**</span><span class="sxs-lookup"><span data-stu-id="15a6e-128"><span id="find"></span><span id="FIND"></span>**find**</span></span>


</dt> <dd>

<span data-ttu-id="15a6e-129">Инициирует поиск, начиная с указанного каталога.</span><span class="sxs-lookup"><span data-stu-id="15a6e-129">Initiates a search starting from the specified directory.</span></span>

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span data-ttu-id="15a6e-130"><span id="open"></span><span id="OPEN"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="15a6e-130"><span id="open"></span><span id="OPEN"></span>**open**</span></span>


</dt> <dd>

<span data-ttu-id="15a6e-131">Открывает файл, указанный параметром *лпфиле* .</span><span class="sxs-lookup"><span data-stu-id="15a6e-131">Opens the file specified by the *lpFile* parameter.</span></span> <span data-ttu-id="15a6e-132">Файл может быть исполняемым файлом, файлом документа или папкой.</span><span class="sxs-lookup"><span data-stu-id="15a6e-132">The file can be an executable file, a document file, or a folder.</span></span>

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="15a6e-133"><span id="print"></span><span id="PRINT"></span>**печатал**</span><span class="sxs-lookup"><span data-stu-id="15a6e-133"><span id="print"></span><span id="PRINT"></span>**print**</span></span>


</dt> <dd>

<span data-ttu-id="15a6e-134">Выводит файл документа, указанный параметром *лпфиле*.</span><span class="sxs-lookup"><span data-stu-id="15a6e-134">Prints the document file specified by *lpFile*.</span></span> <span data-ttu-id="15a6e-135">Если *лпфиле* не является файлом документа, функция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="15a6e-135">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span data-ttu-id="15a6e-136"><span id="NULL"></span><span id="null"></span>**ЗАКАНЧИВАЮЩ**</span><span class="sxs-lookup"><span data-stu-id="15a6e-136"><span id="NULL"></span><span id="null"></span>**NULL**</span></span>


</dt> <dd>

<span data-ttu-id="15a6e-137">Для систем до Windows 2000 используется команда по умолчанию, если она является допустимой и доступна в реестре.</span><span class="sxs-lookup"><span data-stu-id="15a6e-137">For systems prior to Windows 2000, the default verb is used if it is valid and available in the registry.</span></span> <span data-ttu-id="15a6e-138">В противном случае используется команда "Открыть".</span><span class="sxs-lookup"><span data-stu-id="15a6e-138">If not, the "open" verb is used.</span></span>

<span data-ttu-id="15a6e-139">Для систем Windows 2000 и более поздних версий используется команда по умолчанию, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="15a6e-139">For Windows 2000 and later systems, the default verb is used if available.</span></span> <span data-ttu-id="15a6e-140">В противном случае используется команда "Открыть".</span><span class="sxs-lookup"><span data-stu-id="15a6e-140">If not, the "open" verb is used.</span></span> <span data-ttu-id="15a6e-141">Если ни один из этих команд недоступен, система использует первую команду, указанную в реестре.</span><span class="sxs-lookup"><span data-stu-id="15a6e-141">If neither verb is available, the system uses the first verb listed in the registry.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="15a6e-142">*лпфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-142">*lpFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a6e-143">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="15a6e-143">Type: **LPCTSTR**</span></span>

<span data-ttu-id="15a6e-144">Указатель на строку, **завершающуюся нулем,** которая указывает файл или объект, для которого необходимо выполнить указанную команду.</span><span class="sxs-lookup"><span data-stu-id="15a6e-144">A pointer to a **null**-terminated string that specifies the file or object on which to execute the specified verb.</span></span> <span data-ttu-id="15a6e-145">Чтобы указать объект пространства имен оболочки, передайте полное имя синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="15a6e-145">To specify a Shell namespace object, pass the fully qualified parse name.</span></span> <span data-ttu-id="15a6e-146">Обратите внимание, что не все команды поддерживаются для всех объектов.</span><span class="sxs-lookup"><span data-stu-id="15a6e-146">Note that not all verbs are supported on all objects.</span></span> <span data-ttu-id="15a6e-147">Например, не все типы документов поддерживают команду Print.</span><span class="sxs-lookup"><span data-stu-id="15a6e-147">For example, not all document types support the "print" verb.</span></span>

</dd> <dt>

<span data-ttu-id="15a6e-148">*лппараметерс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-148">*lpParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a6e-149">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="15a6e-149">Type: **LPCTSTR**</span></span>

<span data-ttu-id="15a6e-150">Если параметр *лпфиле* Задает исполняемый файл, *лппараметерс* является указателем на строку, **завершающуюся нулем,** которая указывает параметры, передаваемые в приложение.</span><span class="sxs-lookup"><span data-stu-id="15a6e-150">If the *lpFile* parameter specifies an executable file, *lpParameters* is a pointer to a **null**-terminated string that specifies the parameters to be passed to the application.</span></span> <span data-ttu-id="15a6e-151">Формат этой строки определяется вызываемой командой.</span><span class="sxs-lookup"><span data-stu-id="15a6e-151">The format of this string is determined by the verb that is to be invoked.</span></span> <span data-ttu-id="15a6e-152">Если *лпфиле* указывает файл документа, *Лппараметерс* должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="15a6e-152">If *lpFile* specifies a document file, *lpParameters* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="15a6e-153">*лпдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-153">*lpDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a6e-154">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="15a6e-154">Type: **LPCTSTR**</span></span>

<span data-ttu-id="15a6e-155">Указатель на строку, **завершающуюся нулем,** которая указывает каталог по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15a6e-155">A pointer to a **null**-terminated string that specifies the default directory.</span></span>

</dd> <dt>

<span data-ttu-id="15a6e-156">*ншовкмд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-156">*nShowCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a6e-157">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="15a6e-157">Type: **INT**</span></span>

<span data-ttu-id="15a6e-158">Флаги, определяющие способ отображения приложения при его открытии.</span><span class="sxs-lookup"><span data-stu-id="15a6e-158">The flags that specify how an application is to be displayed when it is opened.</span></span> <span data-ttu-id="15a6e-159">Если *лпфиле* указывает файл документа, флаг просто передается связанному приложению.</span><span class="sxs-lookup"><span data-stu-id="15a6e-159">If *lpFile* specifies a document file, the flag is simply passed to the associated application.</span></span> <span data-ttu-id="15a6e-160">Приложение может решить, как его справиться.</span><span class="sxs-lookup"><span data-stu-id="15a6e-160">It is up to the application to decide how to handle it.</span></span> <span data-ttu-id="15a6e-161">Это может быть любое из значений, которое можно указать в параметре *нкмдшов* для функции [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="15a6e-161">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="15a6e-162">*лпфнкбвинексек*</span><span class="sxs-lookup"><span data-stu-id="15a6e-162">*lpfnCBWinExec*</span></span> 
</dt> <dd>

<span data-ttu-id="15a6e-163">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="15a6e-163">Type: **void\***</span></span>

<span data-ttu-id="15a6e-164">Функция обратного вызова, используемая для вызова функции [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) в 16-разрядном ядре.</span><span class="sxs-lookup"><span data-stu-id="15a6e-164">Callback function used to call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in the 16-bit kernel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a6e-165">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15a6e-165">Return value</span></span>

<span data-ttu-id="15a6e-166">Тип: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="15a6e-166">Type: **HINSTANCE**</span></span>

<span data-ttu-id="15a6e-167">Возвращает значение, превышающее 32 в случае успеха, или значение ошибки, которое меньше или равно 32 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="15a6e-167">Returns a value greater than 32 if successful, or an error value that is less than or equal to 32 otherwise.</span></span> <span data-ttu-id="15a6e-168">В следующей таблице перечислены значения ошибок.</span><span class="sxs-lookup"><span data-stu-id="15a6e-168">The following table lists the error values.</span></span> <span data-ttu-id="15a6e-169">Возвращаемое значение приводится как HINSTANCE для обратной совместимости с 16-разрядными приложениями Windows.</span><span class="sxs-lookup"><span data-stu-id="15a6e-169">The return value is cast as an HINSTANCE for backward compatibility with 16-bit Windows applications.</span></span> <span data-ttu-id="15a6e-170">Однако это не является истинным значением HINSTANCE.</span><span class="sxs-lookup"><span data-stu-id="15a6e-170">It is not a true HINSTANCE, however.</span></span> <span data-ttu-id="15a6e-171">Единственное, что можно сделать с помощью возвращенного объекта HINSTANCE, — привести его к типу **int** и сравнить с значением 32 или одним из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="15a6e-171">The only thing that can be done with the returned HINSTANCE is to cast it to an **int** and compare it with the value 32 or one of the error codes below.</span></span>



| <span data-ttu-id="15a6e-172">Код возврата</span><span class="sxs-lookup"><span data-stu-id="15a6e-172">Return code</span></span>                                                                                             | <span data-ttu-id="15a6e-173">Описание</span><span class="sxs-lookup"><span data-stu-id="15a6e-173">Description</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="15a6e-174"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-174"><dt>**0**</dt></span></span> </dl>                        | <span data-ttu-id="15a6e-175">Операционной системе не хватает памяти или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15a6e-175">The operating system is out of memory or resources.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="15a6e-176"><dt>**\_файл ошибок \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-176"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="15a6e-177">Указанный файл не найден.</span><span class="sxs-lookup"><span data-stu-id="15a6e-177">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="15a6e-178"><dt>**\_путь к ошибке \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-178"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="15a6e-179">Указанный путь не найден.</span><span class="sxs-lookup"><span data-stu-id="15a6e-179">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="15a6e-180"><dt>**\_неправильный \_ Формат ошибки**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-180"><dt>**ERROR\_BAD\_FORMAT**</dt></span></span> </dl>       | <span data-ttu-id="15a6e-181">Недопустимый EXE-файл (не Win32. exe или ошибка в образе EXE).</span><span class="sxs-lookup"><span data-stu-id="15a6e-181">The .exe file is invalid (non-Win32 .exe or error in .exe image).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="15a6e-182"><dt>**\_ACCESSDENIED Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-182"><dt>**SE\_ERR\_ACCESSDENIED**</dt></span></span> </dl>    | <span data-ttu-id="15a6e-183">Операционная система отклонила доступ к указанному файлу.</span><span class="sxs-lookup"><span data-stu-id="15a6e-183">The operating system denied access to the specified file.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="15a6e-184"><dt>**\_ассоЦинкомплете Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-184"><dt>**SE\_ERR\_ASSOCINCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="15a6e-185">Неполное или недопустимое сопоставление имени файла.</span><span class="sxs-lookup"><span data-stu-id="15a6e-185">The file name association is incomplete or invalid.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="15a6e-186"><dt>**\_ддебуси Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-186"><dt>**SE\_ERR\_DDEBUSY**</dt></span></span> </dl>         | <span data-ttu-id="15a6e-187">Не удалось завершить транзакцию DDE, так как были обработаны другие транзакции DDE.</span><span class="sxs-lookup"><span data-stu-id="15a6e-187">The DDE transaction could not be completed because other DDE transactions were being processed.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="15a6e-188"><dt>**\_ддефаил Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-188"><dt>**SE\_ERR\_DDEFAIL**</dt></span></span> </dl>         | <span data-ttu-id="15a6e-189">Сбой транзакции DDE.</span><span class="sxs-lookup"><span data-stu-id="15a6e-189">The DDE transaction failed.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="15a6e-190"><dt>**\_ддетимеаут Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-190"><dt>**SE\_ERR\_DDETIMEOUT**</dt></span></span> </dl>      | <span data-ttu-id="15a6e-191">Не удалось завершить транзакцию DDE, так как истекло время ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="15a6e-191">The DDE transaction could not be completed because the request timed out.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="15a6e-192"><dt>**\_дллнотфаунд Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-192"><dt>**SE\_ERR\_DLLNOTFOUND**</dt></span></span> </dl>     | <span data-ttu-id="15a6e-193">Указанная библиотека DLL не найдена.</span><span class="sxs-lookup"><span data-stu-id="15a6e-193">The specified DLL was not found.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="15a6e-194"><dt>**\_фнф Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-194"><dt>**SE\_ERR\_FNF**</dt></span></span> </dl>             | <span data-ttu-id="15a6e-195">Указанный файл не найден.</span><span class="sxs-lookup"><span data-stu-id="15a6e-195">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="15a6e-196"><dt>**SE \_ Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-196"><dt>**SE\_ERR\_NOASSOC**</dt></span></span> </dl>         | <span data-ttu-id="15a6e-197">Отсутствует приложение, связанное с указанным расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="15a6e-197">There is no application associated with the given file name extension.</span></span> <span data-ttu-id="15a6e-198">Эта ошибка также будет возвращена при попытке распечатать непечатаемый файл.</span><span class="sxs-lookup"><span data-stu-id="15a6e-198">This error will also be returned if you attempt to print a file that is not printable.</span></span><br/> |
| <dl> <span data-ttu-id="15a6e-199"><dt>**SE \_ Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-199"><dt>**SE\_ERR\_OOM**</dt></span></span> </dl>             | <span data-ttu-id="15a6e-200">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="15a6e-200">There was not enough memory to complete the operation.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="15a6e-201"><dt>**\_ПНФ Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-201"><dt>**SE\_ERR\_PNF**</dt></span></span> </dl>             | <span data-ttu-id="15a6e-202">Указанный путь не найден.</span><span class="sxs-lookup"><span data-stu-id="15a6e-202">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="15a6e-203"><dt>**\_ \_ Общая папка Err**</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-203"><dt>**SE\_ERR\_SHARE**</dt></span></span> </dl>           | <span data-ttu-id="15a6e-204">Произошло нарушение совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="15a6e-204">A sharing violation occurred.</span></span><br/>                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="15a6e-205">Remarks</span><span class="sxs-lookup"><span data-stu-id="15a6e-205">Remarks</span></span>

<span data-ttu-id="15a6e-206">**Вовшеллексекуте** не включается в заголовок или LIB-файл.</span><span class="sxs-lookup"><span data-stu-id="15a6e-206">**WOWShellExecute** is not included in a header or .lib file.</span></span> <span data-ttu-id="15a6e-207">Он экспортируется из Shell32.dll по имени.</span><span class="sxs-lookup"><span data-stu-id="15a6e-207">It is exported from Shell32.dll by name.</span></span>

<span data-ttu-id="15a6e-208">Этот метод позволяет выполнять любые команды в контекстном меню папки или храниться в реестре.</span><span class="sxs-lookup"><span data-stu-id="15a6e-208">This method allows you to execute any commands in a folder's shortcut menu or stored in the registry.</span></span>

<span data-ttu-id="15a6e-209">Если *лпоператион* имеет **значение NULL**, функция открывает файл, заданный параметром *лпфиле*.</span><span class="sxs-lookup"><span data-stu-id="15a6e-209">If *lpOperation* is **NULL**, the function opens the file specified by *lpFile*.</span></span> <span data-ttu-id="15a6e-210">Если *лпоператион* имеет значение "Open" или "исследовать", функция пытается открыть или просмотреть папку.</span><span class="sxs-lookup"><span data-stu-id="15a6e-210">If *lpOperation* is "open" or "explore", the function attempts to open or explore the folder.</span></span>

<span data-ttu-id="15a6e-211">Чтобы получить сведения о приложении, которое запускается в результате вызова **вовшеллексекуте**, используйте [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="15a6e-211">To obtain information about the application that is launched as a result of calling **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

> [!Note]  
> <span data-ttu-id="15a6e-212">**Окна запуска папки в отдельном** параметре процесса в свойствах папки влияют на **вовшеллексекуте**.</span><span class="sxs-lookup"><span data-stu-id="15a6e-212">The **Launch folder windows in a separate process** setting in Folder Options affects **WOWShellExecute**.</span></span> <span data-ttu-id="15a6e-213">Если этот параметр отключен (значение по умолчанию), **вовшеллексекуте** использует открытое окно проводника вместо запуска нового.</span><span class="sxs-lookup"><span data-stu-id="15a6e-213">If that option is disabled (the default setting), **WOWShellExecute** uses an open Explorer window rather than launch a new one.</span></span> <span data-ttu-id="15a6e-214">Если окно проводника не открыто, **вовшеллексекуте** запускает новый.</span><span class="sxs-lookup"><span data-stu-id="15a6e-214">If no Explorer window is open, **WOWShellExecute** launches a new one.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15a6e-215">Требования</span><span class="sxs-lookup"><span data-stu-id="15a6e-215">Requirements</span></span>



| <span data-ttu-id="15a6e-216">Требование</span><span class="sxs-lookup"><span data-stu-id="15a6e-216">Requirement</span></span> | <span data-ttu-id="15a6e-217">Значение</span><span class="sxs-lookup"><span data-stu-id="15a6e-217">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15a6e-218">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15a6e-218">Minimum supported client</span></span><br/> | <span data-ttu-id="15a6e-219">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-219">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15a6e-220">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15a6e-220">Minimum supported server</span></span><br/> | <span data-ttu-id="15a6e-221">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15a6e-221">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15a6e-222">DLL</span><span class="sxs-lookup"><span data-stu-id="15a6e-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15a6e-223"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15a6e-223"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a6e-224">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15a6e-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a6e-225">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="15a6e-225">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
