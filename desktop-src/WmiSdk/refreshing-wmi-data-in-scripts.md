---
description: В скриптах мониторинга можно избежать последовательных вызовов GetObject с помощью объекта Свбемрефрешер. Объект Свбемрефрешер — это контейнер, который может содержать несколько объектов WMI, данные которых могут быть обновлены в одном вызове.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Обновление данных WMI в скриптах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265373"
---
# <a name="refreshing-wmi-data-in-scripts"></a>Обновление данных WMI в скриптах

В скриптах мониторинга можно избежать последовательных **вызовов GetObject с** помощью объекта [**свбемрефрешер**](swbemrefresher.md) . Объект **свбемрефрешер** — это контейнер, который может содержать несколько объектов WMI, данные которых могут быть обновлены в одном вызове.

Использование объекта [**свбемрефрешер**](swbemrefresher.md) требуется для получения точных данных из классов производительности WMI, таких как [**Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) или другие предустановленные классы, производные от [**\_ производительности Win32**](/windows/desktop/CIMWin32Prov/win32-perf).

В следующей процедуре описывается обновление данных в скриптах.

**Обновление данных в скриптах**

1.  Вызовите функцию **CreateObject** , чтобы создать объект обновления [**свбемрефрешер**](swbemrefresher.md) .

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Подключитесь к пространству имен WMI. Чтобы использовать предварительно установленные классы производительность [**\_ производительности Win32**](/windows/desktop/CIMWin32Prov/win32-perf) , подключитесь к **корневому каталогу \\ CIMV2**.

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Добавьте один объект (вызов [**свбемрефрешер. Add**](swbemrefresher-add.md)) или коллекцию (вызов [**свбемрефрешер. адденум**](swbemrefresher-addenum.md)) в обновитель.

    Используйте предварительно вычисленные классы данных, производные от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), например [**Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) , а не [**Win32 \_ перфравдата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md). В противном случае необходимо вычислить значения для всех свойств, Кроме простых счетчиков.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Обновите данные один раз, чтобы получить исходные данные о производительности.

    Вызовите метод [**свбемрефрешер. Refresh**](swbemrefresher-refresh.md) или универсальный метод [**свбемобжектекс. Refresh \_**](swbemobjectex-refresh-.md) .

    ```VB
    objRefresher.Refresh
    ```

    

5.  При мониторинге производительности и наличии коллекции в объекте обновления пройдите через объекты коллекции.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Очистите элементы из обновления, вызвав [**свбемрефрешер. DeleteAll**](swbemrefresher-deleteall.md) или удалив определенные элементы, вызвав [**Свбемрефрешер. Refresh**](swbemrefresher-remove.md).

В следующем примере кода VBScript показано, как обновить один объект на локальном компьютере. Скрипт создает контейнер обновления и добавляет экземпляр перечислителя для экземпляров [**\_ \_ \_ процесса PerfProc Win32 перфформаттеддата**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) . Вызов [**обновления**](swbemrefresher-refresh.md) выполняется три раза, чтобы продемонстрировать изменения в свойстве **перцентпроцессортиме** для процессов, использующих более одного процента времени процессора.


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



Свойство [**index**](swbemrefreshableitem-index.md) возвращаемого [**свбемрефрешаблеитем**](swbemrefreshableitem.md) представляет индекс объекта в коллекции обновитель. Можно вызвать свойство [**свбемрефрешаблеитем. Иссет**](swbemrefreshableitem-isset.md) , чтобы определить, является ли элемент в обновитель единственным элементом или коллекцией. Для доступа к одному элементу используйте свойство [**свбемрефрешаблеитем. Object**](swbemrefreshableitem-object.md) . Если не выполнить вызов **свбемрефрешаблеитем. Object**, скрипт завершится ошибкой при попытке получить доступ к объекту. Чтобы получить доступ к коллекции, используйте свойство [**свбемрефрешаблеитем. objecting**](swbemrefreshableitem-objectset.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Доступ к данным о производительности в скрипте](accessing-performance-data-in-script.md)
</dt> <dt>

[Задачи WMI: Мониторинг производительности](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Мониторинг данных производительности](monitoring-performance-data.md)
</dt> </dl>

 

 
