---
description: Завершение работы&\# 8194; Метод класса WMI выгружает программы и библиотеки DLL до отключения компьютера.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Метод Shutdown класса Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 068551ee013634bde9a42584764c36f255bf322bedb97e6ebb3a5075c113e742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800844"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Метод Shutdown \_ класса операционной системы Win32

Метод класса **Shutdown** [инструментария WMI](/windows/desktop/WmiSdk/retrieving-a-class) выгружает программы и библиотеки DLL, пока не будет отключено отключение компьютера.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Shutdown();
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

Иногда требуется удалить компьютеры из сети, например для запланированного обслуживания, так как компьютер работает неправильно или не может завершить процесс настройки. Например, если сервер DHCP передает ошибочные IP-адреса, может потребоваться завершить работу компьютера до тех пор, пока не будет подготовлен специалист по обслуживанию для решения проблемы. Если вы подозреваете, что произошло нарушение безопасности, может потребоваться завершить работу некоторых серверов, чтобы убедиться в отсутствии доступа к ним, пока проблема безопасности не будет устранена. Некоторые операции настройки (например, изменение имени компьютера) потребовали перезагрузки компьютера, прежде чем изменение вступит в силу.

Этот метод немедленно завершает работу компьютера, если это возможно. Система останавливает все запущенные процессы, сбрасывает все буферы файлов на диск, а затем выключает систему. вызывающий процесс должен иметь привилегию **SE \_ SHUTDOWN \_ NAME** , как описано в следующем примере.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Дополнительные сведения об установке привилегий см. в статьях [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations) и [выполнение привилегированных операций с помощью VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript). Дополнительные параметры завершения работы, такие как выход из системы или принудительное завершение работы, см. в описании метода [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .

## <a name="examples"></a>Примеры

Следующий код VBScript закрывает локальный компьютер.

> [!Note]  
> Для успешного вызова метода Shutdown необходимо иметь права на завершение работы.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



Следующий код Perl закрывает локальный компьютер.

> [!Note]  
> Для успешного вызова метода Shutdown необходимо иметь права на завершение работы.

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



Следующий код VBScript закрывает указанный удаленный компьютер. В поле *\_ \_ имя удаленной системы* введите имя удаленной системы для завершения работы.

> [!Note]  
> Для успешного вызова метода **Shutdown** необходимо иметь привилегию ремотешутдовн.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32, \_ Операционная система**](win32-operatingsystem.md)
</dt> <dt>

[Задачи WMI: управление рабочим столом](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Выполнение привилегированных операций с помощью VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

