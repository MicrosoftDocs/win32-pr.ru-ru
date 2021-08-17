---
title: Структуры WFP
description: структуры API платформы фильтрации Windows (WFP) приведены ниже.
ms.assetid: e957132f-417b-40c1-afe3-5aec0e2192f7
keywords:
- Windows Перечислимые типы API платформы фильтрации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b1bd45efbe1a93ddeb0c95161aa52764bf1812ecc5f8e914e01317b657f251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069174"
---
# <a name="wfp-structures"></a>Структуры WFP

структуры API платформы фильтрации Windows (WFP) приведены ниже.

Структуры управления

-   [**ФВПМ \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
-   [**ФВПМ \_ CALLOUT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout0)
-   [**\_CHANGE0 выноска фвпм \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_change0)
-   [**\_Перечисление выноски фвпм \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_enum_template0)
-   [**\_SUBSCRIPTION0 выноска фвпм \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)
-   [**ФВПМ \_ классификация \_ OPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)
-   [**ФВПМ \_ классификация \_ OPTIONS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)
-   [**ФВПМ \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**\_ \_ Перечисление \_ TEMPLATE0 подключения фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**ФВПМ \_ подключение \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**ФВПМ \_ дисплей \_ data0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)
-   [**ФВПМ \_ FIELD0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_field0)
-   [**ФВПМ \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)
-   [**\_CHANGE0 Filter \_ фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)
-   [**\_CONDITION0 Filter \_ фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)
-   [**\_TEMPLATE0 фильтра фвпм \_ Enum \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_enum_template0)
-   [**\_SUBSCRIPTION0 Filter \_ фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)
-   [**ФВПМ \_ LAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer0)
-   [**\_ \_ Перечисление \_ TEMPLATE0 уровня фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_enum_template0)
-   [**ФВПМ \_ Layer \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)
-   \_событие фвпм NET \_ :
    -   [**Фвпм \_ NET \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event0) (Windows Vista)
    -   [**Фвпм \_ NET \_ EVENT1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event1) (Windows 7)
    -   [**Фвпм \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2) (Windows 8)
-   [**\_ALLOW0 фвпм NET, \_ возможности для событий \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**\_DROP0 фвпм NET, \_ возможности для событий \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**ФВПМ \_ net \_ event \_ классифицировать \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   ФВПМ \_ net \_ event \_ классификация \_ :
    -   [**Фвпм \_ \_классификация событий \_ NET \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0) (Windows Vista)
    -   [**Фвпм \_ NET \_ EVENT \_ классификация \_ DROP1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1) (Windows 7 и более поздних версий)
    -   [**Фвпм \_ \_классификация событий \_ NET \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2) (Windows 8)
-   [**ФВПМ \_ net \_ event \_ классификация \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**ФВПМ \_ net \_ event \_ Enum \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)
-   \_ \_ заголовок события фвпм NET \_ :
    -   [**Фвпм \_ \_ \_ HEADER0 событий NET**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) (Windows Vista)
    -   [**Фвпм \_ \_ \_ HEADER1 событий NET**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header1) (Windows 7)
    -   [**Фвпм \_ \_ \_ HEADER2 событий NET**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2) (Windows 8)
-   ФВПМ \_ \_ \_ \_ : ошибка EM в событии NET \_ .
    -   [**Фвпм \_ \_ \_ \_ \_ FAILURE0 EM для сетевого события**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0) (Windows Vista)
    -   [**Фвпм \_ NET \_ EVENT \_ IKEEXT \_ EM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1) (Windows 7 и более поздних версий)
-   \_сбой фвпм NET \_ event \_ IKEEXT \_ mm \_ :
    -   [**Фвпм \_ NET \_ EVENT \_ IKEEXT \_ MM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0) (Windows Vista)
    -   [**Фвпм \_ NET \_ EVENT \_ IKEEXT \_ MM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1) (Windows 7 и более поздних версий)
-   [**ФВПМ \_ net \_ event \_ IKEEXT \_ QM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0)
-   [**ФВПМ \_ net \_ event \_ IPSec \_ досп \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0)
-   [**ФВПМ \_ net \_ event \_ IPSec \_ ядра \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0)
-   [**ФВПМ \_ net \_ event \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)
-   [**ФВПМ \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)
-   [**\_CHANGE0 поставщика \_ фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)
-   \_контекст поставщика фвпм \_ :
    -   [**Фвпм \_ поставщик \_ CONTEXT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context0) (Windows Vista)
    -   [**Фвпм \_ противопоставщику \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context1) (Windows 7)
    -   \_CONTEXT2 поставщика фвпм \_ (Windows 8)
-   [**\_ \_ Контекст CHANGE0 поставщика \_ фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)
-   [**\_ \_ \_ TEMPLATE0 перечисление контекста поставщика фвпм \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0)
-   [**\_ \_ Контекст SUBSCRIPTION0 поставщика \_ фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)
-   [**\_ \_ Перечисление \_ TEMPLATE0 поставщика фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0)
-   [**\_SUBSCRIPTION0 поставщика \_ фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)
-   [**ФВПМ \_ SESSION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0)
-   [**\_ \_ TEMPLATE0 перечисление сеансов фвпм \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session_enum_template0)
-   [**ФВПМ \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_statistics0)
-   [**ФВПМ \_ SUBLAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)
-   [**\_ПОДУРОВЕНЬ фвпм \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_change0)
-   [**\_ \_ Перечисление TEMPLATE0 ПОДслоя фвпм \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_enum_template0)
-   [**\_ПОДУРОВЕНЬ фвпм \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)
-   [**ФВПМ \_ System \_ PORTS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)
-   [**ФВПМ \_ системные \_ порты \_ по \_ TYPE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0)
-   [**ФВПМ \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**\_ \_ SUBSCRIPTION0 события фвпм \_ VSWITCH**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

Общие структуры

-   [**FWP \_ байт \_ ARRAY6**](/windows/win32/api/fwptypes/ns-fwptypes-fwp_byte_array6)
-   [**FWP \_ байт \_ ARRAY16**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_array16)
-   [**\_ \_ большой двоичный объект FWP Byte**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_blob)
-   [**\_VALUE0 условие \_ FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)
-   [**FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)
-   [**FWP \_ , \_ тип соответствия**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)
-   [**\_ \_ Адрес \_ и маска FWP \_ v4**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)
-   [**\_ \_ Адрес \_ и маска FWP \_ V6**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)
-   [**FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)

Структуры IKE/AuthIP

-   \_метод проверки подлинности IKEEXT \_ :
    -   [**IKEEXT \_ \_METHOD0 проверки подлинности**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0) (Windows Vista)
    -   [**IKEEXT \_ \_METHOD1 проверки подлинности**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1) (Windows 7)
    -   [**IKEEXT \_ \_METHOD2 проверки подлинности**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2) (Windows 8)
-   [**\_EKUS0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_ \_ Корневой CONFIG0 сертификата IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   \_ \_ Проверка подлинности сертификата в IKEEXT:
    -   [**IKEEXT \_ сертификат \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0) (Windows Vista)
    -   [**IKEEXT \_ сертификат \_ AUTHENTICATION1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1) (Windows 7)
    -   [**IKEEXT \_ \_добавьте сертификата**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2) (Windows 8)
-   \_ \_ учетные данные сертификата IKEEXT:
    -   [**IKEEXT \_ сертификат \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0) (Windows Vista)
    -   [**IKEEXT \_ сертификат \_ учетные данные1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1) (Windows 7 и более поздних версий)
-   [**\_CRITERIA0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_ALGORITHM0 шифра IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   \_Общая \_ Статистика IKEEXT:
    -   [**IKEEXT \_ общие \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ COMMON \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1) (Windows 7 и более поздних версий)
-   [**\_PAIR0 cookie \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   \_учетные данные IKEEXT:
    -   [**IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0) (Windows Vista)
    -   [**IKEEXT \_ учетные данные1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1) (Windows 7 и более поздних версий)
-   \_пара учетных данных IKEEXT \_ :
    -   [**IKEEXT \_ учетные данные \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0) (Windows Vista)
    -   [**IKEEXT \_ учетные данные \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1) (Windows 7 и более поздних версий)
-   \_учетные данные IKEEXT:
    -   [**IKEEXT \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1) (Windows 7 и более поздних версий)
-   [**\_AUTHENTICATION0 EAP для IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   \_Политика EM для IKEEXT \_ :
    -   [**IKEEXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0) (Windows Vista)
    -   [**IKEEXT \_ EM \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1) (Windows 7)
    -   [**IKEEXT \_ EM \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2) (Windows 8)
-   [**\_ALGORITHM0 целостность IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   \_Общая статистика для IP- \_ версии IKEEXT \_ \_ \_ .
    -   [**IKEEXT \_ характерные для IP- \_ версии \_ \_ общие \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ характерные для IP- \_ версии \_ \_ общие \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1) (Windows 7 и более поздние версии)
-   \_Статистика кэймодуле для IP- \_ версии IKEEXT \_ \_ \_ :
    -   [**IKEEXT \_ версия IP-адреса \_ \_ конкретного \_ кэймодуле \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ версия IP-адреса \_ \_ конкретного \_ кэймодуле \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1) (Windows 7 и более поздние версии)
-   [**IKEEXT \_ IPv6 \_ КГА \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   \_Статистика кэймодулеа IKEEXT \_ :
    -   [**IKEEXT \_ KERBEROS \_ AUTHENTICATION0**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0) (Windows Vista и Windows 7)
    -   [**IKEEXT \_ \_AUTHENTICATION1 KERBEROS**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1) (Windows 8)
-   -   \_Статистика кэймодулеа IKEEXT \_ :
    -   [**IKEEXT \_ кэймодуле \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ кэймодуле \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1) (Windows 7 и более поздней версии)
-   [**\_Имя IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**\_ \_ \_ AUTHENTICATION0а NTLM v2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   \_Политика IKEEXT:
    -   [**IKEEXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0) (Windows Vista)
    -   [**IKEEXT \_ POLICY1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1) (Windows 7)
    -   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2) (Windows 8)
-   \_ \_ Проверка подлинности предварительно общего ключа для IKEEXT \_ :
    -   [**IKEEXT \_ AUTHENTICATION0 с общим \_ ключом \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0) (Windows Vista)
    -   [**IKEEXT \_ AUTHENTICATION1 с общим \_ ключом \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1) (Windows 7 и более поздней версии)
-   [**\_PROPOSAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**\_Зарезервированные \_ AUTHENTICATION0ные IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   \_сведения о сопоставлении безопасности IKEEXT \_ :
    -   [**IKEEXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0) (Windows Vista)
    -   [**IKEEXT \_ SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1) (Windows 7 и более поздние версии)
-   [**\_ \_ TEMPLATE0 перечисления SA для IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   \_Статистика IKEEXT:
    -   [**IKEEXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0) (Windows Vista)
    -   [**IKEEXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1) (Windows 7 и более поздних версий)
-   [**\_TRAFFIC0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

Структуры IPsec

-   [**IPSEC \_ address \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   \_ \_ Статистика удаления пакетов по протоколу IPsec \_ \_ :
    -   [**Протокол IPsec \_ \_ \_ пакетная обработка DROP \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0) (Windows Vista)
    -   [**Протокол IPsec \_ агрегатная \_ инструкция DROP \_ \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1) (Windows 7 и более поздние версии)
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
-   \_ЖЕТСПИ IPSec:
    -   [**Протокол IPsec \_ GETSPI0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0) (Windows Vista)
    -   [**Протокол IPsec \_ GETSPI1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1) (Windows 7 и более поздних версий)
-   [**\_ID0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**\_MANAGER0 ключей \_ IPSec**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_ \_ CALLBACKS0 ДИСПЕТЧЕРА ключей \_ IPSec**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   \_Политика ключей IPsec \_ :
    -   [**Протокол IPsec \_ \_POLICY0 ключей**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0) (Windows Vista и Windows 7)
    -   [**Протокол IPsec \_ \_POLICY1 ключа**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1) (Windows 8)
-   [**IPSEC \_ кэймодуле \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**\_PROPOSAL0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**\_SA0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**\_ \_ Проверка подлинности IPsec SA \_ и \_ шифр \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**IPSEC \_ SA \_ AUTH \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   \_пакет SA IPsec \_ :
    -   [**Протокол IPsec \_ SA \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0) (Windows Vista)
    -   [**Протокол IPsec \_ SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) (Windows 7 и более поздние версии)
-   [**\_ \_ INFORMATION0 шифрования IPSec \_ SA**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   \_контекст SA IPsec \_ :
    -   [**Протокол IPsec \_ SA \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0) (Windows Vista)
    -   [**Протокол IPsec \_ соглашение \_ SA**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1) (Windows 7 и более поздних версий)
-   [**\_ \_ CHANGE0 контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_ \_ TEMPLATE0 enum контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**\_ \_ SUBSCRIPTION0 контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   \_сведения SA IPsec \_ :
    -   [**Протокол IPsec \_ SA \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0) (Windows Vista)
    -   [**Протокол IPsec \_ SA \_ DETAILS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1) (Windows 7 и более поздние версии)
-   [**\_Перечисление SA IPsec \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**Бездействие IPSEC \_ SA \_ \_ TIMEOUT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**IPSEC \_ SA \_ LIFETIME0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**IPSEC \_ SA \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   \_Статистика IPsec:
    -   [**Протокол IPsec \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0) (Windows Vista)
    -   [**Протокол IPsec \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1) (Windows 7 и более поздних версий)
-   [**\_TOKEN0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   \_трафик IPSec:
    -   [**Протокол IPsec \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) (Windows Vista)
    -   [**Протокол IPsec \_ TRAFFIC1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1) (Windows 7 и более поздних версий)
-   \_Статистика трафика IPSec \_ :
    -   [**Протокол IPsec \_ \_STATISTICS0 трафика**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) (Windows Vista)
    -   [**Протокол IPsec \_ \_STATISTICS1 трафика**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1) (Windows 7 и более поздних версий)
-   \_Политика транспорта IPSec \_ :
    -   [**Протокол IPsec \_ транспортный \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) (Windows Vista)
    -   [**Протокол IPsec \_ \_POLICY1 транспорта**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1) (Windows 7)
    -   [**Протокол IPsec \_ транспортный \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2) (Windows 8)
-   [**\_ENDPOINT0 туннеля \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   \_ \_ конечные точки туннеля IPSec:
    -   [**Протокол IPsec \_ \_ENDPOINTS0 туннеля**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0) (Windows Vista)
    -   [**Протокол IPsec \_ \_ENDPOINTS1 туннеля**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) (Windows 7)
    -   [**Протокол IPsec \_ \_ENDPOINTS2 туннеля**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2) (Windows 8)
-   \_Политика туннеля IPSec \_ :
    -   [**Протокол IPsec \_ \_POLICY0 туннеля**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0) (Windows Vista)
    -   [**Протокол IPsec \_ \_POLICY1 туннеля**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1) (Windows 7)
    -   [**Протокол IPsec \_ \_POLICY2 туннеля**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2) (Windows 8)
-   [**IPSEC \_ v4 \_ UDP \_ ENCAPSULATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**Виртуальные IP IPSEC, \_ \_ Если \_ туннель \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




