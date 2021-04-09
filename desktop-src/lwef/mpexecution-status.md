---
title: Перечисление MPEXECUTION_STATUS (Мпклиент. h)
description: Возможное состояние выполнения угрозы.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS перечисления устаревшие функции среды Windows
- PMPEXECUTION_STATUS указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891721"
---
# <a name="mpexecution_status-enumeration"></a>\_Перечисление состояния мпексекутион

Возможное состояние выполнения угрозы.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**\_состояние выполнения пакета управления \_ \_ неизвестно**
</dt> <dd>

Состояние выполнения неизвестно.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**\_состояние выполнения пакета управления \_ \_ заблокировано**
</dt> <dd>

Заблокировано выполнение с помощью мини-фильтра.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**\_ \_ разрешено состояние выполнения пакета управления \_**
</dt> <dd>

Разрешено выполнять с помощью мини-фильтра.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**\_ \_ выполнение состояния выполнения пакета управления \_**
</dt> <dd>

Идет запуск угрозы.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**\_состояние выполнения пакета управления \_ \_ не \_ выполняется**
</dt> <dd>

Угроза не исполняется и доступна только из подсистемы во время исправления.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





