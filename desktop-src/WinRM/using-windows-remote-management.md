---
title: Использование служба удаленного управления Windows
description: Служба удаленного управления Windows предназначен для улучшения управления оборудованием в сетевой среде с различными устройствами, работающими под управлением различных операционных систем.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134234"
---
# <a name="using-windows-remote-management"></a><span data-ttu-id="3263f-103">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="3263f-103">Using Windows Remote Management</span></span>

<span data-ttu-id="3263f-104">Служба удаленного управления Windows предназначен для улучшения управления оборудованием в сетевой среде с различными устройствами, работающими под управлением различных операционных систем.</span><span class="sxs-lookup"><span data-stu-id="3263f-104">Windows Remote Management is intended to improve hardware management in a network environment with various devices running a variety of operating systems.</span></span> <span data-ttu-id="3263f-105">Служба полностью предназначена для отслеживания удаленных компьютеров и управления ими посредством реализации стандартного протокола взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="3263f-105">The entire design of the service is focused on monitoring and managing remote computers by implementing an interoperable standard protocol.</span></span>

<span data-ttu-id="3263f-106">Поскольку [API-интерфейсы сценариев WinRM](winrm-scripting-api.md) и [API-интерфейсу WinRM C++](winrm-c---api.md) реализуют и тесно моделируют операции, определенные для протокола WS-Management, скрипты и приложения получают потоки XML в ответ на запросы.</span><span class="sxs-lookup"><span data-stu-id="3263f-106">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) implement and closely model the operations defined for the WS-Management protocol, scripts and applications receive streams of XML in response to requests.</span></span> <span data-ttu-id="3263f-107">Входные параметры для вызовов методов должны быть созданы в формате XML.</span><span class="sxs-lookup"><span data-stu-id="3263f-107">Input parameters to method calls must be constructed in XML.</span></span> <span data-ttu-id="3263f-108">Методы API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) можно использовать для вывода или создания XML-строк.</span><span class="sxs-lookup"><span data-stu-id="3263f-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API to display or construct XML strings.</span></span> <span data-ttu-id="3263f-109">Пример см. в разделе вывод [XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="3263f-109">For an example, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="3263f-110">В следующем списке приведены разделы, в которых описывается использование сценариев WinRM.</span><span class="sxs-lookup"><span data-stu-id="3263f-110">The following list includes topics that describe how to use WinRM scripting:</span></span>

-   [<span data-ttu-id="3263f-111">Определение того, поддерживает ли удаленный компьютер протокол WS-Management</span><span class="sxs-lookup"><span data-stu-id="3263f-111">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [<span data-ttu-id="3263f-112">Получение данных с локального компьютера</span><span class="sxs-lookup"><span data-stu-id="3263f-112">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
-   [<span data-ttu-id="3263f-113">Получение данных с удаленного компьютера</span><span class="sxs-lookup"><span data-stu-id="3263f-113">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
-   [<span data-ttu-id="3263f-114">Перечисление или составление списка всех экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="3263f-114">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
-   [<span data-ttu-id="3263f-115">Запрос конкретных экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="3263f-115">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
-   [<span data-ttu-id="3263f-116">Отображение выходных данных XML из скриптов WinRM</span><span class="sxs-lookup"><span data-stu-id="3263f-116">Displaying XML Output from WinRM Scripts</span></span>](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a><span data-ttu-id="3263f-117">Трассировка действия WinRM</span><span class="sxs-lookup"><span data-stu-id="3263f-117">Tracing WinRM Activity</span></span>

<span data-ttu-id="3263f-118">Поскольку WinRM получает данные с помощью [инструментарий управления Windows (WMI) (WMI)](/windows/desktop/WmiSdk/wmi-start-page), вы можете ОТСЛЕЖИВАТЬ действия WMI, полученные в результате сообщений WinRM.</span><span class="sxs-lookup"><span data-stu-id="3263f-118">Because WinRM obtains data through [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), you can trace WMI activity that results from WinRM messages.</span></span> <span data-ttu-id="3263f-119">Начиная с Windows Vista, служба WMI больше не использует [файлы журнала WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="3263f-119">Starting with Windows Vista, the WMI service no longer uses the [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span> <span data-ttu-id="3263f-120">Вместо этого он использует [трассировку событий](/windows/desktop/ETW/event-tracing-portal) (ETW) и события, доступные через пользовательский интерфейс **Просмотр событий** или программу командной строки евтутил.</span><span class="sxs-lookup"><span data-stu-id="3263f-120">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Evtutil command line tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3263f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="3263f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3263f-122">Удаленное управление Windows</span><span class="sxs-lookup"><span data-stu-id="3263f-122">Windows Remote Management</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="3263f-123">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="3263f-123">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="3263f-124">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="3263f-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="3263f-125">Создание сценариев в служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="3263f-125">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 