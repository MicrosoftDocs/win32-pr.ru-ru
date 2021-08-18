---
title: Trigger.Id, свойство
description: Для создания скриптов Возвращает или задает идентификатор триггера.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Свойство ID планировщик задач
- Свойство ID планировщик задач, объект Trigger
- Планировщик задач объекта триггера, свойство ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c9ff851eab7b5e9cfb124bf03c83986d24b391d5ea109865ff2d59e2e33536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002162"
---
# <a name="triggerid-property"></a>Trigger.Id, свойство

Для создания скриптов Возвращает или задает идентификатор триггера.

## <a name="syntax"></a>Синтаксис


```VB
Trigger.Id As String
```



## <a name="property-value"></a>Значение свойства

Идентификатор триггера. Этот идентификатор используется планировщик задач в целях ведения журнала.

## <a name="remarks"></a>Remarks

При чтении или записи XML-кода для задачи Идентификатор триггера задается в атрибуте ID отдельных элементов Trigger (например, атрибут ID элемента [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md) ) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





