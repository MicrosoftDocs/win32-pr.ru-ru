---
description: Изменяет разрешения безопасности для файла записи логического каталога, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс и наследуется от CIM \_ LogicalFile).
ms.assetid: 5c1f66ba-9aa1-47ca-8fcf-7663782544cd
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2d8ddf4c6ffdbd016db1e8c08d89f2dd6476ccf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655845"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_directory-class"></a><span data-ttu-id="97c3f-103">Метод Чанжесекуритипермиссионсекс \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="97c3f-103">ChangeSecurityPermissionsEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="97c3f-104">Метод **чанжесекуритипермиссионсекс** изменяет разрешения безопасности для файла записи логического каталога, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-cim-directory.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md)).</span><span class="sxs-lookup"><span data-stu-id="97c3f-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md)).</span></span> <span data-ttu-id="97c3f-105">Если логический файл является каталогом, этот метод будет работать рекурсивно, изменяя разрешения безопасности для всех файлов и подкаталогов, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="97c3f-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97c3f-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="97c3f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="97c3f-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="97c3f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="97c3f-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="97c3f-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="97c3f-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="97c3f-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="97c3f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97c3f-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="97c3f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="97c3f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c3f-112">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97c3f-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c3f-113">Указывает сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="97c3f-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="97c3f-114">Список ACL **со значением NULL** в структуре [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="97c3f-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="97c3f-115">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97c3f-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c3f-116">Права безопасности для изменения.</span><span class="sxs-lookup"><span data-stu-id="97c3f-116">Security privilege to modify.</span></span> <span data-ttu-id="97c3f-117">Например, чтобы изменить безопасность владельца и DACL, используйте</span><span class="sxs-lookup"><span data-stu-id="97c3f-117">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="97c3f-118">или</span><span class="sxs-lookup"><span data-stu-id="97c3f-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="97c3f-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="97c3f-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="97c3f-120">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="97c3f-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="97c3f-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="97c3f-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="97c3f-122">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="97c3f-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="97c3f-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="97c3f-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="97c3f-124">Измените список управления доступом для логического файла.</span><span class="sxs-lookup"><span data-stu-id="97c3f-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="97c3f-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="97c3f-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="97c3f-126">Изменение ACL системы для логического файла.</span><span class="sxs-lookup"><span data-stu-id="97c3f-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="97c3f-127">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="97c3f-127">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97c3f-128">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="97c3f-128">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="97c3f-129">Если метод выполнен успешно, этот параметр имеет значение **null** .</span><span class="sxs-lookup"><span data-stu-id="97c3f-129">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="97c3f-130">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="97c3f-130">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97c3f-131">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="97c3f-131">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="97c3f-132">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл (или каталог), в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="97c3f-132">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="97c3f-133">Если значение параметра равно **null**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="97c3f-133">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="97c3f-134">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="97c3f-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97c3f-135">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном экземпляром [**\_ каталога CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="97c3f-135">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="97c3f-136">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="97c3f-136">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c3f-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97c3f-137">Return value</span></span>

<span data-ttu-id="97c3f-138">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="97c3f-138">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-139">0</span><span class="sxs-lookup"><span data-stu-id="97c3f-139">0</span></span>

<span data-ttu-id="97c3f-140">Успешно.</span><span class="sxs-lookup"><span data-stu-id="97c3f-140">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-141">2</span><span class="sxs-lookup"><span data-stu-id="97c3f-141">2</span></span>

<span data-ttu-id="97c3f-142">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="97c3f-142">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-143">8</span><span class="sxs-lookup"><span data-stu-id="97c3f-143">8</span></span>

<span data-ttu-id="97c3f-144">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="97c3f-144">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-145">9</span><span class="sxs-lookup"><span data-stu-id="97c3f-145">9</span></span>

<span data-ttu-id="97c3f-146">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="97c3f-146">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-147">10</span><span class="sxs-lookup"><span data-stu-id="97c3f-147">10</span></span>

<span data-ttu-id="97c3f-148">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="97c3f-148">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-149">11</span><span class="sxs-lookup"><span data-stu-id="97c3f-149">11</span></span>

<span data-ttu-id="97c3f-150">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="97c3f-150">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-151">12</span><span class="sxs-lookup"><span data-stu-id="97c3f-151">12</span></span>

<span data-ttu-id="97c3f-152">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="97c3f-152">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-153">13</span><span class="sxs-lookup"><span data-stu-id="97c3f-153">13</span></span>

<span data-ttu-id="97c3f-154">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="97c3f-154">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-155">14</span><span class="sxs-lookup"><span data-stu-id="97c3f-155">14</span></span>

<span data-ttu-id="97c3f-156">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="97c3f-156">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-157">15</span><span class="sxs-lookup"><span data-stu-id="97c3f-157">15</span></span>

<span data-ttu-id="97c3f-158">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="97c3f-158">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-159">16</span><span class="sxs-lookup"><span data-stu-id="97c3f-159">16</span></span>

<span data-ttu-id="97c3f-160">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="97c3f-160">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-161">17</span><span class="sxs-lookup"><span data-stu-id="97c3f-161">17</span></span>

<span data-ttu-id="97c3f-162">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="97c3f-162">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="97c3f-163">21</span><span class="sxs-lookup"><span data-stu-id="97c3f-163">21</span></span>

<span data-ttu-id="97c3f-164">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="97c3f-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97c3f-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97c3f-165">Remarks</span></span>

<span data-ttu-id="97c3f-166">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="97c3f-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="97c3f-167">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="97c3f-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="97c3f-168">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="97c3f-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="97c3f-169">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="97c3f-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c3f-170">Требования</span><span class="sxs-lookup"><span data-stu-id="97c3f-170">Requirements</span></span>



| <span data-ttu-id="97c3f-171">Требование</span><span class="sxs-lookup"><span data-stu-id="97c3f-171">Requirement</span></span> | <span data-ttu-id="97c3f-172">Значение</span><span class="sxs-lookup"><span data-stu-id="97c3f-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c3f-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97c3f-173">Minimum supported client</span></span><br/> | <span data-ttu-id="97c3f-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97c3f-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97c3f-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97c3f-175">Minimum supported server</span></span><br/> | <span data-ttu-id="97c3f-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97c3f-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97c3f-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="97c3f-177">Namespace</span></span><br/>                | <span data-ttu-id="97c3f-178">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="97c3f-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97c3f-179">MOF</span><span class="sxs-lookup"><span data-stu-id="97c3f-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97c3f-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97c3f-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97c3f-181">DLL</span><span class="sxs-lookup"><span data-stu-id="97c3f-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97c3f-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97c3f-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c3f-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97c3f-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c3f-184">\_Каталог CIM</span><span class="sxs-lookup"><span data-stu-id="97c3f-184">CIM\_Directory</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="97c3f-185">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="97c3f-185">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

