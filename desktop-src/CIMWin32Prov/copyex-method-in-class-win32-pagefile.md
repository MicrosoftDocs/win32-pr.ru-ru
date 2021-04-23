---
description: Копирует логический файл подкачки или каталог, указанный в пути к объекту, в расположение, указанное параметром FileName. Этот метод является расширенной версией метода Copy.
ms.assetid: a8376dc8-eb73-4097-b84c-839432ac3a25
ms.tgt_platform: multiple
title: Метод Копекс класса Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 810f1d3bcf878d33756930f6bd3b6799c3513dc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896522"
---
# <a name="copyex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="e95c4-104">Метод Копекс \_ класса файла подкачки Win32</span><span class="sxs-lookup"><span data-stu-id="e95c4-104">CopyEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="e95c4-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) копекс копирует логический файл подкачки или каталог, указанный в пути к объекту, в расположение, указанное параметром *filename* .</span><span class="sxs-lookup"><span data-stu-id="e95c4-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical paging file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="e95c4-106">Этот метод является расширенной версией метода [**Copy**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="e95c4-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="e95c4-107">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="e95c4-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="e95c4-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e95c4-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e95c4-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e95c4-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e95c4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e95c4-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e95c4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e95c4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e95c4-112">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e95c4-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-113">Полное имя копии файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="e95c4-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="e95c4-114">Пример: c: \\ temp \\ невдиректори</span><span class="sxs-lookup"><span data-stu-id="e95c4-114">Example: c:\\temp\\newdirectory</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-115">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e95c4-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-116">Имя файла или каталога, в котором произошел сбой метода **копекс** .</span><span class="sxs-lookup"><span data-stu-id="e95c4-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="e95c4-117">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="e95c4-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-118">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e95c4-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-119">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **копекс**.</span><span class="sxs-lookup"><span data-stu-id="e95c4-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="e95c4-120">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="e95c4-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="e95c4-121">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="e95c4-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-122">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e95c4-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-123">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e95c4-123">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="e95c4-124">Для экземпляров файлов *рекурсивный* параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e95c4-124">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e95c4-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e95c4-125">Return value</span></span>

<span data-ttu-id="e95c4-126">Возвращает значение 0 (нуль), если файл был успешно скопирован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="e95c4-126">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e95c4-127">**0**</span><span class="sxs-lookup"><span data-stu-id="e95c4-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-128">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e95c4-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-129">**2**</span><span class="sxs-lookup"><span data-stu-id="e95c4-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-130">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="e95c4-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-131">**8**</span><span class="sxs-lookup"><span data-stu-id="e95c4-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-132">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e95c4-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-133">**9**</span><span class="sxs-lookup"><span data-stu-id="e95c4-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-134">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="e95c4-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-135">**10**</span><span class="sxs-lookup"><span data-stu-id="e95c4-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-136">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="e95c4-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-137">**11**</span><span class="sxs-lookup"><span data-stu-id="e95c4-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-138">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="e95c4-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-139">**12**</span><span class="sxs-lookup"><span data-stu-id="e95c4-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-140">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="e95c4-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-141">**13**</span><span class="sxs-lookup"><span data-stu-id="e95c4-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-142">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="e95c4-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-143">**14**</span><span class="sxs-lookup"><span data-stu-id="e95c4-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-144">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="e95c4-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-145">**15**</span><span class="sxs-lookup"><span data-stu-id="e95c4-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-146">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e95c4-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-147">**16**</span><span class="sxs-lookup"><span data-stu-id="e95c4-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-148">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="e95c4-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-149">**17**</span><span class="sxs-lookup"><span data-stu-id="e95c4-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-150">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="e95c4-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="e95c4-151">**открыт**</span><span class="sxs-lookup"><span data-stu-id="e95c4-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e95c4-152">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="e95c4-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e95c4-153">Требования</span><span class="sxs-lookup"><span data-stu-id="e95c4-153">Requirements</span></span>



| <span data-ttu-id="e95c4-154">Требование</span><span class="sxs-lookup"><span data-stu-id="e95c4-154">Requirement</span></span> | <span data-ttu-id="e95c4-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e95c4-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e95c4-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e95c4-156">Minimum supported client</span></span><br/> | <span data-ttu-id="e95c4-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e95c4-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e95c4-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e95c4-158">Minimum supported server</span></span><br/> | <span data-ttu-id="e95c4-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e95c4-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e95c4-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e95c4-160">Namespace</span></span><br/>                | <span data-ttu-id="e95c4-161">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e95c4-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e95c4-162">MOF</span><span class="sxs-lookup"><span data-stu-id="e95c4-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e95c4-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e95c4-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e95c4-164">DLL</span><span class="sxs-lookup"><span data-stu-id="e95c4-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e95c4-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e95c4-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e95c4-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e95c4-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="e95c4-167">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e95c4-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e95c4-168">**\_Файл подкачки Win32**</span><span class="sxs-lookup"><span data-stu-id="e95c4-168">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

