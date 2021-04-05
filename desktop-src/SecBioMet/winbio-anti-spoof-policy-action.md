---
title: Перечисление WINBIO_ANTI_SPOOF_POLICY_ACTION (Винбио \_ types. h)
description: Указывает типы действий, выполняемых для политики антиподмены пользователя.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- API биометрическая платформа Windows перечисления WINBIO_ANTI_SPOOF_POLICY_ACTION
- API биометрическая платформа Windows указателя перечисления PWINBIO_ANTI_SPOOF_POLICY
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988878"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>\_ \_ \_ \_ Перечисление действий политики антифишинга винбио

Указывает типы действий, выполняемых для политики антиподмены пользователя.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**\_отключение антифишинга винбио \_ \_**
</dt> <dd>

Отключает обнаружение подмены для биометрического фактора.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**\_Включение антифишинга винбио \_ \_**
</dt> <dd>

Включает обнаружение подмены для биометрического фактора.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**\_Удаление антифишинга винбио \_ \_**
</dt> <dd>

Удаляет из учетной записи всю политику антиподмены для биометрического коэффициента.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ действие политики АНТИфишинга винбио \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_источник политики \_ винбио**](winbio-policy-source.md)
</dt> </dl>

 

 





