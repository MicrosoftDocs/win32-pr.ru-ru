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
ms.openlocfilehash: 80ae1dc749d1c31ee11809b530fe1b04a59ce3e4e4dc76e84323b7dc078ec44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978294"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





