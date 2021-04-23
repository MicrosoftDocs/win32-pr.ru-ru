---
description: Изменяет разрешения безопасности для файла логических данных, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538999"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a><span data-ttu-id="b6909-103">Метод Чанжесекуритипермиссионсекс \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="b6909-103">ChangeSecurityPermissionsEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="b6909-104">Метод **чанжесекуритипермиссионсекс** изменяет разрешения безопасности для логического файла данных, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-cim-datafile.md) ).</span><span class="sxs-lookup"><span data-stu-id="b6909-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical data file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) method).</span></span> <span data-ttu-id="b6909-105">Если логический файл фактически является каталогом, этот метод будет работать рекурсивно, изменяя разрешения безопасности для всех файлов и подкаталогов, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="b6909-105">If the logical file is actually a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6909-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b6909-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b6909-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b6909-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b6909-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="b6909-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b6909-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b6909-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6909-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6909-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="b6909-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6909-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6909-112">*SecurityDescriptor* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6909-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6909-113">Указывает сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="b6909-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="b6909-114">Список ACL **со значением NULL** в структуре [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="b6909-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="b6909-115">Дополнительные сведения о влиянии неограниченного доступа см. в разделе [Создание дескриптора безопасности для нового объекта](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="b6909-115">For more information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="b6909-116">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6909-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6909-117">Права безопасности для изменения.</span><span class="sxs-lookup"><span data-stu-id="b6909-117">Security privilege to modify.</span></span> <span data-ttu-id="b6909-118">Например, чтобы изменить безопасность владельца и DACL, используйте:</span><span class="sxs-lookup"><span data-stu-id="b6909-118">For example, to change the owner and DACL security, use:</span></span>

<span data-ttu-id="b6909-119">`Option = 1 + 4` или `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span><span class="sxs-lookup"><span data-stu-id="b6909-119">`Option = 1 + 4` or `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span></span>

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="b6909-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)</span><span class="sxs-lookup"><span data-stu-id="b6909-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b6909-121">Изменение владельца логического файла.</span><span class="sxs-lookup"><span data-stu-id="b6909-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="b6909-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)</span><span class="sxs-lookup"><span data-stu-id="b6909-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b6909-123">Измените группу логического файла.</span><span class="sxs-lookup"><span data-stu-id="b6909-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="b6909-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="b6909-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b6909-125">Измените список управления доступом для логического файла.</span><span class="sxs-lookup"><span data-stu-id="b6909-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="b6909-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="b6909-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b6909-127">Изменение ACL системы для логического файла.</span><span class="sxs-lookup"><span data-stu-id="b6909-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b6909-128">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b6909-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6909-129">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="b6909-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="b6909-130">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="b6909-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-131">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b6909-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b6909-132">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b6909-132">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="b6909-133">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b6909-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="b6909-134">Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="b6909-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="b6909-135">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="b6909-135">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-136">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b6909-136">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b6909-137">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**\_ файла данных CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="b6909-137">If **True**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="b6909-138">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b6909-138">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6909-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6909-139">Return value</span></span>

<span data-ttu-id="b6909-140">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="b6909-140">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="b6909-141">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b6909-141">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b6909-142">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b6909-142">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b6909-143">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="b6909-143">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-144">0</span><span class="sxs-lookup"><span data-stu-id="b6909-144">0</span></span>

<span data-ttu-id="b6909-145">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b6909-145">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-146">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="b6909-146">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-147">2</span><span class="sxs-lookup"><span data-stu-id="b6909-147">2</span></span>

<span data-ttu-id="b6909-148">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b6909-148">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-149">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="b6909-149">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-150">8</span><span class="sxs-lookup"><span data-stu-id="b6909-150">8</span></span>

<span data-ttu-id="b6909-151">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="b6909-151">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-152">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="b6909-152">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-153">9</span><span class="sxs-lookup"><span data-stu-id="b6909-153">9</span></span>

<span data-ttu-id="b6909-154">Указано недопустимое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="b6909-154">Object name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-155">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="b6909-155">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-156">10</span><span class="sxs-lookup"><span data-stu-id="b6909-156">10</span></span>

<span data-ttu-id="b6909-157">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="b6909-157">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-158">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="b6909-158">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-159">11</span><span class="sxs-lookup"><span data-stu-id="b6909-159">11</span></span>

<span data-ttu-id="b6909-160">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="b6909-160">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-161">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="b6909-161">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-162">12</span><span class="sxs-lookup"><span data-stu-id="b6909-162">12</span></span>

<span data-ttu-id="b6909-163">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="b6909-163">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-164">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="b6909-164">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-165">13</span><span class="sxs-lookup"><span data-stu-id="b6909-165">13</span></span>

<span data-ttu-id="b6909-166">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="b6909-166">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-167">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="b6909-167">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-168">14</span><span class="sxs-lookup"><span data-stu-id="b6909-168">14</span></span>

<span data-ttu-id="b6909-169">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="b6909-169">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-170">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="b6909-170">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-171">15</span><span class="sxs-lookup"><span data-stu-id="b6909-171">15</span></span>

<span data-ttu-id="b6909-172">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b6909-172">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-173">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="b6909-173">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-174">16</span><span class="sxs-lookup"><span data-stu-id="b6909-174">16</span></span>

<span data-ttu-id="b6909-175">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="b6909-175">The start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-176">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="b6909-176">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-177">17</span><span class="sxs-lookup"><span data-stu-id="b6909-177">17</span></span>

<span data-ttu-id="b6909-178">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="b6909-178">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="b6909-179">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="b6909-179">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b6909-180">21</span><span class="sxs-lookup"><span data-stu-id="b6909-180">21</span></span>

<span data-ttu-id="b6909-181">Недействительный параметр.</span><span class="sxs-lookup"><span data-stu-id="b6909-181">A parameter is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6909-182">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6909-182">Remarks</span></span>

<span data-ttu-id="b6909-183">Метод **чанжесекуритипермиссионсекс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b6909-183">The **ChangeSecurityPermissionsEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="b6909-184">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b6909-184">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b6909-185">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b6909-185">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6909-186">Требования</span><span class="sxs-lookup"><span data-stu-id="b6909-186">Requirements</span></span>



| <span data-ttu-id="b6909-187">Требование</span><span class="sxs-lookup"><span data-stu-id="b6909-187">Requirement</span></span> | <span data-ttu-id="b6909-188">Значение</span><span class="sxs-lookup"><span data-stu-id="b6909-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6909-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6909-189">Minimum supported client</span></span><br/> | <span data-ttu-id="b6909-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6909-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6909-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6909-191">Minimum supported server</span></span><br/> | <span data-ttu-id="b6909-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6909-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6909-193">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6909-193">Namespace</span></span><br/>                | <span data-ttu-id="b6909-194">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b6909-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6909-195">MOF</span><span class="sxs-lookup"><span data-stu-id="b6909-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6909-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6909-196"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6909-197">DLL</span><span class="sxs-lookup"><span data-stu-id="b6909-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6909-198"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6909-198"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6909-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6909-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6909-200">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="b6909-200">**CIM\_DataFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b6909-201">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="b6909-201">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b6909-202">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="b6909-202">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="b6909-203">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="b6909-203">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

