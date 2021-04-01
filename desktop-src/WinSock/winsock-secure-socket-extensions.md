---
description: Расширения защищенных сокетов для Winsock позволяют приложению сокета управлять безопасностью трафика по сети.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Расширения безопасных сокетов Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072736"
---
# <a name="winsock-secure-socket-extensions"></a>Расширения безопасных сокетов Winsock

Расширения защищенных сокетов для Winsock позволяют приложению сокета управлять безопасностью трафика по сети. Эти расширения позволяют приложению предоставлять политику безопасности и требования к сетевому трафику, а также запрашивать примененные параметры безопасности. Например, приложение может использовать эти расширения для запроса маркера безопасности однорангового узла, который можно использовать для проверки доступа на уровне приложения.

Расширения SSL предназначены для интеграции служб, предоставляемых протоколом IPsec и другими протоколами безопасности, с платформой Winsock Framework. До Windows Vista, в Windows Server 2003 и Windows XP, IPsec был настроен администратором с помощью локальных политик и политики домена. В Windows Vista расширения безопасных сокетов позволяют приложениям полностью или частично настраивать и контролировать безопасность своего сетевого трафика на уровне сокета.

Приложения могут уже защищать сетевой трафик с помощью общедоступных API, таких как Управление IPsec, платформа фильтрации Windows и интерфейс поставщика поддержки безопасности (SSPI). Однако использование этих API может усложнить разработку приложения и может усложнить настройку и развертывание. Расширения для безопасного сокета WinSock предназначены для упрощения разработки сетевых приложений, требующих безопасного сетевого трафика путем предоставления Winsock большей части сложности.

Эти расширения SSL доступны в Windows Vista и более поздних версиях.

## <a name="secure-socket-functions"></a>Функции защищенного сокета

Существуют следующие функции расширения SSL.

-   [**всаделетесоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [**всаимперсонатесоккетпир**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [**всакуерисоккетсекурити**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [**всаревертимперсонатион**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [**всасетсоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [**всасетсоккетсекурити**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> Функции защищенного сокета в настоящее время поддерживают только протокол IPsec и доступны в Windows Vista и более поздних версиях.

 

Ниже приведены структуры и перечисления, используемые функциями безопасного сокета.

-   [**\_ \_ имя целевого объекта на уровне сокета \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [**\_протокол безопасности сокета \_**](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [**\_ \_ сведения о запросе безопасности сокета \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [**\_ \_ шаблон запроса безопасности сокета \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [**\_Параметры безопасности сокета \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [**\_Параметры безопасности сокета \_ \_ IPSec**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

Функции безопасного сокета просты в использовании для обычных приложений и достаточно гибкие для приложений, которым требуется высокий уровень контроля над безопасностью. Эти функции позволяют обеспечить скрытие базового механизма безопасности от приложения. Приложение может указать общие требования к безопасности и позволить администратору управлять протоколом безопасности, который используется для поддержки требований. Хотя эти функции можно расширить для добавления других протоколов безопасности, в настоящее время только IPsec интегрируется с функциями безопасных сокетов.

Функция [**всасетсоккетсекурити**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) позволяет приложению включить безопасность и применить параметры безопасности до установки соединения.

Функция [**всасетсоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) позволяет приложению указать целевое имя, соответствующее одноранговой сущности. Выбранный протокол безопасности будет использовать эти сведения при проверке подлинности однорангового узла. Эта функция решает проблемы доверенных атак "злоумышленник в середине".

Функция [**всаделетесоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) используется для удаления ранее указанного однорангового имени для сокета.

После установления соединения функция [**всакуерисоккетсекурити**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) позволяет приложению запрашивать свойства безопасности подключения, которые могут включать одноранговый доступ или маркер доступа к компьютеру.

После установления соединения функция [**всаимперсонатесоккетпир**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) позволяет приложению олицетворять субъект безопасности, соответствующий узлу сокета, для выполнения авторизации на уровне приложения.

[**Всаревертимперсонатион**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) позволяет приложению завершить олицетворение однорангового узла сокета.

## <a name="secure-socket-architecture"></a>Архитектура защищенного сокета

![Базовая архитектура расширений безопасного сокета WinSock](images/ss-arch.png)

-   Приложение вызывает функции безопасного сокета для установки или запроса параметров безопасности для сокета.
-   Функции безопасного сокета — это набор строго типизированных функций расширения, которые заключают вызовы функции [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) , используя только что определенные значения параметра *двиоконтролкоде* , доступного в Windows Vista и более поздних версиях. Эти запросы IOCTL обрабатываются сетевым стеком.
-   Сетевой стек будет направлять вызов [принудительного применения уровня приложения (ALE)](../fwp/application-layer-enforcement--ale-.md) вместе с маркером конечной точки. Для функций [**всаделетесоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**всасетсоккетпиртаржетнаме**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)и [**всасетсоккетсекурити**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , ALE будет настраивать параметры приложения в локальной конечной точке. Для функции [**ВСАКУЕРИСОККЕТСЕКУРИТИ**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) Ale будет считывать запрошенные сведения из соответствующих локальных и удаленных конечных точек.
-   На основе событий сокета принудительное применение прикладного уровня (ALE) обеспечивает применение политик для безопасной архитектуры сокетов с помощью платформы фильтрации Windows. Дополнительные сведения см. в разделе [сведения о платформе фильтрации Windows](../fwp/about-windows-filtering-platform.md) и [применении уровня приложения (ALE)](../fwp/application-layer-enforcement--ale-.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[О платформе фильтрации Windows](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[Расширенные примеры Winsock с использованием расширений SSL](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[Принудительное применение уровня приложения (ALE)](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[Конфигурация IPsec](../fwp/ipsec-configuration.md)
</dt> <dt>

[Функции IPsec](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[Безопасное программирование Winsock](secure-winsock-programming.md)
</dt> <dt>

[интерфейс поставщика поддержки безопасности (SSPI)](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[Использование расширений SSL](using-secure-socket-extensions.md)
</dt> <dt>

[Платформа фильтрации Windows](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[Функции API платформы фильтрации Windows](../fwp/fwp-functions.md)
</dt> </dl>

 

 
