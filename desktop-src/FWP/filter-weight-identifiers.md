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
ms.openlocfilehash: 555ffcda5ef6e8e062577d66f4264c2c4c0ed253b96b9465e5b68eec4bd08587
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813860"
---
# <a name="filter-weight-identifiers"></a>Идентификаторы веса фильтра

Ниже перечислены идентификаторы веса фильтра, используемые модулем базовой фильтрации (BFE) для расчета автоматически создаваемых весовых коэффициентов фильтра.

Дополнительные сведения о создании веса фильтра см. в разделе [назначение веса фильтра](filter-weight-assignment.md) .

<dl> <dt>

<span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**ФВПМ \_ \_ автовесовых \_ разрядов**
</dt> <dd> <dl> <dt>

(60)
</dt> <dt>



Число битов, используемых для автоматически создаваемых весов фильтра.


</dt> </dl> </dd> <dt>

<span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**ФВПМ \_ автоматического \_ веса \_**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 4)
</dt> <dt>



Максимальный автоматически сформированный вес фильтра.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ исключения IKE для диапазона веса \_ фвпм \_**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



BFE назначает вес с этим значением диапазона для фильтров IKE и AuthIP.

Дополнительные сведения о фильтрах IKE/AuthIP см. в разделе [исключения IKE/AuthIP](ike-exemptions.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**ФВПМ \_ вес \_ диапазона \_ IPSec**
</dt> <dd> <dl> <dt>

(0x0)
</dt> <dt>



BFE назначает вес с этим значением диапазона для фильтров политики IPsec.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**\_ \_ максимальный диапазон весов \_ фвпм**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 60)
</dt> <dt>



Максимально допустимое значение диапазона веса фильтра.


</dt> </dl> </dd> </dl>

> [!Note]  
> **MAXUINT64** представляет максимально возможное значение **UINT64**. Значение этой константы — 0xFFFFFFFFFFFFFFFF.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



 

 





