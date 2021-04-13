---
title: Регистратионинфо (taskType), элемент
description: Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- планировщик задач сведения о регистрации, XML-элемент
- планировщик задач элемента Регистратионинфо
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491676"
---
# <a name="registrationinfo-tasktype-element"></a>Регистратионинфо (taskType), элемент

Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

Элемент **регистратионинфо** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                          | Унаследован от                                                 | Описание                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Задача**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Определяет задачу, выполняемую службой планировщик задач.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                                  | Тип     | Описание                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [**Автор (Регистратионинфотипе)**](taskschedulerschema-author-registrationinfotype-element.md)                         | строка   | Указывает автора задачи.<br/>                                                                              |
| [**Дата (Регистратионинфотипе)**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Указывает дату и время регистрации задачи.<br/>                                                       |
| [**Описание (Регистратионинфотипе)**](taskschedulerschema-description-registrationinfotype-element.md)               | строка   | Указание описания задачи.<br/>                                                                         |
| [**Документация (Регистратионинфотипе)**](taskschedulerschema-documentation-registrationinfotype-element.md)           | строка   | Указывает любую дополнительную документацию для задачи.<br/>                                                           |
| [**SecurityDescriptor (Регистратионинфотипе)**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | строка   | Указывает дескриптор безопасности задачи.<br/>                                                                 |
| [**Источник (Регистратионинфотипе)**](taskschedulerschema-source-registrationinfotype-element.md)                         | строка   | Указывает, откуда поступила задача. Например, из компонента, службы, приложения или пользователя.<br/> |
| [**URI (Регистратионинфотипе)**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Указывает универсальный код ресурса (URI) задачи.<br/>                                                                                 |
| [**Версия (Регистратионинфотипе)**](taskschedulerschema-version-registrationinfotype-element.md)                       | строка   | Указывает номер версии задачи.<br/>                                                                      |



## <a name="remarks"></a>Комментарии

Для разработки сценариев сведения о регистрации задачи указываются с помощью свойства [**таскдефинитион. регистратионинфо**](taskdefinition-registrationinfo.md) .

Для разработки на C++ сведения о регистрации задачи указываются с помощью [**Свойства регистратионинфо объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).

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

 

 





