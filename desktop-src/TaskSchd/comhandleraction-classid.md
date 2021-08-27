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
ms.openlocfilehash: 72338d4fe15936fcfe8f158098a798c4a3630cbd0587f46dc2f9346405477a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100464"
---
# <a name="comhandleractionclassid-property"></a>Комхандлерактион. ClassId, свойство

Для создания скриптов Возвращает или задает идентификатор класса обработчика.

## <a name="syntax"></a>Синтаксис


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Значение свойства

Идентификатор класса, определяющего запускаемый обработчик.

## <a name="remarks"></a>Remarks

При чтении или записи XML класс обработчика COM указывается в элементе [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> <dt>

[**комхандлерактион**](comhandleraction.md)
</dt> </dl>

 

 





