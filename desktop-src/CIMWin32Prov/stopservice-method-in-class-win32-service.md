---
description: Помещает службу, представленную \_ объектом службы Win32, в остановленное состояние.
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: Метод «начало» класса Win32_Service (Сдоиас. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c8c055c260f4983622010ced5de652cf673391b7ae02a75b40fd28427a78827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751884"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a>Метод «начало» класса Win32_Service (Сдоиас. h)

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) "неработающий" помещает службу, представленную объектом [**\_ службы Win32**](win32-service.md) , в остановленном состоянии.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 StopService();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Запрос принят.

</dd> <dt>

**1**
</dt> <dd>

Запрос не поддерживается.

</dd> <dt>

**2**
</dt> <dd>

У пользователя нет необходимых прав доступа.

</dd> <dt>

**3**
</dt> <dd>

Службу нельзя остановить, так как от нее зависят другие работающие службы.

</dd> <dt>

**4**
</dt> <dd>

Запрошенный управляющий код недопустим или неприемлем для данной службы.

</dd> <dt>

**5**
</dt> <dd>

Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.

</dd> <dt>

**6**
</dt> <dd>

Служба не запущена.

</dd> <dt>

**7**
</dt> <dd>

Служба не ответила на запрос запуска за отведенное время.

</dd> <dt>

**8**
</dt> <dd>

Неизвестный сбой при запуске службы.

</dd> <dt>

**9**
</dt> <dd>

Не найден путь к каталогу исполняемого файла службы.

</dd> <dt>

**10**
</dt> <dd>

Служба уже запущена.

</dd> <dt>

**11**
</dt> <dd>

База данных для добавления новой службы заблокирована.

</dd> <dt>

**12**
</dt> <dd>

Зависимость, от которой зависит эта служба, удалена из системы.

</dd> <dt>

**13**
</dt> <dd>

Этой службе не удалось найти службу, которая необходима зависимой службе.

</dd> <dt>

**14**
</dt> <dd>

Эта служба была отключена в системе.

</dd> <dt>

**15**
</dt> <dd>

Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.

</dd> <dt>

**16**
</dt> <dd>

Эта служба удаляется из системы.

</dd> <dt>

**17**
</dt> <dd>

Служба не имеет потока выполнения.

</dd> <dt>

**стр**
</dt> <dd>

Служба имеет циклические зависимости при запуске.

</dd> <dt>

**19**
</dt> <dd>

Служба выполняется с тем же именем.

</dd> <dt>

**20**
</dt> <dd>

Имя службы содержит недопустимые символы.

</dd> <dt>

**открыт**
</dt> <dd>

Службе переданы недопустимые параметры.

</dd> <dt>

**22**
</dt> <dd>

Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.

</dd> <dt>

**23**
</dt> <dd>

Служба существует в базе данных доступных в системе служб.

</dd> <dt>

**24**
</dt> <dd>

Служба в данный момент приостановлена в системе.

</dd> </dl>

## <a name="remarks"></a>Remarks

Определив, какие службы могут быть остановлены или приостановлены, можно использовать **методы "** [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) " и "приостановить" для остановки и приостановки служб. Решение о прекращении работы службы, а не приостановке или наоборот, зависит от нескольких факторов, включая следующие:

-   Может ли служба быть приостановлена? В противном случае единственным вариантом будет «останавливает службу».
-   Нужно ли продолжать обработку запросов клиентов для всех, кто уже подключен к службе? Если да, то приостановка службы обычно позволяет ей управлять существующими клиентами при запрете доступа к новым клиентам. Напротив, при прекращении службы все клиенты сразу же отключаются.
-   Нужно ли перенастроить службу, чтобы изменения вступили в силу немедленно? Несмотря на то, что свойства службы могут быть изменены, пока служба приостановлена, большинство из них не вступают в силу, пока служба не будет остановлена и перезапущена.

Код скрипта, необходимый для остановки службы, почти идентичен коду, требуемому для приостановки службы.

При попытке отключить службу, для которой выполняются зависимые службы **, метод «не работает» возвращает** значение 3. Сначала необходимо остановить зависимые службы.

Если служба останавливается, сразу же проверьте [**\_ службу Win32**](win32-service.md).**State** , так как значение по-прежнему может отображать службу как выполняющуюся.

## <a name="examples"></a>Примеры

[Set-ремотесервице](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) Образец PowerShell задает состояние службы для удаленных компьютеров.

При [остановке службы и ее зависимых](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) примеров VBScript останавливается служба и все зависимые службы.

В следующем примере кода VBScript показано, как завершить работу службы.


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



В следующем образце кода Perl показано, как завершить работу службы.


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



В следующем примере кода VBScript показано, что нельзя остановить службу NetDDE до тех пор, пока зависимые службы не будут остановлены. Чтобы запустить сценарий, убедитесь, что служба NetDDE и ее зависимые службы запущены с помощью оснастки MMC Services. msc или команды **net start** .

Класс [**Win32 \_ депендентсервице**](win32-dependentservice.md) позволяет размещать зависимости службы с помощью [соединителей](/windows/desktop/WmiSdk/associators-of-statement) запроса.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| Заголовок<br/>                   | <dl> <dt>Сдоиас. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Служба Win32**](win32-service.md)
</dt> <dt>

[Задачи WMI: службы](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**PauseService**](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 

