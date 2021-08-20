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
ms.openlocfilehash: b8301371acc7624b4beb9b548191afa641ed267592b246cca7ba71ff170a9bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059782"
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
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) | **строка**                                                    | Указывает имя участника, отображаемого в пользовательском интерфейсе планировщик задач.<br/>                 |
| [**Идентификатор**](taskschedulerschema-groupid-principaltype-element.md)         | **строка**                                                    | Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Указывает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.<br/>  |
| [**UserId**](taskschedulerschema-userid-principaltype-element.md)           | **строка**                                                    | Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.<br/>              |



## <a name="attributes"></a>Атрибуты



| Имя | Тип | Описание                                        |
|------|------|----------------------------------------------------|
| Идентификатор   | ID   | Идентификатор определения участника.<br/> |



## <a name="remarks"></a>Remarks

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





