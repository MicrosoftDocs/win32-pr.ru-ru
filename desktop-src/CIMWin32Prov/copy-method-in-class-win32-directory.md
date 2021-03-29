---
description: Копирует файл или каталог записи логического каталога, указанный в пути к объекту, в расположение, указанное параметром input.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Метод Copy класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141662"
---
# <a name="copy-method-of-the-win32_directory-class"></a><span data-ttu-id="1ca49-103">Метод Copy \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="1ca49-103">Copy method of the Win32\_Directory class</span></span>

<span data-ttu-id="1ca49-104">Метод **копирования** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) копирует логический файл или каталог записи каталога, указанный в пути к объекту, в расположение, указанное параметром input.</span><span class="sxs-lookup"><span data-stu-id="1ca49-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="1ca49-105">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="1ca49-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="1ca49-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="1ca49-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1ca49-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1ca49-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ca49-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ca49-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="1ca49-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ca49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ca49-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="1ca49-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="1ca49-111">Полное имя копии файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="1ca49-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="1ca49-112">Пример: c: \\ temp \\ невдиректори</span><span class="sxs-lookup"><span data-stu-id="1ca49-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ca49-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ca49-113">Return value</span></span>

<span data-ttu-id="1ca49-114">Возвращает значение 0 (нуль), если файл был успешно скопирован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="1ca49-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1ca49-115">**0**</span><span class="sxs-lookup"><span data-stu-id="1ca49-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-116">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1ca49-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-117">**2**</span><span class="sxs-lookup"><span data-stu-id="1ca49-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-118">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="1ca49-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-119">**8**</span><span class="sxs-lookup"><span data-stu-id="1ca49-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-120">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1ca49-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-121">**9**</span><span class="sxs-lookup"><span data-stu-id="1ca49-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-122">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="1ca49-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-123">**10**</span><span class="sxs-lookup"><span data-stu-id="1ca49-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-124">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="1ca49-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-125">**11**</span><span class="sxs-lookup"><span data-stu-id="1ca49-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-126">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="1ca49-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-127">**12**</span><span class="sxs-lookup"><span data-stu-id="1ca49-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-128">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="1ca49-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-129">**13**</span><span class="sxs-lookup"><span data-stu-id="1ca49-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-130">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="1ca49-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-131">**14**</span><span class="sxs-lookup"><span data-stu-id="1ca49-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-132">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="1ca49-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-133">**15**</span><span class="sxs-lookup"><span data-stu-id="1ca49-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-134">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="1ca49-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-135">**16**</span><span class="sxs-lookup"><span data-stu-id="1ca49-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-136">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="1ca49-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-137">**17**</span><span class="sxs-lookup"><span data-stu-id="1ca49-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-138">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="1ca49-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1ca49-139">**открыт**</span><span class="sxs-lookup"><span data-stu-id="1ca49-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1ca49-140">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="1ca49-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ca49-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ca49-141">Remarks</span></span>

<span data-ttu-id="1ca49-142">Папки часто необходимо копировать из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="1ca49-142">Folders often need to be copied from one location to another.</span></span> <span data-ttu-id="1ca49-143">Например, вы можете скопировать папку с одного сервера на другой, чтобы создать резервную копию этой папки.</span><span class="sxs-lookup"><span data-stu-id="1ca49-143">For example, you might copy a folder from one server to another to create a backup copy of that folder.</span></span> <span data-ttu-id="1ca49-144">Также можно иметь папку Templates, которую необходимо скопировать на рабочие станции пользователей, или папку Scripts, которая должна быть скопирована на все DNS-серверы.</span><span class="sxs-lookup"><span data-stu-id="1ca49-144">Or you might have a templates folder that needs to be copied to user workstations, or a scripts folder that should be copied to all of your DNS servers.</span></span>

<span data-ttu-id="1ca49-145">\_Метод копирования каталогов Win32 позволяет копировать папку из одного расположения в другое либо на том же компьютере (например, при копировании папки с диска C на диск D), либо на удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="1ca49-145">The Win32\_Directory Copy method enables you to copy a folder from one location to another, either on the same computer (for example, copying a folder from drive C to drive D) or on a remote computer.</span></span> <span data-ttu-id="1ca49-146">Чтобы скопировать папку, необходимо вернуть экземпляр копируемой папки, а затем вызвать метод Copy, передав в качестве параметра целевое расположение новой копии папки.</span><span class="sxs-lookup"><span data-stu-id="1ca49-146">To copy a folder, you return an instance of the folder to be copied and then call the Copy method, passing as a parameter the target location for the new copy of the folder.</span></span> <span data-ttu-id="1ca49-147">Например, эта строка кода копирует папку в папку Scripts на диске F:</span><span class="sxs-lookup"><span data-stu-id="1ca49-147">For example, this line of code copies a folder to the Scripts folder on drive F:</span></span>

`objFolder.Copy("F:\Scripts")`

<span data-ttu-id="1ca49-148">Инструментарий WMI не перезаписывает существующую папку при выполнении метода Copy.</span><span class="sxs-lookup"><span data-stu-id="1ca49-148">WMI will not overwrite an existing folder when executing the Copy method.</span></span> <span data-ttu-id="1ca49-149">Это означает, что операция копирования завершится ошибкой, если папка назначения существует.</span><span class="sxs-lookup"><span data-stu-id="1ca49-149">This means that the copy operation fails if the destination folder exists.</span></span> <span data-ttu-id="1ca49-150">Например, предположим, что у вас есть папка с именем Scripts и вы пытаетесь скопировать эту папку в удаленную общую папку с именем \\ \\ Archive-FS-01 \\ .</span><span class="sxs-lookup"><span data-stu-id="1ca49-150">For example, suppose you have a folder named Scripts and you attempt to copy that folder to a remote share named \\\\atl-fs-01\\archive.</span></span> <span data-ttu-id="1ca49-151">Если папка с именем Scripts уже существует в этой общей папке, операция копирования завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="1ca49-151">If a folder named Scripts already exists on that share, the copy operation fails.</span></span>

## <a name="examples"></a><span data-ttu-id="1ca49-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="1ca49-152">Examples</span></span>

<span data-ttu-id="1ca49-153">Пример кода следующий, взятый из [копии папки с помощью инструментария WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), использует метод Copy для копирования папки C: \\ Scripts в D: \\ Archive.</span><span class="sxs-lookup"><span data-stu-id="1ca49-153">The followng code sample, taken from the [Copy a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), uses the Copy method to copy the folder C:\\Scripts to D:\\Archive.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
Next
```



## <a name="requirements"></a><span data-ttu-id="1ca49-154">Требования</span><span class="sxs-lookup"><span data-stu-id="1ca49-154">Requirements</span></span>



| <span data-ttu-id="1ca49-155">Требование</span><span class="sxs-lookup"><span data-stu-id="1ca49-155">Requirement</span></span> | <span data-ttu-id="1ca49-156">Значение</span><span class="sxs-lookup"><span data-stu-id="1ca49-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca49-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ca49-157">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca49-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ca49-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1ca49-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ca49-159">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca49-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ca49-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ca49-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1ca49-161">Namespace</span></span><br/>                | <span data-ttu-id="1ca49-162">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1ca49-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1ca49-163">MOF</span><span class="sxs-lookup"><span data-stu-id="1ca49-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ca49-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ca49-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ca49-165">DLL</span><span class="sxs-lookup"><span data-stu-id="1ca49-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ca49-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ca49-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ca49-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ca49-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ca49-168">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ca49-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1ca49-169">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="1ca49-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

