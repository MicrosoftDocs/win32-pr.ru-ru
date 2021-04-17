---
title: Стопатдуратионенд (Репетитионтипе), элемент
description: Указывает, что выполняющиеся экземпляры задачи останавливаются в конце шаблона повторения.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- планировщик задач элемента Стопатдуратионенд
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672899"
---
# <a name="stopatdurationend-repetitiontype-element"></a>Стопатдуратионенд (Репетитионтипе), элемент

Указывает, что выполняющийся экземпляр задачи останавливается в конце срока действия шаблона повторения. Это применимо только в том случае, если заданы повторения.

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

Элемент **стопатдуратионенд** определяется сложным типом [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент

| Элемент | Унаследован от | Описание |
|-|-|-|
| [**Повторение**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**репетитионтипе**](taskschedulerschema-repetitiontype-complextype.md) | Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.<br/> |

## <a name="remarks"></a>Комментарии

Для разработки сценариев этот параметр указывается с помощью свойства [**репетитионпаттерн. стопатдуратионенд**](repetitionpattern-stopatdurationend.md) .

Для разработки на C++ этот параметр указывается с помощью свойства [**ирепетитионпаттерн:: стопатдуратионенд**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |

## <a name="see-also"></a>См. также раздел

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)

[Планировщик заданий](task-scheduler-start-page.md)
