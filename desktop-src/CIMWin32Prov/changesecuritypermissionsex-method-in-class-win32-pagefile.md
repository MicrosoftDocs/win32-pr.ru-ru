---
description: Изменяет разрешения безопасности для логического файла подкачки, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: a852a7e6-f26a-4bd9-bb15-e4cdd577697c
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a01a214e626f9c64ccf460eb3f8c031d1b45ff85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895805"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="763be-103">Метод Чанжесекуритипермиссионсекс \_ класса файла подкачки Win32</span><span class="sxs-lookup"><span data-stu-id="763be-103">ChangeSecurityPermissionsEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="763be-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжесекуритипермиссионсекс изменяет разрешения безопасности для логического файла подкачки, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="763be-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file that is specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="763be-105">Если логический файл является каталогом, этот метод является рекурсивным и изменяет разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="763be-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="763be-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="763be-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="763be-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="763be-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="763be-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="763be-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="763be-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="763be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="763be-110">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="763be-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="763be-111">Выражение, которое разрешается в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="763be-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="763be-112">Этот параметр содержит новые разрешения безопасности для экземпляра [**\_ файла подкачки Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="763be-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="763be-113">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="763be-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="763be-114">Права безопасности, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="763be-114">Security privilege to be modified.</span></span> <span data-ttu-id="763be-115">Например, чтобы изменить уровень безопасности владельца и избирательного списка управления доступом (DACL), используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="763be-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="763be-116">-или-</span><span class="sxs-lookup"><span data-stu-id="763be-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="763be-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="763be-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="763be-118">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="763be-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="763be-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="763be-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="763be-120">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="763be-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="763be-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="763be-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="763be-122">Измените список DACL для логического файла.</span><span class="sxs-lookup"><span data-stu-id="763be-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="763be-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="763be-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="763be-124">Измените список управления доступом к системе (SACL) логического файла.</span><span class="sxs-lookup"><span data-stu-id="763be-124">Change the system access control (SACL) list of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="763be-125">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="763be-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="763be-126">Имя файла или каталога, в котором произошел сбой метода **чанжесекуритипермиссионсекс** .</span><span class="sxs-lookup"><span data-stu-id="763be-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="763be-127">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="763be-127">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="763be-128">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="763be-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="763be-129">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **чанжесекуритипермиссионсекс**.</span><span class="sxs-lookup"><span data-stu-id="763be-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="763be-130">Как правило, параметр *StartFileName* является параметром *StartFileName* , указывающим файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="763be-130">Typically, the *StartFileName* parameter is the *StartFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="763be-131">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="763be-131">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="763be-132">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="763be-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="763be-133">Если **значение — true**, изменение владельца применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="763be-133">If **true**, the change of ownership is applied recursively to files and directories in the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="763be-134">Для экземпляров файлов *рекурсивный* параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="763be-134">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="763be-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="763be-135">Return value</span></span>

<span data-ttu-id="763be-136">Возвращает значение 0 (ноль), если разрешения изменяются, и другое число, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="763be-136">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="763be-137">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="763be-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="763be-138">0</span><span class="sxs-lookup"><span data-stu-id="763be-138">0</span></span>

<span data-ttu-id="763be-139">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="763be-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="763be-140">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="763be-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="763be-141">2</span><span class="sxs-lookup"><span data-stu-id="763be-141">2</span></span>

<span data-ttu-id="763be-142">Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="763be-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="763be-143">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="763be-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="763be-144">8</span><span class="sxs-lookup"><span data-stu-id="763be-144">8</span></span>

<span data-ttu-id="763be-145">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="763be-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="763be-146">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="763be-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="763be-147">9</span><span class="sxs-lookup"><span data-stu-id="763be-147">9</span></span>

<span data-ttu-id="763be-148">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="763be-148">The name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="763be-149">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="763be-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="763be-150">10</span><span class="sxs-lookup"><span data-stu-id="763be-150">10</span></span>

<span data-ttu-id="763be-151">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="763be-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="763be-152">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="763be-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="763be-153">11</span><span class="sxs-lookup"><span data-stu-id="763be-153">11</span></span>

<span data-ttu-id="763be-154">Файловая система не является файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="763be-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="763be-155">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="763be-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="763be-156">12</span><span class="sxs-lookup"><span data-stu-id="763be-156">12</span></span>

<span data-ttu-id="763be-157">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="763be-157">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="763be-158">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="763be-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="763be-159">13</span><span class="sxs-lookup"><span data-stu-id="763be-159">13</span></span>

<span data-ttu-id="763be-160">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="763be-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="763be-161">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="763be-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="763be-162">14</span><span class="sxs-lookup"><span data-stu-id="763be-162">14</span></span>

<span data-ttu-id="763be-163">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="763be-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="763be-164">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="763be-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="763be-165">15</span><span class="sxs-lookup"><span data-stu-id="763be-165">15</span></span>

<span data-ttu-id="763be-166">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="763be-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="763be-167">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="763be-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="763be-168">16</span><span class="sxs-lookup"><span data-stu-id="763be-168">16</span></span>

<span data-ttu-id="763be-169">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="763be-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="763be-170">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="763be-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="763be-171">17</span><span class="sxs-lookup"><span data-stu-id="763be-171">17</span></span>

<span data-ttu-id="763be-172">Отсутствует привилегия, необходимая для операции.</span><span class="sxs-lookup"><span data-stu-id="763be-172">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="763be-173">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="763be-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="763be-174">21</span><span class="sxs-lookup"><span data-stu-id="763be-174">21</span></span>

<span data-ttu-id="763be-175">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="763be-175">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="763be-176">Требования</span><span class="sxs-lookup"><span data-stu-id="763be-176">Requirements</span></span>



| <span data-ttu-id="763be-177">Требование</span><span class="sxs-lookup"><span data-stu-id="763be-177">Requirement</span></span> | <span data-ttu-id="763be-178">Значение</span><span class="sxs-lookup"><span data-stu-id="763be-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="763be-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="763be-179">Minimum supported client</span></span><br/> | <span data-ttu-id="763be-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="763be-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="763be-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="763be-181">Minimum supported server</span></span><br/> | <span data-ttu-id="763be-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="763be-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="763be-183">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="763be-183">Namespace</span></span><br/>                | <span data-ttu-id="763be-184">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="763be-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="763be-185">MOF</span><span class="sxs-lookup"><span data-stu-id="763be-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="763be-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="763be-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="763be-187">DLL</span><span class="sxs-lookup"><span data-stu-id="763be-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="763be-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="763be-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="763be-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="763be-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="763be-190">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="763be-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="763be-191">**\_Файл подкачки Win32**</span><span class="sxs-lookup"><span data-stu-id="763be-191">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

