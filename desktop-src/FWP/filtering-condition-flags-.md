---
title: Флаги условий фильтрации (Фвптипес. h)
description: Флаги условий фильтрации платформы фильтрации Windows (WFP) представлены битовыми битами.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803514"
---
# <a name="filtering-condition-flags"></a><span data-ttu-id="36e41-103">Флаги условия фильтрации</span><span class="sxs-lookup"><span data-stu-id="36e41-103">Filtering Condition Flags</span></span>

<span data-ttu-id="36e41-104">Флаги условий фильтрации платформы фильтрации Windows (WFP) представлены битовыми битами.</span><span class="sxs-lookup"><span data-stu-id="36e41-104">The Windows Filtering Platform (WFP) filtering condition flags are each represented by a bitfield.</span></span>

<span data-ttu-id="36e41-105">Эти флаги и слои фильтрации, где их можно использовать, определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="36e41-105">These flags and the filtering layers where they can be used are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="36e41-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**\_флаг условия \_ FWP \_ — \_ замыкание на себя**</span><span class="sxs-lookup"><span data-stu-id="36e41-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-107">Проверяет, является ли сетевой трафик замыканием на себя.</span><span class="sxs-lookup"><span data-stu-id="36e41-107">Tests if the network traffic is loopback traffic.</span></span>

<span data-ttu-id="36e41-108">Фильтрация слоев:</span><span class="sxs-lookup"><span data-stu-id="36e41-108">Filtering layers:</span></span>

-   <span data-ttu-id="36e41-109">ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-109">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-110">ФВПМ \_ уровень \_ исходящей \_ иппаккет \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-110">FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-111">ФВПМ \_ уровень \_ входящего \_ транспорта \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-111">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-112">\_Исходящий \_ транспорт уровня фвпм \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-112">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-113">\_Поток уровня \_ фвпм \_ {v4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-113">FWPM\_LAYER\_STREAM\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="36e41-114">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-114">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="36e41-115">\_ \_ Ошибка входящего ICMP уровня фвпм \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-115">FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="36e41-116">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-116">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="36e41-117">\_Исходящая \_ \_ Ошибка ICMP уровня фвпм \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-117">FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="36e41-118">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-118">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="36e41-119">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-119">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-120">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-120">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="36e41-121">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-121">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="36e41-122">\_ \_ Установлен поток ALE уровня фвпм \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-122">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="36e41-123">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-123">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**\_флаг условия \_ FWP \_ \_ защищен IPsec \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_SECURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-125">Проверяет, защищен ли сетевой трафик протоколом IPsec.</span><span class="sxs-lookup"><span data-stu-id="36e41-125">Tests if the network traffic is protected by IPsec.</span></span>

<span data-ttu-id="36e41-126">Фильтрация слоев:</span><span class="sxs-lookup"><span data-stu-id="36e41-126">Filtering layers:</span></span>

-   <span data-ttu-id="36e41-127">ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-127">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-128">ФВПМ \_ уровень \_ входящего \_ транспорта \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-128">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-129">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-129">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-130">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-130">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**\_флаг условия FWP — повторная \_ \_ \_ авторизация**</span><span class="sxs-lookup"><span data-stu-id="36e41-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-132">Проверяет изменение политики в отличие от нового соединения.</span><span class="sxs-lookup"><span data-stu-id="36e41-132">Tests for a policy change as opposed to a new connection.</span></span>

<span data-ttu-id="36e41-133">Фильтрация слоев:</span><span class="sxs-lookup"><span data-stu-id="36e41-133">Filtering layers:</span></span>

-   <span data-ttu-id="36e41-134">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-134">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-135">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-135">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**\_флаг условия \_ FWP \_ является \_ привязкой с подстановочными знаками \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-137">Проверяет, указал ли приложение адрес с подстановочными знаками при привязке к адресу локальной сети.</span><span class="sxs-lookup"><span data-stu-id="36e41-137">Tests if the application specified a wildcard address when binding to a local network address.</span></span>

<span data-ttu-id="36e41-138">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-138">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-139">\_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-139">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**\_флаг условия \_ FWP \_ — \_ необработанная \_ Конечная точка**</span><span class="sxs-lookup"><span data-stu-id="36e41-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-141">Проверяет, является ли локальная конечная точка, отправляющей и принимающая трафик, конечной точкой необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="36e41-141">Tests if the local endpoint that is sending and receiving traffic is a raw endpoint.</span></span>

<span data-ttu-id="36e41-142">Фильтрация слоев:</span><span class="sxs-lookup"><span data-stu-id="36e41-142">Filtering layers:</span></span>

-   <span data-ttu-id="36e41-143">ФВПМ \_ уровень \_ входящего \_ транспорта \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-143">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="36e41-144">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-144">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="36e41-145">\_Исходящий \_ транспорт уровня фвпм \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-145">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="36e41-146">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-146">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="36e41-147">\_ \_ Данные ДАТАГРАММ уровня \_ фвпм \_ {v4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-147">FWPM\_LAYER\_DATAGRAM\_DATA\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="36e41-148">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-148">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="36e41-149">\_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-149">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-150">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-150">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-151">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-151">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**\_флаг условия \_ FWP \_ — \_ фрагмент**</span><span class="sxs-lookup"><span data-stu-id="36e41-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-153">Проверяет, является ли \_ \_ Структура списка буферных списков, передаваемой драйверу выноски, ФРАГМЕНТОМ IP-пакетов.</span><span class="sxs-lookup"><span data-stu-id="36e41-153">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver is an IP packet fragment.</span></span>

<span data-ttu-id="36e41-154">Фильтрация слоев:</span><span class="sxs-lookup"><span data-stu-id="36e41-154">Filtering layers:</span></span>

-   <span data-ttu-id="36e41-155">ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-155">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-156">ФВПМ \_ уровень \_ входящего \_ иппаккет \_ V {4 \| 6} \_ Отмена</span><span class="sxs-lookup"><span data-stu-id="36e41-156">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}\_DISCARD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**\_флаг условия \_ FWP \_ — \_ Группа фрагментов \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-158">Проверяет, была ли \_ \_ Структура списка буферных списков, переданная в драйвер выноски, описывает связанный список фрагментов пакетов.</span><span class="sxs-lookup"><span data-stu-id="36e41-158">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver describes a linked list of packet fragments.</span></span>

<span data-ttu-id="36e41-159">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-159">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-160">ФВПМ \_ Layer \_ ипфорвард \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-160">FWPM\_LAYER\_IPFORWARD\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**\_флаг условия \_ FWP \_ — \_ \_ \_ переклассификация IPSec Натт**</span><span class="sxs-lookup"><span data-stu-id="36e41-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_NATT\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-162">Указывает, что один и тот же пакет перераспределяется на транспортном уровне, когда оболочка IPsec NAT преобразует значение удаленного порта.</span><span class="sxs-lookup"><span data-stu-id="36e41-162">Indicates that the same packet is being re-classified at the transport layer, when the IPsec NAT shim translates the remote port value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**\_флаг условия \_ FWP \_ требует \_ \_ классификации ALE**</span><span class="sxs-lookup"><span data-stu-id="36e41-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**FWP\_CONDITION\_FLAG\_REQUIRES\_ALE\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-164">Указывает, что пакет будет переклассифицирован на уровне получения/принятия ALE.</span><span class="sxs-lookup"><span data-stu-id="36e41-164">Indicates that the packet will be reclassified at the ALE receive/accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**\_флаг условия \_ FWP \_ является \_ неявной \_ привязкой**</span><span class="sxs-lookup"><span data-stu-id="36e41-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_IMPLICIT\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-166">Проверяет, выполняет ли сокеты Windows неявную привязку.</span><span class="sxs-lookup"><span data-stu-id="36e41-166">Tests if Windows Sockets is performing an implicit bind.</span></span>

<span data-ttu-id="36e41-167">Доступно только в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="36e41-167">Available only on Windows Vista and Windows Server 2008.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**\_флаг условия \_ FWP \_ \_ собран**</span><span class="sxs-lookup"><span data-stu-id="36e41-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**FWP\_CONDITION\_FLAG\_IS\_REASSEMBLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-169">Проверяет, был ли пакет собран.</span><span class="sxs-lookup"><span data-stu-id="36e41-169">Tests if the packet has been reassembled.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-170">Доступно только в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-170">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

 

<span data-ttu-id="36e41-171">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-171">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-172">ФВПМ \_ Layer \_ Inbound \_ иппаккет \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-172">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**\_флаг условия \_ FWP \_ \_ указан как имя \_ приложения \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**FWP\_CONDITION\_FLAG\_IS\_NAME\_APP\_SPECIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-174">Проверяет, было ли имя однорангового компьютера, к которому ожидается подключение, получено через API, например [**всасетсоккетпиртаржетнаме**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) , и не получено через эвристику кэширования.</span><span class="sxs-lookup"><span data-stu-id="36e41-174">Tests if the name of the peer machine that the application is expecting to connect to has been received via an API such as [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) and not obtained via the caching heuristics.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-175">Доступно только в Windows Server 2008 R2, Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-175">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="36e41-176">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-176">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-177">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-177">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**\_флаг условия \_ FWP \_ \_ неизбирательен**</span><span class="sxs-lookup"><span data-stu-id="36e41-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**FWP\_CONDITION\_FLAG\_IS\_PROMISCUOUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-179">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="36e41-179">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**\_флаг условия \_ FWP \_ — \_ встроенное по проверки подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**FWP\_CONDITION\_FLAG\_IS\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-181">Проверяет, является ли подключение сквозной проверкой подлинности, даже если отдельные пакеты не были проверены.</span><span class="sxs-lookup"><span data-stu-id="36e41-181">Tests if the connection is end-to-end authenticated, even if the individual packets have not been verified.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-182">Доступно только в Windows Server 2008 R2, Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-182">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="36e41-183">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-183">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-184">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-184">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-185">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-185">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**\_флаг условия \_ FWP \_ \_ реклассификации**</span><span class="sxs-lookup"><span data-stu-id="36e41-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-187">Проверяет, реклассифицировать ли обработчик фильтрации предыдущий запрос на привязку или прослушивание.</span><span class="sxs-lookup"><span data-stu-id="36e41-187">Tests if the filtering engine is reclassifying a previous bind or listen request.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-188">Доступно только в Windows Server 2008 R2, Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-188">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="36e41-189">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-189">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-190">\_ \_ \_ Прослушивание проверки подлинности ALE уровня фвпм \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-190">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-191">\_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-191">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**\_флаг условия \_ FWP \_ является \_ прокси- \_ соединением**</span><span class="sxs-lookup"><span data-stu-id="36e41-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-193">Проверяет, использует ли соединение прокси-сервер.</span><span class="sxs-lookup"><span data-stu-id="36e41-193">Tests if the connection uses a proxy.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-194">Доступно только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="36e41-194">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**\_флаг условия \_ FWP \_ — \_ это \_ замыкание APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="36e41-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-196">Проверяет, является ли сетевой трафик трафиком замыкания на себя контейнера приложений.</span><span class="sxs-lookup"><span data-stu-id="36e41-196">Tests if the network traffic is app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-197">Доступно только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="36e41-197">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**\_флаг условия \_ FWP \_ не \_ является \_ \_ замыканием APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="36e41-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-199">Проверяет, является ли сетевой трафик трафиком о замыкании на себя для контейнера без приложений.</span><span class="sxs-lookup"><span data-stu-id="36e41-199">Tests if the network traffic is non-app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-200">Доступно только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="36e41-200">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**\_флаг условия \_ FWP \_ \_ зарезервирован**</span><span class="sxs-lookup"><span data-stu-id="36e41-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**FWP\_CONDITION\_FLAG\_IS\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-202">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="36e41-202">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**\_флаг условия \_ FWP \_ \_ учитывает \_ политику \_ авторизации**</span><span class="sxs-lookup"><span data-stu-id="36e41-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-204">Указывает, что текущая классификация выполняется для того, чтобы соответствовать намерениям перенаправленного приложения Магазина Windows подключиться к указанному узлу.</span><span class="sxs-lookup"><span data-stu-id="36e41-204">Indicates that the current classification is being performed to honor the intention of a redirected Windows Store app to connect to a specified host.</span></span> <span data-ttu-id="36e41-205">Такая классификация будет содержать те же значения классификатора полей, что и если приложение никогда не перенаправлялось.</span><span class="sxs-lookup"><span data-stu-id="36e41-205">Such a classification will contain the same classifiable field values as if the app were never redirected.</span></span> <span data-ttu-id="36e41-206">Флаг также указывает, что будущая классификация будет вызываться для сопоставления с действующим перенаправленным назначением.</span><span class="sxs-lookup"><span data-stu-id="36e41-206">The flag also indicates that a future classification will be invoked to match the effective redirected destination.</span></span> <span data-ttu-id="36e41-207">Если приложение перенаправляется в прокси-службу для проверки, это также означает, что в прокси-подключении будет вызываться следующая классификация.</span><span class="sxs-lookup"><span data-stu-id="36e41-207">If the app is redirected to a proxy service for inspection, it also means a future classification will be invoked on the proxy connection.</span></span> <span data-ttu-id="36e41-208">Драйверы выноски обычно разрешают эту классификацию.</span><span class="sxs-lookup"><span data-stu-id="36e41-208">Callout drivers should generally allow this classification.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-209">Доступно только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="36e41-209">Available only on Windows 8 and Windows Server 2012.</span></span>

 

<span data-ttu-id="36e41-210">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-210">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-211">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-211">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="36e41-212">Следующие флаги указывают причину повторной авторизации ранее авторизованного подключения.</span><span class="sxs-lookup"><span data-stu-id="36e41-212">The following flags specify the reason for reauthorizing a previously authorized connection.</span></span> <span data-ttu-id="36e41-213">Эти флаги и слои фильтрации, где их можно использовать, определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="36e41-213">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-214">Эти условия фильтрации доступны только в Windows Server 2008 R2, Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-214">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="36e41-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**\_ \_ \_ \_ изменение политики по причине ПОВТОРНОй авторизации условия FWP \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-216">Указывает, что соединение было повторно создано из-за добавления или удаления фильтров.</span><span class="sxs-lookup"><span data-stu-id="36e41-216">Indicates that the connection was reauthorized due to filters being added or removed.</span></span>

<span data-ttu-id="36e41-217">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-217">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-218">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-218">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-219">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-219">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP \_ условия повторной \_ авторизации — \_ \_ новый \_ \_ интерфейс прибытия**</span><span class="sxs-lookup"><span data-stu-id="36e41-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_ARRIVAL\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-221">Указывает, что пакет был получен из неизвестного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="36e41-221">Indicates that the packet has arrived from an unknown interface.</span></span>

<span data-ttu-id="36e41-222">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-222">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-223">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-223">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-224">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-224">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP \_ условия повторной \_ авторизации, \_ Причина \_ нового \_ \_ интерфейса NEXTHOP**</span><span class="sxs-lookup"><span data-stu-id="36e41-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_NEXTHOP\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-226">Указывает, что пакет будет относиться к неизвестному интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="36e41-226">Indicates that the packet will be departing from an unknown interface.</span></span>

<span data-ttu-id="36e41-227">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-227">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-228">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-228">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-229">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-229">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**\_пересечение \_ \_ \_ профиля причины \_ FWP условия авторизации**</span><span class="sxs-lookup"><span data-stu-id="36e41-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_PROFILE\_CROSSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-231">Указывает, что пакет прошел через интерфейсы более чем одной категории сети.</span><span class="sxs-lookup"><span data-stu-id="36e41-231">Indicates that the packet has passed through interfaces of more than one network category.</span></span>

<span data-ttu-id="36e41-232">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-232">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-233">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-233">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-234">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-234">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP \_ условия повторной \_ авторизации \_ причины \_ \_ завершения классификации**</span><span class="sxs-lookup"><span data-stu-id="36e41-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_CLASSIFY\_COMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-236">Указывает, что теперь разрешено выполнение ранее удерживаемого подключения.</span><span class="sxs-lookup"><span data-stu-id="36e41-236">Indicates that a previously held connection is now being allowed to complete.</span></span>

<span data-ttu-id="36e41-237">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-237">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-238">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-238">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-239">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-239">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP \_ условия повторной \_ авторизации \_ причины \_ \_ изменения свойств IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_IPSEC\_PROPERTIES\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-241">Указывает, что свойства IPsec изменились или что соединение было изменено с открытого текста на безопасное соединение.</span><span class="sxs-lookup"><span data-stu-id="36e41-241">Indicates that IPsec properties have changed, or that the connection has changed from clear text to a secure connection.</span></span>

<span data-ttu-id="36e41-242">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-242">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-243">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-243">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-244">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-244">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP \_ условия повторной \_ авторизации \_ Причина \_ средней \_ \_ проверки потока**</span><span class="sxs-lookup"><span data-stu-id="36e41-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_MID\_STREAM\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-246">Указывает, что ранее установленное подключение TCP проверяется.</span><span class="sxs-lookup"><span data-stu-id="36e41-246">Indicates that a previously established TCP connection is now being inspected.</span></span>

<span data-ttu-id="36e41-247">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-247">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-248">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-248">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-249">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-249">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**\_ \_ \_ \_ изменено свойство сокета причины \_ \_ повторной авторизации FWP**</span><span class="sxs-lookup"><span data-stu-id="36e41-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_SOCKET\_PROPERTY\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-251">Указывает, что свойства сокета были установлены после авторизации и установления соединения.</span><span class="sxs-lookup"><span data-stu-id="36e41-251">Indicates that socket properties have been set after a connection was authorized and established.</span></span>

<span data-ttu-id="36e41-252">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-252">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-253">\_ \_ \_ Проверка подлинности ALE уровня фвпм для \_ подключения \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-253">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-254">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-254">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP \_ условия повторно \_ авторизовать \_ \_ новый \_ входящий \_ \_ пакет бкаст мкаст \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_INBOUND\_MCAST\_BCAST\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-256">Указывает, что новые Входящие многоадресные или широковещательные пакеты допускают повторную авторизацию в \_ \_ выносках приема на получение Ale.</span><span class="sxs-lookup"><span data-stu-id="36e41-256">Indicates that new inbound multicast or broadcast packets are being re-authorized at ALE\_RECV\_ACCEPT callouts.</span></span>

<span data-ttu-id="36e41-257">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-257">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-258">\_ \_ \_ Проверка подлинности на уровне фвпм для проверки \_ \_ приема recv \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-258">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="36e41-259">Следующие флаги задают свойства сокета, которые связаны с тем, требуется ли приложению получать трафик обхода по периметру.</span><span class="sxs-lookup"><span data-stu-id="36e41-259">The following flags specify socket properties which are related to whether an application wants to receive Edge Traversal traffic.</span></span> <span data-ttu-id="36e41-260">Эти флаги и слои фильтрации, где их можно использовать, определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="36e41-260">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-261">Эти условия фильтрации доступны только в Windows Server 2008 R2, Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="36e41-261">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="36e41-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**\_ \_ флаг свойства сокета FWP условия \_ \_ \_ является \_ системным \_ портом \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="36e41-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_IS\_SYSTEM\_PORT\_RPC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-263">Указывает, что приложение взаимодействует с динамическим портом RPC.</span><span class="sxs-lookup"><span data-stu-id="36e41-263">Indicates that the application is communicating with a dynamic RPC port.</span></span>

<span data-ttu-id="36e41-264">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-264">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-265">\_ \_ \_ Прослушивание проверки подлинности ALE уровня фвпм \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-265">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-266">\_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-266">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_ \_ флаг свойства сокета FWP условия \_ \_ \_ разрешения \_ пограничных \_ данных**</span><span class="sxs-lookup"><span data-stu-id="36e41-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_ALLOW\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-268">Указывает, что приложению требуется получить трафик, относящийся к обходу узлов.</span><span class="sxs-lookup"><span data-stu-id="36e41-268">Indicates that the application wants to receive edge traversal-specific traffic.</span></span>

<span data-ttu-id="36e41-269">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-269">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-270">\_ \_ \_ Прослушивание проверки подлинности ALE уровня фвпм \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-270">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-271">\_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-271">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_ \_ флаг свойства сокета FWP условия \_ \_ \_ запрета \_ пограничных \_ данных**</span><span class="sxs-lookup"><span data-stu-id="36e41-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_DENY\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-273">Указывает, что приложению не требуется получение или обработка трафика, относящегося к обходу пограничной сети.</span><span class="sxs-lookup"><span data-stu-id="36e41-273">Indicates that the application does not want to receive or process edge traversal-specific traffic.</span></span>

<span data-ttu-id="36e41-274">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-274">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-275">\_ \_ \_ Прослушивание проверки подлинности ALE уровня фвпм \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-275">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="36e41-276">\_ \_ Назначение ресурса ALE уровня фвпм \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="36e41-276">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="36e41-277">Следующие флаги указывают сведения о соединении, связанные с фильтрацией L2.</span><span class="sxs-lookup"><span data-stu-id="36e41-277">The following flags specify connection details related to L2 filtering.</span></span>

> [!Note]  
> <span data-ttu-id="36e41-278">Эти условия фильтрации доступны только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="36e41-278">These filtering conditions are available only on Windows 8 and Windows Server 2012.</span></span>

 

<dl> <dt>

<span data-ttu-id="36e41-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**\_Условие FWP \_ L2 \_ — \_ собственная \_ сеть Ethernet**</span><span class="sxs-lookup"><span data-stu-id="36e41-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-280">Указывает, что соединение является собственным Ethernet.</span><span class="sxs-lookup"><span data-stu-id="36e41-280">Indicates that the connection is native Ethernet.</span></span>

<span data-ttu-id="36e41-281">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-281">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-282">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="36e41-282">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-283">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="36e41-283">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="36e41-284">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-284">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-285">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-285">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**\_Условие FWP \_ L2 \_ — \_ Wi-Fi**</span><span class="sxs-lookup"><span data-stu-id="36e41-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP\_CONDITION\_L2\_IS\_WIFI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-287">Указывает, что подключение является Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="36e41-287">Indicates that the connection is Wi-Fi.</span></span>

<span data-ttu-id="36e41-288">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-288">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-289">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="36e41-289">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-290">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="36e41-290">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="36e41-291">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-291">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-292">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-292">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**\_Условие FWP \_ L2 \_ — \_ мобильное \_ широкополосное подключение**</span><span class="sxs-lookup"><span data-stu-id="36e41-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-294">Указывает, что подключение является мобильным широкополосным.</span><span class="sxs-lookup"><span data-stu-id="36e41-294">Indicates that the connection is mobile broadband.</span></span>

<span data-ttu-id="36e41-295">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-295">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-296">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="36e41-296">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-297">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="36e41-297">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="36e41-298">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-298">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-299">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-299">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**\_Условие FWP \_ L2 \_ — \_ \_ прямые \_ данные WiFi**</span><span class="sxs-lookup"><span data-stu-id="36e41-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-301">Указывает, что соединение Wi-Fi напрямую.</span><span class="sxs-lookup"><span data-stu-id="36e41-301">Indicates that the connection is Wi-Fi Direct.</span></span>

<span data-ttu-id="36e41-302">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-302">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-303">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="36e41-303">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-304">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="36e41-304">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="36e41-305">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-305">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-306">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-306">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**\_Условие FWP \_ L2 \_ — \_ VM2VM**</span><span class="sxs-lookup"><span data-stu-id="36e41-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP\_CONDITION\_L2\_IS\_VM2VM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-308">Указывает, что соединение установлено между виртуальными машинами.</span><span class="sxs-lookup"><span data-stu-id="36e41-308">Indicates that the connection is between virtual machines.</span></span>

<span data-ttu-id="36e41-309">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-309">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-310">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="36e41-310">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-311">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="36e41-311">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="36e41-312">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-312">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-313">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-313">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**\_Условие FWP \_ L2 \_ имеет \_ неправильный формат \_ пакета**</span><span class="sxs-lookup"><span data-stu-id="36e41-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-315">Указывает, что пакет выглядит неправильно.</span><span class="sxs-lookup"><span data-stu-id="36e41-315">Indicates that a packet appears to be malformed.</span></span>

<span data-ttu-id="36e41-316">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-316">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-317">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="36e41-317">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-318">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="36e41-318">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="36e41-319">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-319">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-320">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-320">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**\_Условие FWP \_ L2 \_ — \_ \_ Группа фрагментов IP-адресов \_**</span><span class="sxs-lookup"><span data-stu-id="36e41-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-322">Указывает группу фрагментов IP-пакетов.</span><span class="sxs-lookup"><span data-stu-id="36e41-322">Indicates an IP packet fragment group.</span></span>

<span data-ttu-id="36e41-323">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-323">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-324">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="36e41-324">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-325">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="36e41-325">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="36e41-326">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-326">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-327">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-327">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="36e41-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**\_Условие FWP \_ L2 \_ , \_ Если \_ имеется соединитель**</span><span class="sxs-lookup"><span data-stu-id="36e41-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="36e41-329">Указывает, что имеется соединитель.</span><span class="sxs-lookup"><span data-stu-id="36e41-329">Indicates that a connector is present.</span></span>

<span data-ttu-id="36e41-330">Слой фильтрации:</span><span class="sxs-lookup"><span data-stu-id="36e41-330">Filtering layer:</span></span>

-   <span data-ttu-id="36e41-331">ФВПМ \_ Layer \_ входящего трафика \_ Mac \_ Frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="36e41-331">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-332">\_ \_ \_ \_ машинный кадр входящего Mac-кадра \_ уровня фвпм</span><span class="sxs-lookup"><span data-stu-id="36e41-332">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="36e41-333">\_ \_ \_ \_ Ethernet-кадр исходящего уровня фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-333">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="36e41-334">\_ \_ \_ машинный кадр исходящего Mac-уровня \_ фвпм \_</span><span class="sxs-lookup"><span data-stu-id="36e41-334">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36e41-335">Требования</span><span class="sxs-lookup"><span data-stu-id="36e41-335">Requirements</span></span>



| <span data-ttu-id="36e41-336">Требование</span><span class="sxs-lookup"><span data-stu-id="36e41-336">Requirement</span></span> | <span data-ttu-id="36e41-337">Значение</span><span class="sxs-lookup"><span data-stu-id="36e41-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36e41-338">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36e41-338">Minimum supported client</span></span><br/> | <span data-ttu-id="36e41-339">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36e41-339">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36e41-340">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36e41-340">Minimum supported server</span></span><br/> | <span data-ttu-id="36e41-341">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36e41-341">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36e41-342">Header</span><span class="sxs-lookup"><span data-stu-id="36e41-342">Header</span></span><br/>                   | <dl> <span data-ttu-id="36e41-343"><dt>Фвптипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="36e41-343"><dt>Fwptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36e41-344">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36e41-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e41-345">**Фильтрация идентификаторов слоя**</span><span class="sxs-lookup"><span data-stu-id="36e41-345">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

