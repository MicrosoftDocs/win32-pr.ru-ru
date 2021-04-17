---
title: Идентификаторы встроенных поставщиков (Фвпму. h)
description: Идентификаторы для поставщиков, встроенных в платформу фильтрации Windows (WFP), представляются с помощью идентификатора GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661951"
---
# <a name="built-in-provider-identifiers"></a><span data-ttu-id="07433-103">Встроенные идентификаторы поставщиков</span><span class="sxs-lookup"><span data-stu-id="07433-103">Built-in Provider Identifiers</span></span>

<span data-ttu-id="07433-104">Идентификаторы для поставщиков, встроенных в платформу фильтрации Windows (WFP), представляются с помощью идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="07433-104">The identifiers for the providers that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="07433-105">Эти идентификаторы определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="07433-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="07433-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**\_IKEEXT поставщика \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="07433-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**FWPM\_PROVIDER\_IKEEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07433-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span><span class="sxs-lookup"><span data-stu-id="07433-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span></span>
</dt> <dt>



<span data-ttu-id="07433-108">Используется для обнаружения всех фильтров, добавленных IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="07433-108">Used to identify all the filters added by IKE/AuthIP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07433-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_Конфигурация фвпм поставщика \_ IPSec для \_ DOS \_**</span><span class="sxs-lookup"><span data-stu-id="07433-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**FWPM\_PROVIDER\_IPSEC\_DOS\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07433-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span><span class="sxs-lookup"><span data-stu-id="07433-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span></span>
</dt> <dt>



<span data-ttu-id="07433-111">Используется для обнаружения всех фильтров, добавленных функцией защиты IPsec в DoS.</span><span class="sxs-lookup"><span data-stu-id="07433-111">Used to identify all the filters added by IPsec DoS Protection.</span></span>

> [!Note]  
> <span data-ttu-id="07433-112">Доступно только в Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="07433-112">Available only on Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="07433-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_ \_ \_ разгрузка TCP \_ CHIMNEY поставщика фвпм**</span><span class="sxs-lookup"><span data-stu-id="07433-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**FWPM\_PROVIDER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07433-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span><span class="sxs-lookup"><span data-stu-id="07433-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span></span>
</dt> <dt>



<span data-ttu-id="07433-115">Используется для обнаружения всех фильтров, добавленных разгрузкой TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="07433-115">Used to identify all the filters added by TCP Chimney Offload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="07433-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**\_ \_ шаблоны TCP поставщика \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="07433-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**FWPM\_PROVIDER\_TCP\_TEMPLATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07433-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span><span class="sxs-lookup"><span data-stu-id="07433-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span></span>
</dt> <dt>



<span data-ttu-id="07433-118">Используется для поиска всех фильтров, добавленных с помощью шаблонов TCP.</span><span class="sxs-lookup"><span data-stu-id="07433-118">Used to identify all the filters added by TCP templates.</span></span>

> [!Note]  
> <span data-ttu-id="07433-119">Доступно только в Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="07433-119">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07433-120">Требования</span><span class="sxs-lookup"><span data-stu-id="07433-120">Requirements</span></span>



| <span data-ttu-id="07433-121">Требование</span><span class="sxs-lookup"><span data-stu-id="07433-121">Requirement</span></span> | <span data-ttu-id="07433-122">Значение</span><span class="sxs-lookup"><span data-stu-id="07433-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07433-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07433-123">Minimum supported client</span></span><br/> | <span data-ttu-id="07433-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07433-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="07433-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07433-125">Minimum supported server</span></span><br/> | <span data-ttu-id="07433-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07433-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="07433-127">Header</span><span class="sxs-lookup"><span data-stu-id="07433-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="07433-128"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="07433-128"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





