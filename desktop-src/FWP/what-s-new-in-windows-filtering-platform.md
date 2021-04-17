---
title: Новые возможности платформы фильтрации Windows
description: Windows 8 и Windows Server 2012 представляют новые элементы программирования платформы фильтрации Windows.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339875"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Новые возможности платформы фильтрации Windows

Windows 8 и Windows Server 2012 представляют новые элементы программирования платформы фильтрации Windows. Новые функции включают следующие:

-   *Фильтрация уровня 2*: обеспечивает доступ к уровню L2 (Mac), позволяя фильтровать трафик на этом уровне.
-   *Фильтрация vSwitch*: позволяет проверять и изменять пакеты vSwitch. Фильтры и выноски WFP можно использовать во входных и выходных данных vSwitch.
-   *Управление контейнерами приложений*: разрешает доступ к сведениям о контейнерах приложений и проблемах с подключением к сетевой изоляции.
-   *Обновления IPSec*: расширенные функции IPSec, включая мониторинг состояния подключения, выбор сертификатов и управление ключами.

В комплект драйверов для Windows также входит информация об [изменениях в WFP для Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Обновления API Windows 8

Для Windows 8 и Windows Server 2012 были добавлены многие новые API-интерфейсы.

## <a name="new-functions"></a>Новые функции

-   [**ФВПМ \_ net \_ event \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [**FwpmConnectionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [**FwpmConnectionDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [**FwpmConnectionEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [**FwpmConnectionGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [**FwpmConnectionGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [**FwpmConnectionSetSecurityInfo0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [**FwpmConnectionSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [**FwpmConnectionSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [**FwpmConnectionUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [**FwpmProviderContextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [**FwpmProviderContextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [**FwpmProviderContextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [**FwpmProviderContextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [**FwpmvSwitchEventsGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [**FwpmvSwitchEventsSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [**FwpmvSwitchEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [**FwpmvSwitchEventUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [**\_ \_ \_ \_ CHECK0 диктофона ключей диспетчера ключей \_ IPSec**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**\_Диспетчер ключей \_ IPSec \_ определяет \_ Key0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**\_ \_ \_ Уведомление \_ Key0 диспетчера ключей IPsec**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**\_ \_ CALLBACK0 контекста SA \_ IPSec**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [**нетворкисолатиондиагносеконнектфаилуреанджетинфо**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [**нетворкисолатионенумаппконтаинерс**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [**нетворкисолатионенумератеаппконтаинеррулес**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [**нетворкисолатионфриаппконтаинерс**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [**нетворкисолатионжетаппконтаинерконфиг**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [**нетворкисолатионрегистерфораппконтаинерчанжес**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [**нетворкисолатионсетаппконтаинерконфиг**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [**нетворкисолатионсетупаппконтаинербинариес**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [**\_ \_ обратный вызов изменений Pac \_ fn**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Новые структуры

-   [**\_METHOD2 проверки подлинности IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_EKUS0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_Добавьте сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CRITERIA0 сертификата \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_POLICY2 EM для IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**IKEEXT \_ Kerberos \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**\_POLICY2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_MANAGER0 ключей \_ IPSec**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_ \_ CALLBACKS0 ДИСПЕТЧЕРА ключей \_ IPSec**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_POLICY1 ключей \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**\_ \_ CHANGE0 контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_ \_ SUBSCRIPTION0 контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**\_POLICY2 транспорта \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_ENDPOINT0 туннеля \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_ENDPOINTS2 туннеля \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_POLICY2 туннеля \_ IPSec**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**ФВПМ \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**\_ \_ Перечисление \_ TEMPLATE0 подключения фвпм**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**ФВПМ \_ подключение \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**ФВПМ \_ net \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**\_ALLOW0 фвпм NET, \_ возможности для событий \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**\_DROP0 фвпм NET, \_ возможности для событий \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**ФВПМ \_ net \_ event \_ классифицировать \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**ФВПМ \_ net \_ event \_ классифицировать \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**ФВПМ \_ net \_ event \_ классификация \_ DROP \_ MAC0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**ФВПМ \_ net \_ event \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**\_CONTEXT2 поставщика \_ фвпм**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**ФВПМ \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**\_ \_ SUBSCRIPTION0 события фвпм \_ VSWITCH**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Новые перечислимые типы

-   [**\_ \_ тип сети VSWITCH \_ FWP**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**\_ \_ \_ Тип возможности сети фвпм \_ APPC**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**\_ \_ Тип события подключения \_ фвпм**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**\_ \_ Тип события фвпм \_ VSWITCH**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**\_ \_ тип имени критерия сертификата IKEEXT \_ \_**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**\_ \_ \_ TYPE0 события контекста SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Новые идентификаторы слоя фильтрации

[**Фильтрация идентификаторов слоя:**](management-filtering-layer-identifiers-.md)

-   ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet
-   \_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_
-   \_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм
-   \_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_
-   уровень ФВПМ входящий трафик \_ \_ \_ VSWITCH \_ Ethernet
-   исходящий слой ФВПМ для \_ \_ \_ vSwitch \_ Ethernet
-   Уровень \_ фвпм \_ входящего трафика \_ VSWITCH \_ \_ v4/фвпм, входящий в \_ \_ \_ транспорт vSwitch \_ \_ версии 6
-   Исходящий уровень ФВПМ, \_ \_ \_ \_ транспорт vSwitch v4/фвпм, исходящий \_ \_ \_ \_ \_ транспорт vSwitch \_ версии 6

## <a name="new-filtering-condition-identifiers"></a>Новые идентификаторы условий фильтрации

[**Фильтрация идентификаторов условий:**](filtering-condition-identifiers-.md)

-   \_ \_ \_ MAC-адрес интерфейса условия фвпм \_
-   \_ \_ \_ локальный \_ адрес Mac условия фвпм
-   \_ \_ \_ Удаленный адрес фвпм условия \_ Mac
-   \_ \_ тип ETHER условия \_ фвпм
-   \_ \_ ИД виртуальной ЛС для условия фвпм \_
-   \_ \_ порт NDIS условия \_ фвпм
-   \_ \_ \_ тип носителя NDIS условия \_ фвпм
-   \_ \_ \_ \_ тип физического носителя \_ для условия фвпм NDIS
-   \_ \_ Флаги фвпм условия L2 \_
-   \_ \_ \_ \_ тип ЛОКАЛЬНОГО адреса Mac условия \_ фвпм
-   \_ \_ \_ \_ Тип удаленного адреса Mac условия \_ фвпм
-   \_ \_ \_ идентификатор пакета ALE фвпм \_ Condition
-   \_ \_ Исходный Mac- \_ \_ адрес условия фвпм
-   ФВПМ \_ условие для \_ Mac- \_ \_ адреса назначения
-   \_ \_ \_ \_ тип ИСХОДНОГО адреса Mac условия \_ фвпм
-   \_ \_ \_ \_ тип адреса назначения для фвпм условия Mac \_
-   \_ \_ Исходный IP-адрес условия \_ фвпм \_
-   \_ \_ порт назначения IP-адреса фвпм Condition \_ \_
-   Идентификатор ФВПМ для \_ состояния \_ VSWITCH \_
-   \_ \_ \_ тип сети VSWITCH фвпм \_ Condition
-   ФВПМ \_ условие \_ \_ идентификации исходного \_ интерфейса \_ VSWITCH
-   \_ \_ \_ \_ идентификатор конечного интерфейса VSWITCH \_ для фвпм условия
-   ФВПМ \_ условие \_ с \_ \_ идентификатором исходной виртуальной машины VSWITCH \_
-   ФВПМ \_ условие \_ , \_ \_ идентификатор целевой виртуальной машины VSWITCH \_
-   ФВПМ \_ условие \_ , \_ \_ Тип исходного интерфейса \_ VSWITCH
-   \_ \_ \_ \_ идентификатор сети клиента VSWITCH с условием фвпм \_

## <a name="new-filtering-condition-flags"></a>Новые флаги условий фильтрации

[**Флаги условия фильтрации:**](filtering-condition-flags-.md)

-   \_флаг условия \_ FWP \_ является \_ прокси- \_ соединением
-   \_флаг условия \_ FWP \_ — \_ это \_ замыкание APPCONTAINER
-   \_флаг условия \_ FWP \_ не \_ является \_ \_ замыканием APPCONTAINER
-   \_флаг условия \_ FWP \_ \_ учитывает \_ политику \_ авторизации
-   \_Условие FWP \_ L2 \_ — \_ собственная \_ сеть Ethernet
-   \_Условие FWP \_ L2 \_ — \_ Wi-Fi
-   \_Условие FWP \_ L2 \_ — \_ мобильное \_ широкополосное подключение
-   \_Условие FWP \_ L2 \_ — \_ \_ прямые \_ данные WiFi
-   \_Условие FWP \_ L2 \_ — \_ VM2VM
-   \_Условие FWP \_ L2 \_ имеет \_ неправильный формат \_ пакета
-   \_Условие FWP \_ L2 \_ — \_ \_ Группа фрагментов IP-адресов \_
-   \_Условие FWP \_ L2 \_ , \_ Если \_ имеется соединитель

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Обновления Windows 7 для платформы фильтрации Windows

В документе « [новые возможности платформы фильтрации Windows]() » подробно описаны многие обновления, внесенные в Windows 7. Сведения также доступны в комплекте драйверов Windows на [изменениях WFP для Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).

 

 