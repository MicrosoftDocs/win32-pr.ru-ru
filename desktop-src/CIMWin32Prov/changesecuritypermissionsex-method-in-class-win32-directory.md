---
description: Изменяет разрешения безопасности для файла записи каталога, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262608"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a><span data-ttu-id="19b53-103">Метод Чанжесекуритипермиссионсекс \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="19b53-103">ChangeSecurityPermissionsEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="19b53-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжесекуритипермиссионсекс изменяет разрешения безопасности для файла записи каталога, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="19b53-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="19b53-105">Если логический файл является каталогом, этот метод является рекурсивным и изменяет разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="19b53-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="19b53-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="19b53-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="19b53-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="19b53-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="19b53-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19b53-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="19b53-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="19b53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19b53-110">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19b53-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19b53-111">Выражение, которое разрешается в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="19b53-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="19b53-112">Этот параметр содержит новые разрешения безопасности для экземпляра [**\_ файла подкачки Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="19b53-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="19b53-113">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19b53-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19b53-114">Права безопасности, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="19b53-114">Security privilege to be modified.</span></span> <span data-ttu-id="19b53-115">Например, чтобы изменить уровень безопасности владельца и избирательного списка управления доступом (DACL), используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="19b53-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="19b53-116">-или-</span><span class="sxs-lookup"><span data-stu-id="19b53-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="19b53-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="19b53-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="19b53-118">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="19b53-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="19b53-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="19b53-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="19b53-120">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="19b53-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="19b53-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="19b53-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="19b53-122">Изменение списка DACL логического файла.</span><span class="sxs-lookup"><span data-stu-id="19b53-122">Change the DACL list of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="19b53-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="19b53-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="19b53-124">Измените системный список управления доступом (SACL) логического файла.</span><span class="sxs-lookup"><span data-stu-id="19b53-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="19b53-125">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="19b53-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19b53-126">Имя файла или каталога, в котором произошел сбой метода **чанжесекуритипермиссионсекс** .</span><span class="sxs-lookup"><span data-stu-id="19b53-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="19b53-127">Если метод выполнен, этот параметр имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="19b53-127">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-128">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="19b53-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19b53-129">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **чанжесекуритипермиссионсекс**.</span><span class="sxs-lookup"><span data-stu-id="19b53-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="19b53-130">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="19b53-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="19b53-131">Если этот параметр имеет значение null, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="19b53-131">If this parameter is null, the operation is performed on the file or directory that is specified in the **ExecMethod** call.</span></span> <span data-ttu-id="19b53-132">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="19b53-132">This parameter is optional.</span></span>

<span data-ttu-id="19b53-133">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="19b53-133">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-134">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="19b53-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="19b53-135">Если **значение — true**, изменение владельца применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="19b53-135">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="19b53-136">Для экземпляров файлов *рекурсивный* входной параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="19b53-136">For file instances, the *Recursive* input parameter is ignored.</span></span> <span data-ttu-id="19b53-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="19b53-137">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19b53-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19b53-138">Return value</span></span>

<span data-ttu-id="19b53-139">Возвращает значение 0 (ноль), если разрешения изменяются, и другое число, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="19b53-139">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="19b53-140">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="19b53-140">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-141">0</span><span class="sxs-lookup"><span data-stu-id="19b53-141">0</span></span>

<span data-ttu-id="19b53-142">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="19b53-142">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-143">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="19b53-143">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-144">2</span><span class="sxs-lookup"><span data-stu-id="19b53-144">2</span></span>

<span data-ttu-id="19b53-145">Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="19b53-145">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-146">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="19b53-146">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-147">8</span><span class="sxs-lookup"><span data-stu-id="19b53-147">8</span></span>

<span data-ttu-id="19b53-148">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="19b53-148">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-149">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="19b53-149">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-150">9</span><span class="sxs-lookup"><span data-stu-id="19b53-150">9</span></span>

<span data-ttu-id="19b53-151">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="19b53-151">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-152">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="19b53-152">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-153">10</span><span class="sxs-lookup"><span data-stu-id="19b53-153">10</span></span>

<span data-ttu-id="19b53-154">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="19b53-154">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-155">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="19b53-155">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-156">11</span><span class="sxs-lookup"><span data-stu-id="19b53-156">11</span></span>

<span data-ttu-id="19b53-157">Файловая система не является файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="19b53-157">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-158">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="19b53-158">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-159">12</span><span class="sxs-lookup"><span data-stu-id="19b53-159">12</span></span>

<span data-ttu-id="19b53-160">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="19b53-160">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-161">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="19b53-161">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-162">13</span><span class="sxs-lookup"><span data-stu-id="19b53-162">13</span></span>

<span data-ttu-id="19b53-163">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="19b53-163">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-164">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="19b53-164">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-165">14</span><span class="sxs-lookup"><span data-stu-id="19b53-165">14</span></span>

<span data-ttu-id="19b53-166">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="19b53-166">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-167">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="19b53-167">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-168">15</span><span class="sxs-lookup"><span data-stu-id="19b53-168">15</span></span>

<span data-ttu-id="19b53-169">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="19b53-169">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-170">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="19b53-170">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-171">16</span><span class="sxs-lookup"><span data-stu-id="19b53-171">16</span></span>

<span data-ttu-id="19b53-172">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="19b53-172">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-173">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="19b53-173">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-174">17</span><span class="sxs-lookup"><span data-stu-id="19b53-174">17</span></span>

<span data-ttu-id="19b53-175">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="19b53-175">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="19b53-176">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="19b53-176">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="19b53-177">21</span><span class="sxs-lookup"><span data-stu-id="19b53-177">21</span></span>

<span data-ttu-id="19b53-178">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="19b53-178">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19b53-179">Требования</span><span class="sxs-lookup"><span data-stu-id="19b53-179">Requirements</span></span>



| <span data-ttu-id="19b53-180">Требование</span><span class="sxs-lookup"><span data-stu-id="19b53-180">Requirement</span></span> | <span data-ttu-id="19b53-181">Значение</span><span class="sxs-lookup"><span data-stu-id="19b53-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19b53-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19b53-182">Minimum supported client</span></span><br/> | <span data-ttu-id="19b53-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19b53-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19b53-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19b53-184">Minimum supported server</span></span><br/> | <span data-ttu-id="19b53-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19b53-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19b53-186">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="19b53-186">Namespace</span></span><br/>                | <span data-ttu-id="19b53-187">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="19b53-187">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19b53-188">MOF</span><span class="sxs-lookup"><span data-stu-id="19b53-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19b53-189"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19b53-189"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19b53-190">DLL</span><span class="sxs-lookup"><span data-stu-id="19b53-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b53-191"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b53-191"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19b53-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19b53-192">See also</span></span>

<dl> <dt>

<span data-ttu-id="19b53-193">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19b53-193">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="19b53-194">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="19b53-194">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

