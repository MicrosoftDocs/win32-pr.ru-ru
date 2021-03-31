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
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071489"
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

## <a name="remarks"></a>Комментарии

Несколько переносов переднего плана и фоновых передач могут выполняться одновременно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob:: предшествовал**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





