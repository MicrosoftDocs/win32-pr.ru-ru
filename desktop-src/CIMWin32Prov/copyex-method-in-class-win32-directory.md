---
description: Копирует файл или каталог записи логического каталога, указанный в пути к объекту, в расположение, указанное параметром FileName. Этот метод является расширенной версией метода Copy.
ms.assetid: c15bd1ae-a60d-4875-a76e-99486820c42c
ms.tgt_platform: multiple
title: Метод Копекс класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55f2fdb0aa4e8306e8ec0aa4f5f265c0a8ee6689
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896525"
---
# <a name="copyex-method-of-the-win32_directory-class"></a><span data-ttu-id="e8538-104">Метод Копекс \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="e8538-104">CopyEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="e8538-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) копекс копирует логический файл или каталог записи каталога, указанный в пути к объекту, в расположение, указанное параметром *filename* .</span><span class="sxs-lookup"><span data-stu-id="e8538-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="e8538-106">Этот метод является расширенной версией метода [**Copy**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="e8538-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="e8538-107">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="e8538-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="e8538-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e8538-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e8538-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e8538-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8538-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8538-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e8538-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8538-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8538-112">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8538-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8538-113">Полное имя копии файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="e8538-113">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="e8538-114">Пример: c: \\ temp \\ невдиректори.</span><span class="sxs-lookup"><span data-stu-id="e8538-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-115">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8538-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8538-116">Имя файла или каталога, в котором произошел сбой метода **копекс** .</span><span class="sxs-lookup"><span data-stu-id="e8538-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="e8538-117">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="e8538-117">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-118">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e8538-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e8538-119">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **копекс**.</span><span class="sxs-lookup"><span data-stu-id="e8538-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="e8538-120">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="e8538-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="e8538-121">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="e8538-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="e8538-122">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="e8538-122">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-123">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e8538-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e8538-124">Если **значение равно true**, файлы и каталоги будут копироваться рекурсивно в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e8538-124">If **true**, files and directories will be copied recursively within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="e8538-125">Для экземпляров файлов *рекурсивный* входной параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e8538-125">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8538-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8538-126">Return value</span></span>

<span data-ttu-id="e8538-127">Возвращает значение 0 (нуль), если файл был успешно скопирован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="e8538-127">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e8538-128">**0**</span><span class="sxs-lookup"><span data-stu-id="e8538-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-129">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e8538-129">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-130">**2**</span><span class="sxs-lookup"><span data-stu-id="e8538-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-131">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="e8538-131">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-132">**8**</span><span class="sxs-lookup"><span data-stu-id="e8538-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-133">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e8538-133">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-134">**9**</span><span class="sxs-lookup"><span data-stu-id="e8538-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-135">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="e8538-135">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-136">**10**</span><span class="sxs-lookup"><span data-stu-id="e8538-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-137">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="e8538-137">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-138">**11**</span><span class="sxs-lookup"><span data-stu-id="e8538-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-139">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="e8538-139">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-140">**12**</span><span class="sxs-lookup"><span data-stu-id="e8538-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-141">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="e8538-141">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-142">**13**</span><span class="sxs-lookup"><span data-stu-id="e8538-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-143">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="e8538-143">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-144">**14**</span><span class="sxs-lookup"><span data-stu-id="e8538-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-145">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="e8538-145">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-146">**15**</span><span class="sxs-lookup"><span data-stu-id="e8538-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-147">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e8538-147">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-148">**16**</span><span class="sxs-lookup"><span data-stu-id="e8538-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-149">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="e8538-149">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-150">**17**</span><span class="sxs-lookup"><span data-stu-id="e8538-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-151">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="e8538-151">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="e8538-152">**открыт**</span><span class="sxs-lookup"><span data-stu-id="e8538-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e8538-153">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="e8538-153">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8538-154">Требования</span><span class="sxs-lookup"><span data-stu-id="e8538-154">Requirements</span></span>



| <span data-ttu-id="e8538-155">Требование</span><span class="sxs-lookup"><span data-stu-id="e8538-155">Requirement</span></span> | <span data-ttu-id="e8538-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e8538-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8538-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8538-157">Minimum supported client</span></span><br/> | <span data-ttu-id="e8538-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8538-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8538-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8538-159">Minimum supported server</span></span><br/> | <span data-ttu-id="e8538-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8538-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8538-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8538-161">Namespace</span></span><br/>                | <span data-ttu-id="e8538-162">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e8538-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e8538-163">MOF</span><span class="sxs-lookup"><span data-stu-id="e8538-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8538-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8538-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8538-165">DLL</span><span class="sxs-lookup"><span data-stu-id="e8538-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8538-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8538-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8538-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8538-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="e8538-168">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8538-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e8538-169">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="e8538-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

