---
title: Сложный тип Кэйвордтипе
description: Определяет ключевое слово, определяющее категорию событий. | Сложный тип Кэйвордтипе
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- Журнал событий сложных типов Кэйвордтипе
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693996"
---
# <a name="keywordtype-complex-type"></a>Сложный тип Кэйвордтипе

Определяет ключевое слово, определяющее категорию событий. Ключевое слово — это тег, который присоединяется к событию для группирования событий в зависимости от их использования.

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Атрибуты



| Имя    | Тип                                                              | Описание                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| маска    | [**HexInt64Type**](eventmanifestschema-hex64type-simpletype.md)  | Битовая маска, которая должна иметь только один бит. Бит представляет категорию событий (например, чтение событий или запись событий). Можно указать битовые значения в диапазоне от 0x0000000000000001 до 0x0000800000000000 (от 0 до 47).<br/>                                                         |
| message | [**стртаблереф**](eventmanifestschema-strtableref-simpletype.md) | Локализованное отображаемое имя для ключевого слова. Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста.<br/>                                                                                                       |
| name    | **QName**                                                         | Имя ключевого слова. Имя должно быть уникальным в списке ключевых слов, определяемых поставщиком.<br/>                                                                                                                                                                                                     |
| символ  | [**ксимболтипе**](eventmanifestschema-csymboltype-simpletype.md) | Символ, используемый для ссылки на ключевое слово в приложении. [**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для ключевого слова в файле заголовка, создаваемом компилятором. Если не указать символ, компилятор создаст его.<br/> |



## <a name="remarks"></a>Комментарии

Файл Winmeta.xml, включенный в Windows SDK, содержит список ключевых слов. Эти ключевые слова зарезервированы и не должны использоваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





