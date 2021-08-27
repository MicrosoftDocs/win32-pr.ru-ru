---
title: Перечисление MPDETECTION_ORIGIN (Мпклиент. h)
description: Источник обнаружения.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN перечисления устаревших Windows компонентов среды
- PMPDETECTION_ORIGINные компоненты среды Windows указателя перечисления
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70b46ed86276ccb3fc3bd4d2b26388d778c102c1c1fa3bb7ced8f1ad64cd0203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092364"
---
# <a name="mpdetection_origin-enumeration"></a>\_Перечисление источника мпдетектион

Источник обнаружения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**\_неизвестный источник мпдетектион \_**
</dt> <dd>

Обнаруженная угрозой причина неизвестна.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**МПДЕТЕКТИОН \_ исходный \_ локальный \_ компьютер**
</dt> <dd>

Обнаружена угроза на локальном компьютере.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**МПДЕТЕКТИОН \_ происхождение \_ нетворкшаре**
</dt> <dd>

Обнаружена угроза на сетевом ресурсе.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**МПДЕТЕКТИОН \_ Источник \_ Интернет**
</dt> <dd>

Обнаружена угроза в Интернете.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**\_исходящий \_ трафик источника мпдетектион**
</dt> <dd>

Обнаружена угроза исходящего подключения.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**\_входящий источник \_ мпдетектион**
</dt> <dd>

Обнаружена угроза во входящем соединении.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





