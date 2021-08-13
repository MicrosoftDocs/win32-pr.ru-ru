---
description: Для получения уведомлений от поставщика системного реестра приложение управления должно быть зарегистрировано как временный потребитель событий.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Регистрация для событий системного реестра
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c6f60b21dee729a879aaeab676da67b06ca0a822bcfd6509bc0f406f96fecec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554249"
---
# <a name="registering-for-system-registry-events"></a>Регистрация для событий системного реестра

Для получения уведомлений от поставщика [системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) приложение управления должно быть зарегистрировано как временный потребитель событий. Большинство требований, регистрируемых для поставщика системного реестра, те же, что и при любой регистрации событий, но также необходимо выполнить следующую процедуру.

Поставщик реестра предоставляет классы событий для событий в системном реестре. Дополнительные сведения о регистрации общих событий см. [в разделе Получение WMI-события](receiving-a-wmi-event.md).

В следующей процедуре описывается регистрация для событий системного реестра.

**Регистрация для событий системного реестра**

1.  Вызов метода запроса уведомления.

    В любом скрипте или C++ используйте запрос уведомления, например [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md) или [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Создайте строку запроса для параметра *Бстркуери* **IWbemServices:: ExecNotificationQueryAsync** или *стркуери* в скрипте.

2.  Определите тип события, которое требуется получить, и создайте запрос.

    В следующей таблице перечислены классы событий реестра, которые можно использовать.

    

    | Класс событий                                                      | Расположение Hive        | Описание                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**регистревент**](/previous-versions/windows/desktop/regprov/registryevent)                       | Н/Д<br/>       | Абстрактный базовый класс для изменений в реестре.<br/> |
    | [**регистритричанжеевент**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Отслеживает изменения в иерархии ключей.<br/>         |
    | [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | Путь<br/>   | Отслеживает изменения в одном ключе.<br/>                |
    | [**События registryvaluechangeevent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Отслеживает изменения в одном значении.<br/>              |

    

     

    Эти классы имеют свойство **Hive** , которое определяет иерархию ключей для отслеживания изменений, таких как **hKey \_ локальный \_ компьютер**.

    Изменения в **\_ классах hKey \_ root** и **hKey \_ текущего \_ пользователя** Hive не поддерживаются [**регистревент**](/previous-versions/windows/desktop/regprov/registryevent) или производными от него классами, например [**регистритричанжеевент**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).

3.  Создайте предложение WHERE для регистрации событий.

    Поставщик системного реестра имеет определенные правила для предложений WHERE. Дополнительные сведения см. в разделе [Создание правильного предложения WHERE для поставщика реестра](creating-a-proper-where-clause-for-the-registry-provider.md). Дополнительные общие сведения о создании предложения WHERE см. в разделе [запросы с помощью WQL](querying-with-wql.md).

4.  Определите, получает ли потребитель события.

    Поставщик системного реестра не гарантирует, что все отправленные события будут доставлены. Дополнительные сведения см. в разделе [получение событий реестра](receiving-registry-events.md).

В следующем примере кода VBScript показано, как определить изменение реестра в **\_ \_** \\  \\ кусте **Microsoft** Hive или поддереве в разделе "программное обеспечение на локальном компьютере". Это скрипт мониторинга, который в демонстрационных целях выполняется в процессе с именем Wscript.exe до тех пор, пока он не будет завершен в **диспетчере задач**, Инструментарий WMI остановлен или операционная система перезагружается. Скрипт использует вызов [*семисинчронаус*](gloss-s.md) для [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md). Дополнительные сведения о вызовах семисинчронаус см. в разделе [выполнение вызова семисинчронаус с помощью VBScript](making-a-semisynchronous-call-with-vbscript.md).


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



В следующем примере кода VBScript показано, как отслеживать изменение значений ключа путем регистрации для события поставщика реестра типа [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Скрипт вызывает асинхронный метод [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md). Дополнительные сведения об асинхронных вызовах и безопасности см. [в разделе выполнение асинхронного вызова с помощью VBScript](making-an-asynchronous-call-with-vbscript.md).

Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен. Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс. Чтобы остановить его программно, используйте метод [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) в \_ классе процесса Win32.


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

