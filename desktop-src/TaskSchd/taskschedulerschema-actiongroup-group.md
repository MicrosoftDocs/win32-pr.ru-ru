---
title: Группа actionGroup
description: Определяет группу действий, которые может выполнять задача.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- планировщик задач группы actionGroup
- actionGroup планировщик задач
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcfd37187373e8bebdcc6b2af22323fd5475a6893791158b83b16c278752e420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357185"
---
# <a name="actiongroup-group"></a>Группа actionGroup

Определяет группу действий, которые может выполнять задача.

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                    | Тип                                                                       | Описание                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**комхандлер**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**комхандлертипе**](taskschedulerschema-comhandlertype-complextype.md)   | Представляет действие, которое вызывает обработчик.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**ексектипе**](taskschedulerschema-exectype-complextype.md)               | Представляет действие, выполняющее операцию командной строки.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md)     | Представляет действие, которое отправляет сообщение электронной почты.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**шовмессажетипе**](taskschedulerschema-showmessagetype-complextype.md) | Представляет действие, показывающее окно сообщения.<br/>               |



## <a name="remarks"></a>Remarks

При чтении или записи XML элементы, определенные этой группой, являются дочерними элементами элемента [**Actions**](taskschedulerschema-actions-tasktype-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





