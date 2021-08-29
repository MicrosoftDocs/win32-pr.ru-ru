---
title: Параметры канала безопасности
description: Параметры канала безопасности контролируют способ применения и проверки безопасности в канале.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- канал безопасности Параметры веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3d6cef77da7a908598e2150ebf09de13a0899a6910a562335c4a5b91d6cf8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927014"
---
# <a name="security-channel-settings"></a>Параметры канала безопасности

Параметры канала безопасности контролируют способ применения и проверки безопасности в канале. Каждый параметр канала безопасности представлен коллекцией пар "свойство-значение" с ключами свойств, определяемыми [**\_ \_ \_ идентификатором свойства WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id). Каждое свойство в коллекции имеет разумное значение по умолчанию. Из-за этих значений по умолчанию можно определить и использовать описание безопасности без указания каких-либо параметров канала безопасности.


[Параметры привязки безопасности](security-binding-settings.md) содержат похожие коллекции пар «свойство-значение», ключи которых определяются структурой [**\_ \_ \_ свойств привязки безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) . Различие между этими двумя параметрами состоит в том, что параметры каналов безопасности ограничены описанием безопасности (то есть содержат свойства безопасности для всего канала), в то время как параметры привязки безопасности ограничены одной из привязок безопасности, и может существовать множество привязок безопасности. Таким образом, например, пользовательское описание безопасности, содержащее три привязки безопасности, будет иметь один набор параметров каналов безопасности для всего канала и три контейнера параметров привязки безопасности, по одному для каждой привязки безопасности.

С параметрами канала безопасности используются следующие перечисления.

-   [**\_уровень защиты \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [**\_ \_ \_ идентификатор свойства маркера \_ безопасности \_ запроса WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [**\_ \_ идентификатор алгоритма безопасности WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [**\_ \_ идентификатор свойства алгоритма безопасности WS \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [**\_ \_ макет заголовка безопасности \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [**\_ \_ версия заголовка безопасности \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [**\_ \_ идентификатор свойства безопасности \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_ \_ Использование метки времени безопасности WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [**\_ \_ \_ идентификатор свойства токена \_ безопасности \_ XML WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

Для параметров канала безопасности используются следующие структуры:

-   [**\_ \_ \_ свойство токена безопасности WS Request \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [**\_ \_ свойство алгоритма безопасности WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [**\_ \_ набор алгоритмов безопасности WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [**\_свойство безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [**\_ \_ \_ свойство токена безопасности XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




