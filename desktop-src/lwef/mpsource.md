---
title: Перечисление МПСАУРЦЕ (Мпклиент. h)
description: Возможная Категория источника.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- мпсаурце перечисления устаревших компонентов среды Windows
- Windows компонентов среды устаревшего указателя перечисления пмпсаурце
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59eb014ab78645d78cd2942c37477d9a19d2572826859be77c6f5ecddfcb1bda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961104"
---
# <a name="mpsource-enumeration"></a>Перечисление МПСАУРЦЕ

Возможная Категория источника.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**МПСАУРЦЕ \_ неизвестный**
</dt> <dd>

Источник неизвестен.

</dd> <dt>

<span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**\_пользователь мпсаурце**
</dt> <dd>

Инициировано пользователем.

</dd> <dt>

<span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**МПСАУРЦЕ \_ система**
</dt> <dd>

инициировано системой.

</dd> <dt>

<span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**МПСАУРЦЕ в \_ реальном времени**
</dt> <dd>

Запущен компонент реального времени.

</dd> <dt>

<span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**МПСАУРЦЕ \_ защиту ioav**
</dt> <dd>

загрузки IE и инициированы Outlookные вложения Express.

</dd> <dt>

<span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**МПСАУРЦЕ \_ NIS**
</dt> <dd>

Система проверки сети.

</dd> <dt>

<span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**\_объект BHO мпсаурце**
</dt> <dd>

Объект BHO — веб-скрипт (не рекомендуется).

</dd> <dt>

<span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**МПСАУРЦЕ \_ иепротект**
</dt> <dd>

IE — Иекстенсионвалидатион.

</dd> <dt>

<span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**МПСАУРЦЕ \_ ELAM**
</dt> <dd>

ELAM

</dd> <dt>

<span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**МПСАУРЦЕ \_ локальную \_ аттестацию**
</dt> <dd>

Локальная аттестация.

</dd> <dt>

<span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**МПСАУРЦЕ \_ Удаленная \_ аттестация**
</dt> <dd>

Удаленная аттестация.

</dd> <dt>

<span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**МПСАУРЦЕ \_ AMSI**
</dt> <dd>

AMSI

</dd> <dt>

<span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**Источник пакета управления \_ \_ MaxValue**
</dt> <dd>

Максимально возможное значение.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





