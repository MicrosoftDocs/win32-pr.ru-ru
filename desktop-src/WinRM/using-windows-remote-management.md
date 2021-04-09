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
# <a name="using-windows-remote-management"></a>Использование служба удаленного управления Windows

Служба удаленного управления Windows предназначен для улучшения управления оборудованием в сетевой среде с различными устройствами, работающими под управлением различных операционных систем. Служба полностью предназначена для отслеживания удаленных компьютеров и управления ими посредством реализации стандартного протокола взаимодействия.

Поскольку [API-интерфейсы сценариев WinRM](winrm-scripting-api.md) и [API-интерфейсу WinRM C++](winrm-c---api.md) реализуют и тесно моделируют операции, определенные для протокола WS-Management, скрипты и приложения получают потоки XML в ответ на запросы. Входные параметры для вызовов методов должны быть созданы в формате XML. Методы API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) можно использовать для вывода или создания XML-строк. Пример см. в разделе вывод [XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).

В следующем списке приведены разделы, в которых описывается использование сценариев WinRM.

-   [Определение того, поддерживает ли удаленный компьютер протокол WS-Management](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [Получение данных с локального компьютера](obtaining-data-from-the-local-computer.md)
-   [Получение данных с удаленного компьютера](obtaining-data-from-a-remote-computer.md)
-   [Перечисление или составление списка всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md)
-   [Запрос конкретных экземпляров ресурса](querying-for-specific-instances-of-a-resource.md)
-   [Отображение выходных данных XML из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a>Трассировка действия WinRM

Поскольку WinRM получает данные с помощью [инструментарий управления Windows (WMI) (WMI)](/windows/desktop/WmiSdk/wmi-start-page), вы можете ОТСЛЕЖИВАТЬ действия WMI, полученные в результате сообщений WinRM. Начиная с Windows Vista, служба WMI больше не использует [файлы журнала WMI](/windows/desktop/WmiSdk/wmi-log-files). Вместо этого он использует [трассировку событий](/windows/desktop/ETW/event-tracing-portal) (ETW) и события, доступные через пользовательский интерфейс **Просмотр событий** или программу командной строки евтутил.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Удаленное управление Windows](portal.md)
</dt> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Справочник по служба удаленного управления Windows](windows-remote-management-reference.md)
</dt> <dt>

[Создание сценариев в служба удаленного управления Windows](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 