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
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "104273351"
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
| [**метаданных**](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [**метадататипе**](eventmanifestschema-metadatatype-complextype.md)               | В этом разделе определяются типы метаданных, которые могут использоваться другими манифестами. Пример см. в файле Winmeta.xml, включенном в \\ папку Include Windows SDK.<br/>                                                                                                                                    |



## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





