---
title: Сложный тип Рендерингинфотипе
description: Определяет отрисованные сообщения для события.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Журнал событий сложных типов Рендерингинфотипе
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d4a70c8bc97abc3dea7cd04e9ce491b64cb62dcc892fcde318d69dcdc996e2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588467"
---
# <a name="renderinginfotype-complex-type"></a>Сложный тип Рендерингинфотипе

Определяет отрисованные сообщения для события.

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                             | Тип   | Описание                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [**Channel**](eventschema-task-renderingtype-element.md)           | строка | Строка отображаемого сообщения канала, указанного в событии.<br/> |
| [**Ключевое слово**](eventschema-keyword-keywords-element.md)             | строка | Строка отображаемого сообщения ключевого слова, указанного в событии.<br/>   |
| [**Словами**](eventschema-keywords-renderingtype-element.md)      |        | Список отображаемых ключевых слов.<br/>                                       |
| [**Уровню**](eventschema-level-renderingtype-element.md)            | строка | Строка отображаемого сообщения уровня, указанного в событии.<br/>   |
| [**Сообщение**](eventschema-message-renderingtype-element.md)        | строка | Строка отображаемого сообщения события.<br/>                          |
| [**Код операции**](eventschema-opcode-renderingtype-element.md)          | строка | Строка отображаемого сообщения кода операции, указанного в событии.<br/>  |
| [**Поставщик**](eventschema-publisher-renderinginfotype-element.md) | строка | Строка отображаемого сообщения для поставщика.<br/>                      |
| [**Задача**](eventschema-task-renderingtype-element.md)              | строка | Строка отображаемого сообщения задачи, указанной в событии.<br/>    |



## <a name="attributes"></a>Атрибуты



| Имя    | Тип     | Описание                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| culture | Язык | Имя языка (например, EN-US), определяющее языковой стандарт, используемый для отображения строк сообщений.<br/> |



## <a name="remarks"></a>Remarks

этот раздел будет содержать только события, собранные с помощью службы [сборщика событий Windows](/windows/desktop/WEC/windows-event-collector) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

