---
title: Сложный тип Системпропертиестипе
description: Определяет сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Журнал событий сложных типов Системпропертиестипе
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803191"
---
# <a name="systempropertiestype-complex-type"></a>Сложный тип Системпропертиестипе

Определяет сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ProcessID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ThreadID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ProcessorID"
                    type="unsignedByte"
                    use="optional"
                 />
                <xs:attribute name="SessionID"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="KernelTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="UserTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="ProcessorTime"
                    type="unsignedInt"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
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



| Элемент                                                                         | Тип                                                        | Описание                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Канал**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | Канал, в который было записано событие.<br/>                                                                                                                                                                                                                                                                                        |
| [**Компьютер**](eventschema-computer-systempropertiestype-element.md)           | строка                                                      | имя компьютера, на котором произошло событие.<br/>                                                                                                                                                                                                                                                                             |
| [**Связей**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Идентификаторы действий, которые потребители могут использовать для группирования связанных событий.<br/>                                                                                                                                                                                                                                                 |
| [**EventID**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | Идентификатор, используемый поставщиком для идентификации события.<br/>                                                                                                                                                                                                                                                                      |
| [**евентрекордид**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | Номер записи, назначенный событию при регистрации.<br/>                                                                                                                                                                                                                                                                       |
| [**Выполнение**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Содержит сведения о процессе и потоке, которые зарегистрировали событие.<br/>                                                                                                                                                                                                                                                          |
| [**Keywords**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Битовая маска ключевых слов, определенных в событии. Ключевые слова используются для классификации типов событий (например, событий, связанных с чтением данных).<br/>                                                                                                                                                                                 |
| [**Уровню**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | Уровень серьезности, определенный в событии.<br/>                                                                                                                                                                                                                                                                                          |
| [**Код операции**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | Код операции, определенный в событии. Задача и код операции — это типЦиалли, используемые для определения расположения в приложении, из которого было зарегистрировано событие.<br/>                                                                                                                                                                                  |
| [**Поставщик**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Определяет поставщика, который зарегистрировал событие. Атрибуты **Name** и **GUID** включаются, если поставщик использовал манифест инструментирования для определения его событий. в противном случае атрибут **евентсаурценаме** включается, если устаревший поставщик событий (с помощью API [ведения журнала событий](/windows/desktop/EventLog/event-logging) ) зарегистрировал событие.<br/> |
| [**Безопасность**](eventschema-security-systempropertiestype-element.md)           |                                                             | Указывает пользователя, который записал в журнал событие.<br/>                                                                                                                                                                                                                                                                                        |
| [**Задача**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | Задача, определенная в событии. Задача и код операции обычно используются для определения расположения в приложении, из которого было зарегистрировано событие.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | Метка времени, определяющая время записи события в журнал. Метка времени будет содержать либо атрибут **SYSTEMTIME** , либо атрибут **равтиме** .<br/>                                                                                                                                                                           |
| [**Версия**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | Номер версии определения события.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Атрибуты



| Имя              | Тип                                                | Описание                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Идентификатор действия        | [**гуидтипе**](eventschema-guidtype-simpletype.md) | Глобальный уникальный идентификатор, определяющий текущее действие. События, опубликованные с помощью этого идентификатора, являются частью одного действия.<br/>                                                                                                                                         |
| евентсаурценаме   | строка                                              | Имя источника события, опубликовавшего событие (если источником события является устаревший API [протоколирования событий](/windows/desktop/EventLog/event-logging) ).<br/>                                                                                                                                                      |
| Guid              | [**гуидтипе**](eventschema-guidtype-simpletype.md) | Глобальный уникальный идентификатор, который однозначно идентифицирует поставщик.<br/>                                                                                                                                                                                                                        |
| кернелтиме        | unsignedInt                                         | Затраченное время выполнения инструкций режима ядра в единицах времени ЦП. Если используется частный сеанс ETW, используйте значение в элементе Процессортиме. Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).<br/>                                               |
| Имя              | anyURI                                              | Имя поставщика.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Указывает процесс, создавший событие.<br/>                                                                                                                                                                                                                                             |
| процессорид       | unsignedByte                                        | Идентификационный номер процессора, который обработал событие. Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).<br/>                                                                                                                                             |
| процессортиме     | unsignedInt                                         | Для частных сеансов ETW — затраченное время выполнения инструкций пользовательского режима в тактах ЦП. Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).<br/>                                                                                                                    |
| Квалификаторы        | **unsignedShort**                                   | Устаревший поставщик использует 32-разрядное число для обнаружения своих событий. Если событие регистрируется устаревшим поставщиком, значение элемента **EventID** содержит 16 младших разрядов идентификатора события, а атрибут **квалификатора** содержит 16 битов идентификатора события с высоким порядковым значением.<br/> |
| равтиме           | unsignedLong                                        | Значение необработанной метки времени; Формат метки времени зависит от источника времени, используемого для накопления трассировки. Необработанная отметка времени обеспечивает большую точность, чем системное время. Выходные данные отображаемого события будут содержать только необработанное время, если вы используете TraceRpt.exe с параметром-RTS.<br/>                 |
| RelatedActivityID | [**гуидтипе**](eventschema-guidtype-simpletype.md) | Глобальный уникальный идентификатор, определяющий действие, в которое был передан элемент управления. Затем связанные события будут иметь этот идентификатор в качестве идентификатора ActivityID.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | Идентификационный номер сеанса сервера терминалов, в котором произошло событие. Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | Системное время, когда событие было зарегистрировано.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Указывает поток, создавший событие.<br/>                                                                                                                                                                                                                                              |
| UserID            | строка                                              | Идентификатор безопасности (SID) пользователя в строковой форме.<br/>                                                                                                                                                                                                                                    |
| усертиме          | unsignedInt                                         | Затраченное время выполнения инструкций пользовательского режима в единицах времени ЦП. Если используется частный сеанс ETW, используйте значение в элементе Процессортиме. Доступно только для событий, регистрируемых в файле журнала трассировки событий (ETL-файле).<br/>                                                 |



## <a name="remarks"></a>Комментарии

По умолчанию событие содержит полное доменное имя (FQDN) компьютера. Чтобы использовать NETBIOS-имя, а не полное доменное имя, необходимо создать параметр реестра DWORD с именем Компатфлагс в следующем разделе реестра и присвоить параметру Компатфлагс значение 0x2.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

