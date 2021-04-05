---
title: Условия фильтрации, доступные на каждом слое фильтрации (Фвпму. h)
description: Механизм фильтрации платформы фильтрации Windows (WFP) поддерживает разные наборы условий фильтрации на каждом из уровней фильтрации.
ms.assetid: 6faace21-44ec-49dd-8e77-e403c258c14a
topic_type:
- apiref
api_name:
- FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD
- FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD
- FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD
- FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6
- FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6
- FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD
- FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6
- FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6
- FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD
- FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD
- FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6
- FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD
- FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD
- FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6
- FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6
- FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6
- FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6
- FWPM_LAYER_RPC_UM
- FWPM_LAYER_RPC_EPMAP
- FWPM_LAYER_RPC_EP_ADD
- FWPM_LAYER_RPC_PROXY_CONN
- FWPM_LAYER_RPC_PROXY_IF
- FWPM_LAYER_KM_AUTHORIZATION
- FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET
- FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE
- FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET
- FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0c3806c7c3c7a5fa7f10af0e5e11c212bd93e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988182"
---
# <a name="filtering-conditions-available-at-each-filtering-layer"></a><span data-ttu-id="16776-103">Условия фильтрации, доступные на каждом слое фильтрации</span><span class="sxs-lookup"><span data-stu-id="16776-103">Filtering Conditions Available at Each Filtering Layer</span></span>

<span data-ttu-id="16776-104">Механизм фильтрации платформы фильтрации Windows (WFP) поддерживает разные наборы условий фильтрации на каждом из уровней фильтрации.</span><span class="sxs-lookup"><span data-stu-id="16776-104">The Windows Filtering Platform (WFP) filter engine supports a different set of filtering conditions at each of its filtering layers.</span></span>

<span data-ttu-id="16776-105">Список условий фильтрации, доступных на каждом уровне, выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="16776-105">The list of filtering conditions that are available at each layer are as follows.</span></span>

## <a name="fwpm_layer_inbound_ippacket_v4--fwpm_layer_inbound_ippacket_v4_discard--fwpm_layer_inbound_ippacket_v6--fwpm_layer_inbound_ippacket_v6_discard"></a><span data-ttu-id="16776-106">FWPM_LAYER_INBOUND_IPPACKET_V4/FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_INBOUND_IPPACKET_V6/FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-106">FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="16776-107">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-107">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-108">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-108">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-109">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-109">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-115">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-115">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_outbound_ippacket_v4--fwpm_layer_outbound_ippacket_v4_discard--fwpm_layer_outbound_ippacket_v6--fwpm_layer_outbound_ippacket_v6_discard"></a><span data-ttu-id="16776-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4/FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_OUTBOUND_IPPACKET_V6/FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="16776-117">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-117">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-118">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-118">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-119">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-119">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-125">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-125">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_ipforward_v4--fwpm_layer_ipforward_v4_discard--fwpm_layer_ipforward_v6--fwpm_layer_ipforward_v6_discard"></a><span data-ttu-id="16776-126">FWPM_LAYER_IPFORWARD_V4/FWPM_LAYER_IPFORWARD_V4_DISCARD/FWPM_LAYER_IPFORWARD_V6/FWPM_LAYER_IPFORWARD_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-126">FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD</span></span>
- <span data-ttu-id="16776-127">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-127">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="16776-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span></span>
- <span data-ttu-id="16776-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="16776-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-137">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-137">Windows 7  and later</span></span>
- <span data-ttu-id="16776-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span></span> 
- <span data-ttu-id="16776-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="16776-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="16776-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_inbound_transport_v4--fwpm_layer_inbound_transport_v4_discard--fwpm_layer_inbound_transport_v6--fwpm_layer_inbound_transport_v6_discard"></a><span data-ttu-id="16776-142">FWPM_LAYER_INBOUND_TRANSPORT_V4/FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_INBOUND_TRANSPORT_V6/FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-142">FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="16776-143">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-143">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-144">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-144">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-145">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-145">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-149">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-149">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-150">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-150">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-152">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-152">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-154">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-154">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-155">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-155">Windows 7  and later</span></span>
- <span data-ttu-id="16776-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_transport_v4--fwpm_layer_outbound_transport_v4_discard--fwpm_layer_outbound_transport_v6--fwpm_layer_outbound_transport_v6_discard"></a><span data-ttu-id="16776-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4/FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_OUTBOUND_TRANSPORT_V6/FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="16776-158">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-158">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-159">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-159">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-160">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-160">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-165">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-165">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-166">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-166">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-168">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-168">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-170">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-170">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-171">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-171">Windows 7  and later</span></span>
- <span data-ttu-id="16776-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_stream_v4--fwpm_layer_stream_v4_discard--fwpm_layer_stream_v6--fwpm_layer_stream_v6_discard"></a><span data-ttu-id="16776-173">FWPM_LAYER_STREAM_V4/FWPM_LAYER_STREAM_V4_DISCARD/FWPM_LAYER_STREAM_V6/FWPM_LAYER_STREAM_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-173">FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD</span></span>
- <span data-ttu-id="16776-174">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="16776-174">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="16776-175">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-175">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-178">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-178">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-180">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-180">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
## <a name="fwpm_layer_datagram_data_v4--fwpm_layer_datagram_data_v4_discard--fwpm_layer_datagram_data_v6--fwpm_layer_datagram_data_v6_discard"></a><span data-ttu-id="16776-181">FWPM_LAYER_DATAGRAM_DATA_V4/FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD/FWPM_LAYER_DATAGRAM_DATA_V6/FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-181">FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span></span>
- <span data-ttu-id="16776-182">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="16776-182">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="16776-183">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-183">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-184">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-184">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-185">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-185">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-189">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-189">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-190">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-190">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-192">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-192">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-194">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-194">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_stream_packet-v4--fwpm_layer_stream_packet-v6"></a><span data-ttu-id="16776-195">FWPM_LAYER_STREAM_PACKET V4/FWPM_LAYER_STREAM_PACKET V6</span><span class="sxs-lookup"><span data-stu-id="16776-195">FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-196">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-196">Windows 7  and later</span></span>
- <span data-ttu-id="16776-197">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="16776-197">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="16776-198">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-198">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-199">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-199">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-200">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-200">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-203">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-203">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-205">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-205">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-207">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-207">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_inbound_icmp_error_v4--fwpm_layer_inbound_icmp_error_v4_discard--fwpm_layer_inbound_icmp_error_v6--fwpm_layer_inbound_icmp_error_v6_discard"></a><span data-ttu-id="16776-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4/FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_INBOUND_ICMP_ERROR_V6/FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="16776-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista или Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="16776-213">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-213">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-214">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="16776-214">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="16776-215">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-215">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="16776-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span></span>
- <span data-ttu-id="16776-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="16776-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista или Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista или Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista или Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-228">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-228">Windows 7  and later</span></span>
- <span data-ttu-id="16776-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_icmp_error_v4--fwpm_layer_outbound_icmp_error_v4_discard--fwpm_layer_outbound_icmp_error_v6--fwpm_layer_outbound_icmp_error_v6_discard"></a><span data-ttu-id="16776-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="16776-231">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-231">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-232">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="16776-232">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="16776-233">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-233">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="16776-234">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-234">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-235">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-235">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-241">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-241">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-242">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-242">Windows 7  and later</span></span>
- <span data-ttu-id="16776-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_ale_bind_redirect_v4--fwpm_layer_ale_bind_redirect-v6"></a><span data-ttu-id="16776-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4 И FWPM_LAYER_ALE_BIND_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="16776-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-245">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-245">Windows 7  and later</span></span>
- <span data-ttu-id="16776-246">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-246">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-247">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-247">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-248">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-248">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-251">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-251">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-252">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-252">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-253">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-253">Windows 8  and later</span></span>
- <span data-ttu-id="16776-254">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-254">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_assignment_v4--fwpm_layer_ale_resource_assignment_v4_discard--fwpm_layer_ale_resource_assignment_v6--fwpm_layer_ale_resource_assignment_v6_discard"></a><span data-ttu-id="16776-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span></span>
- <span data-ttu-id="16776-256">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-256">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span><span class="sxs-lookup"><span data-stu-id="16776-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span></span>
- <span data-ttu-id="16776-258">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-258">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-259">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-259">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-260">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-260">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-264">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-264">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-265">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-265">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-266">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-266">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-267">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-267">Windows 7  and later</span></span>
- <span data-ttu-id="16776-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="16776-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-270">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-270">Windows 8  and later</span></span>
- <span data-ttu-id="16776-271">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-271">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_release_v4--fwpm_layer_ale_resource_release_v6"></a><span data-ttu-id="16776-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 И FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span><span class="sxs-lookup"><span data-stu-id="16776-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-273">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-273">Windows 7  and later</span></span>
- <span data-ttu-id="16776-274">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-274">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-275">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-275">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-276">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-276">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-280">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-280">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-281">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-281">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-282">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-282">Windows 8  and later</span></span>
- <span data-ttu-id="16776-283">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-283">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_endpoint_closure_v4--fwpm_layer_ale_endpoint_closure_v6"></a><span data-ttu-id="16776-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 И FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span><span class="sxs-lookup"><span data-stu-id="16776-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-285">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-285">Windows 7  and later</span></span>
- <span data-ttu-id="16776-286">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-286">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-287">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-287">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-288">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-288">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-292">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-292">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-293">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-293">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-295">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-295">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-296">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-296">Windows 8  and later</span></span>
- <span data-ttu-id="16776-297">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-297">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_listen_v4--fwpm_layer_ale_auth_listen_v4_discard--fwpm_layer_ale_auth_listen_v6--fwpm_layer_ale_auth_listen_v6_discard"></a><span data-ttu-id="16776-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4/FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD/FWPM_LAYER_ALE_AUTH_LISTEN_V6/FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span></span>
- <span data-ttu-id="16776-299">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-299">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-300">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-300">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-301">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-301">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-302">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-302">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-306">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-306">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-307">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-307">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-308">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-308">Windows 7  and later</span></span>
- <span data-ttu-id="16776-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="16776-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-311">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-311">Windows 8  and later</span></span>
- <span data-ttu-id="16776-312">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-312">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_recv_accept_v4--fwpm_layer_ale_auth_recv_accept_v4_discard--fwpm_layer_ale_auth_recv_accept_v6--fwpm_layer_ale_auth_recv_accept_v6_discard"></a><span data-ttu-id="16776-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span></span>
- <span data-ttu-id="16776-314">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-314">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="16776-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span></span>
- <span data-ttu-id="16776-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="16776-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="16776-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
- <span data-ttu-id="16776-319">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-319">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista или Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="16776-324">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-324">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="16776-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-329">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-329">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-330">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-330">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-332">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-332">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista или Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista или Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista или Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-336">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-336">Windows 7  and later</span></span>
- <span data-ttu-id="16776-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="16776-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="16776-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="16776-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="16776-344">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="16776-344">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="16776-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-346">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-346">Windows 8  and later</span></span>
- <span data-ttu-id="16776-347">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-347">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_connect_redirect_v4--fwpm_layer_ale_connect_redirect-v6"></a><span data-ttu-id="16776-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 И FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="16776-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-349">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-349">Windows 7  and later</span></span>
- <span data-ttu-id="16776-350">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-350">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-351">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-351">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-352">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-352">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-355">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-355">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-356">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-356">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-357">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-357">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-360">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-360">Windows 8  and later</span></span>
- <span data-ttu-id="16776-361">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-361">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_connect_v4--fwpm_layer_ale_auth_connect_v4_discard--fwpm_layer_ale_auth_connect_v6--fwpm_layer_ale_auth_connect_v6_discard"></a><span data-ttu-id="16776-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4/FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_CONNECT_V6/FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span></span>
- <span data-ttu-id="16776-363">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-363">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="16776-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="16776-366">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-366">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-367">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-367">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-368">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-368">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-373">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-373">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-374">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-374">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-376">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-376">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-378">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-378">FWPM_CONDITION_TUNNEL_TYPE</span></span>
- <span data-ttu-id="16776-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="16776-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="16776-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX _sp1 и laterFWPM_CONDITION_INTERFACE_INDEX Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16776-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX Windows Vista _sp1 and laterFWPM_CONDITION_INTERFACE_INDEX</span></span> 
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-383">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-383">Windows 7  and later</span></span>
- <span data-ttu-id="16776-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="16776-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="16776-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="16776-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="16776-391">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="16776-391">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="16776-392">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="16776-392">FWPM_CONDITION_PEER_NAME</span></span>
- <span data-ttu-id="16776-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-394">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-394">Windows 8  and later</span></span>
- <span data-ttu-id="16776-395">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-395">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_flow_established_v4--fwpm_layer_ale_flow_established_v4_discard--fwpm_layer_ale_flow_established_v6--fwpm_layer_ale_flow_established_v6_discard"></a><span data-ttu-id="16776-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="16776-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span></span>
- <span data-ttu-id="16776-397">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-397">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="16776-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="16776-400">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-400">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-401">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="16776-401">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="16776-402">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-402">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="16776-403">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-403">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-408">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-408">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-409">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-409">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-411">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-411">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="16776-412">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-412">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-413">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-413">Windows 8  and later</span></span>
- <span data-ttu-id="16776-414">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-414">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_name_resolution_cache_v4--fwpm_layer_name_resolution_cache_v6"></a><span data-ttu-id="16776-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 И FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span><span class="sxs-lookup"><span data-stu-id="16776-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-416">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-416">Windows 7  and later</span></span>
- <span data-ttu-id="16776-417">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="16776-417">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="16776-418">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-418">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="16776-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-420">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="16776-420">FWPM_CONDITION_PEER_NAME</span></span>
## <a name="fwpm_layer_ipsec_km_demux_v4--fwpm_layer_ipsec_km_demux_v6"></a><span data-ttu-id="16776-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4 И FWPM_LAYER_IPSEC_KM_DEMUX_V6</span><span class="sxs-lookup"><span data-stu-id="16776-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6</span></span>
- <span data-ttu-id="16776-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
## <a name="fwpm_layer_ipsec_v4--fwpm_layer_ipsec_v6"></a><span data-ttu-id="16776-424">FWPM_LAYER_IPSEC_V4 И FWPM_LAYER_IPSEC_V6</span><span class="sxs-lookup"><span data-stu-id="16776-424">FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6</span></span>
- <span data-ttu-id="16776-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-426">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-426">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-427">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-427">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-429">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-429">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-430">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-430">Windows 7  and later</span></span>
- <span data-ttu-id="16776-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_ikeext_v4--fwpm_layer_ikeext_v6"></a><span data-ttu-id="16776-433">FWPM_LAYER_IKEEXT_V4 И FWPM_LAYER_IKEEXT_V6</span><span class="sxs-lookup"><span data-stu-id="16776-433">FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6</span></span>
- <span data-ttu-id="16776-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-436">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-436">Windows 7  and later</span></span>
- <span data-ttu-id="16776-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="16776-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_rpc_um"></a><span data-ttu-id="16776-439">FWPM_LAYER_RPC_UM</span><span class="sxs-lookup"><span data-stu-id="16776-439">FWPM_LAYER_RPC_UM</span></span>
- <span data-ttu-id="16776-440">FWPM_CONDITION_DCOM_APP_ID</span><span class="sxs-lookup"><span data-stu-id="16776-440">FWPM_CONDITION_DCOM_APP_ID</span></span>
- <span data-ttu-id="16776-441">FWPM_CONDITION_IMAGE_NAME</span><span class="sxs-lookup"><span data-stu-id="16776-441">FWPM_CONDITION_IMAGE_NAME</span></span>
- <span data-ttu-id="16776-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="16776-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="16776-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="16776-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="16776-444">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-444">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="16776-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="16776-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="16776-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>
- <span data-ttu-id="16776-447">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="16776-447">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="16776-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="16776-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="16776-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="16776-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="16776-450">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-450">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="16776-451">FWPM_CONDITION_RPC_IF_FLAG</span><span class="sxs-lookup"><span data-stu-id="16776-451">FWPM_CONDITION_RPC_IF_FLAG</span></span>
- <span data-ttu-id="16776-452">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="16776-452">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="16776-453">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="16776-453">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="16776-454">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-454">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="16776-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="16776-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="16776-456">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="16776-456">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_epmap"></a><span data-ttu-id="16776-457">FWPM_LAYER_RPC_EPMAP</span><span class="sxs-lookup"><span data-stu-id="16776-457">FWPM_LAYER_RPC_EPMAP</span></span>
- <span data-ttu-id="16776-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="16776-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="16776-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="16776-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="16776-460">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-460">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="16776-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="16776-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="16776-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="16776-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>

- <span data-ttu-id="16776-463">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="16776-463">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="16776-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="16776-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="16776-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="16776-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="16776-466">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-466">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="16776-467">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="16776-467">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="16776-468">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="16776-468">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="16776-469">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-469">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="16776-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="16776-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="16776-471">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="16776-471">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_ep_add"></a><span data-ttu-id="16776-472">FWPM_LAYER_RPC_EP_ADD</span><span class="sxs-lookup"><span data-stu-id="16776-472">FWPM_LAYER_RPC_EP_ADD</span></span>
- <span data-ttu-id="16776-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="16776-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span></span>
- <span data-ttu-id="16776-474">FWPM_CONDITION_RPC_EP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-474">FWPM_CONDITION_RPC_EP_FLAGS</span></span>
- <span data-ttu-id="16776-475">FWPM_CONDITION_RPC_EP_VALUE</span><span class="sxs-lookup"><span data-stu-id="16776-475">FWPM_CONDITION_RPC_EP_VALUE</span></span>
- <span data-ttu-id="16776-476">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-476">FWPM_CONDITION_RPC_PROTOCOL</span></span>
## <a name="fwpm_layer_rpc_proxy_conn"></a><span data-ttu-id="16776-477">FWPM_LAYER_RPC_PROXY_CONN</span><span class="sxs-lookup"><span data-stu-id="16776-477">FWPM_LAYER_RPC_PROXY_CONN</span></span>
- <span data-ttu-id="16776-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="16776-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="16776-479">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="16776-479">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="16776-480">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="16776-480">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="16776-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="16776-482">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="16776-482">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="16776-483">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-483">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_rpc_proxy_if"></a><span data-ttu-id="16776-484">FWPM_LAYER_RPC_PROXY_IF</span><span class="sxs-lookup"><span data-stu-id="16776-484">FWPM_LAYER_RPC_PROXY_IF</span></span>
- <span data-ttu-id="16776-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="16776-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="16776-486">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="16776-486">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="16776-487">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="16776-487">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="16776-488">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="16776-488">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="16776-489">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="16776-489">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="16776-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="16776-491">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="16776-491">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="16776-492">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-492">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_km_authorization"></a><span data-ttu-id="16776-493">FWPM_LAYER_KM_AUTHORIZATION</span><span class="sxs-lookup"><span data-stu-id="16776-493">FWPM_LAYER_KM_AUTHORIZATION</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="16776-494">Windows 7 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-494">Windows 7  and later</span></span>
- <span data-ttu-id="16776-495">FWPM_CONDITION_REMOTE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-495">FWPM_CONDITION_REMOTE_ID</span></span>
- <span data-ttu-id="16776-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span></span>
- <span data-ttu-id="16776-497">FWPM_CONDITION_KM_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-497">FWPM_CONDITION_KM_TYPE</span></span>
- <span data-ttu-id="16776-498">FWPM_CONDITION_KM_MODE</span><span class="sxs-lookup"><span data-stu-id="16776-498">FWPM_CONDITION_KM_MODE</span></span>
- <span data-ttu-id="16776-499">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="16776-499">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="16776-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span><span class="sxs-lookup"><span data-stu-id="16776-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span></span>
## <a name="fwpm_layer_inbound_mac_frame_ethernet--fwpm_layer_outbound_mac_frame_ethernet"></a><span data-ttu-id="16776-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET И FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="16776-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-502">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-502">Windows 8  and later</span></span>
- <span data-ttu-id="16776-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span></span>
- <span data-ttu-id="16776-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="16776-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="16776-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-508">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-508">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="16776-509">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="16776-509">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="16776-510">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-510">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="16776-511">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-511">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-512">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-512">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="16776-513">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-513">FWPM_CONDITION_L2_FLAGS</span></span>
##  <a name="fwpm_layer_inbound_mac_frame_native--fwpm_layer_outbound_mac_frame_native"></a><span data-ttu-id="16776-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE И FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span><span class="sxs-lookup"><span data-stu-id="16776-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-515">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-515">Windows 8  and later</span></span>
- <span data-ttu-id="16776-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span></span>
- <span data-ttu-id="16776-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span></span>
- <span data-ttu-id="16776-518">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="16776-518">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="16776-519">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-519">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-520">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="16776-520">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="16776-521">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-521">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="16776-522">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-522">FWPM_CONDITION_L2_FLAGS</span></span>
## <a name="fwpm_layer_egress_vswitch_ethernet--fwpm_layer_ingress_vswitch_ethernet"></a><span data-ttu-id="16776-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET И FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="16776-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-524">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-524">Windows 8  and later</span></span>
- <span data-ttu-id="16776-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="16776-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="16776-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="16776-529">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-529">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="16776-530">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="16776-530">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="16776-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="16776-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="16776-532">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="16776-532">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="16776-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="16776-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="16776-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="16776-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="16776-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>
##  <a name="fwpm_layer_egress_vswitch_transport_v4--fwpm_layer_ingress_vswitch_transport_v4--fwpm_layer_egressvswitch_transport_v6--fwpm_layer_ingress_vswitch_transport_v6"></a><span data-ttu-id="16776-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span><span class="sxs-lookup"><span data-stu-id="16776-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="16776-539">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="16776-539">Windows 8  and later</span></span>
- <span data-ttu-id="16776-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="16776-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="16776-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="16776-542">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="16776-542">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="16776-543">FWPM_CONDITION_IP_SOURCE_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-543">FWPM_CONDITION_IP_SOURCE_PORT</span></span>
- <span data-ttu-id="16776-544">FWPM_CONDITION_IP_DESTINATION_PORT</span><span class="sxs-lookup"><span data-stu-id="16776-544">FWPM_CONDITION_IP_DESTINATION_PORT</span></span>
- <span data-ttu-id="16776-545">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="16776-545">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="16776-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="16776-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="16776-547">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="16776-547">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="16776-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="16776-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="16776-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="16776-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="16776-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="16776-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span></span>
- <span data-ttu-id="16776-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="16776-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="16776-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16776-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>



## <a name="remarks"></a><span data-ttu-id="16776-555">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16776-555">Remarks</span></span>

<span data-ttu-id="16776-556">Суффиксы v4 и V6 в конце идентификаторов слоя указывают, находится ли слой в сетевом стеке IPv4 или в стеке сети IPv6.</span><span class="sxs-lookup"><span data-stu-id="16776-556">The V4 and V6 suffixes at the end of the layer identifiers indicate whether the layer is located in the IPv4 network stack or in the IPv6 network stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="16776-557">Требования</span><span class="sxs-lookup"><span data-stu-id="16776-557">Requirements</span></span>



| <span data-ttu-id="16776-558">Требование</span><span class="sxs-lookup"><span data-stu-id="16776-558">Requirement</span></span> | <span data-ttu-id="16776-559">Значение</span><span class="sxs-lookup"><span data-stu-id="16776-559">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16776-560">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16776-560">Minimum supported client</span></span><br/> | <span data-ttu-id="16776-561">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16776-561">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16776-562">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16776-562">Minimum supported server</span></span><br/> | <span data-ttu-id="16776-563">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16776-563">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="16776-564">Header</span><span class="sxs-lookup"><span data-stu-id="16776-564">Header</span></span><br/>                   | <dl> <span data-ttu-id="16776-565"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="16776-565"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





