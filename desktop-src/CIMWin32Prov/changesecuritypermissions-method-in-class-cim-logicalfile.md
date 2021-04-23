---
description: Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионс класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 929e05047af203d8e2344afa8175228e3bd969fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655975"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="21527-103">Метод Чанжесекуритипермиссионс \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="21527-103">ChangeSecurityPermissions method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="21527-104">Метод **чанжесекуритипермиссионс** изменяет разрешения безопасности для логического файла, указанного в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="21527-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="21527-105">Если логический файл является каталогом, **чанжесекуритипермиссионс** будет работать рекурсивно, изменив разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="21527-105">If the logical file is a directory, then **ChangeSecurityPermissions** will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21527-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="21527-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="21527-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="21527-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="21527-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="21527-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="21527-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="21527-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="21527-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21527-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="21527-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="21527-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21527-112">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21527-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21527-113">Указывает сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="21527-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="21527-114">**Пустой** список управления доступом (ACL) в [**\_ дескрипторе безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="21527-114">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="21527-115">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21527-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21527-116">Права безопасности для изменения.</span><span class="sxs-lookup"><span data-stu-id="21527-116">Security privilege to modify.</span></span> <span data-ttu-id="21527-117">Например, чтобы изменить безопасность владельца и DACL, используйте:</span><span class="sxs-lookup"><span data-stu-id="21527-117">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="21527-118">или</span><span class="sxs-lookup"><span data-stu-id="21527-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="21527-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="21527-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="21527-120">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="21527-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="21527-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="21527-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="21527-122">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="21527-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="21527-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="21527-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="21527-124">Измените список управления доступом для логического файла.</span><span class="sxs-lookup"><span data-stu-id="21527-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="21527-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="21527-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="21527-126">Изменение ACL системы для логического файла.</span><span class="sxs-lookup"><span data-stu-id="21527-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21527-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21527-127">Return value</span></span>

<span data-ttu-id="21527-128">Возвращает значение 0 в случае успешного выполнения и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="21527-128">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="21527-129">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="21527-129">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="21527-130">0</span><span class="sxs-lookup"><span data-stu-id="21527-130">0</span></span>

<span data-ttu-id="21527-131">Успешно.</span><span class="sxs-lookup"><span data-stu-id="21527-131">Success.</span></span>

</dd> <dt>

<span data-ttu-id="21527-132">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="21527-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="21527-133">2</span><span class="sxs-lookup"><span data-stu-id="21527-133">2</span></span>

<span data-ttu-id="21527-134">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="21527-134">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="21527-135">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="21527-135">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="21527-136">8</span><span class="sxs-lookup"><span data-stu-id="21527-136">8</span></span>

<span data-ttu-id="21527-137">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="21527-137">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="21527-138">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="21527-138">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="21527-139">9</span><span class="sxs-lookup"><span data-stu-id="21527-139">9</span></span>

<span data-ttu-id="21527-140">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="21527-140">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="21527-141">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="21527-141">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="21527-142">10</span><span class="sxs-lookup"><span data-stu-id="21527-142">10</span></span>

<span data-ttu-id="21527-143">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="21527-143">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="21527-144">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="21527-144">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="21527-145">11</span><span class="sxs-lookup"><span data-stu-id="21527-145">11</span></span>

<span data-ttu-id="21527-146">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="21527-146">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="21527-147">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="21527-147">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="21527-148">12</span><span class="sxs-lookup"><span data-stu-id="21527-148">12</span></span>

<span data-ttu-id="21527-149">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="21527-149">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="21527-150">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="21527-150">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="21527-151">13</span><span class="sxs-lookup"><span data-stu-id="21527-151">13</span></span>

<span data-ttu-id="21527-152">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="21527-152">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="21527-153">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="21527-153">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="21527-154">14</span><span class="sxs-lookup"><span data-stu-id="21527-154">14</span></span>

<span data-ttu-id="21527-155">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="21527-155">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="21527-156">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="21527-156">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="21527-157">15</span><span class="sxs-lookup"><span data-stu-id="21527-157">15</span></span>

<span data-ttu-id="21527-158">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="21527-158">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="21527-159">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="21527-159">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="21527-160">16</span><span class="sxs-lookup"><span data-stu-id="21527-160">16</span></span>

<span data-ttu-id="21527-161">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="21527-161">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="21527-162">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="21527-162">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="21527-163">17</span><span class="sxs-lookup"><span data-stu-id="21527-163">17</span></span>

<span data-ttu-id="21527-164">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="21527-164">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="21527-165">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="21527-165">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="21527-166">21</span><span class="sxs-lookup"><span data-stu-id="21527-166">21</span></span>

<span data-ttu-id="21527-167">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="21527-167">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21527-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21527-168">Remarks</span></span>

<span data-ttu-id="21527-169">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="21527-169">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="21527-170">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="21527-170">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="21527-171">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="21527-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="21527-172">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="21527-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="21527-173">Требования</span><span class="sxs-lookup"><span data-stu-id="21527-173">Requirements</span></span>



| <span data-ttu-id="21527-174">Требование</span><span class="sxs-lookup"><span data-stu-id="21527-174">Requirement</span></span> | <span data-ttu-id="21527-175">Значение</span><span class="sxs-lookup"><span data-stu-id="21527-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21527-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21527-176">Minimum supported client</span></span><br/> | <span data-ttu-id="21527-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21527-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21527-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21527-178">Minimum supported server</span></span><br/> | <span data-ttu-id="21527-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21527-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21527-180">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="21527-180">Namespace</span></span><br/>                | <span data-ttu-id="21527-181">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="21527-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21527-182">MOF</span><span class="sxs-lookup"><span data-stu-id="21527-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21527-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21527-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21527-184">DLL</span><span class="sxs-lookup"><span data-stu-id="21527-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21527-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21527-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21527-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21527-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21527-187">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="21527-187">**CIM\_LogicalFile**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="21527-188">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="21527-188">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

