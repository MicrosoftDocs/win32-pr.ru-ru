---
title: Перечисление BG_JOB_STATE (Deliveryoptimization. h)
description: Перечисление BG_JOB_STATE определяет константные значения для различных состояний задания.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Перечисление BG_JOB_STATE
- Перечисление BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710456"
---
# <a name="bg_job_state-enumeration"></a>Перечисление BG_JOB_STATE

Перечисление **BG_JOB_STATE** определяет константные значения для различных состояний задания.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**
</dt> <dd>

Указывает, что задание находится в очереди и ожидает запуска. Если пользователь выходит из системы во время передачи задания, задание переходит в состояние очереди.

</dd> <dt>

<span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**
</dt> <dd>

Не поддерживается.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**
</dt> <dd>

Указывает, что передает данные для задания.

</dd> <dt>

<span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**
</dt> <dd>

Указывает, что задание приостановлено (приостановлено). Чтобы приостановить задание, вызовите метод [**использованием метода ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md) . Задание остается приостановленным до тех пор, пока не будет вызван метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md), [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)или [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .

</dd> <dt>

<span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**
</dt> <dd>

Указывает, что произошла неустранимая ошибка (службе не удается переместить файл). Если ошибку, например ошибку отказа в доступе, можно исправить, вызовите метод [**использованием метода ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) после устранения ошибки. Однако если ошибку невозможно исправить, вызовите метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) , чтобы отменить задание, или вызовите метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) , чтобы принять часть задания загрузки, которая успешно прошла передачу.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**
</dt> <dd>

Указывает, что произошла устранимая ошибка. Будут повторены задания в состоянии временной ошибки на основе внутренней конфигурации повторных попыток. Состояние задания меняется на **BG_JOB_STATE_ERROR** , если задание не выполняется (см. раздел [**использованием метода ibackgroundcopyjob:: сетнопрогресстимеаут**](ibackgroundcopyjob-setnoprogresstimeout.md)).

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**
</dt> <dd>

Указывает, что задание успешно обработано. Чтобы подтвердить завершение задания и предоставить доступ к файлам клиенту, необходимо вызвать метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .

</dd> <dt>

<span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**
</dt> <dd>

Указывает, что вы вызвали метод [**использованием метода ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) , чтобы подтвердить успешное завершение задания.

</dd> <dt>

<span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**
</dt> <dd>

Указывает, что вы вызвали метод [**использованием метода ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) для отмены задания (удалите задание из очереди на перемещение).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob:: State**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





