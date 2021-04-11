---
description: Изменяет разрешения безопасности для файла устройства, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2c7261844542f6414052517432c2e8ff3f1194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141911"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="2da5e-103">Метод Чанжесекуритипермиссионсекс \_ класса CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="2da5e-103">ChangeSecurityPermissionsEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="2da5e-104">Метод **чанжесекуритипермиссионсекс** изменяет разрешения безопасности для файла устройства, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-cim-devicefile.md) ).</span><span class="sxs-lookup"><span data-stu-id="2da5e-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the device file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) method).</span></span> <span data-ttu-id="2da5e-105">Если логический файл является каталогом, этот метод работает рекурсивно, изменяя разрешения безопасности для всех файлов и подкаталогов, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="2da5e-105">If the logical file is a directory, then this method acts recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="2da5e-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2da5e-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2da5e-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2da5e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2da5e-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2da5e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2da5e-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="2da5e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2da5e-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2da5e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2da5e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2da5e-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="2da5e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2da5e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da5e-113">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2da5e-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da5e-114">Задает сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="2da5e-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="2da5e-115">Список ACL **со значением NULL** в структуре [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="2da5e-115">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="2da5e-116">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2da5e-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da5e-117">Права безопасности для изменения.</span><span class="sxs-lookup"><span data-stu-id="2da5e-117">Security privilege to modify.</span></span> <span data-ttu-id="2da5e-118">Например, чтобы изменить безопасность владельца и DACL, используйте</span><span class="sxs-lookup"><span data-stu-id="2da5e-118">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="2da5e-119">или</span><span class="sxs-lookup"><span data-stu-id="2da5e-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="2da5e-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="2da5e-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2da5e-121">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="2da5e-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="2da5e-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="2da5e-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2da5e-123">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="2da5e-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="2da5e-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="2da5e-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2da5e-125">Измените список управления доступом для логического файла.</span><span class="sxs-lookup"><span data-stu-id="2da5e-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="2da5e-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="2da5e-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2da5e-127">Изменение ACL системы для логического файла.</span><span class="sxs-lookup"><span data-stu-id="2da5e-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2da5e-128">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2da5e-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2da5e-129">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="2da5e-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="2da5e-130">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="2da5e-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2da5e-131">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2da5e-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2da5e-132">Дочерний файл (или каталог) для использования в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="2da5e-132">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="2da5e-133">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="2da5e-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2da5e-134">Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="2da5e-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="2da5e-135">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="2da5e-135">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2da5e-136">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ девицефиле**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="2da5e-136">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="2da5e-137">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2da5e-137">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da5e-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2da5e-138">Return value</span></span>

<span data-ttu-id="2da5e-139">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="2da5e-139">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-140">0</span><span class="sxs-lookup"><span data-stu-id="2da5e-140">0</span></span>

<span data-ttu-id="2da5e-141">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2da5e-141">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-142">2</span><span class="sxs-lookup"><span data-stu-id="2da5e-142">2</span></span>

<span data-ttu-id="2da5e-143">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2da5e-143">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-144">8</span><span class="sxs-lookup"><span data-stu-id="2da5e-144">8</span></span>

<span data-ttu-id="2da5e-145">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="2da5e-145">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-146">9</span><span class="sxs-lookup"><span data-stu-id="2da5e-146">9</span></span>

<span data-ttu-id="2da5e-147">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="2da5e-147">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-148">10</span><span class="sxs-lookup"><span data-stu-id="2da5e-148">10</span></span>

<span data-ttu-id="2da5e-149">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="2da5e-149">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-150">11</span><span class="sxs-lookup"><span data-stu-id="2da5e-150">11</span></span>

<span data-ttu-id="2da5e-151">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="2da5e-151">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-152">12</span><span class="sxs-lookup"><span data-stu-id="2da5e-152">12</span></span>

<span data-ttu-id="2da5e-153">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="2da5e-153">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-154">13</span><span class="sxs-lookup"><span data-stu-id="2da5e-154">13</span></span>

<span data-ttu-id="2da5e-155">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="2da5e-155">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-156">14</span><span class="sxs-lookup"><span data-stu-id="2da5e-156">14</span></span>

<span data-ttu-id="2da5e-157">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="2da5e-157">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-158">15</span><span class="sxs-lookup"><span data-stu-id="2da5e-158">15</span></span>

<span data-ttu-id="2da5e-159">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="2da5e-159">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-160">16</span><span class="sxs-lookup"><span data-stu-id="2da5e-160">16</span></span>

<span data-ttu-id="2da5e-161">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="2da5e-161">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-162">17</span><span class="sxs-lookup"><span data-stu-id="2da5e-162">17</span></span>

<span data-ttu-id="2da5e-163">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="2da5e-163">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2da5e-164">21</span><span class="sxs-lookup"><span data-stu-id="2da5e-164">21</span></span>

<span data-ttu-id="2da5e-165">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="2da5e-165">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2da5e-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2da5e-166">Remarks</span></span>

<span data-ttu-id="2da5e-167">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="2da5e-167">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2da5e-168">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="2da5e-168">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="2da5e-169">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2da5e-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2da5e-170">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2da5e-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da5e-171">Требования</span><span class="sxs-lookup"><span data-stu-id="2da5e-171">Requirements</span></span>



| <span data-ttu-id="2da5e-172">Требование</span><span class="sxs-lookup"><span data-stu-id="2da5e-172">Requirement</span></span> | <span data-ttu-id="2da5e-173">Значение</span><span class="sxs-lookup"><span data-stu-id="2da5e-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da5e-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2da5e-174">Minimum supported client</span></span><br/> | <span data-ttu-id="2da5e-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2da5e-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2da5e-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2da5e-176">Minimum supported server</span></span><br/> | <span data-ttu-id="2da5e-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2da5e-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2da5e-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2da5e-178">Namespace</span></span><br/>                | <span data-ttu-id="2da5e-179">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2da5e-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2da5e-180">MOF</span><span class="sxs-lookup"><span data-stu-id="2da5e-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2da5e-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2da5e-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2da5e-182">DLL</span><span class="sxs-lookup"><span data-stu-id="2da5e-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2da5e-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2da5e-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da5e-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2da5e-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da5e-185">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="2da5e-185">CIM\_DeviceFile</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="2da5e-186">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="2da5e-186">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

