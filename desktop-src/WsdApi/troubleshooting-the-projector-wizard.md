---
description: Список диагностических процедур, используемых при устранении неполадок мастера проекторов.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Устранение неполадок мастера проекторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692265"
---
# <a name="troubleshooting-the-projector-wizard"></a>Устранение неполадок мастера проекторов

Мастер проекторов:

-   Всегда использует UDP-WS-Discovery для обнаружения устройств
-   Всегда использует HTTP для обмена метаданными
-   Иногда использует направленное обнаружение

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем мастера проекторов.

**Устранение неполадок мастера проекторов**

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
</dt> </dl>

 

 



