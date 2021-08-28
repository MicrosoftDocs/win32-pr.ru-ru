---
title: Инструментатионманифест, элемент
description: Корневой узел манифеста.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- Журнал событий элемента Инструментатионманифест
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dac9ab8c8aa2a6caeacf43023c4995be69f293affd5dd5a904d7fb96d710266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343732"
---
# <a name="instrumentationmanifest-element"></a>Инструментатионманифест, элемент

Корневой узел манифеста.

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                        | Тип                                                                               | Описание                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**инструментирования**](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [**инструментатионтипе**](eventmanifestschema-instrumentationtype-complextype.md) | В этом разделе определяется один или несколько поставщиков событий и событий, которые они регистрируют.<br/>                                                                                                                                                                                                                     |
| [**локализации**](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [**локализатионтипе**](eventmanifestschema-localizationtype-complextype.md)       | В этом разделе определяются строки локализованных сообщений, используемые потребителями для вывода. Например, в этом разделе будет содержаться локализованная строка сообщения для имени поставщика, заданных Вами событий и всех определенных атрибутов событий, таких как каналы, задачи и коды операций.<br/> |
| [**метаданных**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**метадататипе**](eventmanifestschema-metadatatype-complextype.md)               | В этом разделе определяются типы метаданных, которые могут использоваться другими манифестами. пример см. в файле Winmeta.xml, включенном в \\ папку Include Windows SDK.<br/>                                                                                                                                    |



## <a name="remarks"></a>Remarks

Элемент **инструментатионманифест** должен содержать следующие пространства имен:

<dl> xmlns = " https://schemas.microsoft.com/win/2004/08/events "  
xmlns: Win = " https://manifests.microsoft.com/win/2004/08/windows/events "  
xmlns: XS = " https://www.w3.org/2001/XMLSchema "  
</dl>

Манифест должен содержать раздел инструментирования и раздел локализации. Раздел "инструментирование" и раздел метаданных являются взаимоисключающими (нельзя определить оба одновременно в одном манифесте). Несмотря на то, что можно создать манифест, содержащий раздел метаданных, служба не будет использовать ее. единственными метаданными, распознаваемыми службой, являются метаданные, найденные в файле Winmeta.xml.

## <a name="examples"></a>Примеры

В следующем примере показана скелет полностью определенного манифеста инструментирования.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





