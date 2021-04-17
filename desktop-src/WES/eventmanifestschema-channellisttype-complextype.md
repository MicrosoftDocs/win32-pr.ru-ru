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
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694070"
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



## <a name="remarks"></a>Комментарии

Можно указать до восьми каналов (любое сочетание импортированных каналов или каналов).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





