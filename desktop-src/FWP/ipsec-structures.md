---
title: Структуры IPsec
description: Структуры IPsec
ms.assetid: FF1FE626-B9F9-4091-8B82-BEB9D229B93D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd268fda1ee98ec80d20d8c75625d4f68526c741
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2020
ms.locfileid: "105681588"
---
# <a name="ipsec-structures"></a>Структуры IPsec

## <a name="in-this-section"></a>Содержание раздела

-   [**IPSEC \_ address \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   [**\_ \_ \_ STATISTICS0 ПАКЕТной обработки \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0)
-   [**\_ \_ \_ STATISTICS1 ПАКЕТной обработки \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1)
-   [**\_Сводный \_ SA IPsec \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**IPSEC \_ AH \_ \_ Packet \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**\_Проверка подлинности IPsec \_ и \_ TRANSFORM0 шифра \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**\_Проверка подлинности IPsec \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**\_ID0 преобразования проверки подлинности IPsec \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**\_TRANSFORM0 шифра IPsec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**\_ID0 преобразования шифра IPsec \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**IPSEC \_ досп \_ OPTIONS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**IPSEC \_ досп \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**\_ \_ \_ TEMPLATE0 перечисление состояния досп IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**IPSEC \_ досп \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**IPSEC \_ ESP \_ , \_ пакет \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   [**\_GETSPI0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0)
-   [**\_GETSPI1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1)
-   [**\_ID0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**\_MANAGER0 ключей \_ IPSec**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_ \_ CALLBACKS0 ДИСПЕТЧЕРА ключей \_ IPSec**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_POLICY0 ключей \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0)
-   [**\_POLICY1 ключей \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**IPSEC \_ кэймодуле \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**\_PROPOSAL0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**\_SA0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**\_ \_ Проверка подлинности IPsec SA \_ и \_ шифр \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**IPSEC \_ SA \_ AUTH \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   [**IPSEC \_ SA \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)
-   [**IPSEC \_ SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)
-   [**\_ \_ INFORMATION0 шифрования IPSec \_ SA**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   [**IPSEC \_ SA \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0)
-   [**Согласование \_ SA IPsec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1)
-   [**\_ \_ CHANGE0 контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_ \_ \_ TEMPLATE0 enum контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**\_ \_ SUBSCRIPTION0 контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**IPSEC \_ SA \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0)
-   [**IPSEC \_ SA \_ DETAILS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1)
-   [**\_Перечисление SA IPsec \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**Бездействие IPSEC \_ SA \_ \_ TIMEOUT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**IPSEC \_ SA \_ LIFETIME0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**\_STATISTICS0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0)
-   [**\_STATISTICS1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1)
-   [**IPSEC \_ SA \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   [**\_TOKEN0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   [**\_TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0)
-   [**\_TRAFFIC1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1)
-   [**\_STATISTICS0 трафика \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0)
-   [**\_STATISTICS1 трафика \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1)
-   [**\_POLICY0 транспорта \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)
-   [**\_POLICY1 транспорта \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1)
-   [**\_POLICY2 транспорта \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_ENDPOINT0 туннеля \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_ENDPOINTS0 туннеля \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0)
-   [**\_ENDPOINTS1 туннеля \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1)
-   [**\_ENDPOINTS2 туннеля \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_POLICY0 туннеля \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0)
-   [**\_POLICY1 туннеля \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)
-   [**\_POLICY2 туннеля \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**IPSEC \_ v4 \_ UDP \_ ENCAPSULATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**Виртуальные IP IPSEC, \_ \_ Если \_ туннель \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




