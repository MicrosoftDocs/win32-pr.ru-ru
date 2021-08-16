---
description: Список диагностических процедур, используемых при устранении неполадок в сетевом обозревателе.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Устранение неполадок обозревателя сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a7c8e270fa3f1e07ce9b44fb9ce619d9fe5225e2c4d3ae87896d5e7cf20a2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120584"
---
# <a name="troubleshooting-the-network-explorer"></a>Устранение неполадок обозревателя сети

Обозреватель сети:

-   Всегда использует UDP-WS-Discovery для обнаружения устройств
-   Всегда инициирует подключение HTTP или HTTPS для обмена метаданными
-   Иногда использует безопасный канал (HTTPS) для обмена метаданными

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем в сетевом обозревателе.

**Устранение неполадок обозревателя сети**

1.  [Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).
2.  [Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).

Сетевой обозреватель использует [обнаружение функций](/previous-versions/windows/desktop/fundisc/fd-portal) для перечисления сетевых устройств. Дополнительные сведения об устранении неполадок см. в разделе [Устранение неполадок клиентов обнаружения функций](troubleshooting-function-discovery-clients.md).

Если источник проблемы не удается определить с помощью описанных выше процедур диагностики, следуйте инструкциям в статьях [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[начало работы с разрешениями WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Устранение неполадок клиентов обнаружения функций](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
