---
title: Идентификаторы веса фильтра (Фвпму. h)
description: Фильтрация идентификаторов веса, используемых модулем базовой фильтрации (BFE) для расчета автоматически создаваемых весов фильтра.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682056"
---
# <a name="filter-weight-identifiers"></a><span data-ttu-id="c610c-103">Идентификаторы веса фильтра</span><span class="sxs-lookup"><span data-stu-id="c610c-103">Filter Weight Identifiers</span></span>

<span data-ttu-id="c610c-104">Ниже перечислены идентификаторы веса фильтра, используемые модулем базовой фильтрации (BFE) для расчета автоматически создаваемых весовых коэффициентов фильтра.</span><span class="sxs-lookup"><span data-stu-id="c610c-104">The filter weight identifiers used by the Base Filtering Engine (BFE) to compute auto-generated filter weights are listed below.</span></span>

<span data-ttu-id="c610c-105">Дополнительные сведения о создании веса фильтра см. в разделе [назначение веса фильтра](filter-weight-assignment.md) .</span><span class="sxs-lookup"><span data-stu-id="c610c-105">See [Filter Weight Assignment](filter-weight-assignment.md) for more information on filter weight generation.</span></span>

<dl> <dt>

<span data-ttu-id="c610c-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**ФВПМ \_ \_ автовесовых \_ разрядов**</span><span class="sxs-lookup"><span data-stu-id="c610c-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM\_AUTO\_WEIGHT\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c610c-107">(60)</span><span class="sxs-lookup"><span data-stu-id="c610c-107">(60)</span></span>
</dt> <dt>



<span data-ttu-id="c610c-108">Число битов, используемых для автоматически создаваемых весов фильтра.</span><span class="sxs-lookup"><span data-stu-id="c610c-108">Number of bits used for auto-generated filter weights.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c610c-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**ФВПМ \_ автоматического \_ веса \_**</span><span class="sxs-lookup"><span data-stu-id="c610c-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM\_AUTO\_WEIGHT\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c610c-110">(**MAXUINT64** >> 4)</span><span class="sxs-lookup"><span data-stu-id="c610c-110">(**MAXUINT64** >> 4)</span></span>
</dt> <dt>



<span data-ttu-id="c610c-111">Максимальный автоматически сформированный вес фильтра.</span><span class="sxs-lookup"><span data-stu-id="c610c-111">Maximum auto-generated filter weight.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c610c-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**</span><span class="sxs-lookup"><span data-stu-id="c610c-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c610c-113">0xC</span><span class="sxs-lookup"><span data-stu-id="c610c-113">(0xC)</span></span>
</dt> <dt>



<span data-ttu-id="c610c-114">BFE назначает вес с этим значением диапазона для фильтров IKE и AuthIP.</span><span class="sxs-lookup"><span data-stu-id="c610c-114">BFE assigns a weight with this range value to IKE and AuthIP filters.</span></span>

<span data-ttu-id="c610c-115">Дополнительные сведения о фильтрах IKE/AuthIP см. в разделе [исключения IKE/AuthIP](ike-exemptions.md) .</span><span class="sxs-lookup"><span data-stu-id="c610c-115">See [IKE/AuthIP Exemptions](ike-exemptions.md) for more information on IKE/AuthIP filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c610c-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**ФВПМ \_ вес \_ диапазона \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="c610c-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM\_WEIGHT\_RANGE\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c610c-117">(0x0)</span><span class="sxs-lookup"><span data-stu-id="c610c-117">(0x0)</span></span>
</dt> <dt>



<span data-ttu-id="c610c-118">BFE назначает вес с этим значением диапазона для фильтров политики IPsec.</span><span class="sxs-lookup"><span data-stu-id="c610c-118">BFE assigns a weight with this range value to IPsec policy filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c610c-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**\_ \_ максимальный диапазон весов \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="c610c-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM\_WEIGHT\_RANGE\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c610c-120">(**MAXUINT64** >> 60)</span><span class="sxs-lookup"><span data-stu-id="c610c-120">(**MAXUINT64** >> 60)</span></span>
</dt> <dt>



<span data-ttu-id="c610c-121">Максимально допустимое значение диапазона веса фильтра.</span><span class="sxs-lookup"><span data-stu-id="c610c-121">Maximum allowed filter weight range value.</span></span>


</dt> </dl> </dd> </dl>

> [!Note]  
> <span data-ttu-id="c610c-122">**MAXUINT64** представляет максимально возможное значение **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="c610c-122">**MAXUINT64** represents the largest possible value of **UINT64**.</span></span> <span data-ttu-id="c610c-123">Значение этой константы — 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c610c-123">The value of this constant is 0xFFFFFFFFFFFFFFFF.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c610c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c610c-124">Requirements</span></span>



| <span data-ttu-id="c610c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c610c-125">Requirement</span></span> | <span data-ttu-id="c610c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c610c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c610c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c610c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c610c-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c610c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c610c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c610c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c610c-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c610c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c610c-131">Header</span><span class="sxs-lookup"><span data-stu-id="c610c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c610c-132"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="c610c-132"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





