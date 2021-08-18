---
description: Следующие перечисления поддерживают API таблиц распределенной маршрутизации (DRT).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Перечисление таблиц распределенной маршрутизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ff0a955aed8d6ed6cdf14f3d0e7f6ac2605960123f8008c831dbef5be2da98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011602"
---
# <a name="distributed-routing-table-enumerations"></a>Перечисление таблиц распределенной маршрутизации

Следующие перечисления поддерживают API таблиц распределенной маршрутизации (DRT).



| Перечисление                                                            | Описание                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_область DRT**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Определяет набор областей IPv6, в которых будет выполняться сервер DRT при использовании транспортного протокола IPv6 UDP, созданного [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport). |
| [**\_ \_ Флаги адреса DRT**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Определяет набор ответов, которые могут возвращаться промежуточным узлом при выполнении поиска ключа.                                                         |
| [**\_состояние DRT**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Определяет возможные состояния подключения и ошибки локального узла.                                                                                                   |
| [**\_тип соответствия \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Определяет точное совпадение результатов, возвращаемых при выполнении поиска.                                                                                                 |
| [**\_ \_ \_ тип изменения ключа конечного элемента \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Определяет набор типов изменений, которые могут быть выполнены с локальным узлом конечного набора в локальном кэше DRT.                                                                |
| [**\_Тип события \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Определяет набор событий, которые могут быть вызваны DRT.                                                                                                              |
| [**\_режим безопасности \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Определяет возможные режимы безопасности DRT. Это перечисление является полем структуры [**\_ параметров DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .                                   |
| [**\_состояние регистрации \_ DRT**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Определяет состояние зарегистрированного ключа.                                                                                                                                |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Структуры таблиц распределенной маршрутизации](distributed-routing-table-structures.md)
</dt> <dt>

[Функции таблиц распределенной маршрутизации](distributed-routing-table-functions.md)
</dt> <dt>

[Справочник по распределенной маршрутизации API таблиц](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



