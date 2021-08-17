---
title: Нетворкпрофиленаме (Сеттингстипе), элемент
description: Содержит имя сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента Рунонлифнетворкаваилабле задано значение true. Имя используется в целях показа.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- планировщик задач элемента Нетворкпрофиленаме
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 464c8b8f23dfeed6ea7c3412c3eeec07f20e5a8a7fcea662b4a16dfac7cb3fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758494"
---
# <a name="networkprofilename-settingstype-element"></a>Нетворкпрофиленаме (Сеттингстипе), элемент

Содержит имя сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**. Имя используется в целях показа.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

Элемент **нетворкпрофиленаме** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                      | Унаследован от                                                         | Описание                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Параметры (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Задает параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





