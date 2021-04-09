---
description: Сжимает логический файл записи каталога (или каталог), указанный в пути объекта.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Метод сжатия класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141063"
---
# <a name="compress-method-of-the-win32_directory-class"></a><span data-ttu-id="fdeef-103">Метод сжатия \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="fdeef-103">Compress method of the Win32\_Directory class</span></span>

<span data-ttu-id="fdeef-104">Метод **сжатия** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) сжимает логический файл записи каталога (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="fdeef-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="fdeef-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="fdeef-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fdeef-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fdeef-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fdeef-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdeef-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="fdeef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdeef-108">Parameters</span></span>

<span data-ttu-id="fdeef-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fdeef-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdeef-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdeef-110">Return value</span></span>

<span data-ttu-id="fdeef-111">Возвращает значение 0 (ноль), если файл был успешно сжат, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="fdeef-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="fdeef-112">**0**</span><span class="sxs-lookup"><span data-stu-id="fdeef-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-113">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="fdeef-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-114">**2**</span><span class="sxs-lookup"><span data-stu-id="fdeef-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-115">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="fdeef-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-116">**8**</span><span class="sxs-lookup"><span data-stu-id="fdeef-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-117">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fdeef-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-118">**9**</span><span class="sxs-lookup"><span data-stu-id="fdeef-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-119">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="fdeef-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-120">**10**</span><span class="sxs-lookup"><span data-stu-id="fdeef-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-121">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="fdeef-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-122">**11**</span><span class="sxs-lookup"><span data-stu-id="fdeef-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-123">Файловая система не является файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="fdeef-123">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-124">**12**</span><span class="sxs-lookup"><span data-stu-id="fdeef-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-125">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="fdeef-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-126">**13**</span><span class="sxs-lookup"><span data-stu-id="fdeef-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-127">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="fdeef-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-128">**14**</span><span class="sxs-lookup"><span data-stu-id="fdeef-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-129">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="fdeef-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-130">**15**</span><span class="sxs-lookup"><span data-stu-id="fdeef-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-131">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="fdeef-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-132">**16**</span><span class="sxs-lookup"><span data-stu-id="fdeef-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-133">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="fdeef-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-134">**17**</span><span class="sxs-lookup"><span data-stu-id="fdeef-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-135">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="fdeef-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="fdeef-136">**открыт**</span><span class="sxs-lookup"><span data-stu-id="fdeef-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fdeef-137">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="fdeef-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdeef-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fdeef-138">Remarks</span></span>

<span data-ttu-id="fdeef-139">Сжатие позволяет освободить дополнительное пространство для хранения на диске без приобретения нового оборудования и без удаления файлов или папок.</span><span class="sxs-lookup"><span data-stu-id="fdeef-139">Compression provides a way to free additional storage space on a disk drive without purchasing new hardware and without removing files or folders.</span></span> <span data-ttu-id="fdeef-140">В зависимости от размера жесткого диска и типа файлов, хранящихся на этом диске, вы можете восстановить сотни мегабайт дискового пространства и, таким же, отказаться от приобретения нового жесткого диска и перевести компьютер в режим «вне сети», пока не будет установлен новый диск.</span><span class="sxs-lookup"><span data-stu-id="fdeef-140">Depending on the size of your hard disk and the type of files stored on that disk, you might be able to recover hundreds of megabytes of disk space and thus preclude the need to purchase a new hard drive and to take the computer offline until the new drive is installed.</span></span>

<span data-ttu-id="fdeef-141">Метод сжатия сжимает все файлы и вложенные папки в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="fdeef-141">The Compress method compresses all the files and subfolders within a specified folder.</span></span> <span data-ttu-id="fdeef-142">Кроме того, класс также включает метод uncompressия, который удаляет сжатие из всех файлов и вложенных папок в папке.</span><span class="sxs-lookup"><span data-stu-id="fdeef-142">In addition, the class also includes an Uncompress method that removes compression from all the files and subfolders in a folder.</span></span> <span data-ttu-id="fdeef-143">Аналогичные методы также предоставляются с помощью класса CIM \_ File.</span><span class="sxs-lookup"><span data-stu-id="fdeef-143">Similar methods are also provided with the CIM\_Datafile class.</span></span> <span data-ttu-id="fdeef-144">Это позволяет выборочно сжимать или распаковывать определенные файлы в папке.</span><span class="sxs-lookup"><span data-stu-id="fdeef-144">This allows you to selectively compress or uncompress specific files within a folder.</span></span>

<span data-ttu-id="fdeef-145">Поскольку сжатие является незначительным снижением производительности, не рекомендуется использовать для файлов и папок, к которым осуществляется обращение по отдельности. Например, вы, вероятно, не хотите сжимать файлы базы данных, файлы журналов или папки профилей пользователей.</span><span class="sxs-lookup"><span data-stu-id="fdeef-145">Because compression imparts a slight performance penalty, it is not recommended for files or folders that are accessed on a routine basis; for example, you probably do not want to compress database files, log files, or user profile folders.</span></span> <span data-ttu-id="fdeef-146">Лучшим кандидатом на сжатие являются файлы и папки, к которым не обращаются очень часто.</span><span class="sxs-lookup"><span data-stu-id="fdeef-146">Better candidates for compression are files and folders that are not accessed very often.</span></span> <span data-ttu-id="fdeef-147">Например, можно написать сценарий, возвращающий коллекцию папок на диске, к которым не осуществлялся доступ в течение месяца или более, а затем сжимать каждую из этих папок.</span><span class="sxs-lookup"><span data-stu-id="fdeef-147">For example, you might write a script to return a collection of folders on a drive that have not been accessed for a month or more and then compress each of those folders.</span></span>

<span data-ttu-id="fdeef-148">Объем дискового пространства, освобожденного путем сжатия папок, зависит от типа файлов, хранящихся в этой папке.</span><span class="sxs-lookup"><span data-stu-id="fdeef-148">The amount of disk space freed by compressing folders varies depending on the type of files stored in that folder.</span></span> <span data-ttu-id="fdeef-149">Например, JPG файлы уже сжаты, а дальнейшее сжатие практически не влияет на размер файла.</span><span class="sxs-lookup"><span data-stu-id="fdeef-149">For example, .jpg files are already compressed, and further compression has little effect on the size of the file.</span></span> <span data-ttu-id="fdeef-150">Однако при использовании других типов файлов экономия может быть значительной.</span><span class="sxs-lookup"><span data-stu-id="fdeef-150">With other file types, however, the savings can be considerable.</span></span> <span data-ttu-id="fdeef-151">Например, на тестовом компьютере под управлением Windows 2000 была создана новая папка, а в 33 документов Microsoft Word — 15 мегабайт (МБ) дискового пространства, которые были скопированы в эту папку.</span><span class="sxs-lookup"><span data-stu-id="fdeef-151">For example, a new folder was created on a Windows 2000-based test computer, and 33 Microsoft Word documents, taking up a total of 15 megabytes (MB) of disk space, were copied into that folder.</span></span> <span data-ttu-id="fdeef-152">Когда документы были сжаты, папка занимает всего 7 МБ дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="fdeef-152">When the documents were compressed, the folder took up only 7 MB of disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="fdeef-153">Примеры</span><span class="sxs-lookup"><span data-stu-id="fdeef-153">Examples</span></span>

<span data-ttu-id="fdeef-154">Следующий пример сценария VBScript сжимает папку C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="fdeef-154">The following VBScript sample compresses the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="fdeef-155">Требования</span><span class="sxs-lookup"><span data-stu-id="fdeef-155">Requirements</span></span>



| <span data-ttu-id="fdeef-156">Требование</span><span class="sxs-lookup"><span data-stu-id="fdeef-156">Requirement</span></span> | <span data-ttu-id="fdeef-157">Значение</span><span class="sxs-lookup"><span data-stu-id="fdeef-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdeef-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdeef-158">Minimum supported client</span></span><br/> | <span data-ttu-id="fdeef-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdeef-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fdeef-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdeef-160">Minimum supported server</span></span><br/> | <span data-ttu-id="fdeef-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdeef-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fdeef-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fdeef-162">Namespace</span></span><br/>                | <span data-ttu-id="fdeef-163">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fdeef-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fdeef-164">MOF</span><span class="sxs-lookup"><span data-stu-id="fdeef-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdeef-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdeef-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdeef-166">DLL</span><span class="sxs-lookup"><span data-stu-id="fdeef-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdeef-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdeef-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdeef-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdeef-168">See also</span></span>

<dl> <dt>

<span data-ttu-id="fdeef-169">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fdeef-169">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fdeef-170">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="fdeef-170">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="fdeef-171">**Распаковать**</span><span class="sxs-lookup"><span data-stu-id="fdeef-171">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

