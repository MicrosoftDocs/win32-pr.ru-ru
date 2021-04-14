---
title: Сложный тип EventType
description: Определяет корневой узел схемы событий.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- Журнал событий сложного типа EventType
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414881"
---
# <a name="eventtype-complex-type"></a>Сложный тип EventType

Определяет корневой узел схемы событий.

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                          | Тип                                                                               | Описание                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**бинаревентдата**](eventschema-binaryeventdata-eventtype-element.md)         | hexBinary                                                                          | Содержит данные события как двоичный BLOB-объект. Данные события подготавливаются к просмотру как двоичный BLOB-объект, если функция отрисовки не может найти метаданные, используемые для декодирования события.<br/>                                                                                                                                                            |
| [**дебугдата**](eventschema-debugdata-eventtype-element.md)                     | [**дебугдататипе**](eventschema-debugdatatype-complextype.md)                     | Содержит данные, которые могут быть зарегистрированы для событий препроцессора трассировки программного обеспечения Windows (WPP).<br/>                                                                                                                                                                                                                                    |
| [**EventData**](eventschema-eventdata-eventtype-element.md)                     | [**евентдататипе**](eventschema-eventdatatype-complextype.md)                     | Содержит данные о событии. Порядок элементов данных в шаблоне определяет макет данных события.<br/>                                                                                                                                                                                                                 |
| [**процессинжеррордата**](eventschema-processingerrordata-eventtype-element.md) | [**процессинжеррордататипе**](eventschema-processingerrordatatype-complextype.md) | Содержит подробные сведения об ошибке, возникшей при попытке подготовки к просмотру события. Это может произойти, если данные события не соответствуют определению данных события в манифесте. Данные события включаются в двоичный BLOB-объект.<br/>                                                                                                         |
| [**рендерингинфо**](eventschema-renderinginfo-eventtype-element.md)             | [**рендерингинфотипе**](eventschema-renderingtype-complextype.md)                 | Содержит строки отображаемых сообщений для события (включая строку сообщения события и строки сообщения для любого свойства события, например уровень, задача и код операции). Этот раздел будет содержать только события, собранные с помощью службы [сборщика событий Windows](/windows/desktop/WEC/windows-event-collector) .<br/> |
| [**Система**](eventschema-system-eventtype-element.md)                           | [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md)       | Содержит сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**усердататипе**](eventschema-userdatatype-complextype.md)                       | Содержит данные о событии. Раздел данных пользователя шаблона определяет макет данных события.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Комментарии

Как правило, этот раздел будет содержать раздел **EVENTDATA** или **UserData** . Раздел **EVENTDATA** используется, если шаблон не содержит раздел **UserData** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

