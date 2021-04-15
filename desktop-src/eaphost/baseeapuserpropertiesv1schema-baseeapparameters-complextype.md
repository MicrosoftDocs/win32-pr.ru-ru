---
title: Сложный тип Басиаппараметерс — свойства пользователя
description: Определяет элемент, в котором был указан устаревший метод и учетные данные, зависящие от метода.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105714057"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Сложный тип Басиаппараметерс — свойства пользователя

Сложный тип **басиаппараметерс** определяет элемент, в котором был указан устаревший метод, и учетные данные, зависящие от метода.

Метод может определять составные элементы внутри **басиаппараметерс**; метод также выполняет проверку схемы для элементов в **басиаппараметерс**.

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



| Элемент                                                                      | Тип    | Описание                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [**Тип**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | Целое число | Определяет элемент заполнителя для выбранного типа метода и учетные данные для конкретного метода. <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





