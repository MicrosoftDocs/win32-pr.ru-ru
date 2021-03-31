---
title: Структура BG_JOB_TIMES (Deliveryoptimization. h)
description: Структура BG_JOB_TIMES предоставляет штампы времени, связанные с заданием.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Структура BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801391"
---
# <a name="bg_job_times-structure"></a>Структура BG_JOB_TIMES

Структура **BG_JOB_TIMES** предоставляет штампы времени, связанные с заданием.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a>Члены

<dl> <dt>

**CreationTime**
</dt> <dd>

Время создания задания. Время указывается в виде [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**модификатионтиме**
</dt> <dd>

Время последнего изменения задания или передачи байтов. Изменение этого значения осуществляется путем добавления файлов или вызова любого из методов Set в интерфейсах [ * *использованием метода ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) . Кроме того, изменения в состоянии задания и вызов методов [_ *Suspend* *](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)и [**Complete**](ibackgroundcopyjob-complete.md) изменяют это значение. Время указывается в виде [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**трансферкомплетионтиме**
</dt> <dd>

Время, когда задание перешло в состояние BG_JOB_STATE_TRANSFERRED. Время указывается в виде [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob:: навремя**](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

