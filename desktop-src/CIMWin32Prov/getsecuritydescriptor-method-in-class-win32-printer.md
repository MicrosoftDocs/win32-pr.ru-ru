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
ms.openlocfilehash: 4ea96e021972855b75d04c3c9e5a9294d241f524bb27f31e0b42093815a5bf2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918354"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a>Метод Жетсекуритидескриптор \_ класса принтера Win32

Метод **жетсекуритидескриптор** возвращает дескриптор безопасности, управляющий доступом к принтеру. Дескриптор возвращается в виде экземпляра [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дескриптор* \[ заполняет\]
</dt> <dd>

Дескриптор безопасности, связанный с принтером.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Успешное завершение.

</dd> <dt>

**2**
</dt> <dd>

У пользователя нет доступа к запрошенной информации.

</dd> <dt>

**8**
</dt> <dd>

Неизвестный сбой.

</dd> <dt>

**9**
</dt> <dd>

У пользователя нет необходимых прав для выполнения метода.

</dd> <dt>

**открыт**
</dt> <dd>

В вызове метода указан недопустимый параметр.

</dd> </dl>

## <a name="remarks"></a>Remarks

Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL). Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).

Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL. Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Примеры

Следующий пример кода VBScript перечисляет принтеры, подключенные к локальному компьютеру, и получает дескриптор безопасности для каждого принтера. Затем извлекаются [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) в [*списке управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL), чтобы определить, какие пользователи имеют доступ к принтеру.


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Принтер Win32**](win32-printer.md)
</dt> <dt>

[**Константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Изменение параметров безопасности доступа для защищаемых объектов](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

