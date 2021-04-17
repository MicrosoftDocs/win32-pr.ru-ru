---
title: Сложный тип TaskType
description: Определяет компонент или подкомпонент приложения. | Сложный тип TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- Журнал событий сложных типов TaskType
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694067"
---
# <a name="tasktype-complex-type"></a>Сложный тип TaskType

Определяет компонент или подкомпонент приложения.

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                         | Тип                                                                     | Описание                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**коды операций**](eventmanifestschema-opcodes-tasktype-element.md) | [**опкоделисттипе**](eventmanifestschema-opcodelisttype-complextype.md) | Определяет список кодов операций, относящихся к задачам. Нельзя использовать значения кодов операций, определенные в Winmeta.xml, для кодов операций, относящихся к задачам.<br/> |



## <a name="attributes"></a>Атрибуты



| Имя      | Тип                                                              | Описание                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| евентгуид | [**гуидтипе**](eventmanifestschema-guidtype-simpletype.md)       | Глобальный уникальный идентификатор в формате реестра, определяющий задачу. Этот атрибут является обязательным, если для создания класса MOF для поддержки прежних версий используется аргумент компилятора сообщений-MOF.<br/>                                                                                                   |
| message   | [**стртаблереф**](eventmanifestschema-strtableref-simpletype.md) | Локализованное отображаемое имя для задачи. Строка сообщения ссылается на локализованную строку в разделе " [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) " манифеста. <br/>                                                                                                   |
| name      | **QName**                                                         | Имя данной задачи.<br/>                                                                                                                                                                                                                                                                                 |
| символ    | [**ксимболтипе**](eventmanifestschema-csymboltype-simpletype.md) | Символ, используемый для ссылки на задачу в приложении. [**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для задачи в файле заголовка, создаваемом компилятором. Если не указать символ, компилятор создаст его.<br/> |
| значение     | [**UInt16Type**](eventmanifestschema-hexint16type-simpletype.md) | Числовое значение, однозначно идентифицирующее эту задачу в списке задач, определяемых поставщиком. Значение должно находиться в диапазоне от 1 до 239.<br/>                                                                                                                                             |



## <a name="examples"></a>Примеры

В следующем примере показано, как указать задачу.


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





