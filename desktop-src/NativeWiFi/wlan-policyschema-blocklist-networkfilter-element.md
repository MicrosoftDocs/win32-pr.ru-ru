---
description: Указывает список беспроводных ЛОКАЛЬНЫХ сетей, к которым компьютер не должен подключаться.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Списка блокировки (Нетворкфилтер), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c5bd795ee9f5fc21dc205c24306820b4dec7f074638aa0e4f11ba3acde68cd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684424"
---
# <a name="blocklist-networkfilter-element"></a>Списка блокировки (Нетворкфилтер), элемент

Элемент списка блокировки (Нетворкфилтер) указывает список беспроводных ЛОКАЛЬНЫХ сетей, к которым компьютер не должен подключаться.

``` syntax
<xs:element name="blockList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент **списка блокировки** определяется элементом [**нетворкфилтер**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                        | Тип                                                                     | Описание                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [**сети**](wlan-policyschema-network-blocklist-element.md) | [**нетворкитемтипе**](wlan-policyschema-networkitemtype-complextype.md) | Заблокированная сеть. <br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**нетворкфилтер**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Нетворкфилтер (Вланполици)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




