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
ms.openlocfilehash: 111b292c5f355aceefa95fb01bafc2cb9220757618d39d4b3ca29bbf77ca4570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948684"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 




