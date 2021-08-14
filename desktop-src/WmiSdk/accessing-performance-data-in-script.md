---
description: Сценарии WMI могут получать доступ к предварительно установленным классам счетчиков производительности WMI либо на локальном компьютере, либо удаленно.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Доступ к данным о производительности в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 42fe1ecdbaf5cdc5cbafc53117ad7c8f370dae2b4e1a3adcee3a4fcf719c995a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320447"
---
# <a name="accessing-performance-data-in-script"></a>Доступ к данным о производительности в скрипте

Сценарии WMI могут получать доступ к предварительно установленным [классам счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI либо на локальном компьютере, либо удаленно. Хотя скрипты могут получать данные из невычисляемых классов, таких как [**Win32 \_ перфравдата \_ перфос \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)или форматированные классы, [**Win32 \_ перфформаттеддата \_ перфос \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), классы форматированных данных могут быть проще в использовании.

Для мониторинга данных производительности с помощью классов счетчиков производительности необходимо использовать [*Обновитель*](gloss-r.md). Используйте объект [**свбемрефрешер**](swbemrefresher.md) для хранения одного или нескольких объектов производительности для обновления или обновления одного объекта с помощью вызова [**свбемобжектекс. Refresh**](swbemobjectex-refresh-.md) . Дополнительные сведения см. [в разделе Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md).

Если установить для свойства [**свбемрефрешер. Аутореконнект**](swbemrefresher-autoreconnect.md) **значение true**, WMI автоматически повторно подключится к удаленному поставщику, если соединение разорвано, поэтому нет необходимости проверять состояние подключения.

Как показано в следующем скрипте примера кода скрипта, необходимо выполнить начальный вызов обновления, чтобы получить начальное значение для обновляемого объекта. Последующие вызовы обновления содержат данные.

> [!Note]  
> Когда скрипт обращается к данным счетчика производительности WMI с удаленного компьютера, сценарий может выполняться только под текущей учетной записью пользователя, выполнившего вход в систему. Инструментарий WMI не поддерживает вызов [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) , который передает различные учетные данные пользователя. Таким образом, учетная запись, вызывающая удаленный компьютер, должна иметь соответствующие права доступа к этому компьютеру.

 

В следующем примере кода скрипта показано, как использовать объект [**свбемрефрешер**](swbemrefresher.md) для обновления данных в объектах счетчиков производительности. Дополнительные сведения об использовании счетчиков производительности в WMI см. в разделе [доступ к предустановленным классам производительности WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a>Пример

В следующем примере кода скрипта показано, что необходимо выполнить начальный вызов обновления, чтобы получить начальное значение для обновленного объекта. Последующие вызовы обновления содержат данные.

В следующем примере кода скрипта показано, как использовать объект [**свбемрефрешер**](swbemrefresher.md) для обновления данных в объектах счетчиков производительности. Дополнительные сведения об использовании счетчиков производительности в WMI см. в разделе [доступ к предустановленным классам производительности WMI](accessing-wmi-preinstalled-performance-classes.md).


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Задачи WMI: Мониторинг производительности](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Мониторинг данных производительности](monitoring-performance-data.md)
</dt> </dl>

 

 
