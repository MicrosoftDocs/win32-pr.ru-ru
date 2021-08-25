---
description: Список диагностических процедур, используемых при устранении неполадок мастера добавления принтера.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Устранение неполадок мастера добавления принтера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6c6971108b0f6fb46a373be47943a3ccbc7fcd97b830733c139653f991debd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860054"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[начало работы с разрешениями WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Устранение неполадок в приложениях с помощью направленного обнаружения](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



