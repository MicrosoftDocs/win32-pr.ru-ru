---
title: Сложный тип Басиаппараметерс — свойства соединения
description: Определяет элемент-заполнитель для конкретного типа метода и конфигурации метода.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- Басиаппараметерс сложный тип EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105694370"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Сложный тип Басиаппараметерс — свойства соединения

Сложный тип **басиаппараметерс** определяет элемент-заполнитель для конкретного типа метода и конфигурации метода.

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип    | Описание                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [**Тип**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | Целое число | Здесь можно использовать любой экземпляр схемы.<br/> |



## <a name="remarks"></a>Комментарии

В **басиаппараметерс** метод может определять составные элементы. Метод также выполняет проверку схемы для элементов в **басиаппараметерс**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





