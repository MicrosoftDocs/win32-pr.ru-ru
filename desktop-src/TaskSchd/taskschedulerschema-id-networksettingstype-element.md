---
title: Элемент ID (Нетворксеттингстипе)
description: Содержит значение идентификатора GUID, определяющее сетевой профиль.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Элемент ID планировщик задач
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06196710b9db9d39d45a24b78bccabf479ef210a97f3cea1fd19286b76f2fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125844"
---
# <a name="id-networksettingstype-element"></a>Элемент ID (Нетворксеттингстипе)

Содержит значение идентификатора GUID, определяющее сетевой профиль.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

Элемент **ID** определяется сложным типом [**нетворксеттингстипе**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                            | Унаследован от                                                                       | Описание                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Нетворксеттингс (Сеттингстипе)**](taskschedulerschema-networksettings-settingstype-element.md) | [**нетворксеттингстипе**](taskschedulerschema-networksettingstype-complextype.md) | Содержит параметры, используемые службой планировщик задач для получения сетевого профиля. Служба планировщик задач проверяет доступность этой сети, если для элемента [**рунонлифнетворкаваилабле**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) задано значение **true**.<br/> |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе [**свойство ID объекта инетворксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Сведения о разработке сценариев см. в разделе [**NetworkSettings.ID**](networksettings-id.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





