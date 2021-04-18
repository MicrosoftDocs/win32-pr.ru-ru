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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Фвпму. h</dt> </dl> |



 

 





