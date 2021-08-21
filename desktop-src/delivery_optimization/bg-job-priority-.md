---
title: Перечисление BG_JOB_PRIORITY (Deliveryoptimization. h)
description: Перечисление BG_JOB_PRIORITY определяет постоянные значения, указывающие уровень приоритета задания.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Перечисление BG_JOB_PRIORITY
- Перечисление BG_JOB_PRIORITY
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ddeb3ea128f173d53c71467d4098c1b777beea48f7b1304922f7468d55fc3b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810957"
---
# <a name="bg_job_priority-enumeration"></a>Перечисление BG_JOB_PRIORITY

Перечисление **BG_JOB_PRIORITY** определяет постоянные значения, указывающие уровень приоритета задания.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**
</dt> <dd>

Передает задание на передний план. Переносы переднего плана приводят к пропускной способности сети с другими приложениями, что может помешать работе пользователя в сети. Это уровень наивысшего приоритета.

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

Передает задание в фоновом режиме. Фоновая передача использует небольшой процент пропускной способности сети.

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

Поведение выполняется для всех заданий, не являющихся основными. Дополнительные сведения см. в комментариях в BG_JOB_PRIORITY_HIGH.

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

Поведение выполняется для всех заданий, не являющихся основными. Дополнительные сведения см. в комментариях в BG_JOB_PRIORITY_HIGH.

</dd> </dl>

## <a name="remarks"></a>Remarks

Несколько переносов переднего плана и фоновых передач могут выполняться одновременно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob:: предшествовал**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





