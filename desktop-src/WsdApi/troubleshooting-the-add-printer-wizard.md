---
description: Список диагностических процедур, используемых при устранении неполадок мастера добавления принтера.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Устранение неполадок мастера добавления принтера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692804"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Устранение неполадок мастера добавления принтера

Мастер добавления принтера:

-   Всегда использует UDP-WS-Discovery для обнаружения устройств
-   Всегда инициирует подключение HTTP или HTTPS для обмена метаданными
-   Иногда использует направленное обнаружение
-   Иногда использует безопасный канал (HTTPS) для обмена метаданными

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с мастером добавления принтера.

**Устранение неполадок мастера добавления принтера**

1.  Если используется направленное обнаружение, [Устранение неполадок с помощью направленного обнаружения](troubleshooting-applications-using-directed-discovery.md).
2.  [Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).
3.  [Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).
5.  [Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
6.  [Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).
7.  [Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).

Если источник проблемы не удается определить с помощью описанных выше процедур диагностики, следуйте инструкциям в статьях [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт.

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с разрешениями WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Устранение неполадок в приложениях с помощью направленного обнаружения](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



