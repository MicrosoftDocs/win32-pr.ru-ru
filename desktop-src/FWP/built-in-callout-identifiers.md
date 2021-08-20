---
title: Встроенные идентификаторы выноски (Фвпму. h)
description: идентификаторы для вызываемых функций, встроенных в платформу фильтрации Windows (WFP), представляются идентификатором GUID. Эти идентификаторы определяются следующим образом.
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d430f44e6e72f575d5e2ff0fd30681c04e81892f0438f0508be994d53c1643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151430"
---
# <a name="built-in-callout-identifiers"></a>Встроенные идентификаторы выноски

идентификаторы для вызываемых функций, встроенных в платформу фильтрации Windows (WFP), представляются идентификатором GUID. Эти идентификаторы определяются следующим образом.

Суффиксы v4 и V6 в конце идентификаторов выноски указывают, предназначен ли вызов для сетевого стека IPv4 или для сетевого стека IPv6.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**\_Вызов фвпм \_ \_ входящего транспорта \_ IPSec \_ v4/фвпм (входящий \_ \_ \_ трафик \_ IPSec \_ версии 4)** 
</dt> <dd> <dl> <dt>



Проверяет, что каждый полученный пакет, который должен быть доставлен по сопоставлению безопасности транспортного режима, безопасен.

Эта выноска применима на транспортном уровне.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**Исходящий \_ \_ \_ транспорт IPSec \_ \_ IPv4/ФВПМ \_ с \_ \_ \_ \_ вызываемым фвпм** 
</dt> <dd> <dl> <dt>



Указывает IPsec на исходящий трафик, который должен быть защищен с помощью сопоставлений безопасности транспортного режима.

Эта выноска применима на транспортном уровне.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**ФВПМ \_ выноска \_ \_ входящего \_ туннеля IPSec \_ v4/фвпм с вызовом входящего \_ \_ трафика IPsec версии \_ \_ \_ 6** 
</dt> <dd> <dl> <dt>



Проверяет, что каждый полученный пакет, который должен приступать через сопоставление безопасности режима туннелирования, прибывает безопасно.

Эта выноска применима на транспортном уровне.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**Исходящий \_ \_ \_ туннель IPsec \_ \_ v4/фвпм \_ в \_ \_ \_ \_ выноски фвпм** 
</dt> <dd> <dl> <dt>



Указывает IPsec на исходящий трафик, который должен быть защищен с помощью взаимосвязей безопасности режима туннелирования.

Эта выноска применима на транспортном уровне.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**ФВПМ \_ выноска \_ \_ перенаправления \_ входящего \_ туннеля IPSec \_ v4/фвпм \_ \_ \_ \_ \_ \_ с вызываемым перенаправлением IPSec V6**
</dt> <dd> <dl> <dt>



Проверяет, что каждый полученный пакет, который должен приступать через сопоставление безопасности режима туннелирования, прибывает безопасно.

Эта выноска применима на уровне перенаправления.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**ФВПМ \_ выноска \_ IPSec \_ Forwarded \_ Outbound \_ туннели \_ v4/фвпм \_ выноски \_ IPSec с \_ прямым \_ исходящим \_ туннелем \_ V6**
</dt> <dd> <dl> <dt>



Указывает IPsec на исходящий трафик, который должен быть защищен при взаимосвязи безопасности режима туннелирования.

Эта выноска применима на уровне перенаправления.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**ФВПМ \_ выноска \_ IPSec " \_ Входящие" \_ инициирует \_ безопасный \_ вызов v4/фвпм \_ выноску \_ IPSec инициирующее получение \_ \_ \_ безопасный \_ V6** 
</dt> <dd> <dl> <dt>



Проверяет, что каждое входящее подключение, которое должно быть защищено, приступает безопасно.

Эта выноска применима на уровне приема ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**Прием \_ \_ \_ \_ ALE входящего туннеля IPSec \_ \_ \_ IPv4/фвпм \_ \_ \_ \_ \_ \_ \_ с вызываемым фвпм**
</dt> <dd> <dl> <dt>



Разрешает использование пакетов IP-IP в туннельном режиме IPsec, если они классифицируются на уровне принятия ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**ФВПМ \_ выноска \_ \_ ALE IPSec \_ Connect \_ v4/фвпм \_ выноски IPSec \_ \_ \_ \_ V6 Connect**
</dt> <dd> <dl> <dt>



Применяет модификаторы политики IPsec к клиентским приложениям.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**ФВПМ \_ выноска \_ IPSec \_ досп \_ Forward \_ v4/фвпм \_ выноска \_ IPSec \_ досп \_ Forward \_ V6**
</dt> <dd> <dl> <dt>



Сообщает о защите IPsec в DoS, что трафик должен проверяться на наличие потенциальных DoS, и может потребоваться ограничить частоту.

> [!Note]  
> доступно только в Windows 7 и Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**ФВПМ \_ выноски \_ WFP \_ транспортного уровня версии \_ \_ 4 WFP \_ без вмешательства \_ \_ \_ \_ \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Реализует фильтрацию в скрытом режиме путем автоматического удаления всех входящих пакетов, для которых у TCP нет конечной точки прослушивания.

Эта выноска применима на уровне отклонения входящего транспорта.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**Выноска ФВПМ: \_ \_ TCP \_ Chimney \_ Connect \_ Layer \_ v4/фвпм \_ выноска \_ TCP \_ Chimney \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Включает или отключает разгрузку TCP Chimney для каждого исходящего подключения.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**ФВПМ \_ выноска \_ \_ приема TCP Chimney \_ \_ \_ версии 4 и фвпм \_ выноски \_ TCP \_ Chimney \_ Accept \_ уровня \_ V6**
</dt> <dd> <dl> <dt>



Включает или отключает разгрузку TCP Chimney для каждого входящего подключения.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**ФВПМ \_ выноски \_ \_ параметров \_ Проверка подлинности \_ подключения \_ Layer \_ v4/фвпм \_ \_ \_ параметры набора \_ проверки подлинности \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Задает параметры классификации исходящих потоков.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**ФВПМ \_ выноски \_ \_ параметров \_ Проверка подлинности \_ \_ приема recv \_ уровень \_ v4/фвпм \_ \_ параметры набора выноски \_ \_ Проверка подлинности \_ recv \_ \_ уровень \_ V6**
</dt> <dd> <dl> <dt>



Задает параметры классификации входящих потоков.

> [!Note]  
> доступно только в Windows 8 и Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**ФВПМ \_ выноска \_ зарезервированная \_ Проверка подлинности \_ Connect \_ Layer \_ v4/фвпм \_ \_ зарезервированная \_ Проверка подлинности \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Этот идентификатор зарезервирован для внутреннего использования.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**ФВПМ \_ выноска обхода выносной стороны, прослушиваемая \_ \_ \_ \_ \_ V6/фвпм \_ выноски \_ TEREDO \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Сообщает службе Teredo, что для приложения требуется адрес Teredo.

> [!Note]  
> для Windows 7 и более поздних версий используйте **фвпм \_ выноску " \_ обходные выносные стороны" \_ \_ \_ LISTEN \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**Назначение ресурсов ALE ФВПМ выноски внешнего \_ вызова \_ \_ \_ \_ \_ \_ V6 или фвпм \_ выноски \_ TEREDO \_ \_ \_ \_ в выпуске IPv6**
</dt> <dd> <dl> <dt>



Сообщает службе Teredo, что для приложения требуется адрес Teredo.

> [!Note]  
> для Windows 7 и более поздних версий используйте **\_ \_ \_ \_ \_ \_ назначение ресурсов \_ ALE фвпм для обхода ребра**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**\_ \_ \_ \_ \_ Назначение ресурсов ALE \_ для обхода \_ фвпм на границе выноски** 
</dt> <dd> <dl> <dt>



Этот идентификатор зарезервирован для использования в будущем.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**\_Прослушиваемый ALE фвпм выноски на \_ границе \_ \_ \_ \_ v4**
</dt> <dd> <dl> <dt>



Этот идентификатор зарезервирован для использования в будущем.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**ФВПМ \_ выноска \_ \_ шаблоны TCP \_ Connect \_ Layer \_ v4/фвпм \_ выноски \_ TCP \_ Templates \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Применяет параметры шаблона TCP для сопоставления исходящих соединений.

> [!Note]  
> доступно только в Windows 8 и Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**\_ \_ Шаблоны TCP-фвпм выноски \_ \_ принимают \_ уровень \_ IPv4/фвпм \_ выноски для \_ \_ шаблонов TCP \_ принимают \_ уровень \_ V6**
</dt> <dd> <dl> <dt>



Применяет параметры шаблона TCP для сопоставления входящих подключений.

> [!Note]  
> доступно только в Windows 8 и Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



 

 





