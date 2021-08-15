---
title: Нетворксеттингс (Сеттингстипе), элемент
description: Содержит параметры, используемые службой планировщик задач для получения сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента Рунонлифнетворкаваилабле задано значение true.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- планировщик задач элемента Нетворксеттингс
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b81e1ff2a9f03646d124f5fd2d3aae27f18069f4b32631f9f8d9e66a193ac3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758484"
---
# <a name="networksettings-settingstype-element"></a>Нетворксеттингс (Сеттингстипе), элемент

Содержит параметры, используемые службой планировщик задач для получения сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

Элемент **нетворксеттингс** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                      | Унаследован от                                                         | Описание                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Параметры (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) | Задает параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство нетворксеттингс объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings).

Сведения о разработке сценариев см. в разделе [**тасксеттингс. нетворксеттингс**](tasksettings-networksettings.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





