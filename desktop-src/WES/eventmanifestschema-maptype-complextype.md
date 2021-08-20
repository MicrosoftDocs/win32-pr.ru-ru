---
title: Сложный тип Маптипе
description: Определяет список пар "имя-значение".
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- Журнал событий сложных типов Маптипе
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 162676ab5d017c8fa6d6d280a07d1e4500e77cc79e0eacf25e23d5f20c0b3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120922"
---
# <a name="maptype-complex-type"></a>Сложный тип Маптипе

Определяет список пар "имя-значение".

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                          | Тип                                                                 | Описание                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Массив**](eventmanifestschema-bitmap-maptype-element.md)     | [**битмаптипе**](eventmanifestschema-bitmaptype-complextype.md)     | Определяет список пар "имя-значение", которые сопоставляют битовые значения и строковые значения.<br/>     |
| [**valueMap**](eventmanifestschema-valuemap-maptype-element.md) | [**валуемаптипе**](eventmanifestschema-valuemaptype-complextype.md) | Определяет список пар "имя-значение", которые сопоставляют целочисленные значения и строковые значения.<br/> |



## <a name="remarks"></a>Remarks

Как правило, карты создаются для предоставления перечисленных строковых значений для данных событий.

## <a name="examples"></a>Примеры

В следующем примере показано, как указать карту значений и битовую карту.


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





