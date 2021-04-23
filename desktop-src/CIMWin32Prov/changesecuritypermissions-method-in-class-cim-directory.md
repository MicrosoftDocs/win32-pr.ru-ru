---
description: Изменяет разрешения безопасности для файла записи логического каталога, указанного в пути к объекту.
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионс класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bf767dc45907a90354b2c00fb30c6b31ce6d09a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807619"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="4a61c-103">Метод Чанжесекуритипермиссионс \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="4a61c-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="4a61c-104">Метод **чанжесекуритипермиссионс** изменяет разрешения безопасности для файла записи логического каталога, указанного в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="4a61c-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="4a61c-105">Если логический файл является каталогом, этот метод будет работать рекурсивно, изменяя разрешения безопасности для всех файлов и подкаталогов, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="4a61c-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="4a61c-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="4a61c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a61c-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4a61c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4a61c-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4a61c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4a61c-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4a61c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4a61c-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4a61c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a61c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a61c-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="4a61c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a61c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a61c-113">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a61c-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a61c-114">Указывает сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="4a61c-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="4a61c-115">**Пустой** список управления доступом (ACL) в структуре [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="4a61c-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="4a61c-116">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a61c-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a61c-117">Права безопасности для изменения.</span><span class="sxs-lookup"><span data-stu-id="4a61c-117">Security privilege to modify.</span></span> <span data-ttu-id="4a61c-118">Например, чтобы изменить безопасность владельца и DACL, используйте:</span><span class="sxs-lookup"><span data-stu-id="4a61c-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="4a61c-119">или</span><span class="sxs-lookup"><span data-stu-id="4a61c-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="4a61c-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="4a61c-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4a61c-121">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="4a61c-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="4a61c-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="4a61c-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4a61c-123">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="4a61c-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="4a61c-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="4a61c-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4a61c-125">Измените список управления доступом для логического файла.</span><span class="sxs-lookup"><span data-stu-id="4a61c-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="4a61c-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="4a61c-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4a61c-127">Изменение ACL системы для логического файла.</span><span class="sxs-lookup"><span data-stu-id="4a61c-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a61c-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a61c-128">Return value</span></span>

<span data-ttu-id="4a61c-129">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="4a61c-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-130">0</span><span class="sxs-lookup"><span data-stu-id="4a61c-130">0</span></span>

<span data-ttu-id="4a61c-131">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4a61c-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-132">2</span><span class="sxs-lookup"><span data-stu-id="4a61c-132">2</span></span>

<span data-ttu-id="4a61c-133">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="4a61c-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-134">8</span><span class="sxs-lookup"><span data-stu-id="4a61c-134">8</span></span>

<span data-ttu-id="4a61c-135">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="4a61c-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-136">9</span><span class="sxs-lookup"><span data-stu-id="4a61c-136">9</span></span>

<span data-ttu-id="4a61c-137">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="4a61c-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-138">10</span><span class="sxs-lookup"><span data-stu-id="4a61c-138">10</span></span>

<span data-ttu-id="4a61c-139">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="4a61c-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-140">11</span><span class="sxs-lookup"><span data-stu-id="4a61c-140">11</span></span>

<span data-ttu-id="4a61c-141">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="4a61c-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-142">12</span><span class="sxs-lookup"><span data-stu-id="4a61c-142">12</span></span>

<span data-ttu-id="4a61c-143">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="4a61c-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-144">13</span><span class="sxs-lookup"><span data-stu-id="4a61c-144">13</span></span>

<span data-ttu-id="4a61c-145">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="4a61c-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-146">14</span><span class="sxs-lookup"><span data-stu-id="4a61c-146">14</span></span>

<span data-ttu-id="4a61c-147">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="4a61c-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-148">15</span><span class="sxs-lookup"><span data-stu-id="4a61c-148">15</span></span>

<span data-ttu-id="4a61c-149">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="4a61c-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-150">16</span><span class="sxs-lookup"><span data-stu-id="4a61c-150">16</span></span>

<span data-ttu-id="4a61c-151">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="4a61c-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-152">17</span><span class="sxs-lookup"><span data-stu-id="4a61c-152">17</span></span>

<span data-ttu-id="4a61c-153">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="4a61c-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4a61c-154">21</span><span class="sxs-lookup"><span data-stu-id="4a61c-154">21</span></span>

<span data-ttu-id="4a61c-155">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="4a61c-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a61c-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a61c-156">Remarks</span></span>

<span data-ttu-id="4a61c-157">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4a61c-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4a61c-158">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="4a61c-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4a61c-159">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4a61c-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4a61c-160">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4a61c-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a61c-161">Требования</span><span class="sxs-lookup"><span data-stu-id="4a61c-161">Requirements</span></span>



| <span data-ttu-id="4a61c-162">Требование</span><span class="sxs-lookup"><span data-stu-id="4a61c-162">Requirement</span></span> | <span data-ttu-id="4a61c-163">Значение</span><span class="sxs-lookup"><span data-stu-id="4a61c-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a61c-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a61c-164">Minimum supported client</span></span><br/> | <span data-ttu-id="4a61c-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a61c-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a61c-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a61c-166">Minimum supported server</span></span><br/> | <span data-ttu-id="4a61c-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a61c-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a61c-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4a61c-168">Namespace</span></span><br/>                | <span data-ttu-id="4a61c-169">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4a61c-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a61c-170">MOF</span><span class="sxs-lookup"><span data-stu-id="4a61c-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a61c-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a61c-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a61c-172">DLL</span><span class="sxs-lookup"><span data-stu-id="4a61c-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a61c-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a61c-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a61c-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a61c-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a61c-175">\_Каталог CIM</span><span class="sxs-lookup"><span data-stu-id="4a61c-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="4a61c-176">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="4a61c-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

