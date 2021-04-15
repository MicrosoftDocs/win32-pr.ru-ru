---
description: Переименовывает файл записи каталога, указанный в пути объекта.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Метод Rename класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655640"
---
# <a name="rename-method-of-the-win32_directory-class"></a><span data-ttu-id="92c6c-103">Переименование метода \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="92c6c-103">Rename method of the Win32\_Directory class</span></span>

<span data-ttu-id="92c6c-104">Метод класса **Rename** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) переименовывает файл записи каталога, указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="92c6c-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the directory entry file specified in the object path.</span></span> <span data-ttu-id="92c6c-105">Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="92c6c-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="92c6c-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="92c6c-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="92c6c-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="92c6c-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="92c6c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92c6c-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="92c6c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="92c6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c6c-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="92c6c-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="92c6c-111">Полное новое имя файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="92c6c-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="92c6c-112">Пример: c: \\ temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="92c6c-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c6c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92c6c-113">Return value</span></span>

<span data-ttu-id="92c6c-114">Возвращает значение 0 (нуль), если файл был успешно переименован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="92c6c-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="92c6c-115">**0**</span><span class="sxs-lookup"><span data-stu-id="92c6c-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-116">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="92c6c-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-117">**2**</span><span class="sxs-lookup"><span data-stu-id="92c6c-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-118">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="92c6c-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-119">**8**</span><span class="sxs-lookup"><span data-stu-id="92c6c-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-120">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="92c6c-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-121">**9**</span><span class="sxs-lookup"><span data-stu-id="92c6c-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-122">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="92c6c-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-123">**10**</span><span class="sxs-lookup"><span data-stu-id="92c6c-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-124">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="92c6c-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-125">**11**</span><span class="sxs-lookup"><span data-stu-id="92c6c-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-126">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="92c6c-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-127">**12**</span><span class="sxs-lookup"><span data-stu-id="92c6c-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-128">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="92c6c-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-129">**13**</span><span class="sxs-lookup"><span data-stu-id="92c6c-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-130">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="92c6c-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-131">**14**</span><span class="sxs-lookup"><span data-stu-id="92c6c-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-132">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="92c6c-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-133">**15**</span><span class="sxs-lookup"><span data-stu-id="92c6c-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-134">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="92c6c-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-135">**16**</span><span class="sxs-lookup"><span data-stu-id="92c6c-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-136">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="92c6c-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-137">**17**</span><span class="sxs-lookup"><span data-stu-id="92c6c-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-138">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="92c6c-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="92c6c-139">**открыт**</span><span class="sxs-lookup"><span data-stu-id="92c6c-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="92c6c-140">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="92c6c-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92c6c-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92c6c-141">Remarks</span></span>

<span data-ttu-id="92c6c-142">Чтобы переименовать папку, сначала выполните привязку к рассматриваемой папке, а затем вызовите метод Rename.</span><span class="sxs-lookup"><span data-stu-id="92c6c-142">To rename a folder, first bind to the folder in question and then call the Rename method.</span></span> <span data-ttu-id="92c6c-143">В качестве единственного параметра для метода передайте новое имя папки в качестве полного пути.</span><span class="sxs-lookup"><span data-stu-id="92c6c-143">As the sole parameter to the method, pass the new name for the folder as a complete path name.</span></span> <span data-ttu-id="92c6c-144">Например, если папка в \\ \\ резервной копии журналов c: Scripts \\ переименована c: \\ Scripts \\ Archive, необходимо передать в c: \\ Scripts \\ Archive в качестве полного имени папки.</span><span class="sxs-lookup"><span data-stu-id="92c6c-144">For example, if the folder in the C:\\Scripts\\Logs\\Backup is to be renamed C:\\Scripts\\Archive, you must pass C:\\Scripts\\Archive as the complete folder name.</span></span> <span data-ttu-id="92c6c-145">Передача только имени папки-Archive-приводит к ошибке недопустимого пути.</span><span class="sxs-lookup"><span data-stu-id="92c6c-145">Passing only the folder name - Archive - results in an Invalid path error.</span></span>

<span data-ttu-id="92c6c-146">\_Класс каталога Win32 не предоставляет одношаговый метод для перемещения папок.</span><span class="sxs-lookup"><span data-stu-id="92c6c-146">The Win32\_Directory class does not provide a one-step method for moving folders.</span></span> <span data-ttu-id="92c6c-147">Вместо этого перемещение папки обычно состоит из двух этапов:</span><span class="sxs-lookup"><span data-stu-id="92c6c-147">Instead, moving a folder generally involves two steps:</span></span>

<dl> 1. <span data-ttu-id="92c6c-148">Копирование папки в новое расположение</span><span class="sxs-lookup"><span data-stu-id="92c6c-148">Copying the folder to its new location</span></span>  
2. <span data-ttu-id="92c6c-149">Удаление исходной папки</span><span class="sxs-lookup"><span data-stu-id="92c6c-149">Deleting the original folder</span></span>  
</dl>

<span data-ttu-id="92c6c-150">Единственным исключением из этого двух этапов является перемещение папки в новое расположение на том же диске.</span><span class="sxs-lookup"><span data-stu-id="92c6c-150">The one exception to this two-step process involves moving a folder to a new location on the same drive.</span></span> <span data-ttu-id="92c6c-151">Например, предположим, что вы хотите переместить C: \\ TEMP в c: \\ скрипты \\ временных файлов \\ .</span><span class="sxs-lookup"><span data-stu-id="92c6c-151">For example, suppose you want to move C:\\Temp to C:\\Scripts\\Temporary Files\\Archive.</span></span> <span data-ttu-id="92c6c-152">Пока текущее расположение и новое расположение находятся на одном диске, можно переместить папку, просто вызвав метод Rename и передав новое расположение в качестве параметра метода.</span><span class="sxs-lookup"><span data-stu-id="92c6c-152">As long as the current location and the new location are on the same drive, you can move the folder by simply calling the Rename method and passing the new location as the method parameter.</span></span> <span data-ttu-id="92c6c-153">Этот подход позволяет эффективно перемещать папку за один шаг.</span><span class="sxs-lookup"><span data-stu-id="92c6c-153">This approach effectively allows you to move the folder in a single step.</span></span> <span data-ttu-id="92c6c-154">Однако сценарий завершается ошибкой, если текущий диск и новый диск отличаются.</span><span class="sxs-lookup"><span data-stu-id="92c6c-154">However, the script fails if the current drive and the new drive are different.</span></span> <span data-ttu-id="92c6c-155">Попытка переименовать C: \\ TEMP в D: \\ TEMP завершается сбоем с ошибкой "диск не совпадает".</span><span class="sxs-lookup"><span data-stu-id="92c6c-155">An attempt to rename C:\\Temp to D:\\Temp fails with a "Drive not the same" error.</span></span>

## <a name="examples"></a><span data-ttu-id="92c6c-156">Примеры</span><span class="sxs-lookup"><span data-stu-id="92c6c-156">Examples</span></span>

<span data-ttu-id="92c6c-157">Следующий код из примера [перемещения папки с помощью WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript в коллекции TechNet использует метод Rename для перемещения папки c: \\ Scripts to c: \\ Администраторы \\ документы \\ Архив \\ VBScript.</span><span class="sxs-lookup"><span data-stu-id="92c6c-157">The following code, from the [Move a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript sample on TechNet Gallery, uses the Rename method to move the folder C:\\Scripts to C:\\Admins\\Documents\\Archive\\VBScript.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
Next
```



## <a name="requirements"></a><span data-ttu-id="92c6c-158">Требования</span><span class="sxs-lookup"><span data-stu-id="92c6c-158">Requirements</span></span>



| <span data-ttu-id="92c6c-159">Требование</span><span class="sxs-lookup"><span data-stu-id="92c6c-159">Requirement</span></span> | <span data-ttu-id="92c6c-160">Значение</span><span class="sxs-lookup"><span data-stu-id="92c6c-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92c6c-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92c6c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="92c6c-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92c6c-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92c6c-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92c6c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="92c6c-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92c6c-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92c6c-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92c6c-165">Namespace</span></span><br/>                | <span data-ttu-id="92c6c-166">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="92c6c-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92c6c-167">MOF</span><span class="sxs-lookup"><span data-stu-id="92c6c-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92c6c-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92c6c-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92c6c-169">DLL</span><span class="sxs-lookup"><span data-stu-id="92c6c-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92c6c-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92c6c-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c6c-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92c6c-171">See also</span></span>

<dl> <dt>

<span data-ttu-id="92c6c-172">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92c6c-172">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="92c6c-173">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="92c6c-173">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

