---
description: Объект скриптов SWbemObject — это универсальный объект WMI, определяющий свойства и методы, которые могут использоваться независимо от конкретного объекта WMI, к которому привязан объект SWbemObject.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Создание сценариев с помощью SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d6ba0cccca8fcd62af490aa91ab1cc965fdad4d3682d99a8fda52151135500ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739700"
---
# <a name="scripting-with-swbemobject"></a>Создание сценариев с помощью SWbemObject

Объект скриптов [**SWbemObject**](swbemobject.md) — это универсальный объект WMI, определяющий свойства и методы, которые могут использоваться независимо от конкретного объекта WMI, к которому привязан объект **SWbemObject** . Все объекты WMI, такие как экземпляр [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) или любого другого класса данных WMI, представлены [**SWbemObject**](swbemobject.md) и могут использовать общие свойства и методы **SWbemObject** в дополнение к их собственным свойствам и методам.

Например, используйте следующий скрипт, чтобы получить все экземпляры [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , вызвав метод [**SWbemObject \_ . Instances**](swbemobject-instances-.md) . Клсобжпроцесс представляет как определение класса **\_ процесса Win32** , так и [**SWbemObject**](swbemobject.md).


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



В следующем примере получается экземпляр [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) , который представляет службу оповещений, и сохраняет ее в обжалертер. Затем можно вызвать либо методы [**SWbemObject**](swbemobject.md) , такие как WScript. Echo Обжалертер. Path \_ , либо методы, определенные классом данных, такие как WScript. Echo обжалертер. State. Обжалертер, который представляет экземпляр \_ службы Win32 и **SWbemObject**.


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



Вызов [**SWbemObject. Instances \_**](swbemobject-instances-.md) получает другой универсальный объект скрипта WMI, [**SWbemObjectSet**](swbemobjectset.md). Как показано на рисунке, объект **SWbemObjectSet** можно рассматривать как [коллекцию](accessing-a-collection.md).


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



Вы можете найти методы [**SWbemObject**](swbemobject.md) , так как они заканчиваются символом подчеркивания ( \_ ), например [**SWbemObject. Instances \_**](swbemobject-instances-.md).

[**Свбемобжектекс**](swbemobjectex.md) расширяет свойства [**SWbemObject**](swbemobject.md). Например, теперь можно обновить данные любого объекта WMI, например экземпляра [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process), путем вызова [**\_ свбемобжектекс. Refresh**](swbemobjectex-refresh-.md).

В следующем примере показано, как данные об ошибках на странице системных процессов можно обновлять каждые пять секунд.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



Дополнительные сведения об обновлении данных с помощью объекта [**свбемрефрешер**](swbemrefresher.md) см. [в разделе Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md).

[**SWbemObject. \_**](swbemobject-put-.md) Write и [**путасинк \_**](swbemobject-putasync-.md) позволяют записывать изменения обратно в любой объект WMI. Эти методы фиксируют изменения только в объекте в пространстве имен, в котором был создан объект. Объект можно записать в другое пространство имен с помощью [**свбемсервицесекс.**](swbemservicesex-put.md) WHERE или [**свбемсервицесекс. путасинк**](swbemservicesex-putasync.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[API сценариев для инструментария WMI](scripting-api-for-wmi.md)
</dt> <dt>

[Создание скрипта WMI](creating-a-wmi-script.md)
</dt> <dt>

[Обновление всего экземпляра](updating-an-entire-instance.md)
</dt> <dt>

[Вызов метода](calling-a-method.md)
</dt> </dl>

 

 
