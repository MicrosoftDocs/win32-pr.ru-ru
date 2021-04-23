---
description: Изменяет разрешения безопасности для логического файла данных, указанного в пути к объекту.
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141959"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a><span data-ttu-id="753ac-103">Метод Чанжесекуритипермиссионс \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="753ac-103">ChangeSecurityPermissions method of the CIM\_DataFile class</span></span>

<span data-ttu-id="753ac-104">Метод **чанжесекуритипермиссионс** изменяет разрешения безопасности для логического файла данных, указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="753ac-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical data file specified in the object path.</span></span> <span data-ttu-id="753ac-105">Если логический файл является каталогом, этот метод будет работать рекурсивно, изменяя разрешения безопасности для всех файлов и подкаталогов, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="753ac-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="753ac-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="753ac-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="753ac-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="753ac-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="753ac-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="753ac-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="753ac-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="753ac-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="753ac-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="753ac-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="753ac-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="753ac-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="753ac-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="753ac-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="753ac-113">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="753ac-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="753ac-114">Задает сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="753ac-114">Specifies the security information.</span></span>

> [!Note]  
> <span data-ttu-id="753ac-115">**Пустой** список управления доступом (ACL) в структуре [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="753ac-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="753ac-116">Сведения о влиянии неограниченного доступа см. в разделе [Создание дескриптора безопасности для нового объекта](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="753ac-116">For information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="753ac-117">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="753ac-117">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="753ac-118">Права безопасности для изменения.</span><span class="sxs-lookup"><span data-stu-id="753ac-118">Security privilege to modify.</span></span> <span data-ttu-id="753ac-119">Например, чтобы изменить безопасность владельца и DACL, используйте:</span><span class="sxs-lookup"><span data-stu-id="753ac-119">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="753ac-120">или</span><span class="sxs-lookup"><span data-stu-id="753ac-120">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="753ac-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="753ac-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="753ac-122">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="753ac-122">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="753ac-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="753ac-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="753ac-124">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="753ac-124">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="753ac-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="753ac-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="753ac-126">Измените список управления доступом для логического файла.</span><span class="sxs-lookup"><span data-stu-id="753ac-126">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="753ac-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="753ac-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="753ac-128">Изменение ACL системы для логического файла.</span><span class="sxs-lookup"><span data-stu-id="753ac-128">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="753ac-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="753ac-129">Return value</span></span>

<span data-ttu-id="753ac-130">Возвращает значение 0 в случае успешного выполнения и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="753ac-130">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="753ac-131">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="753ac-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="753ac-132">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="753ac-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="753ac-133">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="753ac-133">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-134">0</span><span class="sxs-lookup"><span data-stu-id="753ac-134">0</span></span>

<span data-ttu-id="753ac-135">Успешно.</span><span class="sxs-lookup"><span data-stu-id="753ac-135">Success.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-136">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="753ac-136">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-137">2</span><span class="sxs-lookup"><span data-stu-id="753ac-137">2</span></span>

<span data-ttu-id="753ac-138">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="753ac-138">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-139">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="753ac-139">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-140">8</span><span class="sxs-lookup"><span data-stu-id="753ac-140">8</span></span>

<span data-ttu-id="753ac-141">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="753ac-141">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-142">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="753ac-142">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-143">9</span><span class="sxs-lookup"><span data-stu-id="753ac-143">9</span></span>

<span data-ttu-id="753ac-144">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="753ac-144">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-145">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="753ac-145">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-146">10</span><span class="sxs-lookup"><span data-stu-id="753ac-146">10</span></span>

<span data-ttu-id="753ac-147">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="753ac-147">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-148">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="753ac-148">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-149">11</span><span class="sxs-lookup"><span data-stu-id="753ac-149">11</span></span>

</dd> <dt>

<span data-ttu-id="753ac-150">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="753ac-150">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-151">12</span><span class="sxs-lookup"><span data-stu-id="753ac-151">12</span></span>

<span data-ttu-id="753ac-152">Платформа не на базе Windows NT.</span><span class="sxs-lookup"><span data-stu-id="753ac-152">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-153">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="753ac-153">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-154">13</span><span class="sxs-lookup"><span data-stu-id="753ac-154">13</span></span>

<span data-ttu-id="753ac-155">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="753ac-155">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-156">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="753ac-156">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-157">14</span><span class="sxs-lookup"><span data-stu-id="753ac-157">14</span></span>

<span data-ttu-id="753ac-158">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="753ac-158">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-159">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="753ac-159">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-160">15</span><span class="sxs-lookup"><span data-stu-id="753ac-160">15</span></span>

<span data-ttu-id="753ac-161">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="753ac-161">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-162">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="753ac-162">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-163">16</span><span class="sxs-lookup"><span data-stu-id="753ac-163">16</span></span>

<span data-ttu-id="753ac-164">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="753ac-164">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-165">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="753ac-165">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-166">17</span><span class="sxs-lookup"><span data-stu-id="753ac-166">17</span></span>

<span data-ttu-id="753ac-167">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="753ac-167">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="753ac-168">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="753ac-168">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="753ac-169">21</span><span class="sxs-lookup"><span data-stu-id="753ac-169">21</span></span>

<span data-ttu-id="753ac-170">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="753ac-170">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="753ac-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="753ac-171">Remarks</span></span>

<span data-ttu-id="753ac-172">Метод **чанжесекуритипермиссионс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="753ac-172">The **ChangeSecurityPermissions** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="753ac-173">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="753ac-173">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="753ac-174">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="753ac-174">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="753ac-175">Требования</span><span class="sxs-lookup"><span data-stu-id="753ac-175">Requirements</span></span>



| <span data-ttu-id="753ac-176">Требование</span><span class="sxs-lookup"><span data-stu-id="753ac-176">Requirement</span></span> | <span data-ttu-id="753ac-177">Значение</span><span class="sxs-lookup"><span data-stu-id="753ac-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="753ac-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="753ac-178">Minimum supported client</span></span><br/> | <span data-ttu-id="753ac-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="753ac-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="753ac-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="753ac-180">Minimum supported server</span></span><br/> | <span data-ttu-id="753ac-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="753ac-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="753ac-182">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="753ac-182">Namespace</span></span><br/>                | <span data-ttu-id="753ac-183">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="753ac-183">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="753ac-184">MOF</span><span class="sxs-lookup"><span data-stu-id="753ac-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="753ac-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="753ac-185"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="753ac-186">DLL</span><span class="sxs-lookup"><span data-stu-id="753ac-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="753ac-187"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="753ac-187"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="753ac-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="753ac-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="753ac-189">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="753ac-189">**CIM\_DataFile**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="753ac-190">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="753ac-190">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="753ac-191">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="753ac-191">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="753ac-192">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="753ac-192">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

