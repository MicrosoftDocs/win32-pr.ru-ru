---
description: Метод удаления класса WMI удалит логический файл (или каталог), указанный в пути объекта.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Метод Delete класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 843583698c11c1b9ad8f08e83aa6e4b894b55db8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656079"
---
# <a name="delete-method-of-the-win32_directory-class"></a><span data-ttu-id="f31a1-103">Метод DELETE \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="f31a1-103">Delete method of the Win32\_Directory class</span></span>

<span data-ttu-id="f31a1-104">Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удалит логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="f31a1-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span>

<span data-ttu-id="f31a1-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="f31a1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f31a1-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f31a1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f31a1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f31a1-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="f31a1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f31a1-108">Parameters</span></span>

<span data-ttu-id="f31a1-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f31a1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f31a1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f31a1-110">Return value</span></span>

<span data-ttu-id="f31a1-111">Возвращает значение 0 (нуль), если файл был успешно удален, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="f31a1-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f31a1-112">**0**</span><span class="sxs-lookup"><span data-stu-id="f31a1-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-113">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f31a1-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-114">**2**</span><span class="sxs-lookup"><span data-stu-id="f31a1-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-115">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="f31a1-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-116">**8**</span><span class="sxs-lookup"><span data-stu-id="f31a1-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-117">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f31a1-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-118">**9**</span><span class="sxs-lookup"><span data-stu-id="f31a1-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-119">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="f31a1-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-120">**10**</span><span class="sxs-lookup"><span data-stu-id="f31a1-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-121">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="f31a1-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-122">**11**</span><span class="sxs-lookup"><span data-stu-id="f31a1-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-123">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="f31a1-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-124">**12**</span><span class="sxs-lookup"><span data-stu-id="f31a1-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-125">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="f31a1-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-126">**13**</span><span class="sxs-lookup"><span data-stu-id="f31a1-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-127">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="f31a1-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-128">**14**</span><span class="sxs-lookup"><span data-stu-id="f31a1-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-129">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="f31a1-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-130">**15**</span><span class="sxs-lookup"><span data-stu-id="f31a1-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-131">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f31a1-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-132">**16**</span><span class="sxs-lookup"><span data-stu-id="f31a1-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-133">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="f31a1-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-134">**17**</span><span class="sxs-lookup"><span data-stu-id="f31a1-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-135">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="f31a1-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f31a1-136">**открыт**</span><span class="sxs-lookup"><span data-stu-id="f31a1-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f31a1-137">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="f31a1-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f31a1-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f31a1-138">Remarks</span></span>

<span data-ttu-id="f31a1-139">Папки не обязательно являются постоянными добавлениями в файловую систему.</span><span class="sxs-lookup"><span data-stu-id="f31a1-139">Folders are not necessarily permanent additions to a file system.</span></span> <span data-ttu-id="f31a1-140">В какой-то момент может потребоваться удалить папки, возможно, потому, что они больше не требуются, так как роль компьютера изменилась или папки были созданы по ошибке.</span><span class="sxs-lookup"><span data-stu-id="f31a1-140">At some point, folders might need to be deleted, perhaps because they are no longer required, because the role of the computer has changed, or because the folders were created by mistake.</span></span>

<span data-ttu-id="f31a1-141">Delete позволяет удалять папки. Вы просто выполняете привязку к рассматриваемой папке, а затем вызываете метод Delete.</span><span class="sxs-lookup"><span data-stu-id="f31a1-141">Delete allows you to delete folders: you simply bind to the folder in question and then call the Delete method.</span></span> <span data-ttu-id="f31a1-142">После вызова метода Delete папка удаляется из файловой системы без возможности восстановления. Он не отправляется в корзину.</span><span class="sxs-lookup"><span data-stu-id="f31a1-142">After the Delete method is called, the folder is permanently removed from the file system; it is not sent to the Recycle Bin.</span></span> <span data-ttu-id="f31a1-143">Кроме того, выдается сообщение об отсутствии подтверждения ("вы действительно хотите удалить эту папку?").</span><span class="sxs-lookup"><span data-stu-id="f31a1-143">In addition, no confirmation notice ("Are you sure you want to delete this folder?") is issued.</span></span> <span data-ttu-id="f31a1-144">Вместо этого папка немедленно удаляется.</span><span class="sxs-lookup"><span data-stu-id="f31a1-144">Instead, the folder is immediately removed.</span></span>

<span data-ttu-id="f31a1-145">Нельзя удалять папки, которые доступны только для чтения, с помощью FileSystemObject; Однако это можно сделать с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="f31a1-145">You cannot delete read-only folders using the FileSystemObject; however, this can be done using WMI.</span></span> <span data-ttu-id="f31a1-146">Если скрипт использует инструментарий WMI и вы не хотите удалять папку только для чтения, необходимо использовать свойство для чтения, чтобы проверить состояние папки перед его удалением.</span><span class="sxs-lookup"><span data-stu-id="f31a1-146">If your script uses WMI and you do not want to remove a read-only folder, you must use the Readable property to check the folder status before deleting it.</span></span>

## <a name="examples"></a><span data-ttu-id="f31a1-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="f31a1-147">Examples</span></span>

<span data-ttu-id="f31a1-148">Следующий пример кода VBScript удаляет папку C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="f31a1-148">The following VBScript code sample deletes the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="f31a1-149">Требования</span><span class="sxs-lookup"><span data-stu-id="f31a1-149">Requirements</span></span>



| <span data-ttu-id="f31a1-150">Требование</span><span class="sxs-lookup"><span data-stu-id="f31a1-150">Requirement</span></span> | <span data-ttu-id="f31a1-151">Значение</span><span class="sxs-lookup"><span data-stu-id="f31a1-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f31a1-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f31a1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f31a1-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f31a1-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f31a1-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f31a1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f31a1-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f31a1-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f31a1-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f31a1-156">Namespace</span></span><br/>                | <span data-ttu-id="f31a1-157">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f31a1-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f31a1-158">MOF</span><span class="sxs-lookup"><span data-stu-id="f31a1-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f31a1-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f31a1-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f31a1-160">DLL</span><span class="sxs-lookup"><span data-stu-id="f31a1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f31a1-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f31a1-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31a1-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f31a1-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="f31a1-163">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f31a1-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f31a1-164">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="f31a1-164">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

