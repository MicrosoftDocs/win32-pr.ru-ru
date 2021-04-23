---
description: Изменяет разрешения безопасности для файла логического кодека, указанного в пути объекта.
ms.assetid: d7945666-e514-4bfc-81bc-8e98aa90bcf0
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионс класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b0789164b2bb28b5c3c84e907cf7ae2acb96e01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655648"
---
# <a name="changesecuritypermissions-method-of-the-win32_codecfile-class"></a><span data-ttu-id="223c9-103">Метод Чанжесекуритипермиссионс \_ класса Win32 кодекфиле</span><span class="sxs-lookup"><span data-stu-id="223c9-103">ChangeSecurityPermissions method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="223c9-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжесекуритипермиссионс изменяет разрешения безопасности для файла логического кодека, указанного в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="223c9-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical codec file specified in the object path.</span></span> <span data-ttu-id="223c9-105">Если логический файл является каталогом, то **чанжесекуритипермиссионс** является рекурсивным и изменяет разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="223c9-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories the directory contains.</span></span> <span data-ttu-id="223c9-106">**Чанжесекуритипермиссионс** возвращает целочисленное значение 0 (ноль) при изменении разрешений и другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="223c9-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="223c9-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="223c9-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="223c9-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="223c9-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="223c9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="223c9-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="223c9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="223c9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223c9-111">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="223c9-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223c9-112">Выражение, которое разрешается в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="223c9-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="223c9-113">Этот дескриптор содержит новые разрешения безопасности для экземпляра [**Win32 \_ кодекфиле**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="223c9-113">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="223c9-114">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="223c9-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223c9-115">Права безопасности, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="223c9-115">Security privilege to be modified.</span></span> <span data-ttu-id="223c9-116">Например, чтобы изменить уровень безопасности владельца и избирательного списка управления доступом (DACL), используйте:</span><span class="sxs-lookup"><span data-stu-id="223c9-116">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="223c9-117">-или-</span><span class="sxs-lookup"><span data-stu-id="223c9-117">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="223c9-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="223c9-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="223c9-119">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="223c9-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="223c9-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="223c9-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="223c9-121">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="223c9-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="223c9-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="223c9-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="223c9-123">Изменение списка управления доступом на уровне пользователей (DACL) логического файла.</span><span class="sxs-lookup"><span data-stu-id="223c9-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="223c9-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="223c9-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="223c9-125">Измените системный список управления доступом (SACL) логического файла.</span><span class="sxs-lookup"><span data-stu-id="223c9-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="223c9-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="223c9-126">Return value</span></span>

<span data-ttu-id="223c9-127">Возвращает значение 0 (ноль), если разрешения изменяются, и другое число, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="223c9-127">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="223c9-128">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="223c9-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-129">0</span><span class="sxs-lookup"><span data-stu-id="223c9-129">0</span></span>

<span data-ttu-id="223c9-130">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="223c9-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-131">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="223c9-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-132">2</span><span class="sxs-lookup"><span data-stu-id="223c9-132">2</span></span>

<span data-ttu-id="223c9-133">Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="223c9-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-134">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="223c9-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-135">8</span><span class="sxs-lookup"><span data-stu-id="223c9-135">8</span></span>

<span data-ttu-id="223c9-136">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="223c9-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-137">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="223c9-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-138">9</span><span class="sxs-lookup"><span data-stu-id="223c9-138">9</span></span>

<span data-ttu-id="223c9-139">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="223c9-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-140">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="223c9-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-141">10</span><span class="sxs-lookup"><span data-stu-id="223c9-141">10</span></span>

<span data-ttu-id="223c9-142">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="223c9-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-143">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="223c9-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-144">11</span><span class="sxs-lookup"><span data-stu-id="223c9-144">11</span></span>

<span data-ttu-id="223c9-145">Файловая система не является файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="223c9-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-146">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="223c9-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-147">12</span><span class="sxs-lookup"><span data-stu-id="223c9-147">12</span></span>

<span data-ttu-id="223c9-148">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="223c9-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-149">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="223c9-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-150">13</span><span class="sxs-lookup"><span data-stu-id="223c9-150">13</span></span>

<span data-ttu-id="223c9-151">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="223c9-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-152">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="223c9-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-153">14</span><span class="sxs-lookup"><span data-stu-id="223c9-153">14</span></span>

<span data-ttu-id="223c9-154">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="223c9-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-155">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="223c9-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-156">15</span><span class="sxs-lookup"><span data-stu-id="223c9-156">15</span></span>

<span data-ttu-id="223c9-157">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="223c9-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-158">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="223c9-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-159">16</span><span class="sxs-lookup"><span data-stu-id="223c9-159">16</span></span>

<span data-ttu-id="223c9-160">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="223c9-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-161">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="223c9-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-162">17</span><span class="sxs-lookup"><span data-stu-id="223c9-162">17</span></span>

<span data-ttu-id="223c9-163">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="223c9-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="223c9-164">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="223c9-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="223c9-165">21</span><span class="sxs-lookup"><span data-stu-id="223c9-165">21</span></span>

<span data-ttu-id="223c9-166">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="223c9-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="223c9-167">Требования</span><span class="sxs-lookup"><span data-stu-id="223c9-167">Requirements</span></span>



| <span data-ttu-id="223c9-168">Требование</span><span class="sxs-lookup"><span data-stu-id="223c9-168">Requirement</span></span> | <span data-ttu-id="223c9-169">Значение</span><span class="sxs-lookup"><span data-stu-id="223c9-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="223c9-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="223c9-170">Minimum supported client</span></span><br/> | <span data-ttu-id="223c9-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="223c9-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="223c9-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="223c9-172">Minimum supported server</span></span><br/> | <span data-ttu-id="223c9-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="223c9-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="223c9-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="223c9-174">Namespace</span></span><br/>                | <span data-ttu-id="223c9-175">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="223c9-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="223c9-176">MOF</span><span class="sxs-lookup"><span data-stu-id="223c9-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="223c9-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="223c9-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="223c9-178">DLL</span><span class="sxs-lookup"><span data-stu-id="223c9-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="223c9-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="223c9-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="223c9-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="223c9-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="223c9-181">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="223c9-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="223c9-182">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="223c9-182">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

