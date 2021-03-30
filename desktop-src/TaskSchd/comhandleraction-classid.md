---
title: Комхандлерактион. ClassId, свойство
description: Для создания скриптов Возвращает или задает идентификатор класса обработчика.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Свойство ClassId планировщик задач
- Свойство ClassId планировщик задач, объект Комхандлерактион
- Планировщик задач объекта Комхандлерактион, свойство ClassId
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801799"
---
# <a name="comhandleractionclassid-property"></a>Комхандлерактион. ClassId, свойство

Для создания скриптов Возвращает или задает идентификатор класса обработчика.

## <a name="syntax"></a>Синтаксис


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Значение свойства

Идентификатор класса, определяющего запускаемый обработчик.

## <a name="remarks"></a>Комментарии

При чтении или записи XML класс обработчика COM указывается в элементе [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) схемы планировщик задач.

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
</dt> <dt>

[**комхандлерактион**](comhandleraction.md)
</dt> </dl>

 

 





