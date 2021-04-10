---
description: Распаковывает логический файл записи каталога (или каталог), указанный в пути к объекту.
ms.assetid: dd39aae3-7c88-48fc-93ed-5225d2f1491c
ms.tgt_platform: multiple
title: Метод uncompressия класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c46a6bb90d43c1b793350bb96822a1aaed8dd9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142544"
---
# <a name="uncompress-method-of-the-win32_directory-class"></a><span data-ttu-id="5cbc9-103">Метод uncompressия \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="5cbc9-103">Uncompress method of the Win32\_Directory class</span></span>

<span data-ttu-id="5cbc9-104">Метод **uncompressия** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) распаковывает логический файл записи каталога (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="5cbc9-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="5cbc9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5cbc9-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5cbc9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5cbc9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cbc9-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="5cbc9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cbc9-108">Parameters</span></span>

<span data-ttu-id="5cbc9-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5cbc9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5cbc9-110">Return value</span></span>

<span data-ttu-id="5cbc9-111">Возвращает целочисленное значение 0 (ноль), если файл был успешно распакован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5cbc9-112">**0**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-113">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-114">**2**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-115">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-116">**8**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-117">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-118">**9**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-119">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-120">**10**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-121">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-122">**11**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-123">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-124">**12**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-125">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-126">**13**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-127">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-128">**14**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-129">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-130">**15**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-131">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-132">**16**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-133">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-134">**17**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-135">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5cbc9-136">**открыт**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5cbc9-137">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5cbc9-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="5cbc9-138">Examples</span></span>

<span data-ttu-id="5cbc9-139">Следующий пример сценария VBScript распаковывает папку c: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="5cbc9-139">The following VBScript sample uncompresses the folder c:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Uncompress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="5cbc9-140">Требования</span><span class="sxs-lookup"><span data-stu-id="5cbc9-140">Requirements</span></span>



| <span data-ttu-id="5cbc9-141">Требование</span><span class="sxs-lookup"><span data-stu-id="5cbc9-141">Requirement</span></span> | <span data-ttu-id="5cbc9-142">Значение</span><span class="sxs-lookup"><span data-stu-id="5cbc9-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cbc9-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5cbc9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5cbc9-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cbc9-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5cbc9-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5cbc9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5cbc9-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cbc9-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5cbc9-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5cbc9-147">Namespace</span></span><br/>                | <span data-ttu-id="5cbc9-148">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5cbc9-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5cbc9-149">MOF</span><span class="sxs-lookup"><span data-stu-id="5cbc9-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cbc9-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5cbc9-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cbc9-151">DLL</span><span class="sxs-lookup"><span data-stu-id="5cbc9-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cbc9-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cbc9-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cbc9-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cbc9-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="5cbc9-154">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5cbc9-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5cbc9-155">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-155">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="5cbc9-156">**Повторно**</span><span class="sxs-lookup"><span data-stu-id="5cbc9-156">**Compress**</span></span>](compress-method-in-class-win32-directory.md)
</dt> </dl>

 

