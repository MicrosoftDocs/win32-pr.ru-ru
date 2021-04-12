---
description: Содержит сведения о процессоре.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Структура PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345485"
---
# <a name="processor_power_information-structure"></a>\_ \_ Структура сведений о ПИТАНИи процессора

Содержит сведения о процессоре.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a>Члены

<dl> <dt>

**Число**
</dt> <dd>

Номер системного процессора.

</dd> <dt>

**максмхз**
</dt> <dd>

Максимальная заданная частота таймера системного процессора в мегагерцах.

</dd> <dt>

**куррентмхз**
</dt> <dd>

Тактовая частота процессора в мегагерцах. Это число — это максимально заданная частота такта процессора, умноженная на текущее регулирование процессора.

</dd> <dt>

**мхзлимит**
</dt> <dd>

Ограничение тактовой частоты процессора в мегагерцах. Это число является максимальной тактовой частотой процессора, умноженной на текущий предел регулирования температуры процессора.

</dd> <dt>

**максидлестате**
</dt> <dd>

Максимальное состояние простоя этого процессора.

</dd> <dt>

**куррентидлестате**
</dt> <dd>

Текущее состояние простоя этого процессора.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Обратите внимание, что это определение структуры было случайно опущено в WinNT. h. Эта ошибка будет исправлена в будущем. Тем временем, чтобы скомпилировать приложение, включите в исходный код определение структуры, содержащееся в этом разделе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**каллнтповеринформатион**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




