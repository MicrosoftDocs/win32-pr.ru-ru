---
description: API веб-служб на устройствах (WSDAPI) обеспечивает поддержку профиля устройств для веб-служб (DPWS) в Windows Vista, что позволяет осуществлять обмен данными между компьютерами на базе Windows и подключенными к сети устройствами с помощью веб-служб (WS).
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Соответствие спецификации WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264633"
---
# <a name="wsdapi-specification-compliance"></a>Соответствие спецификации WSDAPI

API веб-служб на устройствах (WSDAPI) обеспечивает поддержку [профиля устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) в Windows Vista, что позволяет осуществлять обмен данными между компьютерами на базе Windows и подключенными к сети устройствами с помощью веб-служб (WS). DPWS собирает базовые спецификации WS, такие как [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)и [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), а также повышает или ограничивает их, предоставляющую базовый набор возможностей для устройств с ограниченными ресурсами. Эта спецификация базовых показателей содержит необходимые функции, такие как возможность описания свойств устройства с помощью метаданных, а также дополнительные функциональные возможности, например возможность отклонять определенные сообщения по соображениям безопасности.

Реализация WSDAPI в Windows Vista является первым выпуском явной поддержки DPWS, а является неуправляемой реализацией DPWS, которая отличается от других реализаций веб-служб (таких как [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) или [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).

Следующие разделы представляют интерес для изготовителей устройств и других разработчиков устройств, которые создают устройства, взаимодействующие с клиентами и узлами WSDAPI на основе Windows, без использования WSDAPI. В этих разделах описывается реализация WSDAPI относительно базовых спецификаций. Они охватывают реализацию требуемых функций, дополнительные функциональные возможности и дополнительные функциональные возможности, не определенные в спецификации.

-   [Соответствие спецификации DPWS](dpws-specification-compliance.md)
-   [Соответствие спецификации WS-Discovery](ws-discovery-specification-compliance.md)
-   [Соответствие спецификации WS-MetadataExchange и WS-Transfer](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Дополнительные функции WS-Discovery](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Разработка устройств WSD](wsd-device-development.md)
</dt> <dt>

[Рекомендации по реализации устройств WSD](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
