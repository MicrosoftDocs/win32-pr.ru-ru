---
title: Элемент Name (Нетворксеттингстипе)
description: Содержит имя сетевого профиля. Имя используется в целях показа.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Элемент Name планировщик задач
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41b92c7e63a820c2a2a34378b041bec3a49f432b52887a732c3f3bfd360b10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758505"
---
# <a name="name-networksettingstype-element"></a>Элемент Name (Нетворксеттингстипе)

Содержит имя сетевого профиля. Имя используется в целях показа.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

Элемент **Name** определяется сложным типом [**нетворксеттингстипе**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                            | Унаследован от                                                                       | Описание                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Нетворксеттингс (Сеттингстипе)**](taskschedulerschema-networksettings-settingstype-element.md) | [**нетворксеттингстипе**](taskschedulerschema-networksettingstype-complextype.md) | Содержит параметры, используемые службой планировщик задач для получения сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство Name объекта инетворксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Сведения о разработке сценариев см. в разделе [**NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





