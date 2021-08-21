---
title: Сложный тип Чаннеллисттипе
description: Определяет список каналов, к которым поставщики могут регистрировать события. | Сложный тип Чаннеллисттипе
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Журнал событий сложных типов Чаннеллисттипе
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8602594bdbdf6d39532213b0be660b5b3cfb6a90cd8281d9555ed2ff3a9d401
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121054"
---
# <a name="channellisttype-complex-type"></a>Сложный тип Чаннеллисттипе

Определяет список каналов, к которым поставщики могут регистрировать события.

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                            | Тип                                                                           | Описание                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**маркетинг**](eventmanifestschema-channel-channellisttype-element.md)             | [**чаннелтипе**](eventmanifestschema-channeltype-complextype.md)             | Определяет канал, на который могут регистрироваться события.<br/>                                                                  |
| [**импортчаннел**](eventmanifestschema-importchannel-channellisttype-element.md) | [**импортчаннелтипе**](eventmanifestschema-importchanneltype-complextype.md) | Определяет канал, который был определен другим поставщиком или манифестом, содержащим раздел метаданных.<br/> |



## <a name="remarks"></a>Remarks

Можно указать до восьми каналов (любое сочетание импортированных каналов или каналов).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





