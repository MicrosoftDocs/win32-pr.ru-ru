---
title: Principal (taskType), элемент
description: Указывает контексты безопасности, которые могут использоваться для выполнения задачи.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- планировщик задач элементов Principal
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988293"
---
# <a name="principals-tasktype-element"></a>Principal (taskType), элемент

Указывает контексты безопасности, которые могут использоваться для выполнения задачи.

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

Элемент **Principals** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                          | Унаследован от                                                 | Описание                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Задача**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Определяет задачу, выполняемую службой планировщик задач.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                  | Тип                                                                   | Описание                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Основного**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="remarks"></a>Комментарии

Для задачи можно указать до 32 участников.

Для разработки сценариев участники задачи указываются с помощью свойства [**таскдефинитион. Principal**](taskdefinition-principal.md) .

Для разработки на C++ субъекты задачи указываются с помощью [**Свойства Principal объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).

## <a name="examples"></a>Примеры

Следующий XML-код определяет двух участников: идентификатор пользователя и участника идентификатора группы для задачи.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





