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
ms.openlocfilehash: e203acfc7fc23fe0dab466eee383223aad0bf889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693752"
---
# <a name="accessing-performance-data-in-script"></a><span data-ttu-id="1bc89-103">Доступ к данным о производительности в скрипте</span><span class="sxs-lookup"><span data-stu-id="1bc89-103">Accessing Performance Data in Script</span></span>

<span data-ttu-id="1bc89-104">Сценарии WMI могут получать доступ к предварительно установленным [классам счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI либо на локальном компьютере, либо удаленно.</span><span class="sxs-lookup"><span data-stu-id="1bc89-104">WMI scripts can access the preinstalled WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes), either on the local computer or remotely.</span></span> <span data-ttu-id="1bc89-105">Хотя скрипты могут получать данные из невычисляемых классов, таких как [**Win32 \_ перфравдата \_ перфос \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)или форматированные классы, [**Win32 \_ перфформаттеддата \_ перфос \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), классы форматированных данных могут быть проще в использовании.</span><span class="sxs-lookup"><span data-stu-id="1bc89-105">While scripts can obtain data from uncalculated classes, such as [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), or formatted classes, [**Win32\_PerfFormattedData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), the formatted data classes can be easier to use.</span></span>

<span data-ttu-id="1bc89-106">Для мониторинга данных производительности с помощью классов счетчиков производительности необходимо использовать [*Обновитель*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="1bc89-106">Monitoring performance data with the performance counter classes requires the use of a [*refresher*](gloss-r.md).</span></span> <span data-ttu-id="1bc89-107">Используйте объект [**свбемрефрешер**](swbemrefresher.md) для хранения одного или нескольких объектов производительности для обновления или обновления одного объекта с помощью вызова [**свбемобжектекс. Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc89-107">Use the [**SWbemRefresher**](swbemrefresher.md) object to store one or more performance objects for refresh or refresh a single object by the [**SWbemObjectEx.Refresh**](swbemobjectex-refresh-.md) call.</span></span> <span data-ttu-id="1bc89-108">Дополнительные сведения см. [в разделе Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="1bc89-108">For more information, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="1bc89-109">Если установить для свойства [**свбемрефрешер. Аутореконнект**](swbemrefresher-autoreconnect.md) **значение true**, WMI автоматически повторно подключится к удаленному поставщику, если соединение разорвано, поэтому нет необходимости проверять состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="1bc89-109">By setting the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **TRUE**, WMI automatically reconnects to a remote provider if the connection is broken so that you do not need to check for connection status.</span></span>

<span data-ttu-id="1bc89-110">Как показано в следующем скрипте примера кода скрипта, необходимо выполнить начальный вызов обновления, чтобы получить начальное значение для обновляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="1bc89-110">As shown in the following script code example script, you must make an initial refresh call to get a starting value for the object you are refreshing.</span></span> <span data-ttu-id="1bc89-111">Последующие вызовы обновления содержат данные.</span><span class="sxs-lookup"><span data-stu-id="1bc89-111">Subsequent refresh calls then contain data.</span></span>

> [!Note]  
> <span data-ttu-id="1bc89-112">Когда скрипт обращается к данным счетчика производительности WMI с удаленного компьютера, сценарий может выполняться только под текущей учетной записью пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="1bc89-112">When a script is accessing WMI performance counter data from a remote computer, the script can only run under the current logged-on user account.</span></span> <span data-ttu-id="1bc89-113">Инструментарий WMI не поддерживает вызов [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) , который передает различные учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="1bc89-113">WMI does not support an [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) call that passes in different user credentials.</span></span> <span data-ttu-id="1bc89-114">Таким образом, учетная запись, вызывающая удаленный компьютер, должна иметь соответствующие права доступа к этому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="1bc89-114">Therefore, the account calling the remote computer must already have the appropriate privileges on that computer.</span></span>

 

<span data-ttu-id="1bc89-115">В следующем примере кода скрипта показано, как использовать объект [**свбемрефрешер**](swbemrefresher.md) для обновления данных в объектах счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="1bc89-115">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="1bc89-116">Дополнительные сведения об использовании счетчиков производительности в WMI см. в разделе [доступ к предустановленным классам производительности WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1bc89-116">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


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



## <a name="example"></a><span data-ttu-id="1bc89-117">Пример</span><span class="sxs-lookup"><span data-stu-id="1bc89-117">Example</span></span>

<span data-ttu-id="1bc89-118">В следующем примере кода скрипта показано, что необходимо выполнить начальный вызов обновления, чтобы получить начальное значение для обновленного объекта.</span><span class="sxs-lookup"><span data-stu-id="1bc89-118">The following script code example shows that you must make an initial refresh call to get a starting value for the refreshed object.</span></span> <span data-ttu-id="1bc89-119">Последующие вызовы обновления содержат данные.</span><span class="sxs-lookup"><span data-stu-id="1bc89-119">Subsequent refresh calls then contain data.</span></span>

<span data-ttu-id="1bc89-120">В следующем примере кода скрипта показано, как использовать объект [**свбемрефрешер**](swbemrefresher.md) для обновления данных в объектах счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="1bc89-120">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="1bc89-121">Дополнительные сведения об использовании счетчиков производительности в WMI см. в разделе [доступ к предустановленным классам производительности WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1bc89-121">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1bc89-122">См. также</span><span class="sxs-lookup"><span data-stu-id="1bc89-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bc89-123">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="1bc89-123">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="1bc89-124">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="1bc89-124">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="1bc89-125">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="1bc89-125">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
