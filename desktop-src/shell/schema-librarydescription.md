---
description: <libraryDescription>Элемент является контейнером верхнего уровня для определения библиотеки. Этот элемент является обязательным.
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: Элемент Либраридескриптион (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125cb01ce1bd38418c10f5b14ff7b28f64efba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984581"
---
# <a name="librarydescription-element-library-schema"></a>Элемент Либраридескриптион (схема библиотеки)

<libraryDescription>Элемент является контейнером верхнего уровня для определения библиотеки. Этот элемент является обязательным.

## <a name="syntax"></a>Синтаксис


```
<!-- libraryDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
    <xs:include schemaLocation="commonTypes-ms.xsd"/>
    <xs:element name="libraryDescription">
        <xs:complexType>
            <xs:all>
                <xs:element name="name" type="xs:string"/>
                <xs:element name="ownerSID" minOccurs="0"/>
                <xs:element name="version" type="xs:int" minOccurs="0"/>
                <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
                <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
                <xs:element name="propertyStore" minOccurs="0">
                    <xs:complexType>
                        <xs:complexContent>
                            <xs:extension base="propertyStoreType"/>
                        </xs:complexContent>
                    </xs:complexType>
                </xs:element>
                <xs:element name="templateInfo" minOccurs="0">
                    <xs:complexType>
                        <xs:all>
                            <xs:element name="folderType" minOccurs="0"/>
                        </xs:all>
                    </xs:complexType>
                </xs:element>
                <xs:element name="searchConnectorDescriptionList" minOccurs="0">
                    <xs:complexType>
                        <xs:sequence minOccurs="0">
                            <xs:element name="searchConnectorDescription" 
                             type="searchConnectorDescriptionType" minOccurs="0" 
                             maxOccurs="unbounded"/>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:all>
        </xs:complexType>
    </xs:element>
</xs:schema>
```



## <a name="element-information"></a>Сведения об элементе



| Родительский элемент | Дочерние элементы                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | [элемент Name (схема библиотеки)](schema-library-name.md). Обязательный.                                                     |
|                | [элемент ownerSID (схема библиотеки)](schema-library-ownersid.md). Необязательный параметр.                                             |
|                | [элемент Version (схема библиотеки)](schema-library-version.md). Необязательный параметр.                                               |
|                | [элемент ислибрарипиннед (схема библиотеки)](schema-library-islibrarypinned.md). Необязательный параметр.                               |
|                | [элемент иконреференце (схема библиотеки)](schema-library-iconreference.md). Необязательный параметр.                                   |
|                | [элемент пропертисторе (схема библиотеки)](schema-library-propertystore.md). Необязательный параметр.                                   |
|                | [элемент темплатеинфо (схема библиотеки)](schema-library-templateinfo.md). Необязательный параметр.                                     |
|                | [элемент сеарчконнектордескриптионлист (схема библиотеки)](schema-library-searchconnectordescriptionlist.md). Обязательный. |



 

## <a name="remarks"></a>Примечания

Каждая библиотека может содержать одно или несколько расположений, которые можно просматривать или искать пользователем с помощью проводника Windows. Расположения определяются соединителями поиска с помощью [<searchConnectorDescription>](schema-library-searchconnectordescription.md) элементов в [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) элементе-контейнере.

Библиотека может иметь уникальный набор свойств, а расположения в библиотеке также могут иметь уникальные наборы свойств. Эти свойства определяются в [<property>](schema-library-property.md) [<propertyStore>](schema-library-propertystore.md) элементах внутри элемента Container.

## <a name="example"></a>Например, .


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Схема описания библиотеки](library-schema-entry.md)
</dt> <dt>

[Схема описания соединителя поиска](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
