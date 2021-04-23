---
description: Записывает обновленную версию дескриптора безопасности, которая управляет доступом к принтеру.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Метод Сетсекуритидескриптор класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1572919d0ac0b5c18a6fc5084636c52b9b3ea1c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262777"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="9426f-103">Метод Сетсекуритидескриптор \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="9426f-103">SetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="9426f-104">Метод **сетсекуритидескриптор** записывает обновленную версию дескриптора безопасности, которая управляет доступом к принтеру.</span><span class="sxs-lookup"><span data-stu-id="9426f-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="9426f-105">Дескриптор безопасности является экземпляром класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="9426f-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="9426f-106">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="9426f-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="9426f-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="9426f-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9426f-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9426f-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9426f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9426f-109">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="9426f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9426f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9426f-111">*Дескриптор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9426f-111">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9426f-112">Дескриптор безопасности, связанный с принтером.</span><span class="sxs-lookup"><span data-stu-id="9426f-112">The security descriptor that is associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9426f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9426f-113">Return value</span></span>

<span data-ttu-id="9426f-114">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="9426f-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="9426f-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9426f-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9426f-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9426f-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9426f-117">**0**</span><span class="sxs-lookup"><span data-stu-id="9426f-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9426f-118">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="9426f-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="9426f-119">**2**</span><span class="sxs-lookup"><span data-stu-id="9426f-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9426f-120">У пользователя нет доступа к запрошенной информации.</span><span class="sxs-lookup"><span data-stu-id="9426f-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9426f-121">**8**</span><span class="sxs-lookup"><span data-stu-id="9426f-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9426f-122">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="9426f-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9426f-123">**9**</span><span class="sxs-lookup"><span data-stu-id="9426f-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9426f-124">У пользователя нет необходимых прав для выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="9426f-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="9426f-125">**открыт**</span><span class="sxs-lookup"><span data-stu-id="9426f-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9426f-126">В вызове метода указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="9426f-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9426f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9426f-127">Remarks</span></span>

<span data-ttu-id="9426f-128">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="9426f-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="9426f-129">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="9426f-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="9426f-130">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="9426f-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="9426f-131">Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="9426f-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="9426f-132">При вызове этого метода можно обновить списки DACL и SACL в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , но можно также обновить только список DACL или только список SACL.</span><span class="sxs-lookup"><span data-stu-id="9426f-132">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you can also update only the DACL or only the SACL.</span></span>

<span data-ttu-id="9426f-133">Следующие значения в [**\_ \_ элементе управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) определяют, обновляются ли списки DACL, SACL или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="9426f-133">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="9426f-134">**\_присутствие DACL \_ SE**</span><span class="sxs-lookup"><span data-stu-id="9426f-134">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="9426f-135">Указывает, что список DACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="9426f-135">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="9426f-136">Если значение не задано, Инструментарий WMI сохраняет исходное значение DACL.</span><span class="sxs-lookup"><span data-stu-id="9426f-136">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="9426f-137">**\_имеется список SACL для SE \_**</span><span class="sxs-lookup"><span data-stu-id="9426f-137">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="9426f-138">Указывает, что список SACL должен быть обновлен.</span><span class="sxs-lookup"><span data-stu-id="9426f-138">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="9426f-139">Если этот параметр не задан, Инструментарий WMI сохраняет исходное значение списка SACL.</span><span class="sxs-lookup"><span data-stu-id="9426f-139">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="9426f-140">Для обновления списка SACL учетная запись должна иметь права **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="9426f-140">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="9426f-141">Для сценариев имя привилегии — **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="9426f-141">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="9426f-142">Дополнительные сведения см. в разделе [**константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="9426f-142">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="9426f-143">Если доверенное лицо группы и свойства доверенного лица владельца не равны **null**, они обновляются.</span><span class="sxs-lookup"><span data-stu-id="9426f-143">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="9426f-144">В противном случае Инструментарий WMI сохраняет исходные значения.</span><span class="sxs-lookup"><span data-stu-id="9426f-144">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="9426f-145">Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="9426f-145">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="9426f-146">Если при вызове этого метода новый список SACL имеет **значение NULL** , то список SACL дескриптора безопасности на целевом защищаемом объекте остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="9426f-146">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="examples"></a><span data-ttu-id="9426f-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="9426f-147">Examples</span></span>

<span data-ttu-id="9426f-148">Образец PowerShell [Copy-Аклтопринтер](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) заменяет разрешения (ACL) с одного принтера на другой.</span><span class="sxs-lookup"><span data-stu-id="9426f-148">The [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell sample Replace the permissions (ACL) from one printer to another.</span></span>

<span data-ttu-id="9426f-149">В следующем образце кода PowerShell описывается, как задать дескриптор безопасности для принтера.</span><span class="sxs-lookup"><span data-stu-id="9426f-149">The following PowerShell code sample describes how to set the security descriptor for a printer.</span></span>


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a><span data-ttu-id="9426f-150">Требования</span><span class="sxs-lookup"><span data-stu-id="9426f-150">Requirements</span></span>



| <span data-ttu-id="9426f-151">Требование</span><span class="sxs-lookup"><span data-stu-id="9426f-151">Requirement</span></span> | <span data-ttu-id="9426f-152">Значение</span><span class="sxs-lookup"><span data-stu-id="9426f-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9426f-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9426f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="9426f-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9426f-154">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="9426f-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9426f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="9426f-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9426f-156">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="9426f-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9426f-157">Namespace</span></span><br/>                | <span data-ttu-id="9426f-158">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9426f-158">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="9426f-159">MOF</span><span class="sxs-lookup"><span data-stu-id="9426f-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9426f-160"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9426f-160"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="9426f-161">DLL</span><span class="sxs-lookup"><span data-stu-id="9426f-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9426f-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9426f-162"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="9426f-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9426f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9426f-164">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="9426f-164">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="9426f-165">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="9426f-165">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="9426f-166">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="9426f-166">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="9426f-167">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="9426f-167">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

