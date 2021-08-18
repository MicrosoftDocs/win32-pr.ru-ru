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
ms.openlocfilehash: f65fec198a0784bf076eb90224318bd36a88ba3ed96258ffd2014a27da5c8f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911273"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ действие политики АНТИфишинга винбио \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_источник политики \_ винбио**](winbio-policy-source.md)
</dt> </dl>

 

 





