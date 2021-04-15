---
description: Список диагностических процедур для использования при устранении неполадок в приложениях WSDAPI.
ms.assetid: befe4234-8d3a-4fc5-9a7d-faca94964af6
title: Устранение неполадок других приложений WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a421f26237cc14d07a43e00faeb6d8bf49aa02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701784"
---
# <a name="troubleshooting-other-wsdapi-applications"></a>Устранение неполадок других приложений WSDAPI

Приложения могут напрямую вызывать интерфейсы и функции WSDAPI для выполнения обнаружения устройств и обмена метаданными. Шаблоны сообщений, используемые этими приложениями, различаются.

Цель этого руководство по устранению неполадок заключается в том, чтобы разработчики приложений могли успешно реализовать прокси-сервер устройства. Это средство не предназначено для диагностики всех аспектов WSDAPI. Если прокси-сервер устройства был успешно создан, а клиент и узел могут видеть друг друга в сети, это не поможет решить проблемы приложения. Чтобы устранить эти проблемы с приложением, следуйте инструкциям в разделе [Включение трассировки WSDAPI](enabling-wsdapi-tracing.md) и обратитесь в службу поддержки Майкрософт за дальнейшей помощью.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxy"></a>Устранение неполадок клиентов, вызывающих Всдкреатедевицепрокси

Приложения вызывают [**всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) для создания и инициализации экземпляра интерфейса [**ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . Этот объект прокси-сервера устройства можно использовать для объявления служб на устройстве, а также для обмена метаданными.

Приложение, вызывающее [**всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) , всегда использует следующие сообщения.

-   [Получить](get--metadata-exchange--http-request-and-message.md)
-   [GetResponse](getresponse--metadata-exchange--message.md)

Приложение, вызывающее [**всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) , иногда использует следующие сообщения.

-   [Разрешить](resolve-message.md)
-   [ресолвематчес](resolvematches-message.md)

[Разрешения](resolve-message.md) и [ресолвематчес](resolvematches-message.md) сообщения создаются, когда адрес логического устройства (т. е. адрес устройства в формате urn: UUID: {GUID}) передается в *псздевицеид*. Эти сообщения не создаются, когда адрес физического устройства передается в *псздевицеид*. При использовании разрешения и Ресолвематчес сообщений они отправляются перед сообщениями [Get](get--metadata-exchange--http-request-and-message.md) и [GetResponse](getresponse--metadata-exchange--message.md) .

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с приложением, вызывающим [**всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) с адресом физического устройства.

1.  [Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).
2.  [Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с приложением, вызывающим [**всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) с адресом логического устройства.

1.  [Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).
2.  [Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).

Убедитесь, что сообщения [Resolve](resolve-message.md) и [ресолвематчес](resolvematches-message.md) созданы и соответствуют требованиям к трафику. Нет необходимости искать сообщения [зонда](probe-message.md) или [ProbeMatch](probematches-message.md) в выходных данных клиента отладки WSD или в трассировках сети.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxyadvanced"></a>Устранение неполадок клиентов, вызывающих Всдкреатедевицепроксядванцед

Приложения вызывают [**всдкреатедевицепроксядванцед**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) для создания и инициализации экземпляра интерфейса [**ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . В отличие от [**всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy), **Всдкреатедевицепроксядванцед** имеет параметр *пдевицеаддресс* , который используется для определения адреса транспортного устройства. Если указан этот транспортный адрес, разрешение логического адреса не требуется, а [разрешения](resolve-message.md) и [ресолвематчес](resolvematches-message.md) сообщения не создаются.

Если *пдевицеаддресс* имеет значение **null** , а *псздевицеид* является логическим адресом, необходимо разрешение [адреса и разрешение и](resolve-message.md) [ресолвематчес](resolvematches-message.md) сообщений.

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с приложением, вызывающим [**всдкреатедевицепроксядванцед**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) , с параметром _пдевицеаддресс_ , отличным от **null**. Эти процедуры также можно использовать, если *пдевицеаддресс* имеет **значение NULL** , а *псздевицеид* — физический адрес.

1.  [Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).
2.  [Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с приложением, вызывающим [**всдкреатедевицепроксядванцед**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) с *пдевицеаддресс* , для которых задано **значение NULL** , а для *псздевицеид* задан логический адрес.

1.  [Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).
2.  [Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Используйте универсальный узел и клиент для обмена метаданными HTTP](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Используйте ведение журнала WinHTTP для проверки получения трафика](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Проверьте сетевые трассировки для обмена метаданными HTTP](inspecting-network-traces-for-http-metadata-exchange.md).

Убедитесь, что сообщения [Resolve](resolve-message.md) и [ресолвематчес](resolvematches-message.md) созданы и соответствуют требованиям к трафику. Нет необходимости искать сообщения [зонда](probe-message.md) или [ProbeMatch](probematches-message.md) в выходных данных клиента отладки WSD или в трассировках сети.

## <a name="troubleshooting-clients-using-the-iwsdiscoveryprovider-interface"></a>Устранение неполадок клиентов с помощью интерфейса Ивсдисковерипровидер

Приложения, вызывающие интерфейс [**ивсдисковерипровидер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) , не выполняют обмен метаданными. Этот интерфейс используется только для обнаружения. Шаблоны сообщений и процедуры устранения неполадок различаются для каждого метода, вызываемого в интерфейсе **ивсдисковерипровидер** .

Когда приложение вызывает [**ивсдисковерипровидер:: сеарчбитипе**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype), создается сообщение [пробы](probe-message.md) . Сообщение пробы отправляется с помощью многоадресной рассылки UDP на порт 3702. В ответе создается сообщение [ProbeMatch](probematches-message.md) . Сообщение ProbeMatch отправляется по адресу UDP и исходит из порта 3702.

Когда приложение вызывает [**ивсдисковерипровидер:: сеарчбид**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid), создается сообщение [разрешения](resolve-message.md) . Сообщение с разрешением отправляется многоадресной передачей UDP на порт 3702. В ответе создается сообщение [ресолвематчес](resolvematches-message.md) . Ресолвематчес отправляется по адресу UDP и исходит от порта 3702.

Следующие процедуры диагностики следует использовать (по порядку) для выявления проблем с приложением, вызывающим [**ивсдисковерипровидер:: сеарчбитипе**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) или [**Ивсдисковерипровидер:: сеарчбид**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid). Убедитесь, что сообщения, созданные вызванным API, удовлетворяют требованиям к трафику.

1.  [Проверьте параметры адаптера и брандмауэра](inspecting-adapter-and-firewall-settings.md).
2.  [Используйте универсальный узел и клиент для протокола UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Используйте клиент отладки WSD для проверки многоадресного трафика](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Проверьте сетевые трассировки для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).

Если приложение вызывает [**ивсдисковерипровидер:: сеарчбяддресс**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress), это приложение с направленным обнаружением. Дополнительные сведения об устранении неполадок см. в разделе [Устранение неполадок приложений с помощью](troubleshooting-applications-using-directed-discovery.md)управляемого обнаружения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с разрешениями WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



