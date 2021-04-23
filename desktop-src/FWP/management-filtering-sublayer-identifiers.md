---
title: Фильтрация идентификаторов подслоя (Фвпму. h)
description: Константы идентификатора подслоя фильтрации управления API WFP.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e015d590c19395987bbd47d1c3c4b918296ab5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892425"
---
# <a name="filtering-sublayer-identifiers"></a><span data-ttu-id="ff093-103">Фильтрация идентификаторов подслоя</span><span class="sxs-lookup"><span data-stu-id="ff093-103">Filtering Sublayer Identifiers</span></span>

<span data-ttu-id="ff093-104">Идентификаторы подслоя платформы фильтрации Windows (WFP) представлены с помощью идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="ff093-104">The Windows Filtering Platform (WFP) sublayer identifiers are each represented by a GUID.</span></span>

<span data-ttu-id="ff093-105">Эти идентификаторы определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ff093-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="ff093-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**подслой ФВПМ для \_ \_ обхода краев подслоя \_ фвпм ( \_ \_ TEREDO)**</span><span class="sxs-lookup"><span data-stu-id="ff093-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM\_SUBLAYER\_EDGE\_TRAVERSAL / FWPM\_SUBLAYER\_TEREDO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-107">Фильтры обхода узлов добавляются в этот подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-107">Edge traversal filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="ff093-108">Для Windows 7 и более поздних версий используйте **\_ \_ \_ обход фвпм для подслоя**.</span><span class="sxs-lookup"><span data-stu-id="ff093-108">For Windows 7 and later, use **FWPM\_SUBLAYER\_EDGE\_TRAVERSAL**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_Проверка ПОДСЛОЯ \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="ff093-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM\_SUBLAYER\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-110">Это самый низкий взвешенный подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-110">This is the lowest weighted sublayer.</span></span> <span data-ttu-id="ff093-111">Он используется только для фильтров проверки.</span><span class="sxs-lookup"><span data-stu-id="ff093-111">It is used only for inspection filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_ПОДУРОВЕНЬ фвпм \_ IPSec \_ досп**</span><span class="sxs-lookup"><span data-stu-id="ff093-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM\_SUBLAYER\_IPSEC\_DOSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-113">Фильтры защиты IPsec DoS добавляются в этот подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-113">IPsec DoS Protection filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="ff093-114">Доступно только в Windows Vista с пакетом обновления 1 (SP1), Windows Server 2008 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ff093-114">Available only on Windows Vista with SP1, Windows Server 2008, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_ \_ \_ Перенаправление \_ исходящего \_ туннеля IPSec на подуровне фвпм**</span><span class="sxs-lookup"><span data-stu-id="ff093-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-116">Фильтры перенаправления исходящих туннелей IPsec добавляются в этот подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-116">IPsec forward outbound tunnel filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="ff093-117">Доступно только в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ff093-117">Available only on Windows 7, Windows Server 2008 R2, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_ \_ Туннелирование IPSec ПОДслоя фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="ff093-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-119">Фильтры туннеля IPsec добавляются в этот подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-119">IPsec tunnel filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_пакеты LIP ПОДСЛОЯ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="ff093-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM\_SUBLAYER\_LIPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-121">В этот подуровень добавляются устаревшие фильтры IPsec.</span><span class="sxs-lookup"><span data-stu-id="ff093-121">Legacy IPsec filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_Аудит RPC ПОДСЛОЯ фвпм \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ff093-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM\_SUBLAYER\_RPC\_AUDIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-123">Фильтры аудита RPC добавляются в этот подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-123">RPC audit filters are added to this sublayer.</span></span> <span data-ttu-id="ff093-124">Эти фильтры Произведите аудит входящих вызовов RPC как часть C2 и соответствие стандарту Common условия_отбора.</span><span class="sxs-lookup"><span data-stu-id="ff093-124">These filters audit RPC incoming calls as part of C2 and common criteria compliance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_ \_ защищенный сокет ПОДслоя фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="ff093-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM\_SUBLAYER\_SECURE\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-126">Фильтры защищенных сокетов добавляются в этот подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-126">Secure socket filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ разгрузка TCP \_ CHIMNEY подслоя фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="ff093-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM\_SUBLAYER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-128">Фильтры разгрузки TCP Chimney добавляются в этот подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-128">TCP Chimney Offload filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_шаблоны TCP ПОДСЛОЯ фвпм \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ff093-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM\_SUBLAYER\_TCP\_TEMPLATES**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-130">Фильтры шаблонов TCP добавляются в этот подуровень.</span><span class="sxs-lookup"><span data-stu-id="ff093-130">TCP template filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="ff093-131">Доступно только в Windows 8, Windows Server 2012 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ff093-131">Available only on Windows 8, Windows Server 2012, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff093-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**\_универсальный ПОДУРОВЕНЬ \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="ff093-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM\_SUBLAYER\_UNIVERSAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff093-133">Этот подуровень содержит все фильтры, которые не назначены ни одному из других подслоев.</span><span class="sxs-lookup"><span data-stu-id="ff093-133">This sublayer hosts all filters that are not assigned to any of the other sublayers.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff093-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ff093-134">Requirements</span></span>



| <span data-ttu-id="ff093-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ff093-135">Requirement</span></span> | <span data-ttu-id="ff093-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ff093-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff093-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff093-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ff093-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff093-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ff093-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff093-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ff093-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff093-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ff093-141">Header</span><span class="sxs-lookup"><span data-stu-id="ff093-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff093-142"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff093-142"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





