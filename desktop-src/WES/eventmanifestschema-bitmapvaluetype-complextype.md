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
ms.openlocfilehash: 6d5f1b254ad4a833c1523f5a139224fc1fed508d4530a056ffdb0f111db5769e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032354"
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
| Значение   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | Битовое значение, сопоставляемое со строковым значением. Необходимо указать шестнадцатеричное число, для которого задан один бит.<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>Remarks

Карты шестнадцатеричное значение (перед числом должно быть указано 0x), а для одного бита задается имя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





