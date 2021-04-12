---
title: Principal.Id, свойство
description: Для создания скриптов Возвращает или задает идентификатор участника.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Свойство ID планировщик задач
- Свойство ID планировщик задач, объект Principal
- Объект Principal планировщик задач, свойство ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415884"
---
# <a name="principalid-property"></a>Principal.Id, свойство

Для создания скриптов Возвращает или задает идентификатор участника.

## <a name="syntax"></a>Синтаксис


```VB
Principal.Id As String
```



## <a name="property-value"></a>Значение свойства

Идентификатор участника.

## <a name="remarks"></a>Комментарии

Этот идентификатор также используется при указании свойства [**ActionCollection. Context**](actioncollection-context.md) .

При чтении или записи XML для задачи идентификатор участника указывается в атрибуте ID элемента [**Principal**](taskschedulerschema-principal-principaltype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ActionCollection. Context**](actioncollection-context.md)
</dt> <dt>

[**Основного**](principal.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





