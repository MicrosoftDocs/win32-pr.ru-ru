---
title: BITS_COST_STATE (Bits5 \_ 0. h)
description: '\_ \_ Перечисление состояния затрат BITS определяет постоянные значения, которые определяют состояние стоимости BITS.'
ms.assetid: A8C36D4E-98B3-45C4-9ECD-9B5280133176
topic_type:
- apiref
api_name:
- BITS_COST_STATE_UNRESTRICTED
- BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
- BITS_COST_STATE_BELOW_CAP
- BITS_COST_STATE_NEAR_CAP
- BITS_COST_STATE_OVERCAP_CHARGED
- BITS_COST_STATE_OVERCAP_THROTTLED
- BITS_COST_STATE_USAGE_BASED
- BITS_COST_OPTION_IGNORE_CONGESTION
- BITS_COST_STATE_RESERVED
- BITS_COST_STATE_TRANSFER_NOT_ROAMING
- BITS_COST_STATE_TRANSFER_NO_SURCHARGE
- BITS_COST_STATE_TRANSFER_STANDARD
- BITS_COST_STATE_TRANSFER_UNRESTRICTED
- BITS_COST_STATE_TRANSFER_ALWAYS
api_location:
- Bits5_0.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/20/2019
ms.openlocfilehash: ecbe54966a54310af71a4c96a3d3c2423f524f9b8a8067b10350fba05675a54b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701984"
---
# <a name="bits_cost_state"></a>\_состояние стоимости \_ BITS

Определяет константы, указывающие состояние стоимости BITS.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**\_ \_ неограниченное состояние стоимости BITS \_**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**\_ \_ \_ \_ неизвестное использование состояния затрат \_ BITS**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**\_состояние стоимости \_ BITS \_ ниже \_ ограничения**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**\_состояние стоимости BITS при \_ \_ приближении к \_ концу**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**\_оверкап по \_ состоянию стоимости \_ службы BITS \_**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**\_состояние стоимости \_ BITS \_ оверкап \_ регулируется**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**\_ \_ использование состояния стоимости \_ BITS \_ на основе**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**\_ \_ параметр "стоимость BITS" \_ игнорирует \_ перегрузку**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**\_состояние стоимости \_ BITS \_ зарезервировано**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Зарезервировано.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**\_Отслеживание состояния расхода BITS — \_ \_ \_ нет \_ роуминга**
</dt> <dd> <dl> <dt>

(BITS \_ \_параметр "стоимость" \_ пропуск \_ перегруженных \| разрядов \_ состояние расхода \_ \_ \_ на основе \| BITS \_ стоимость \_ состояния \_ оверкап \_ регулируемые \| биты \_ затраты \_ состояния \_ оверкап \_ плата за \| BITS \_ \_ состояние \_ почти \_ Cap \| бит \_ стоимость \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**\_ \_ Отслеживание состояния стоимости \_ BITS \_ без \_ доплаты**
</dt> <dd> <dl> <dt>

(BITS \_ \_параметр "стоимость" \_ пропустить \_ перегруженность \| бит \_ стоимость \_ \_ использования \_ на основе \| BITS \_ стоимость \_ состояния \_ оверкап \_ регулируемые \| биты \_ затраты \_ состояние \_ почти \_ закрепления \| биты \_ стоимость \_ \_ ниже \_ ограничения \| \_ \_ \_ \_ \_ \| \_ \_ \_
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**\_ \_ \_ стандарт передачи состояния затрат \_ BITS**
</dt> <dd> <dl> <dt>

(BITS \_ \_параметр "стоимость" \_ пропустить \_ перегруженность \| бит \_ стоимость \_ \_ использования \_ на основе \| BITS \_ стоимость \_ состояния \_ оверкап \_ регулируемых \| битов \_ \_ состояние стоимости \_ ниже \_ ограничения затраты на \| \_ \_ \_ \_ использование \_ неизвестного состояния стоимость \| \_ \_ \_ неограниченно 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**\_Отслеживание состояния затрат BITS — \_ \_ \_ неограниченное перемещение**
</dt> <dd> <dl> <dt>

(BITS \_ \_параметр "стоимость" \_ пропуск \_ перегруженных \| битов \_ \_ состояние стоимости \_ оверкап \_ регулируемые \| биты \_ стоимость \_ \_ неограниченного состояния)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**\_Отслеживание состояния расхода BITS \_ \_ \_ всегда**
</dt> <dd> <dl> <dt>

(BITS \_ \_параметр "стоимость" \_ пропуск \_ перегруженных \| битов \_ затраты \_ состояния \_ роуминг \| бит \_ стоимость \_ \_ использования \_ на основе \| бит \_ стоимость \_ состояния \_ оверкап \_ регулируемые \| биты \_ стоимость \_ состояния \_ оверкап \_ плата за \| биты \_ \_ состояние \_ почти \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \_ \| \_ \_ \_ заряжена состояние затраты
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>Bits5 \_ 0. h (включить BITS. h)</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Bits5 \_ 0. idl</dt> </dl>                |



 

 





