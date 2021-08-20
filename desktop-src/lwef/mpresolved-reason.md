---
title: Перечисление MPRESOLVED_REASON (Мпклиент. h)
description: Возможные причины сбоя исправления.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON перечисления устаревших Windows компонентов среды
- PMPRESOLVED_REASONные компоненты среды Windows указателя перечисления
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a365ef55d9fe2d76e619f3c772cc1df2e6c5e1c8c33721f24dc844d064b33398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975984"
---
# <a name="mpresolved_reason-enumeration"></a>\_Перечисление причин мпресолвед

Возможные причины сбоя исправления.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**\_Причина мпресолвед \_ неизвестна**
</dt> <dd>

В состоянии ошибки.

</dd> <dt>

<span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**МПРЕСОЛВЕД \_ Причина \_ полной \_ проверки**
</dt> <dd>

Выполнена полная проверка.

</dd> <dt>

<span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**Причина истечения \_ \_ времени \_ ожидания мпресолвед**
</dt> <dd>

Прошло достаточно времени. Значение по умолчанию — одна неделя.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





