---
description: API веб-служб на устройствах (WSDAPI) обеспечивает поддержку профиля устройств для веб-служб (DPWS) в Windows Vista, что обеспечивает обмен данными между компьютерами на основе Windows и подключенными к сети устройствами с помощью веб-служб (WS).
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Соответствие спецификации WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dcf649d8d2771d17f24e983a739c0119a0fe8af67f70b706ba35bcddec20d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991394"
---
# <a name="wsdapi-specification-compliance"></a>Соответствие спецификации WSDAPI

API веб-служб на устройствах (WSDAPI) обеспечивает поддержку [профиля устройств для веб-служб](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) в Windows Vista, что обеспечивает обмен данными между компьютерами на основе Windows и подключенными к сети устройствами с помощью веб-служб (WS). DPWS собирает базовые спецификации WS, такие как [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)и [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), а также повышает или ограничивает их, предоставляющую базовый набор возможностей для устройств с ограниченными ресурсами. Эта спецификация базовых показателей содержит необходимые функции, такие как возможность описания свойств устройства с помощью метаданных, а также дополнительные функциональные возможности, например возможность отклонять определенные сообщения по соображениям безопасности.

реализация WSDAPI в Windows Vista является первым выпуском явной поддержки DPWS, а является неуправляемой реализацией DPWS, которая является отдельной и отличается от других реализаций веб-служб (таких как [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) или [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).

следующие разделы представляют интерес для производителей устройств и других разработчиков устройств, которые создают устройства, взаимодействующие с клиентами и узлами wsdapi на основе Windows, без использования wsdapi. В этих разделах описывается реализация WSDAPI относительно базовых спецификаций. Они охватывают реализацию требуемых функций, дополнительные функциональные возможности и дополнительные функциональные возможности, не определенные в спецификации.

-   [Соответствие спецификации DPWS](dpws-specification-compliance.md)
-   [Соответствие спецификации WS-Discovery](ws-discovery-specification-compliance.md)
-   [Соответствие спецификации WS-MetadataExchange и WS-Transfer](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Дополнительные функции WS-Discovery](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разработка устройств WSD](wsd-device-development.md)
</dt> <dt>

[Рекомендации реализации устройства WSD](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
