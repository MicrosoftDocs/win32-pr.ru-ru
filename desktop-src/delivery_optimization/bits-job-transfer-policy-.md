---
title: Перечисление BITS_JOB_TRANSFER_POLICY (Deliveryoptimization. h)
description: Перечисление BITS_JOB_TRANSFER_POLICY определяет значения ИДЕНТИФИКАТОРов, соответствующие свойствам DO.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- Перечисление BITS_JOB_TRANSFER_POLICY
- Перечисление BITS_JOB_TRANSFER_POLICY
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 022d12b78416ce4ec84cf02ae8696f17bf5c315a207ae04f28a8980f6aaac073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544602"
---
# <a name="bits_job_transfer_policy-enumeration"></a>Перечисление BITS_JOB_TRANSFER_POLICY

Перечисление **BITS_JOB_TRANSFER_POLICY** определяет значения идентификаторов, соответствующие свойствам Do.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**
</dt> <dd>

Указывает, что задание будет передано при наличии подключения, независимо от стоимости.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**
</dt> <dd>

Указывает, что задание будет передано при наличии подключения, если это подключение не подлежит доплатам роуминга.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**
</dt> <dd>

Указывает, что задание будет передано только при наличии подключения, которое не подлежит оплате.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**
</dt> <dd>

Указывает, что задание будет передано только при наличии подключения, которое не подлежит оплате или приближается к исчерпанию.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**
</dt> <dd>

Указывает, что задание будет передано только при наличии подключения, которое не накладывает затраты или лимиты трафика.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





