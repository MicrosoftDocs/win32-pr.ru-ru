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
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492684"
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
| [**Канал**](eventschema-task-renderingtype-element.md)           | строка | Строка отображаемого сообщения канала, указанного в событии.<br/> |
| [**Ключевое слово**](eventschema-keyword-keywords-element.md)             | строка | Строка отображаемого сообщения ключевого слова, указанного в событии.<br/>   |
| [**Keywords**](eventschema-keywords-renderingtype-element.md)      |        | Список отображаемых ключевых слов.<br/>                                       |
| [**Уровню**](eventschema-level-renderingtype-element.md)            | строка | Строка отображаемого сообщения уровня, указанного в событии.<br/>   |
| [**Сообщение**](eventschema-message-renderingtype-element.md)        | строка | Строка отображаемого сообщения события.<br/>                          |
| [**Код операции**](eventschema-opcode-renderingtype-element.md)          | строка | Строка отображаемого сообщения кода операции, указанного в событии.<br/>  |
| [**Поставщик**](eventschema-publisher-renderinginfotype-element.md) | строка | Строка отображаемого сообщения для поставщика.<br/>                      |
| [**Задача**](eventschema-task-renderingtype-element.md)              | строка | Строка отображаемого сообщения задачи, указанной в событии.<br/>    |



## <a name="attributes"></a>Атрибуты



| Имя    | Тип     | Описание                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| culture | Язык | Имя языка (например, EN-US), определяющее языковой стандарт, используемый для отображения строк сообщений.<br/> |



## <a name="remarks"></a>Комментарии

Этот раздел будет содержать только события, собранные с помощью службы [сборщика событий Windows](/windows/desktop/WEC/windows-event-collector) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

