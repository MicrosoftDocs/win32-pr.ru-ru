---
title: Сложный тип Битмапвалуетипе
description: Определяет сопоставление между битовым значением и строковым значением. | Сложный тип Битмапвалуетипе
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- Журнал событий сложных типов Битмапвалуетипе
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000158"
---
# <a name="bitmapvaluetype-complex-type"></a>Сложный тип Битмапвалуетипе

Определяет сопоставление между битовым значением и строковым значением.

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя    | Тип                                                              | Описание                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**стртаблереф**](eventmanifestschema-strtableref-simpletype.md) | Локализованное строковое значение, с которым сопоставляется битовое значение. Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста. <br/>                                                                                  |
| символ  | [**ксимболтипе**](eventmanifestschema-csymboltype-simpletype.md) | Символ, используемый для ссылки на карту в приложении. [**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ для создания константы для Map в файле заголовка, создаваемого компилятором. Если не указать символ, компилятор создаст его.<br/> |
| значение   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | Битовое значение, сопоставляемое со строковым значением. Необходимо указать шестнадцатеричное число, для которого задан один бит.<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>Комментарии

Сопоставляет шестнадцатеричное значение (перед числом должно стоять 0x) с одним битом, равным имени.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





