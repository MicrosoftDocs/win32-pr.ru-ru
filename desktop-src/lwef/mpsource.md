---
title: Перечисление МПСАУРЦЕ (Мпклиент. h)
description: Возможная Категория источника.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Перечисление МПСАУРЦЕ. устаревшие функции среды Windows
- Устаревшие компоненты среды Windows в указателе перечисления ПМПСАУРЦЕ
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
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988921"
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

Загрузки IE и инициированные вложения Outlook Express.

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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





