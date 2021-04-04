---
title: Сложный тип Еапмесодтипе
description: Определяет элементы, которые уникально идентифицируют один тип метода EAP, VendorId, Вендортипе и Аусорид.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- Еапмесодтипе сложный тип EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802531"
---
# <a name="eapmethodtype-complex-type"></a>Сложный тип Еапмесодтипе

Сложный тип **еапмесодтипе** определяет элементы, которые уникально идентифицируют один метод EAP: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md), [**вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md)и [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md).

[**Type**](eapcommonschema-type-eapmethodtype-element.md) и [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md) являются обязательными элементами, тогда как [**вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md) и [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) являются обязательными только в том случае, если элемент **Type** имеет значение 254 (Расширенный метод EAP).

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                | Тип         | Описание                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | Ссылается на автора метода. <br/>                                                                                                                                                                                                                 |
| [**Тип**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | Относится к типу метода EAP. <br/>                                                                                                                                                                                                               |
| [**Поставщика**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Относится к поставщику, который определил метод — если элемент [**Type**](eapcommonschema-type-eapmethodtype-element.md) равен 254 (Расширенный метод EAP). [**ИД поставщика**](eapcommonschema-vendorid-eapmethodtype-element.md) является необязательным. <br/> |
| [**вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | Тип, определяемый поставщиком для метода. [**Вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md) является необязательным. <br/>                                                                                                           |



## <a name="remarks"></a>Комментарии

Элементы [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md) и [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) не обязательно должны быть одинаковыми для конкретного метода.

Элементы [**аусорид**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) и [**вендортипе**](eapcommonschema-vendortype-eapmethodtype-element.md) — это уникальные номера, выдаваемые центром Интернета, которым назначены номера (IANA).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[EAPHost и схема прежних версий](eaphost-schemas.md)
</dt> <dt>

[Схема еапкоммон](eapcommonschema-schema.md)
</dt> </dl>

 

 





