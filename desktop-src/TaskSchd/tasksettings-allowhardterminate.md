---
title: Тасксеттингс. Алловхардтерминате, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача может быть завершена планировщик задачной службой с помощью Терминатепроцесс.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- планировщик задач свойства Алловхардтерминате
- Планировщик задач свойства Алловхардтерминате, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Алловхардтерминате
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802962"
---
# <a name="tasksettingsallowhardterminate-property"></a>Тасксеттингс. Алловхардтерминате, свойство

Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача может быть завершена планировщик задачной службой с помощью [**терминатепроцесс**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Служба попытается закрыть выполняющуюся задачу, отправив уведомление [**о \_ закрытии WM**](../winmsg/wm-close.md) . Если задача не отвечает, задача будет прервана, только если для этого свойства задано значение true.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a>Значение свойства

Если значение — true, задача может быть прервана с помощью [**терминатепроцесс**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Если задано значение false, задача не может быть завершена с помощью **терминатепроцесс**.

## <a name="remarks"></a>Комментарии

При чтении или записи XML для задачи этот параметр указывается в элементе [алловхардтерминате](taskschedulerschema-allowhardterminate-settingstype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

