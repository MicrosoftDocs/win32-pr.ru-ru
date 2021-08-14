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
ms.openlocfilehash: d9969e4e3827d926d8c295d4e1a3ce7b77550804eb4995a267a920a16871837f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758474"
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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





