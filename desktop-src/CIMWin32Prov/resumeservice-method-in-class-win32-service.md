---
description: Пытается поместить службу, на которую указывает ссылка, в состоянии возобновления.
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Метод ResumeService класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ed4141b02d6e08bd4b106d2c1f72ce3fe0620fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896438"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Метод ResumeService класса Win32_Service (поставщики WMI CIMWin32)

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ResumeService пытается поместить службу, на которую указывает ссылка, в состоянии возобновления.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ResumeService();
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

**стр**
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

## <a name="remarks"></a>Комментарии

Хотя может показаться, что непрактичное различие между остановленной службой и приостановленной службой, два состояния по-разному отображаются в SCM. Остановленная служба — это служба, которая не запущена и должна проходить всю процедуру запуска службы. Однако Приостановленная служба все еще работает, но ее работа приостановлена. По этой причине Приостановленная служба не обязана проходить всю процедуру запуска службы, но для ее возобновления требуется другая процедура.

Необходимо использовать правильный метод для запуска остановленной службы или возобновления работы приостановленной службы. Методы [**\_ службы Win32**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) и **ResumeService** следует использовать в следующих ситуациях:

-   Если служба в данный момент остановлена, для ее перезапуска необходимо использовать метод [**StartService**](startservice-method-in-class-win32-service.md) . **ResumeService** не может запустить службу, которая в данный момент остановлена.
-   Если служба приостановлена, необходимо использовать **ResumeService**. При использовании метода [**StartService**](startservice-method-in-class-win32-service.md) в приостановленной службе появляется сообщение "служба уже запущена". Однако служба остается приостановленной до тех пор, пока в нее не будет отправлен код управления службой возобновления.

## <a name="examples"></a>Примеры

В [службах возобновления работы, приостановленных](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) с помощью VBScript, перезапускаются все приостановленные службы автозапуска.

Следующий пример кода VBScript описывает, как возобновить приостановленную службу из экземпляров [**\_ службы Win32**](win32-service.md).

> [!Note]  
> Служба должна поддерживать приостановку и выполнение уже запущено.

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



В следующем образце кода Perl описывается, как возобновить приостановленную службу из экземпляров [**\_ службы Win32**](win32-service.md).

> [!Note]  
> Служба должна поддерживать приостановку и выполнение уже запущено.

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
    }
   }
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Служба Win32**](win32-service.md)
</dt> <dt>

[Задачи WMI: службы](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

