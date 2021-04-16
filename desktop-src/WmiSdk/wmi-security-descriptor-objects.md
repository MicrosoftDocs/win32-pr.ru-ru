---
description: Инструментарий WMI содержит объекты и методы, позволяющие считывать дескрипторы безопасности и управлять ими, чтобы определить, кто имеет доступ к защищаемым объектам.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Объекты дескрипторов безопасности WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568000"
---
# <a name="wmi-security-descriptor-objects"></a>Объекты дескрипторов безопасности WMI

Инструментарий WMI содержит объекты и методы, позволяющие считывать дескрипторы безопасности и управлять ими, чтобы определить, кто имеет доступ к защищаемым объектам.

-   [Роль дескрипторов безопасности](#the-role-of-security-descriptors)
-   [Управление доступом и объекты безопасности WMI](#access-control-and-wmi-security-objects)
-   [\_Объект Win32 SecurityDescriptor](/windows)
-   [Списки DACL и SACL](#dacl-and-sacl)
-   [\_ACE Win32, \_ доверенное лицо Win32, \_ идентификатор безопасности Win32](/windows)
-   [Пример: Проверка доступа к принтерам](#example-checking-who-has-access-to-printers)
-   [См. также](#related-topics)

## <a name="the-role-of-security-descriptors"></a>Роль дескрипторов безопасности

Дескрипторы безопасности определяют атрибуты безопасности защищаемых объектов, таких как файлы, разделы реестра, пространства имен WMI, принтеры, службы или общие ресурсы. Дескриптор безопасности содержит сведения о владельце и основной группе объекта. Поставщик может сравнить дескриптор безопасности ресурса с удостоверением запрашивающего пользователя и определить, имеет ли пользователь право на доступ к ресурсу, запрашиваемому пользователем. Дополнительные сведения см. [в разделе доступ к защищаемым ОБЪЕКТАМ WMI](access-to-wmi-securable-objects.md).

Некоторые методы WMI, например [**Получение**](--systemsecurity-getsd.md), возвращают дескриптор безопасности в двоичном формате байтового массива. Начиная с Windows Vista, используйте методы класса [**Win32 \_ секуритидескрипторхелпер**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) для преобразования двоичного дескриптора безопасности в экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), который можно легко манипулировать. Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).

## <a name="access-control-and-wmi-security-objects"></a>Управление доступом и объекты безопасности WMI

Ниже приведен список объектов безопасности WMI.

-   [**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [**\_Доверенное лицо Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [**\_Идентификатор безопасности Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

На следующей схеме показаны связи между объектами безопасности WMI.

![отношения между объектами безопасности WMI](images/security-descriptor.png)

Дополнительные сведения о роли безопасности доступа см. в разделе [рекомендации по обеспечению безопасности](/windows/desktop/SecBP/best-practices-for-the-security-apis), [обеспечению безопасности WMI](maintaining-wmi-security.md)и [контролю доступа](/windows/desktop/SecAuthZ/access-control).

## <a name="win32_securitydescriptor-object"></a>\_Объект Win32 SecurityDescriptor

В следующей таблице перечислены свойства класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .



| Свойство         | Описание                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **контролфлагс** | Набор контрольных битов, соответствующих значению SD или его отдельным элементам. Дополнительные сведения о задании значений битов **контролфлагс** см. в разделе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).<br/>                                                                                                                                                                      |
| **КОНТРОЛЯ**         | [Избирательный список управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) для пользователей и групп, а также права доступа к защищенному объекту. Это свойство содержит массив экземпляров [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , которые представляют [записи управления доступом](/windows/desktop/SecAuthZ/access-control-entries). Дополнительные сведения см. [в разделе Создание списка DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).<br/> |
| **Группа**        | Группа, к которой принадлежит этот защищенный объект. Это свойство содержит экземпляр [**\_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , который содержит имя, домен и идентификатор безопасности (SID) группы, которой принадлежит владелец.<br/>                                                                                                                                                             |
| **Владелец**        | Владелец защищенного объекта. Это свойство содержит экземпляр [ \_ доверенного лица Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , который содержит имя, домен и идентификатор безопасности (SID) владельца.<br/>                                                                                                                                                                                                          |
| **СИСТЕМНЫЙ**         | [Системный список управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) содержит массив экземпляров [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , которые представляют тип попыток доступа, создающих записи аудита для пользователей или групп. Дополнительные сведения см. [в разделе SACL для нового объекта](/windows/desktop/SecAuthZ/sacl-for-a-new-object).<br/>                                                                        |



 

## <a name="dacl-and-sacl"></a>Списки DACL и SACL

Массивы объектов [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) в списке управления доступом на уровне пользователей (DACL) и системном списке управления доступом (SACL) создают связь между пользователем или группой и их правами доступа.

Если свойство DACL не содержит записи управления доступом (ACE), права доступа не предоставляются и доступ к объекту будет запрещен.

> [!Note]  
> **Пустой** список DACL предоставляет полный доступ всем, что является серьезной угрозой безопасности. Дополнительные сведения см. [в разделе Создание списка DACL](/windows/desktop/SecBP/creating-a-dacl).

 

## <a name="win32_ace-win32_trustee-win32_sid"></a>\_ACE Win32, \_ доверенное лицо Win32, \_ идентификатор безопасности Win32

Объект [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) содержит экземпляр класса [**\_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , который определяет пользователя или группу, и свойство **AccessMask** , которое является битовой маской, указывающей действия, которые может выполнять пользователь или группа. Например, пользователю или группе может быть предоставлено право на чтение файла, но не на запись в файл. Объект **\_ ACE Win32** также содержит запись ACE, которая указывает, является ли это разрешение или запретом доступа.

> [!Note]  
> Порядок элементов [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) в списке DACL важен, так как в списке DACL разрешены и запрещены запись контроля доступа (ACE). Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Каждая учетная запись пользователя или группа, представленная [**\_ доверенным лицом Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , имеет идентификатор безопасности (SID), однозначно определяющий учетную запись, и указывает привилегии доступа учетной записи. Определение данных SID зависит от операционной системы. Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).

На следующей диаграмме показано содержимое одного экземпляра [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

![содержимое одного \- экземпляра ACE Win32](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a>Пример: Проверка доступа к принтерам

В следующем примере кода VBScript показано, как использовать дескриптор безопасности принтера. Скрипт вызывает метод [**жетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) в классе [**\_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) для получения дескриптора, а затем определяет, присутствует ли в дескрипторе безопасности список управления доступом на уровне пользователей (DACL). При наличии списка DACL сценарий получает список записей управления доступом (ACE) из списка DACL. Каждый элемент ACE представлен экземпляром [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Сценарий проверяет каждый ACE, чтобы получить имя пользователя и определить, имеет ли пользователь доступ к принтеру. Пользователь представлен в экземпляре [**\_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , внедренного в экземпляр **\_ ACE Win32** .


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

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
        colACEs = objSD.DACL
    For Each objACE in colACEs
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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md)
</dt> <dt>

[Вспомогательный класс дескриптора безопасности](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Рекомендации по обеспечению безопасности](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> <dt>

[Управление доступом](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Доступ к пространствам имен WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

