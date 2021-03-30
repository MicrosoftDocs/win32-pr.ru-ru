---
title: Execution (Системпропертиестипе), элемент
description: Содержит сведения о процессе и потоке, которые зарегистрировали событие.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Журнал событий элемента выполнения
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801420"
---
# <a name="execution-systempropertiestype-element"></a>Execution (Системпропертиестипе), элемент

Содержит сведения о процессе и потоке, которые зарегистрировали событие.

``` syntax
<xs:element name="Execution">
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
```

Элемент **Execution** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Атрибуты



| Имя          | Тип         | Описание                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| кернелтиме    | unsignedInt  | Затраченное время выполнения инструкций режима ядра в единицах времени ЦП.<br/>                        |
| ProcessID     | unsignedInt  | Указывает процесс, создавший событие.<br/>                                               |
| процессорид   | unsignedByte | Идентификационный номер процессора, который обработал событие.<br/>                          |
| процессортиме | unsignedInt  | Для частных сеансов ETW — затраченное время выполнения инструкций пользовательского режима в тактах ЦП.<br/> |
| SessionID     | unsignedInt  | Идентификационный номер сеанса сервера терминалов, в котором произошло событие.<br/>         |
| ThreadID      | unsignedInt  | Указывает поток, создавший событие.<br/>                                                |
| усертиме      | unsignedInt  | Затраченное время выполнения инструкций пользовательского режима в единицах времени ЦП.<br/>                          |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**системпропертиестипе**](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**Система (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





