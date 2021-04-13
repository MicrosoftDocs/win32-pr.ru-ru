---
description: Приложения, использующие направленное обнаружение, отправляют сообщения проверки по протоколу HTTP или HTTPS для обнаружения устройств.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Устранение неполадок приложений WSDAPI с использованием направленного обнаружения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544791"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a>Устранение неполадок приложений WSDAPI с использованием направленного обнаружения

Приложения, использующие направленное обнаружение, отправляют сообщения [проверки](probe-message.md) по протоколу HTTP или HTTPS для обнаружения устройств. Соответствующие сообщения [ProbeMatch](probematches-message.md) , отправленные в ответе, также передаются по протоколу HTTP или HTTPS. Направленное обнаружение может инициироваться мастером добавления принтера, клиентом обнаружения функций или приложением WSDAPI. Сообщения зонда и ProbeMatch структурно идентичны переданным по протоколу UDP. Сообщения добавляются с соответствующими заголовками HTTP или HTTPS.

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с приложением с помощью направленного обнаружения.

**Устранение неполадок приложения WSDAPI с помощью направленного обнаружения**

1.  [Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).
2.  [Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Проверка трассировки сети для приложения с помощью направленного обнаружения](inspecting-network-traces-for-applications-using-directed-discovery.md).

Если источник проблемы не удается определить с помощью описанных выше процедур диагностики, следуйте инструкциям в статьях [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт.

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с разрешениями WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Устранение неполадок мастера добавления принтера](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[Устранение неполадок приложений WSDAPI](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



