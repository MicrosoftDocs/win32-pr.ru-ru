---
title: Перечисление MPEXECUTION_STATUS (Мпклиент. h)
description: Возможное состояние выполнения угрозы.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS перечисления устаревших Windows компонентов среды
- PMPEXECUTION_STATUSные компоненты среды Windows указателя перечисления
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
ms.openlocfilehash: 6e4748b6d97e1b7ee05db8044837b89e2653a14fd1e6f87068a40107cdd9ee60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943914"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





