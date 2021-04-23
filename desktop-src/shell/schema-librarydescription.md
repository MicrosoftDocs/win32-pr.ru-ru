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
# <a name="librarydescription-element-library-schema"></a><span data-ttu-id="6b5aa-104">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="6b5aa-104">libraryDescription Element (Library Schema)</span></span>

<span data-ttu-id="6b5aa-105"><libraryDescription>Элемент является контейнером верхнего уровня для определения библиотеки.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-105">The <libraryDescription> element is the top-level container for the library definition.</span></span> <span data-ttu-id="6b5aa-106">Этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-106">This element is required.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b5aa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b5aa-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="6b5aa-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6b5aa-108">Element Information</span></span>



| <span data-ttu-id="6b5aa-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="6b5aa-109">Parent element</span></span> | <span data-ttu-id="6b5aa-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b5aa-110">Child elements</span></span>                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | <span data-ttu-id="6b5aa-111">[элемент Name (схема библиотеки)](schema-library-name.md).</span><span class="sxs-lookup"><span data-stu-id="6b5aa-111">[name Element (Library Schema)](schema-library-name.md).</span></span> <span data-ttu-id="6b5aa-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-112">Required.</span></span>                                                     |
|                | <span data-ttu-id="6b5aa-113">[элемент ownerSID (схема библиотеки)](schema-library-ownersid.md).</span><span class="sxs-lookup"><span data-stu-id="6b5aa-113">[ownerSID Element (Library Schema)](schema-library-ownersid.md).</span></span> <span data-ttu-id="6b5aa-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-114">Optional.</span></span>                                             |
|                | <span data-ttu-id="6b5aa-115">[элемент Version (схема библиотеки)](schema-library-version.md).</span><span class="sxs-lookup"><span data-stu-id="6b5aa-115">[version Element (Library Schema)](schema-library-version.md).</span></span> <span data-ttu-id="6b5aa-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-116">Optional.</span></span>                                               |
|                | <span data-ttu-id="6b5aa-117">[элемент ислибрарипиннед (схема библиотеки)](schema-library-islibrarypinned.md).</span><span class="sxs-lookup"><span data-stu-id="6b5aa-117">[isLibraryPinned Element (Library Schema)](schema-library-islibrarypinned.md).</span></span> <span data-ttu-id="6b5aa-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-118">Optional.</span></span>                               |
|                | <span data-ttu-id="6b5aa-119">[элемент иконреференце (схема библиотеки)](schema-library-iconreference.md).</span><span class="sxs-lookup"><span data-stu-id="6b5aa-119">[iconReference Element (Library Schema)](schema-library-iconreference.md).</span></span> <span data-ttu-id="6b5aa-120">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-120">Optional.</span></span>                                   |
|                | <span data-ttu-id="6b5aa-121">[элемент пропертисторе (схема библиотеки)](schema-library-propertystore.md).</span><span class="sxs-lookup"><span data-stu-id="6b5aa-121">[propertyStore Element (Library Schema)](schema-library-propertystore.md).</span></span> <span data-ttu-id="6b5aa-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-122">Optional.</span></span>                                   |
|                | <span data-ttu-id="6b5aa-123">[элемент темплатеинфо (схема библиотеки)](schema-library-templateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="6b5aa-123">[templateInfo Element (Library Schema)](schema-library-templateinfo.md).</span></span> <span data-ttu-id="6b5aa-124">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-124">Optional.</span></span>                                     |
|                | <span data-ttu-id="6b5aa-125">[элемент сеарчконнектордескриптионлист (схема библиотеки)](schema-library-searchconnectordescriptionlist.md).</span><span class="sxs-lookup"><span data-stu-id="6b5aa-125">[searchConnectorDescriptionList Element (Library Schema)](schema-library-searchconnectordescriptionlist.md).</span></span> <span data-ttu-id="6b5aa-126">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-126">Required.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6b5aa-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b5aa-127">Remarks</span></span>

<span data-ttu-id="6b5aa-128">Каждая библиотека может содержать одно или несколько расположений, которые можно просматривать или искать пользователем с помощью проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-128">Each library can contain one or more locations that can be browsed or searched by a user using Windows Explorer.</span></span> <span data-ttu-id="6b5aa-129">Расположения определяются соединителями поиска с помощью [<searchConnectorDescription>](schema-library-searchconnectordescription.md) элементов в [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) элементе-контейнере.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-129">The locations are defined by search connectors using [<searchConnectorDescription>](schema-library-searchconnectordescription.md) elements in a [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) container element.</span></span>

<span data-ttu-id="6b5aa-130">Библиотека может иметь уникальный набор свойств, а расположения в библиотеке также могут иметь уникальные наборы свойств.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-130">A library can have a unique set of properties, and locations in the library can also have unique sets of properties.</span></span> <span data-ttu-id="6b5aa-131">Эти свойства определяются в [<property>](schema-library-property.md) [<propertyStore>](schema-library-propertystore.md) элементах внутри элемента Container.</span><span class="sxs-lookup"><span data-stu-id="6b5aa-131">These properties are defined in [<property>](schema-library-property.md) elements within a [<propertyStore>](schema-library-propertystore.md) container element.</span></span>

## <a name="example"></a><span data-ttu-id="6b5aa-132">Например, .</span><span class="sxs-lookup"><span data-stu-id="6b5aa-132">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6b5aa-133">См. также</span><span class="sxs-lookup"><span data-stu-id="6b5aa-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b5aa-134">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="6b5aa-134">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="6b5aa-135">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="6b5aa-135">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
