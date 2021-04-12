---
description: Формат строки моникера аналогичен стандартному пути к объекту WMI. Дополнительные сведения см. в разделе Требования к пути к объектам WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Создание строки моникера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344935"
---
# <a name="constructing-a-moniker-string"></a>Создание строки моникера

Формат строки моникера аналогичен стандартному пути к объекту WMI. Дополнительные сведения см. в разделе [требования к пути к объектам WMI](wmi-object-path-requirements.md).

Моникер состоит из следующих частей:

-   Префикс Винмгмтс: (обязательный). Префикс инструктирует сервер сценариев Windows (WSH), что следующий код будет использовать [объекты API скрипта](scripting-api-objects.md).
-   Компонент параметров безопасности (необязательно)
-   Компонент пути объекта WMI (необязательно)

В строке моникера WMI нельзя указать пароль. Если необходимо изменить пароль (параметр *стрпассворд* ) или тип проверки подлинности (параметр *страусорити* ) при подключении к WMI, вызовите [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md). Имейте в виду, что в подключениях к удаленным компьютерам можно указать только пароль и полномочия. Попытка задать эти значения в скрипте, который выполняется на локальном компьютере, приведет к ошибке. Дополнительные сведения о том, когда используются параметры безопасности и компоненты пути к объекту, см. в разделе [Параметры безопасности WMI](/previous-versions/tn-archive/ee156574(v=technet.10)).

В следующем моникере указывается объект [**SwbemServices**](swbemservices.md) , представляющий корневой элемент пространства имен \\ по умолчанию с включенным параметром олицетворения и привилегией вбемпривилежедебуг (SeDebugPrivilege), а также разрешение вбемпривилежесекурити (SeSecurityPrivilege).


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> Все строковые литералы не учитывают регистр.
>
> Префикс "!" в привилегии означает, что привилегия должна быть отключена; упущение этого префикса означает, что права доступа должны быть включены.
>
> Префикс "!" используется для имени компьютера или пространства имен, если параметры безопасности указаны в квадратных скобках перед именем компьютера или пространством имен.

 

При указании пути к объекту разрешены следующие назначения по умолчанию:

-   Имя компьютера может быть опущено в пути к объекту, в этом случае предполагается имя локального компьютера.
-   Пространство имен можно опустить из пути объекта. в этом случае предполагается использование пространства имен по умолчанию.

    Это определяется по значению раздела реестра **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Скрипт** \\ **по умолчанию**, значение по умолчанию — root \\ CIMv2.

-   Можно также указать класс или экземпляр, в этом случае возвращаемый объект является WMI-объектом, а не объектом служб.

> [!Note]  
> Если указан класс или экземпляр, пространство имен нельзя опустить при указании имени компьютера.

 

Ссылки на константы прав доступа, используемые в строке моникера WMI, см. в разделе [константы прав](privilege-constants.md)и дескрипторы "краткое имя скрипта".

## <a name="valid-moniker-strings"></a>Допустимые строки моникера

В следующих примерах показаны допустимые строки моникера.

Следующий моникер определяет пространство имен по умолчанию на локальном компьютере. Возвращается объект [**SwbemServices**](swbemservices.md) .


```VB
WinMgmts:
```



Следующий моникер определяет пространство имен по умолчанию на компьютере myServer. Возвращается объект [**SwbemServices**](swbemservices.md) .


```VB
"WinMgmts://myServer"
```



Следующий моникер определяет корневое \\ пространство имен CIMV2 на компьютере MyServer. Возвращается объект [**SwbemServices**](swbemservices.md) .


```VB
"WinMgmts://myServer/root/cimv2"
```



Следующий моникер определяет корневое \\ пространство имен CIMV2 на локальном сервере. Возвращается объект [**SwbemServices**](swbemservices.md) .


```VB
"WinMgmts:root/cimv2"
```



Следующий моникер определяет класс [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в корневом \\ пространстве имен CIMV2 на сервере MyServer. Возвращается объект [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



Следующий моникер определяет класс [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в корневом \\ пространстве имен CIMV2 на локальном сервере. Возвращается объект [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



Следующий моникер определяет класс [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в пространстве имен по умолчанию на локальном сервере. Возвращается объект [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



Следующий моникер определяет экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , соответствующий диску C: в пространстве имен сценариев по умолчанию на локальном сервере. Возвращается объект [**SWbemObject**](swbemobject.md) . Пространство имен по умолчанию для сценариев определяется параметром конфигурации пространства имен по умолчанию, как указано в элементе управления WMI. Дополнительные сведения см. [в разделе Настройка безопасности пространства имен с помощью элемента управления WMI](setting-namespace-security-with-the-wmi-control.md).


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



Следующий моникер определяет экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , соответствующий диску C: в корневом \\ пространстве имен CIMV2 на сервере MyServer. Возвращается объект [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



Следующий моникер определяет экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , соответствующий диску C: в корневом \\ пространстве имен CIMV2 на локальном сервере. Возвращается объект [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



Следующий моникер определяет экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , соответствующий диску C: в пространстве имен по умолчанию на локальном сервере. Возвращается объект [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



Следующий моникер задает уровень олицетворения для олицетворения и устанавливает \_ право доступа для отладки SE.


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



Следующий моникер задает уровень олицетворения для олицетворения и устанавливает \_ право доступа для отладки SE. Он также отменяет \_ право на завершение работы SE.


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



Следующий моникер извлекает локализованные описания для класса **MyClass** на английском языке из корневого \\ пространства имен WMI.


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



Следующий моникер запрашивает проверку подлинности Kerberos с помощью основного \\ сервера mydomain.


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



Следующий моникер запрашивает проверку подлинности NTLM с помощью домена mydomain.


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



В следующем примере кода VBScript показано, как объединить параметры безопасности и языкового стандарта в моникере.


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Хотя моникеры предоставляют более прямой доступ к объектам, в некоторых обстоятельствах многократное использование моникеров может оказаться менее эффективным, чем эквивалентный код, который явно подключается к инструментарию WMI. Если необходимо учитывать производительность приложения, попробуйте использовать альтернативные механизмы.
>
> Функцию **GetObject** , предоставляемую сценарием VBScript, нельзя использовать для обновления или установки данных при выполнении скриптов, внедренных в HTML-страницу, так как Microsoft Internet Explorer запрещает использование этого вызова в целях безопасности.

 

 

 
