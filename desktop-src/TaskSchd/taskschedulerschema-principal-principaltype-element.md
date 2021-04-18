---
title: Элемент Principal (ПринЦипалтипе)
description: Указывает учетные данные безопасности для участника.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Основной элемент планировщик задач
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681788"
---
# <a name="principal-principaltype-element"></a>Элемент Principal (ПринЦипалтипе)

Указывает учетные данные безопасности для участника. Эти учетные данные определяют контекст безопасности, в котором выполняется задача.

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

Элемент **Principal** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                               | Унаследован от                                                             | Описание                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Субъекты**](taskschedulerschema-principals-tasktype-element.md) | [**принЦипалстипе**](taskschedulerschema-principalstype-complextype.md) | Указывает субъекты безопасности, связанные с задачей.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                      | Тип                                                          | Описание                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) | **string**                                                    | Указывает имя участника, отображаемого в пользовательском интерфейсе планировщик задач.<br/>                 |
| [**Идентификатор**](taskschedulerschema-groupid-principaltype-element.md)         | **string**                                                    | Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Указывает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.<br/>  |
| [**UserId**](taskschedulerschema-userid-principaltype-element.md)           | **string**                                                    | Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.<br/>              |



## <a name="attributes"></a>Атрибуты



| Имя | Тип | Описание                                        |
|------|------|----------------------------------------------------|
| Идентификатор   | ID   | Идентификатор определения участника.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки сценариев учетные данные безопасности участника указываются с помощью объекта [**Principal**](principal.md) .

Для разработки на C++ учетные данные безопасности для субъекта задаются с помощью интерфейса [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .

Перечисленные выше дочерние элементы определяются сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) . Сведения о последовательности для этих дочерних элементов см. в разделе [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md).

## <a name="examples"></a>Примеры

Следующий XML-код определяет участника с идентификатором пользователя.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



Следующий XML-код определяет участника с идентификатором группы.


```XML
<Principals>
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

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





