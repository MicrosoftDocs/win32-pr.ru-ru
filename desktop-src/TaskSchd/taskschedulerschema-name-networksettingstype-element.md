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
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534457"
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



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе [**свойство Name объекта инетворксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Сведения о разработке сценариев см. в разделе [**NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





