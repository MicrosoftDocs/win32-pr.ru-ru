---
description: Изменяет разрешения безопасности для логического файла подкачки, указанного в пути к объекту.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионс класса Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990627"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a><span data-ttu-id="d580d-103">Метод Чанжесекуритипермиссионс \_ класса файла подкачки Win32</span><span class="sxs-lookup"><span data-stu-id="d580d-103">ChangeSecurityPermissions method of the Win32\_PageFile class</span></span>

<span data-ttu-id="d580d-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжесекуритипермиссионс изменяет разрешения безопасности для логического файла подкачки, указанного в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d580d-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file specified in the object path.</span></span> <span data-ttu-id="d580d-105">Если логический файл является каталогом, то **чанжесекуритипермиссионс** является рекурсивным и изменяет разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="d580d-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="d580d-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d580d-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d580d-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d580d-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d580d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d580d-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="d580d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d580d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d580d-110">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d580d-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d580d-111">Выражение, которое разрешается в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="d580d-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="d580d-112">Этот дескриптор содержит новые разрешения безопасности для экземпляра [**\_ файла подкачки Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="d580d-112">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="d580d-113">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d580d-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d580d-114">Права безопасности, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="d580d-114">Security privilege to be modified.</span></span> <span data-ttu-id="d580d-115">Например, чтобы изменить уровень безопасности владельца и избирательного списка управления доступом (DACL), используйте:</span><span class="sxs-lookup"><span data-stu-id="d580d-115">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="d580d-116">-или-</span><span class="sxs-lookup"><span data-stu-id="d580d-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="d580d-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="d580d-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d580d-118">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="d580d-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="d580d-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="d580d-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d580d-120">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="d580d-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="d580d-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="d580d-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d580d-122">Измените список DACL для логического файла.</span><span class="sxs-lookup"><span data-stu-id="d580d-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="d580d-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="d580d-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d580d-124">Измените системный список управления доступом (SACL) логического файла.</span><span class="sxs-lookup"><span data-stu-id="d580d-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d580d-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d580d-125">Return value</span></span>

<span data-ttu-id="d580d-126">Возвращает значение 0 (ноль), если разрешения изменяются, и другое число, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="d580d-126">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d580d-127">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="d580d-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-128">0</span><span class="sxs-lookup"><span data-stu-id="d580d-128">0</span></span>

<span data-ttu-id="d580d-129">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d580d-129">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-130">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="d580d-130">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-131">2</span><span class="sxs-lookup"><span data-stu-id="d580d-131">2</span></span>

<span data-ttu-id="d580d-132">Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="d580d-132">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-133">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="d580d-133">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-134">8</span><span class="sxs-lookup"><span data-stu-id="d580d-134">8</span></span>

<span data-ttu-id="d580d-135">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d580d-135">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-136">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="d580d-136">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-137">9</span><span class="sxs-lookup"><span data-stu-id="d580d-137">9</span></span>

<span data-ttu-id="d580d-138">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="d580d-138">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-139">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="d580d-139">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-140">10</span><span class="sxs-lookup"><span data-stu-id="d580d-140">10</span></span>

<span data-ttu-id="d580d-141">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="d580d-141">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-142">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="d580d-142">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-143">11</span><span class="sxs-lookup"><span data-stu-id="d580d-143">11</span></span>

<span data-ttu-id="d580d-144">Файловая система не является файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="d580d-144">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-145">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="d580d-145">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-146">12</span><span class="sxs-lookup"><span data-stu-id="d580d-146">12</span></span>

<span data-ttu-id="d580d-147">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="d580d-147">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-148">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="d580d-148">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-149">13</span><span class="sxs-lookup"><span data-stu-id="d580d-149">13</span></span>

<span data-ttu-id="d580d-150">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="d580d-150">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-151">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="d580d-151">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-152">14</span><span class="sxs-lookup"><span data-stu-id="d580d-152">14</span></span>

<span data-ttu-id="d580d-153">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="d580d-153">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-154">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="d580d-154">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-155">15</span><span class="sxs-lookup"><span data-stu-id="d580d-155">15</span></span>

<span data-ttu-id="d580d-156">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d580d-156">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-157">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="d580d-157">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-158">16</span><span class="sxs-lookup"><span data-stu-id="d580d-158">16</span></span>

<span data-ttu-id="d580d-159">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="d580d-159">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-160">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="d580d-160">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-161">17</span><span class="sxs-lookup"><span data-stu-id="d580d-161">17</span></span>

<span data-ttu-id="d580d-162">Отсутствует привилегия, необходимая для операции.</span><span class="sxs-lookup"><span data-stu-id="d580d-162">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="d580d-163">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="d580d-163">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d580d-164">21</span><span class="sxs-lookup"><span data-stu-id="d580d-164">21</span></span>

<span data-ttu-id="d580d-165">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="d580d-165">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d580d-166">Требования</span><span class="sxs-lookup"><span data-stu-id="d580d-166">Requirements</span></span>



| <span data-ttu-id="d580d-167">Требование</span><span class="sxs-lookup"><span data-stu-id="d580d-167">Requirement</span></span> | <span data-ttu-id="d580d-168">Значение</span><span class="sxs-lookup"><span data-stu-id="d580d-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d580d-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d580d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="d580d-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d580d-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d580d-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d580d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="d580d-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d580d-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d580d-173">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d580d-173">Namespace</span></span><br/>                | <span data-ttu-id="d580d-174">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d580d-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d580d-175">MOF</span><span class="sxs-lookup"><span data-stu-id="d580d-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d580d-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d580d-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d580d-177">DLL</span><span class="sxs-lookup"><span data-stu-id="d580d-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d580d-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d580d-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d580d-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d580d-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="d580d-180">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d580d-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d580d-181">**\_Файл подкачки Win32**</span><span class="sxs-lookup"><span data-stu-id="d580d-181">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

