---
description: Возвращает дескриптор безопасности, управляющий доступом к принтеру.
ms.assetid: c12ca35c-07b3-41ad-98c4-48ee584059d1
ms.tgt_platform: multiple
title: Метод Жетсекуритидескриптор класса Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c74d79430d15fa136c6edeb2a6e77e79e76b02ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655789"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="40bc1-103">Метод Жетсекуритидескриптор \_ класса принтера Win32</span><span class="sxs-lookup"><span data-stu-id="40bc1-103">GetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="40bc1-104">Метод **жетсекуритидескриптор** возвращает дескриптор безопасности, управляющий доступом к принтеру.</span><span class="sxs-lookup"><span data-stu-id="40bc1-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="40bc1-105">Дескриптор возвращается в виде экземпляра [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="40bc1-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="40bc1-106">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="40bc1-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="40bc1-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="40bc1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="40bc1-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="40bc1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="40bc1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40bc1-109">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="40bc1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="40bc1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40bc1-111">*Дескриптор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="40bc1-111">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40bc1-112">Дескриптор безопасности, связанный с принтером.</span><span class="sxs-lookup"><span data-stu-id="40bc1-112">The security descriptor associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40bc1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40bc1-113">Return value</span></span>

<span data-ttu-id="40bc1-114">Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="40bc1-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="40bc1-115">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="40bc1-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="40bc1-116">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="40bc1-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="40bc1-117">**0**</span><span class="sxs-lookup"><span data-stu-id="40bc1-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="40bc1-118">Успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="40bc1-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="40bc1-119">**2**</span><span class="sxs-lookup"><span data-stu-id="40bc1-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="40bc1-120">У пользователя нет доступа к запрошенной информации.</span><span class="sxs-lookup"><span data-stu-id="40bc1-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="40bc1-121">**8**</span><span class="sxs-lookup"><span data-stu-id="40bc1-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="40bc1-122">Неизвестный сбой.</span><span class="sxs-lookup"><span data-stu-id="40bc1-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="40bc1-123">**9**</span><span class="sxs-lookup"><span data-stu-id="40bc1-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="40bc1-124">У пользователя нет необходимых прав для выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="40bc1-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="40bc1-125">**открыт**</span><span class="sxs-lookup"><span data-stu-id="40bc1-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="40bc1-126">В вызове метода указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="40bc1-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40bc1-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40bc1-127">Remarks</span></span>

<span data-ttu-id="40bc1-128">Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="40bc1-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="40bc1-129">Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="40bc1-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="40bc1-130">Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL.</span><span class="sxs-lookup"><span data-stu-id="40bc1-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="40bc1-131">Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="40bc1-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="40bc1-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="40bc1-132">Examples</span></span>

<span data-ttu-id="40bc1-133">Следующий пример кода VBScript перечисляет принтеры, подключенные к локальному компьютеру, и получает дескриптор безопасности для каждого принтера.</span><span class="sxs-lookup"><span data-stu-id="40bc1-133">The following VBScript code example lists the printers attached to the local computer and gets the security descriptor for each printer.</span></span> <span data-ttu-id="40bc1-134">Затем извлекаются [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) в [*списке управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL), чтобы определить, какие пользователи имеют доступ к принтеру.</span><span class="sxs-lookup"><span data-stu-id="40bc1-134">Then the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACE) in the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) are extracted to determine which users have access to the printer.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set objWMIService = GetObject("winmgmts:")
Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        arrACEs = objSD.DACL
    For Each objACE in arrACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="requirements"></a><span data-ttu-id="40bc1-135">Требования</span><span class="sxs-lookup"><span data-stu-id="40bc1-135">Requirements</span></span>



| <span data-ttu-id="40bc1-136">Требование</span><span class="sxs-lookup"><span data-stu-id="40bc1-136">Requirement</span></span> | <span data-ttu-id="40bc1-137">Значение</span><span class="sxs-lookup"><span data-stu-id="40bc1-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40bc1-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40bc1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="40bc1-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40bc1-139">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="40bc1-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40bc1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="40bc1-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40bc1-141">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="40bc1-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40bc1-142">Namespace</span></span><br/>                | <span data-ttu-id="40bc1-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="40bc1-143">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="40bc1-144">MOF</span><span class="sxs-lookup"><span data-stu-id="40bc1-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40bc1-145"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40bc1-145"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="40bc1-146">DLL</span><span class="sxs-lookup"><span data-stu-id="40bc1-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40bc1-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40bc1-147"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="40bc1-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40bc1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40bc1-149">**\_Принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="40bc1-149">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="40bc1-150">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="40bc1-150">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="40bc1-151">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="40bc1-151">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="40bc1-152">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="40bc1-152">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

