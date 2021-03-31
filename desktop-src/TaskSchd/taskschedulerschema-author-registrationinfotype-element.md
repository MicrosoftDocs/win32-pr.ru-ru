---
title: Author (Регистратионинфотипе), элемент
description: Указывает автора задачи.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Элемент Author планировщик задач
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988873"
---
# <a name="author-registrationinfotype-element"></a>Author (Регистратионинфотипе), элемент

Указывает автора задачи.

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

Элемент **Author** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                           | Унаследован от                                                                         | Описание                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) | Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки сценариев автор задачи указывается с помощью свойства [**регистратионинфо. Author**](registrationinfo-author.md) .

Для разработки на C++ автор задачи указывается с помощью свойства [**ирегистратионинфо:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет автора задачи.


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
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

 

 





