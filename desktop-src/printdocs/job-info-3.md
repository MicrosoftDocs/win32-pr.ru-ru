---
description: '\_Структура сведений о задании \_ 3 используется для связывания набора заданий печати.'
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Структура JOB_INFO_3 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272482"
---
# <a name="job_info_3-structure"></a>\_Структура сведений о задании \_ 3

Структура **\_ сведений о \_ задании 3** используется для связывания набора заданий печати.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a>Члены

<dl> <dt>

**JobId**
</dt> <dd>

Идентификатор задания печати.

</dd> <dt>

**некстжобид**
</dt> <dd>

Идентификатор задания печати для следующего задания печати в связанном наборе заданий печати.

</dd> <dt>

**Reserved**
</dt> <dd>

Это значение зарезервировано для использования в будущем. Необходимо присвоить ему нулевое значение.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**енумжобс**](enumjobs.md)
</dt> <dt>

[**жетжоб**](getjob.md)
</dt> <dt>

[**сетжоб**](setjob.md)
</dt> </dl>

 

 




