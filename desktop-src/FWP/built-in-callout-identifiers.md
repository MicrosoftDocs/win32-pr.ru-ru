---
title: Встроенные идентификаторы выноски (Фвпму. h)
description: Идентификаторы для функций вызова, встроенных в платформу фильтрации Windows (WFP), представляются с помощью GUID. Эти идентификаторы определяются следующим образом.
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
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989325"
---
# <a name="built-in-callout-identifiers"></a><span data-ttu-id="2d265-104">Встроенные идентификаторы выноски</span><span class="sxs-lookup"><span data-stu-id="2d265-104">Built-in Callout Identifiers</span></span>

<span data-ttu-id="2d265-105">Идентификаторы для функций вызова, встроенных в платформу фильтрации Windows (WFP), представляются с помощью GUID.</span><span class="sxs-lookup"><span data-stu-id="2d265-105">The identifiers for the callout functions that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="2d265-106">Эти идентификаторы определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2d265-106">These identifiers are defined as follows.</span></span>

<span data-ttu-id="2d265-107">Суффиксы v4 и V6 в конце идентификаторов выноски указывают, предназначен ли вызов для сетевого стека IPv4 или для сетевого стека IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d265-107">The V4 and V6 suffixes at the end of the callout identifiers indicate whether the callout is for the IPv4 network stack or for the IPv6 network stack.</span></span>

<dl> <dt>

<span data-ttu-id="2d265-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**\_Вызов фвпм \_ \_ входящего транспорта \_ IPSec \_ v4/фвпм (входящий \_ \_ \_ трафик \_ IPSec \_ версии 4)**</span><span class="sxs-lookup"><span data-stu-id="2d265-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-109">Проверяет, что каждый полученный пакет, который должен быть доставлен по сопоставлению безопасности транспортного режима, безопасен.</span><span class="sxs-lookup"><span data-stu-id="2d265-109">Verifies that each received packet that is supposed to arrive over a transport mode security association arrives securely.</span></span>

<span data-ttu-id="2d265-110">Эта выноска применима на транспортном уровне.</span><span class="sxs-lookup"><span data-stu-id="2d265-110">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**Исходящий \_ \_ \_ транспорт IPSec \_ \_ IPv4/ФВПМ \_ с \_ \_ \_ \_ вызываемым фвпм**</span><span class="sxs-lookup"><span data-stu-id="2d265-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-112">Указывает IPsec на исходящий трафик, который должен быть защищен с помощью сопоставлений безопасности транспортного режима.</span><span class="sxs-lookup"><span data-stu-id="2d265-112">Indicates to IPsec the outbound traffic that must be secured over transport mode security associations.</span></span>

<span data-ttu-id="2d265-113">Эта выноска применима на транспортном уровне.</span><span class="sxs-lookup"><span data-stu-id="2d265-113">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**ФВПМ \_ выноска \_ \_ входящего \_ туннеля IPSec \_ v4/фвпм с вызовом входящего \_ \_ трафика IPsec версии \_ \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="2d265-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-115">Проверяет, что каждый полученный пакет, который должен приступать через сопоставление безопасности режима туннелирования, прибывает безопасно.</span><span class="sxs-lookup"><span data-stu-id="2d265-115">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="2d265-116">Эта выноска применима на транспортном уровне.</span><span class="sxs-lookup"><span data-stu-id="2d265-116">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**Исходящий \_ \_ \_ туннель IPsec \_ \_ v4/фвпм \_ в \_ \_ \_ \_ выноски фвпм**</span><span class="sxs-lookup"><span data-stu-id="2d265-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-118">Указывает IPsec на исходящий трафик, который должен быть защищен с помощью взаимосвязей безопасности режима туннелирования.</span><span class="sxs-lookup"><span data-stu-id="2d265-118">Indicates to IPsec the outbound traffic that must be secured over tunnel mode security associations.</span></span>

<span data-ttu-id="2d265-119">Эта выноска применима на транспортном уровне.</span><span class="sxs-lookup"><span data-stu-id="2d265-119">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**ФВПМ \_ выноска \_ \_ перенаправления \_ входящего \_ туннеля IPSec \_ v4/фвпм \_ \_ \_ \_ \_ \_ с вызываемым перенаправлением IPSec V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-121">Проверяет, что каждый полученный пакет, который должен приступать через сопоставление безопасности режима туннелирования, прибывает безопасно.</span><span class="sxs-lookup"><span data-stu-id="2d265-121">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="2d265-122">Эта выноска применима на уровне перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2d265-122">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**ФВПМ \_ выноска \_ IPSec \_ Forwarded \_ Outbound \_ туннели \_ v4/фвпм \_ выноски \_ IPSec с \_ прямым \_ исходящим \_ туннелем \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-124">Указывает IPsec на исходящий трафик, который должен быть защищен при взаимосвязи безопасности режима туннелирования.</span><span class="sxs-lookup"><span data-stu-id="2d265-124">Indicates to IPsec the outbound traffic that must be secured over a tunnel mode security association.</span></span>

<span data-ttu-id="2d265-125">Эта выноска применима на уровне перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2d265-125">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**ФВПМ \_ выноска \_ IPSec " \_ Входящие" \_ инициирует \_ безопасный \_ вызов v4/фвпм \_ выноску \_ IPSec инициирующее получение \_ \_ \_ безопасный \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-127">Проверяет, что каждое входящее подключение, которое должно быть защищено, приступает безопасно.</span><span class="sxs-lookup"><span data-stu-id="2d265-127">Verifies that each incoming connection that is supposed to arrive secure arrives securely.</span></span>

<span data-ttu-id="2d265-128">Эта выноска применима на уровне приема ALE.</span><span class="sxs-lookup"><span data-stu-id="2d265-128">This callout is applicable at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**Прием \_ \_ \_ \_ ALE входящего туннеля IPSec \_ \_ \_ IPv4/фвпм \_ \_ \_ \_ \_ \_ \_ с вызываемым фвпм**</span><span class="sxs-lookup"><span data-stu-id="2d265-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-130">Разрешает использование пакетов IP-IP в туннельном режиме IPsec, если они классифицируются на уровне принятия ALE.</span><span class="sxs-lookup"><span data-stu-id="2d265-130">Permits the IPsec tunnel mode IP-in-IP packets when they get classified at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**ФВПМ \_ выноска \_ \_ ALE IPSec \_ Connect \_ v4/фвпм \_ выноски IPSec \_ \_ \_ \_ V6 Connect**</span><span class="sxs-lookup"><span data-stu-id="2d265-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V4 / FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-132">Применяет модификаторы политики IPsec к клиентским приложениям.</span><span class="sxs-lookup"><span data-stu-id="2d265-132">Applies IPsec policy modifiers to client applications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**ФВПМ \_ выноска \_ IPSec \_ досп \_ Forward \_ v4/фвпм \_ выноска \_ IPSec \_ досп \_ Forward \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V4 / FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-134">Сообщает о защите IPsec в DoS, что трафик должен проверяться на наличие потенциальных DoS, и может потребоваться ограничить частоту.</span><span class="sxs-lookup"><span data-stu-id="2d265-134">Signals to IPsec DoS Protection that traffic needs to be verified for potential DoS and may need to be rate limited.</span></span>

> [!Note]  
> <span data-ttu-id="2d265-135">Доступно только в Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2d265-135">Available only in Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**ФВПМ \_ выноски \_ WFP \_ транспортного уровня версии \_ \_ 4 WFP \_ без вмешательства \_ \_ \_ \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d265-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V4\_SILENT\_DROP / FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V6\_SILENT\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-137">Реализует фильтрацию в скрытом режиме путем автоматического удаления всех входящих пакетов, для которых у TCP нет конечной точки прослушивания.</span><span class="sxs-lookup"><span data-stu-id="2d265-137">Implements stealth-mode filtering by silently dropping all incoming packets for which TCP does not have a listening endpoint.</span></span>

<span data-ttu-id="2d265-138">Эта выноска применима на уровне отклонения входящего транспорта.</span><span class="sxs-lookup"><span data-stu-id="2d265-138">This callout is applicable at the inbound transport discard layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**Выноска ФВПМ: \_ \_ TCP \_ Chimney \_ Connect \_ Layer \_ v4/фвпм \_ выноска \_ TCP \_ Chimney \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-140">Включает или отключает разгрузку TCP Chimney для каждого исходящего подключения.</span><span class="sxs-lookup"><span data-stu-id="2d265-140">Enables or disables TCP chimney offload for each outgoing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**ФВПМ \_ выноска \_ \_ приема TCP Chimney \_ \_ \_ версии 4 и фвпм \_ выноски \_ TCP \_ Chimney \_ Accept \_ уровня \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-142">Включает или отключает разгрузку TCP Chimney для каждого входящего подключения.</span><span class="sxs-lookup"><span data-stu-id="2d265-142">Enables or disables TCP chimney offload for each incoming connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**ФВПМ \_ выноски \_ \_ параметров \_ Проверка подлинности \_ подключения \_ Layer \_ v4/фвпм \_ \_ \_ параметры набора \_ проверки подлинности \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-144">Задает параметры классификации исходящих потоков.</span><span class="sxs-lookup"><span data-stu-id="2d265-144">Sets classify options on outbound flows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**ФВПМ \_ выноски \_ \_ параметров \_ Проверка подлинности \_ \_ приема recv \_ уровень \_ v4/фвпм \_ \_ параметры набора выноски \_ \_ Проверка подлинности \_ recv \_ \_ уровень \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-146">Задает параметры классификации входящих потоков.</span><span class="sxs-lookup"><span data-stu-id="2d265-146">Sets classify options on inbound flows.</span></span>

> [!Note]  
> <span data-ttu-id="2d265-147">Доступно только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2d265-147">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**ФВПМ \_ выноска \_ зарезервированная \_ Проверка подлинности \_ Connect \_ Layer \_ v4/фвпм \_ \_ зарезервированная \_ Проверка подлинности \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-149">Этот идентификатор зарезервирован для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="2d265-149">This identifier is reserved for internal use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**ФВПМ \_ выноска обхода выносной стороны, прослушиваемая \_ \_ \_ \_ \_ V6/фвпм \_ выноски \_ TEREDO \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_LISTEN\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-151">Сообщает службе Teredo, что для приложения требуется адрес Teredo.</span><span class="sxs-lookup"><span data-stu-id="2d265-151">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="2d265-152">Для Windows 7 и более поздних версий используйте **фвпм \_ выноску " \_ обходной выносной стороны" \_ \_ \_ Listen \_ V6**.</span><span class="sxs-lookup"><span data-stu-id="2d265-152">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**Назначение ресурсов ALE ФВПМ выноски внешнего \_ вызова \_ \_ \_ \_ \_ \_ V6 или фвпм \_ выноски \_ TEREDO \_ \_ \_ \_ в выпуске IPv6**</span><span class="sxs-lookup"><span data-stu-id="2d265-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_RESOURCE\_ASSIGNMENT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-154">Сообщает службе Teredo, что для приложения требуется адрес Teredo.</span><span class="sxs-lookup"><span data-stu-id="2d265-154">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="2d265-155">Для Windows 7 и более поздних версий следует использовать **\_ \_ \_ \_ \_ \_ назначение \_ ресурсов ALE фвпм** в выпуске границы выноски.</span><span class="sxs-lookup"><span data-stu-id="2d265-155">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**\_ \_ \_ \_ \_ Назначение ресурсов ALE \_ для обхода \_ фвпм на границе выноски**</span><span class="sxs-lookup"><span data-stu-id="2d265-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V4**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-157">Этот идентификатор зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="2d265-157">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**\_Прослушиваемый ALE фвпм выноски на \_ границе \_ \_ \_ \_ v4**</span><span class="sxs-lookup"><span data-stu-id="2d265-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V4**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-159">Этот идентификатор зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="2d265-159">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**ФВПМ \_ выноска \_ \_ шаблоны TCP \_ Connect \_ Layer \_ v4/фвпм \_ выноски \_ TCP \_ Templates \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-161">Применяет параметры шаблона TCP для сопоставления исходящих соединений.</span><span class="sxs-lookup"><span data-stu-id="2d265-161">Applies TCP template settings for matching outgoing connections.</span></span>

> [!Note]  
> <span data-ttu-id="2d265-162">Доступно только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2d265-162">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d265-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**\_ \_ Шаблоны TCP-фвпм выноски \_ \_ принимают \_ уровень \_ IPv4/фвпм \_ выноски для \_ \_ шаблонов TCP \_ принимают \_ уровень \_ V6**</span><span class="sxs-lookup"><span data-stu-id="2d265-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2d265-164">Применяет параметры шаблона TCP для сопоставления входящих подключений.</span><span class="sxs-lookup"><span data-stu-id="2d265-164">Applies TCP template settings for matching incoming connections.</span></span>

> [!Note]  
> <span data-ttu-id="2d265-165">Доступно только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2d265-165">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d265-166">Требования</span><span class="sxs-lookup"><span data-stu-id="2d265-166">Requirements</span></span>



| <span data-ttu-id="2d265-167">Требование</span><span class="sxs-lookup"><span data-stu-id="2d265-167">Requirement</span></span> | <span data-ttu-id="2d265-168">Значение</span><span class="sxs-lookup"><span data-stu-id="2d265-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d265-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d265-169">Minimum supported client</span></span><br/> | <span data-ttu-id="2d265-170">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d265-170">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2d265-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d265-171">Minimum supported server</span></span><br/> | <span data-ttu-id="2d265-172">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d265-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2d265-173">Header</span><span class="sxs-lookup"><span data-stu-id="2d265-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d265-174"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d265-174"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





