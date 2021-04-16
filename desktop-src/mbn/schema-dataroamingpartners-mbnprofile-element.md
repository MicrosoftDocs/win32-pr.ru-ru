---
description: Указывает список предпочтительных поставщиков сети во время перемещения.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Датароамингпартнерс (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656539"
---
# <a name="dataroamingpartners-mbnprofile-element"></a>Датароамингпартнерс (Мбнпрофиле), элемент

Элемент **датароамингпартнерс (мбнпрофиле)** указывает список предпочтительных поставщиков сети во время перемещения.

Служба мобильной широкополосной связи использует этот элемент, чтобы выбрать предпочитаемую сеть в роуминге.

Элемент имеет следующий дочерний элемент, который должен быть определен по крайней мере один раз, но может быть определен несколько раз.

-   [**Поставщик**](schema-provider-dataroamingpartners-element.md)

Этот элемент может иметь максимум одно вхождение.

Этот элемент является необязательным.

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Элемент **датароамингпартнерс** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                         | Тип                                                    | Описание                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [**Поставщик**](schema-provider-dataroamingpartners-element.md) | [**providerType**](schema-providertype-complextype.md) | Имя и идентификатор поставщика сотовой сети.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




