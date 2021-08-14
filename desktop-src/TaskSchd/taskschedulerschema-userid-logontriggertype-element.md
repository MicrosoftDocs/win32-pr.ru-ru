---
title: UserId (Логонтригжертипе), элемент
description: Идентификатор пользователя. Задача запускается, когда пользователь входит в систему на компьютере.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- Элемент UserId планировщик задач
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33a1e0f82a3005bfec8e689d088a8d8e28ebbf0a949e4288338d27e68c3a0314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355570"
---
# <a name="userid-logontriggertype-element"></a>UserId (Логонтригжертипе), элемент

Идентификатор пользователя. Задача запускается, когда пользователь входит в систему на компьютере.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

Элемент **UserID** определяется сложным типом [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                       | Унаследован от                                                                 | Описание                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md) | Указывает триггер, который запускает задачу при входе пользователя в систему.<br/> |



## <a name="remarks"></a>Remarks

Для разработки сценариев идентификатор пользователя для триггера LOGON указывается с помощью свойства [**логонтригжер. UserID**](logontrigger-userid.md) .

Для разработки на C++ идентификатор пользователя для триггера LOGON указывается с помощью свойства [**илогонтригжер:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей триггер входа, см. в разделе [пример триггера LOGON (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





