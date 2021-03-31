---
title: Сложный тип Нетворксеттингстипе
description: Определяет элементы, которые предоставляют параметры, которые служба планировщик задач использует для получения сетевого профиля.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- планировщик задач сложного типа Нетворксеттингстипе
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988869"
---
# <a name="networksettingstype-complex-type"></a>Сложный тип Нетворксеттингстипе

Определяет элементы, которые предоставляют параметры, которые служба планировщик задач использует для получения сетевого профиля.

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                              | Тип                                                        | Описание                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Удостоверения**](taskschedulerschema-id-networksettingstype-element.md)     | [**гуидтипе**](taskschedulerschema-guidtype-simpletype.md) | Указывает значение идентификатора GUID, определяющее сетевой профиль. <br/>                       |
| [**Имя**](taskschedulerschema-name-networksettingstype-element.md) | нонемптистринг                                              | Указывает имя сетевого профиля. Имя используется в целях показа. <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





