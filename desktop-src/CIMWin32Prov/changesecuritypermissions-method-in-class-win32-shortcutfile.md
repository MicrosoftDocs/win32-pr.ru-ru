---
description: Изменяет разрешения безопасности для логического файла ярлыка, указанного в пути объекта.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионс класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad2d482e0be93a1abec80fc710a1a43d7873dd99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496380"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="a8b45-103">Метод Чанжесекуритипермиссионс \_ класса Win32 шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="a8b45-103">ChangeSecurityPermissions method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="a8b45-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжесекуритипермиссионс изменяет разрешения безопасности для логического файла ярлыка, указанного в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="a8b45-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="a8b45-105">Если логический файл является каталогом, то **чанжесекуритипермиссионс** является рекурсивным и изменяет разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="a8b45-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="a8b45-106">**Чанжесекуритипермиссионс** возвращает целочисленное значение 0 (ноль) при изменении разрешений и другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="a8b45-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="a8b45-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a8b45-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a8b45-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a8b45-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b45-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8b45-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="a8b45-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8b45-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b45-111">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8b45-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-112">Выражение, которое разрешается в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="a8b45-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="a8b45-113">Этот дескриптор содержит новые разрешения безопасности для экземпляра [**\_ файла подкачки Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="a8b45-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-114">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8b45-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-115">Фактические права безопасности для изменения.</span><span class="sxs-lookup"><span data-stu-id="a8b45-115">Actual security privilege to be modified.</span></span> <span data-ttu-id="a8b45-116">Например, чтобы изменить безопасность владельца и DACL, используйте:</span><span class="sxs-lookup"><span data-stu-id="a8b45-116">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="a8b45-117">или</span><span class="sxs-lookup"><span data-stu-id="a8b45-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="a8b45-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="a8b45-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a8b45-119">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="a8b45-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="a8b45-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="a8b45-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a8b45-121">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="a8b45-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="a8b45-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="a8b45-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a8b45-123">Изменение списка управления доступом на уровне пользователей (DACL) логического файла.</span><span class="sxs-lookup"><span data-stu-id="a8b45-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="a8b45-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="a8b45-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a8b45-125">Измените системный список управления доступом (SACL) логического файла.</span><span class="sxs-lookup"><span data-stu-id="a8b45-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b45-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8b45-126">Return value</span></span>

<span data-ttu-id="a8b45-127">Возвращает значение 0 (ноль), если разрешения изменяются, и другое число, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="a8b45-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a8b45-128">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="a8b45-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-129">0</span><span class="sxs-lookup"><span data-stu-id="a8b45-129">0</span></span>

<span data-ttu-id="a8b45-130">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a8b45-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-131">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="a8b45-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-132">2</span><span class="sxs-lookup"><span data-stu-id="a8b45-132">2</span></span>

<span data-ttu-id="a8b45-133">Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="a8b45-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-134">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="a8b45-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-135">8</span><span class="sxs-lookup"><span data-stu-id="a8b45-135">8</span></span>

<span data-ttu-id="a8b45-136">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a8b45-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-137">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="a8b45-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-138">9</span><span class="sxs-lookup"><span data-stu-id="a8b45-138">9</span></span>

<span data-ttu-id="a8b45-139">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="a8b45-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-140">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="a8b45-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-141">10</span><span class="sxs-lookup"><span data-stu-id="a8b45-141">10</span></span>

<span data-ttu-id="a8b45-142">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="a8b45-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-143">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="a8b45-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-144">11</span><span class="sxs-lookup"><span data-stu-id="a8b45-144">11</span></span>

<span data-ttu-id="a8b45-145">Файловая система не является файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="a8b45-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-146">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="a8b45-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-147">12</span><span class="sxs-lookup"><span data-stu-id="a8b45-147">12</span></span>

<span data-ttu-id="a8b45-148">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="a8b45-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-149">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="a8b45-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-150">13</span><span class="sxs-lookup"><span data-stu-id="a8b45-150">13</span></span>

<span data-ttu-id="a8b45-151">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="a8b45-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-152">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="a8b45-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-153">14</span><span class="sxs-lookup"><span data-stu-id="a8b45-153">14</span></span>

<span data-ttu-id="a8b45-154">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="a8b45-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-155">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="a8b45-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-156">15</span><span class="sxs-lookup"><span data-stu-id="a8b45-156">15</span></span>

<span data-ttu-id="a8b45-157">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="a8b45-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-158">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="a8b45-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-159">16</span><span class="sxs-lookup"><span data-stu-id="a8b45-159">16</span></span>

<span data-ttu-id="a8b45-160">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="a8b45-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-161">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="a8b45-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-162">17</span><span class="sxs-lookup"><span data-stu-id="a8b45-162">17</span></span>

<span data-ttu-id="a8b45-163">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="a8b45-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="a8b45-164">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="a8b45-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a8b45-165">21</span><span class="sxs-lookup"><span data-stu-id="a8b45-165">21</span></span>

<span data-ttu-id="a8b45-166">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="a8b45-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8b45-167">Требования</span><span class="sxs-lookup"><span data-stu-id="a8b45-167">Requirements</span></span>



| <span data-ttu-id="a8b45-168">Требование</span><span class="sxs-lookup"><span data-stu-id="a8b45-168">Requirement</span></span> | <span data-ttu-id="a8b45-169">Значение</span><span class="sxs-lookup"><span data-stu-id="a8b45-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b45-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8b45-170">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b45-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8b45-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8b45-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8b45-172">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b45-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8b45-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8b45-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a8b45-174">Namespace</span></span><br/>                | <span data-ttu-id="a8b45-175">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a8b45-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8b45-176">MOF</span><span class="sxs-lookup"><span data-stu-id="a8b45-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8b45-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8b45-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8b45-178">DLL</span><span class="sxs-lookup"><span data-stu-id="a8b45-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8b45-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8b45-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b45-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8b45-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8b45-181">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a8b45-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a8b45-182">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="a8b45-182">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

