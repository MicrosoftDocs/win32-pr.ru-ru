---
title: Идентификаторы контекста фильтра (Фвпму. h)
description: Идентификаторы для контекстов фильтра, встроенных в платформу фильтрации Windows.
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09968f1ab68016405f22460409e83cfd826b716
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661973"
---
# <a name="filter-context-identifiers"></a><span data-ttu-id="41493-103">Фильтровать идентификаторы контекста</span><span class="sxs-lookup"><span data-stu-id="41493-103">Filter Context Identifiers</span></span>

<span data-ttu-id="41493-104">Идентификаторы контекстов фильтров, встроенных в платформу фильтрации Windows, определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="41493-104">The identifiers for the filter contexts that are built in to the Windows Filtering Platform are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="41493-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**ФВПМ \_ контекст \_ \_ входящего трафика IPSec \_ , фвпм \_ контекст \_ IPSec \_ для \_ входящего \_ подключения сохранить \_ безопасность, \_ фвпм \_ контекст \_ входящего трафика IPSec \_ зарезервирован**</span><span class="sxs-lookup"><span data-stu-id="41493-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PASSTHRU, FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY, FWPM\_CONTEXT\_IPSEC\_INBOUND\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41493-106">Контексты фильтра транспорта IPsec на входящем уровне.</span><span class="sxs-lookup"><span data-stu-id="41493-106">IPsec transport filter contexts in inbound layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41493-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**ФВПМ \_ контекст \_ IPSec для \_ исходящей \_ согласованности \_ обнаружения, фвпм \_ контекст \_ IPSec \_ \_ исключать \_ согласование**</span><span class="sxs-lookup"><span data-stu-id="41493-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER, FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41493-108">Контексты фильтра транспорта IPsec на исходящем уровне.</span><span class="sxs-lookup"><span data-stu-id="41493-108">IPsec transport filter contexts in outbound layer.</span></span>

> [!Note]  
> <span data-ttu-id="41493-109">В Windows 7 Используйте **контекст фвпм \_ контексте \_ IPSec \_ \_ исключать \_ согласование**.</span><span class="sxs-lookup"><span data-stu-id="41493-109">For Windows 7, use **FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="41493-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**для \_ \_ \_ подключения к набору ALE контекста фвпм \_ \_ требуется \_ \_ безопасность IPSec, фвпм. \_ \_ \_ Установка \_ подключения " \_ ленивый \_ SD \_ "**</span><span class="sxs-lookup"><span data-stu-id="41493-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_SECURITY, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_LAZY\_SD\_EVALUATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41493-111">Контексты фильтра, используемые на уровне соединения ALE.</span><span class="sxs-lookup"><span data-stu-id="41493-111">Filter contexts used in the ALE connect layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41493-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**для \_ \_ \_ подключения к набору ALE контекста фвпм \_ \_ требуется \_ \_ шифрование IPSec, \_ \_ Подключение набора ALE контекста фвпм — \_ \_ \_ Разрешить \_ первый входящий незашифрованный общедоступный маркер общедоступного \_ \_ \_ контекста, фвпм \_ контекст \_ \_ \_ проверки подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="41493-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED, FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41493-113">Контексты фильтра, используемые на уровне соединения или принятия ALE.</span><span class="sxs-lookup"><span data-stu-id="41493-113">Filter contexts used in the ALE connect or accept layer.</span></span>

> [!Note]  
> <span data-ttu-id="41493-114">Для Windows 7 Используйте **\_ \_ Подключение Set ALE фвпм \_ , \_ \_ разрешающее получение \_ первого \_ входящего \_ \_ незашифрованного** или **фвпм \_ контекста, \_ \_ разрешающего \_ \_ встроенное по проверки подлинности**.</span><span class="sxs-lookup"><span data-stu-id="41493-114">For Windows 7, use **FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED** or **FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="41493-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_контекст фвпм \_ \_ \_ , включение разгрузки TCP CHIMNEY \_ , \_ Отключение контекста фвпм \_ TCP \_ Chimney \_ \_ Disable**</span><span class="sxs-lookup"><span data-stu-id="41493-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_ENABLE, FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_DISABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41493-116">Контексты, используемые выносками разгрузки TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="41493-116">Contexts used by the TCP Chimney Offload callouts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41493-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_ \_ Аудит RPC context \_ фвпм \_ включен**</span><span class="sxs-lookup"><span data-stu-id="41493-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**FWPM\_CONTEXT\_RPC\_AUDIT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="41493-118">Контексты, используемые в подуровне аудита RPC.</span><span class="sxs-lookup"><span data-stu-id="41493-118">Contexts used in the RPC audit sublayer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41493-119">Требования</span><span class="sxs-lookup"><span data-stu-id="41493-119">Requirements</span></span>



| <span data-ttu-id="41493-120">Требование</span><span class="sxs-lookup"><span data-stu-id="41493-120">Requirement</span></span> | <span data-ttu-id="41493-121">Значение</span><span class="sxs-lookup"><span data-stu-id="41493-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41493-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41493-122">Minimum supported client</span></span><br/> | <span data-ttu-id="41493-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41493-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="41493-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41493-124">Minimum supported server</span></span><br/> | <span data-ttu-id="41493-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41493-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="41493-126">Header</span><span class="sxs-lookup"><span data-stu-id="41493-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="41493-127"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="41493-127"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





