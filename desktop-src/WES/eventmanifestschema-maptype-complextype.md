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
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801444"
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



## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





