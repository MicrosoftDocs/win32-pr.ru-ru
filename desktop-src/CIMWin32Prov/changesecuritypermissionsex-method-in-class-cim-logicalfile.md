---
description: Изменяет разрешения безопасности для логического файла, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af2dc82ef54b6f32eee20f17cd61c0769cc64b1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538786"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="e0a27-103">Метод Чанжесекуритипермиссионсекс \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="e0a27-103">ChangeSecurityPermissionsEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="e0a27-104">Метод **чанжесекуритипермиссионсекс** изменяет разрешения безопасности для логического файла, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-cim-logicalfile.md) ).</span><span class="sxs-lookup"><span data-stu-id="e0a27-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) method).</span></span> <span data-ttu-id="e0a27-105">Если логический файл является каталогом, этот метод будет работать рекурсивно, изменяя разрешения безопасности для всех файлов и подкаталогов, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="e0a27-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0a27-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e0a27-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e0a27-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e0a27-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e0a27-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e0a27-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e0a27-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e0a27-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a27-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0a27-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="e0a27-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0a27-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0a27-112">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0a27-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-113">Задает сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="e0a27-113">Specifies the security information.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-114">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0a27-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-115">Права безопасности для изменения.</span><span class="sxs-lookup"><span data-stu-id="e0a27-115">Security privilege to modify.</span></span> <span data-ttu-id="e0a27-116">Например, чтобы изменить безопасность владельца и DACL, используйте</span><span class="sxs-lookup"><span data-stu-id="e0a27-116">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="e0a27-117">или</span><span class="sxs-lookup"><span data-stu-id="e0a27-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="e0a27-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="e0a27-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e0a27-119">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="e0a27-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="e0a27-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="e0a27-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e0a27-121">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="e0a27-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="e0a27-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="e0a27-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e0a27-123">Измените список управления доступом для логического файла.</span><span class="sxs-lookup"><span data-stu-id="e0a27-123">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="e0a27-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="e0a27-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e0a27-125">Изменение ACL системы для логического файла.</span><span class="sxs-lookup"><span data-stu-id="e0a27-125">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e0a27-126">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e0a27-126">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-127">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="e0a27-127">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="e0a27-128">Если метод выполнен успешно, этот параметр имеет значение **null** .</span><span class="sxs-lookup"><span data-stu-id="e0a27-128">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-129">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e0a27-129">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-130">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="e0a27-130">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="e0a27-131">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл (или каталог), в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="e0a27-131">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="e0a27-132">Если значение параметра равно **null**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="e0a27-132">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-133">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e0a27-133">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-134">Если **значение — true**, разрешения безопасности применяются рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="e0a27-134">If **TRUE**, the security permissions are applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="e0a27-135">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e0a27-135">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0a27-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0a27-136">Return value</span></span>

<span data-ttu-id="e0a27-137">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0a27-137">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e0a27-138">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="e0a27-138">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-139">0</span><span class="sxs-lookup"><span data-stu-id="e0a27-139">0</span></span>

<span data-ttu-id="e0a27-140">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e0a27-140">Success.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-141">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="e0a27-141">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-142">2</span><span class="sxs-lookup"><span data-stu-id="e0a27-142">2</span></span>

<span data-ttu-id="e0a27-143">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="e0a27-143">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-144">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="e0a27-144">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-145">8</span><span class="sxs-lookup"><span data-stu-id="e0a27-145">8</span></span>

<span data-ttu-id="e0a27-146">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="e0a27-146">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-147">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="e0a27-147">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-148">9</span><span class="sxs-lookup"><span data-stu-id="e0a27-148">9</span></span>

<span data-ttu-id="e0a27-149">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="e0a27-149">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-150">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="e0a27-150">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-151">10</span><span class="sxs-lookup"><span data-stu-id="e0a27-151">10</span></span>

<span data-ttu-id="e0a27-152">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="e0a27-152">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-153">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="e0a27-153">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-154">11</span><span class="sxs-lookup"><span data-stu-id="e0a27-154">11</span></span>

<span data-ttu-id="e0a27-155">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="e0a27-155">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-156">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="e0a27-156">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-157">12</span><span class="sxs-lookup"><span data-stu-id="e0a27-157">12</span></span>

<span data-ttu-id="e0a27-158">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="e0a27-158">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-159">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="e0a27-159">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-160">13</span><span class="sxs-lookup"><span data-stu-id="e0a27-160">13</span></span>

<span data-ttu-id="e0a27-161">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="e0a27-161">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-162">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="e0a27-162">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-163">14</span><span class="sxs-lookup"><span data-stu-id="e0a27-163">14</span></span>

<span data-ttu-id="e0a27-164">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="e0a27-164">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-165">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="e0a27-165">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-166">15</span><span class="sxs-lookup"><span data-stu-id="e0a27-166">15</span></span>

<span data-ttu-id="e0a27-167">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e0a27-167">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-168">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="e0a27-168">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-169">16</span><span class="sxs-lookup"><span data-stu-id="e0a27-169">16</span></span>

<span data-ttu-id="e0a27-170">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="e0a27-170">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-171">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="e0a27-171">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-172">17</span><span class="sxs-lookup"><span data-stu-id="e0a27-172">17</span></span>

<span data-ttu-id="e0a27-173">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="e0a27-173">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="e0a27-174">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="e0a27-174">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e0a27-175">21</span><span class="sxs-lookup"><span data-stu-id="e0a27-175">21</span></span>

<span data-ttu-id="e0a27-176">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="e0a27-176">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0a27-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0a27-177">Remarks</span></span>

<span data-ttu-id="e0a27-178">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="e0a27-178">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e0a27-179">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="e0a27-179">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0a27-180">Требования</span><span class="sxs-lookup"><span data-stu-id="e0a27-180">Requirements</span></span>



| <span data-ttu-id="e0a27-181">Требование</span><span class="sxs-lookup"><span data-stu-id="e0a27-181">Requirement</span></span> | <span data-ttu-id="e0a27-182">Значение</span><span class="sxs-lookup"><span data-stu-id="e0a27-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a27-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0a27-183">Minimum supported client</span></span><br/> | <span data-ttu-id="e0a27-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0a27-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0a27-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0a27-185">Minimum supported server</span></span><br/> | <span data-ttu-id="e0a27-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0a27-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0a27-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e0a27-187">Namespace</span></span><br/>                | <span data-ttu-id="e0a27-188">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e0a27-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0a27-189">MOF</span><span class="sxs-lookup"><span data-stu-id="e0a27-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0a27-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0a27-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0a27-191">DLL</span><span class="sxs-lookup"><span data-stu-id="e0a27-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0a27-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0a27-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a27-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0a27-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a27-194">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e0a27-194">**CIM\_LogicalFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="e0a27-195">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e0a27-195">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

