---
title: Элемент Source (Регистратионинфотипе)
description: Указывает, откуда поступила задача. Например, из компонента, службы, приложения или пользователя.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- планировщик задач исходного элемента
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414969"
---
# <a name="source-registrationinfotype-element"></a>Элемент Source (Регистратионинфотипе)

Указывает, откуда поступила задача. Например, из компонента, службы, приложения или пользователя.

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

Элемент **Source** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                           | Унаследован от                                                                         | Описание                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) | Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки сценариев источник задачи указывается с помощью свойства [**регистратионинфо. Source**](registrationinfo-source.md) .

Для разработки на C++ источник задачи указывается с помощью свойства [**ирегистратионинфо:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .

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

 

 





