---
description: Распаковывает логический файл записи каталога (или каталог), указанный в пути к объекту. Этот метод является расширенной версией метода uncompressия.
ms.assetid: cd18d8b7-ab63-475c-a3a6-79611c9e032d
ms.tgt_platform: multiple
title: Метод Ункомпрессекс класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd02d0757745199249d64fa08d73f8b5ec65a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142529"
---
# <a name="uncompressex-method-of-the-win32_directory-class"></a><span data-ttu-id="90b1f-104">Метод Ункомпрессекс \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="90b1f-104">UncompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="90b1f-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ункомпрессекс распаковывает логический файл записи каталога (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="90b1f-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="90b1f-106">Этот метод является расширенной версией метода [**uncompressия**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="90b1f-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="90b1f-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="90b1f-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="90b1f-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="90b1f-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="90b1f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90b1f-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="90b1f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="90b1f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90b1f-111">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="90b1f-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-112">Имя файла или каталога, в котором произошел сбой метода **ункомпрессекс** .</span><span class="sxs-lookup"><span data-stu-id="90b1f-112">Name of the file/directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="90b1f-113">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="90b1f-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-114">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="90b1f-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-115">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **ункомпрессекс**.</span><span class="sxs-lookup"><span data-stu-id="90b1f-115">Names the child file/directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="90b1f-116">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="90b1f-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="90b1f-117">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="90b1f-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

<span data-ttu-id="90b1f-118">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="90b1f-118">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-119">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="90b1f-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-120">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="90b1f-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="90b1f-121">Примечание. для экземпляров файлов входной параметр *recursive* не учитывается.</span><span class="sxs-lookup"><span data-stu-id="90b1f-121">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90b1f-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90b1f-122">Return value</span></span>

<span data-ttu-id="90b1f-123">Возвращает значение 0 (нуль), если файл был успешно распакован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="90b1f-123">Returns an value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="90b1f-124">**0**</span><span class="sxs-lookup"><span data-stu-id="90b1f-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-125">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="90b1f-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-126">**2**</span><span class="sxs-lookup"><span data-stu-id="90b1f-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-127">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="90b1f-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-128">**8**</span><span class="sxs-lookup"><span data-stu-id="90b1f-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-129">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="90b1f-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-130">**9**</span><span class="sxs-lookup"><span data-stu-id="90b1f-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-131">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="90b1f-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-132">**10**</span><span class="sxs-lookup"><span data-stu-id="90b1f-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-133">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="90b1f-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-134">**11**</span><span class="sxs-lookup"><span data-stu-id="90b1f-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-135">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="90b1f-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-136">**12**</span><span class="sxs-lookup"><span data-stu-id="90b1f-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-137">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="90b1f-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-138">**13**</span><span class="sxs-lookup"><span data-stu-id="90b1f-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-139">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="90b1f-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-140">**14**</span><span class="sxs-lookup"><span data-stu-id="90b1f-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-141">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="90b1f-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-142">**15**</span><span class="sxs-lookup"><span data-stu-id="90b1f-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-143">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="90b1f-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-144">**16**</span><span class="sxs-lookup"><span data-stu-id="90b1f-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-145">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="90b1f-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-146">**17**</span><span class="sxs-lookup"><span data-stu-id="90b1f-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-147">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="90b1f-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="90b1f-148">**открыт**</span><span class="sxs-lookup"><span data-stu-id="90b1f-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="90b1f-149">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="90b1f-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90b1f-150">Требования</span><span class="sxs-lookup"><span data-stu-id="90b1f-150">Requirements</span></span>



| <span data-ttu-id="90b1f-151">Требование</span><span class="sxs-lookup"><span data-stu-id="90b1f-151">Requirement</span></span> | <span data-ttu-id="90b1f-152">Значение</span><span class="sxs-lookup"><span data-stu-id="90b1f-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90b1f-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90b1f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="90b1f-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90b1f-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90b1f-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90b1f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="90b1f-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90b1f-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90b1f-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="90b1f-157">Namespace</span></span><br/>                | <span data-ttu-id="90b1f-158">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="90b1f-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90b1f-159">MOF</span><span class="sxs-lookup"><span data-stu-id="90b1f-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90b1f-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90b1f-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90b1f-161">DLL</span><span class="sxs-lookup"><span data-stu-id="90b1f-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90b1f-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90b1f-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90b1f-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90b1f-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="90b1f-164">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90b1f-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="90b1f-165">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="90b1f-165">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

