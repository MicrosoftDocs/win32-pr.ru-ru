---
description: Схема профиля сканирования определяет формат XML, который может использоваться для хранения свойств элементов для загрузки изображений (WIA), таких как сканеры и камеры.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Схема профиля сканирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692420"
---
# <a name="scan-profile-schema"></a>Схема профиля сканирования

Схема профиля сканирования определяет формат XML, который может использоваться для хранения свойств элементов для загрузки изображений (WIA), таких как сканеры и камеры. Эти постоянные файлы позволяют приложениям обеспечивать автоматическое сканирование, не требуя от пользователей запоминать параметры свойств элементов.

У любого устройства [**IWiaItem2**](-wia-iwiaitem2.md) может быть профиль сканирования. Однако **IWiaItem2** элементы типов \_ Категория WIA \_ Finished \_ File и WIA \_ Category \_ не могут иметь профили.

Профили сканирования создаются и управляются с помощью интерфейсов [**исканпрофиле**](-wia-iscanprofile.md), [**исканпрофилемгр**](-wia-iscanprofilemgr.md)и [**исканпрофилеуи**](-wia-iscanprofileui.md) . Пользователи приложения могут изменять профили с помощью метода [**исканпрофилеуи:: сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) с ограниченными возможностями.

Все профили сканирования имеют следующие элементы: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , и `<Properties>` . Профиль по умолчанию для устройства также имеет `<Default>` элемент.

`<ProfileGUID>`Элемент и `<DeviceID>` элемент не могут быть изменены после создания профиля сканирования. Значения `<ProfileName>` элемента и `<WiaItem>` элемента могут быть изменены. `<Default>`Элемент можно добавить или удалить. Это можно сделать программно с помощью методов [**исканпрофиле:: SetName**](-wia-iscanprofile-setname.md), [**Исканпрофиле:: сетитем**](-wia-iscanprofile-setitem.md)и [**исканпрофилемгр:: сетдефаулт**](-wia-iscanprofilemgr-setdefault.md) . Эти свойства также могут быть изменены пользователями с помощью метода [**исканпрофилеуи:: сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .

`<Properties>`Элемент содержит `<Property>` дочерние элементы. Используйте их для добавления в профиль любого элемента WIA или свойства устройства. Вы также можете разработать собственные `<Property>` дочерние элементы приобретения Image. Это делает схему профиля сканирования расширяемой. (Дополнительные сведения о расширении схемы см. в разделе [Определение пользовательских свойств](-wia-defining-custom-properties.md), [**исканпрофиле::-Property**](-wia-iscanprofile-getproperty.md)и [**исканпрофиле:: SetProperty**](-wia-iscanprofile-setproperty.md).)

Ниже приведена полная схема профиля сканирования. Ниже приведен пример профиля.


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



Щелкните **Показать пример** , чтобы просмотреть пример профиля.


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[**Исканпрофиле:: Property**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**Исканпрофиле:: SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Константы свойств WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Определение пользовательских свойств](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



