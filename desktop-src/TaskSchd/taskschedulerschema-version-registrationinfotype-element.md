---
title: Version (Регистратионинфотипе), элемент
description: Указывает номер версии задачи.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- планировщик задач элемента Version
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63d69b501b12890939f3bd0b146c959278eeaa0d5eb596851a488cef87f0770a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610429"
---
# <a name="version-registrationinfotype-element"></a>Version (Регистратионинфотипе), элемент

Указывает номер версии задачи.

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

Элемент **Version** определяется сложным типом [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                           | Унаследован от                                                                         | Описание                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) | Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.<br/> |



## <a name="remarks"></a>Remarks

Для разработки скриптов версия задачи указывается с помощью свойства [**регистратионинфо. Version**](registrationinfo-version.md) .

Для разработки на C++ версия задачи указывается с помощью свойства [**ирегистратионинфо:: Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .

## <a name="examples"></a>Примеры

Следующий код XML определяет версию задачи.


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a>Требования



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

 

 





