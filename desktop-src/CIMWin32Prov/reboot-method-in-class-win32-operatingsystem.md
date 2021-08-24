---
description: Перезагрузка&\# 8194; Метод класса WMI завершает работу системы компьютера, а затем перезапускает ее.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Метод reboot класса Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 700d497650e8950c72467bbad8e11cf450b2302f0b68ef762e8a11e3c6aaceee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752734"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Метод reboot \_ класса Win32 операционной системы

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) reboot закрывает компьютерную систему, а затем перезапускает его.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль (0), чтобы указать на успешное выполнение. Любое другое значение указывает на ошибку. Коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Другие** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarks

Возможность программной перезагрузки компьютера позволяет администраторам удаленно выполнять многие задачи управления компьютером.

Например, при создании сценария для установки программного обеспечения или при изменении конфигурации, требующей перезагрузки компьютера, можно включить в сценарий команду перезапуска и выполнить всю операцию удаленно. Метод **reboot** можно использовать для перезагрузки компьютера. Как и метод [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , методу **reboot** требуется пользователь, чьи учетные данные безопасности используются сценарием для предоставления прав на завершение работы.

## <a name="examples"></a>Примеры

В следующем примере кода VBScript вызывается метод reboot класса операционной системы [**Win32 \_**](win32-operatingsystem.md) .

> [!Note]  
> Для успешного вызова метода Shutdown необходимо иметь права на завершение работы.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Следующий код Perl вызывает метод reboot класса [**Win32 \_ операционной**](win32-operatingsystem.md) системы.

> [!Note]  
> Для успешного вызова метода Shutdown необходимо иметь права на завершение работы.

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



Следующий сценарий VBScript вызывает метод reboot класса [**Win32 \_ операционной**](win32-operatingsystem.md) системы в удаленной системе. В поле \_ имя удаленной системы введите \_ имя удаленной системы для перезагрузки.

> [!Note]  
> Для успешного вызова метода reboot необходимо иметь привилегию Ремотешутдовн

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Следующий вызов Perl вызывает метод перезагрузки класса операционной системы [**Win32 \_**](win32-operatingsystem.md) в удаленной системе. В поле \_ имя удаленной системы введите \_ имя удаленной системы для перезагрузки.

> [!Note]  
> Для успешного вызова метода reboot необходимо иметь привилегию Ремотешутдовн.

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32, \_ Операционная система**](win32-operatingsystem.md)
</dt> <dt>

[**\_Метод операционной системы для CIM. Shutdown**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[Задачи WMI: управление рабочим столом](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

