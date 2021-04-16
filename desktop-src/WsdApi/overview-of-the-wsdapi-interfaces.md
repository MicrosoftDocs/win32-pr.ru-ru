---
description: API веб-служб на устройствах (WSDAPI) используется для разработки клиентских приложений, позволяющих находить и получать доступ к устройствам, а для разработки узлов устройств и связанных служб, работающих под управлением Windows Vista и Windows Server 2008.
ms.assetid: 2b23d7d3-3b06-48c8-993e-49c72b139624
title: Общие сведения о интерфейсах WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3e728971741f97707c1dc72effdaf0ca17dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692810"
---
# <a name="overview-of-the-wsdapi-interfaces"></a>Общие сведения о интерфейсах WSDAPI

API веб-служб на устройствах (WSDAPI) используется для разработки клиентских приложений, позволяющих находить и получать доступ к устройствам, а для разработки узлов устройств и связанных служб, работающих под управлением Windows Vista и Windows Server 2008. API [обнаружения функций](/previous-versions/windows/desktop/fundisc/fd-portal) и средство [всдкодежен](web-services-for-devices-code-generator.md) — это дополнительные средства, которые можно использовать для разработки клиентов, устройств и служб. Интерфейсы WSDAPI можно использовать непосредственно для предоставления расширенной функциональности.

## <a name="major-wsdapi-interfaces"></a>Основные интерфейсы WSDAPI

Четыре основных интерфейса WSDAPI: [**ивсдисковерипровидер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider), [**ивсдисковерипублишер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher), [**ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)и [**ивсддевицехост**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost). Список всех интерфейсов WSDAPI см. в разделе [Web Services on Devices interfaces](web-services-for-devices-interfaces.md).

## <a name="iwsdiscoveryprovider"></a>ивсдисковерипровидер

[**Ивсдисковерипровидер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) используется для реализации функции WS-Discovery на клиентах.

[**Ивсдисковерипровидер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) проблемы WS-Discovery [проверку](probe-message.md) и [разрешение](resolve-message.md) сообщений, а затем получает сообщения [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatch](probematches-message.md)и [ресолвематчес](resolvematches-message.md) . Используйте сведения, полученные через интерфейс **ивсдисковерипровидер** при создании интерфейса [**ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) , используемого для описания и управления конкретным устройством DPWS.

Интерфейс [**ивсдисковерипровидер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) необязателен при простом разрешении определенного адреса DPWS устройства перед созданием прокси-сервера устройства. [**Всдкреатедевицепрокси**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) будет автоматически разрешать адрес устройства, если это необходимо.

API [обнаружения функций](/previous-versions/windows/desktop/fundisc/fd-portal) можно использовать для универсального обнаружения устройств и служб, так как API может обнаруживать DPWS устройства, а также устройства, использующие другие протоколы. При написании универсального приложения обнаружения рассмотрите возможность использования обнаружения функций.

## <a name="iwsdiscoverypublisher"></a>ивсдисковерипублишер

[**Ивсдисковерипублишер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) используется для реализации WS-Discovery функциональных возможностей в целевых службах, таких как устройства.

[**Ивсдисковерипублишер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) позволяет приложению публиковать свое присутствие с помощью WS-Discovery сообщений Hello и Bye. Этот интерфейс позволяет приложению получать зонды и разрешать запросы, а затем создавать и отправлять ответы ProbeMatch и Ресолвематчес.

Интерфейс [**ивсдисковерипублишер**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) необязателен, если просто публикуется существование объекта [**ивсддевицехост**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) . **Ивсддевицехост** управляет собственным присутствием WS-Discovery.

## <a name="iwsddeviceproxy"></a>ивсддевицепрокси

[**Ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) используется для реализации функций WS-Discovery, WS-MetadataExchange и управления на стороне клиента. Эта функция включает необязательные возможности безопасного канала, WS-Eventing и вложений.

Интерфейс [**ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) имеет три следующих применения.

-   Разрешает адреса логических устройств, если это необходимо.
-   Инициирует запросы метаданных к устройствам для перечисления типов и адресов служб.
-   Предоставляет источник для объектов [**ивсдсервицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) , которые можно использовать для выдаче управляющих сообщений конкретным службам на устройстве.

Объект [**ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) обычно создается и используется целиком в коде, созданном [всдкодежен](web-services-for-devices-code-generator.md).

## <a name="iwsddevicehost"></a>ивсддевицехост

[**Ивсддевицехост**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) используется для реализации функций WS-Discovery, WS-MetadataExchange и размещения служб на стороне устройства. Размещенные службы могут реагировать на управляющие сообщения и могут поддерживать безопасный канал, WS-Eventing и вложения.

Интерфейс [**ивсддевицехост**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) использует следующие способы.

-   Размещает объекты службы.
-   Сообщает о присутствии узла устройства в сети с помощью WS-Discovery.
-   Реагирует на запросы WS-MetadataExchange и описывает типы и расположения размещенных служб.
-   Отправляет сетевые запросы в объекты службы.

Функции управления подписками WS-Discovery, WS-MetadataExchange и WS-Eventing полностью обрабатываются в объекте узла устройства. Чтобы служба могла быть размещена внутри узла устройства, должны выполняться следующие требования.

-   Узел должен быть создан путем вызова [**всдкреатедевицехост**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost).
-   Необходимо зарегистрировать метаданные, связанные со службой.
-   Сама служба должна быть зарегистрирована.
-   Необходимо запустить узел устройства.

Объект [**ивсддевицехост**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) обычно создается и используется внутри кода, созданного [всдкодежен](web-services-for-devices-code-generator.md).

 

 
