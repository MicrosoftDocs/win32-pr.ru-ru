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
# <a name="scan-profile-schema"></a><span data-ttu-id="73288-103">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="73288-103">Scan Profile Schema</span></span>

<span data-ttu-id="73288-104">Схема профиля сканирования определяет формат XML, который может использоваться для хранения свойств элементов для загрузки изображений (WIA), таких как сканеры и камеры.</span><span class="sxs-lookup"><span data-stu-id="73288-104">The Scan Profile Schema defines an XML format that can be used to store the properties of Windows Image Acquisition (WIA) items, such as scanners and cameras.</span></span> <span data-ttu-id="73288-105">Эти постоянные файлы позволяют приложениям обеспечивать автоматическое сканирование, не требуя от пользователей запоминать параметры свойств элементов.</span><span class="sxs-lookup"><span data-stu-id="73288-105">These persistent files enable applications to provide automatic scanning without requiring users to remember the property settings of the items.</span></span>

<span data-ttu-id="73288-106">У любого устройства [**IWiaItem2**](-wia-iwiaitem2.md) может быть профиль сканирования.</span><span class="sxs-lookup"><span data-stu-id="73288-106">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="73288-107">Однако **IWiaItem2** элементы типов \_ Категория WIA \_ Finished \_ File и WIA \_ Category \_ не могут иметь профили.</span><span class="sxs-lookup"><span data-stu-id="73288-107">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="73288-108">Профили сканирования создаются и управляются с помощью интерфейсов [**исканпрофиле**](-wia-iscanprofile.md), [**исканпрофилемгр**](-wia-iscanprofilemgr.md)и [**исканпрофилеуи**](-wia-iscanprofileui.md) .</span><span class="sxs-lookup"><span data-stu-id="73288-108">Scan profiles are created and managed through the [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md), and [**IScanProfileUI**](-wia-iscanprofileui.md) interfaces.</span></span> <span data-ttu-id="73288-109">Пользователи приложения могут изменять профили с помощью метода [**исканпрофилеуи:: сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="73288-109">Users of your application can modify profiles in limited ways using the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="73288-110">Все профили сканирования имеют следующие элементы: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , и `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="73288-110">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="73288-111">Профиль по умолчанию для устройства также имеет `<Default>` элемент.</span><span class="sxs-lookup"><span data-stu-id="73288-111">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="73288-112">`<ProfileGUID>`Элемент и `<DeviceID>` элемент не могут быть изменены после создания профиля сканирования.</span><span class="sxs-lookup"><span data-stu-id="73288-112">The `<ProfileGUID>` element and the `<DeviceID>` element cannot be changed after the scan profile is created.</span></span> <span data-ttu-id="73288-113">Значения `<ProfileName>` элемента и `<WiaItem>` элемента могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="73288-113">The values of the `<ProfileName>` element and the `<WiaItem>` element can be modified.</span></span> <span data-ttu-id="73288-114">`<Default>`Элемент можно добавить или удалить.</span><span class="sxs-lookup"><span data-stu-id="73288-114">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="73288-115">Это можно сделать программно с помощью методов [**исканпрофиле:: SetName**](-wia-iscanprofile-setname.md), [**Исканпрофиле:: сетитем**](-wia-iscanprofile-setitem.md)и [**исканпрофилемгр:: сетдефаулт**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="73288-115">This can be done programatically using the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="73288-116">Эти свойства также могут быть изменены пользователями с помощью метода [**исканпрофилеуи:: сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="73288-116">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="73288-117">`<Properties>`Элемент содержит `<Property>` дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="73288-117">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="73288-118">Используйте их для добавления в профиль любого элемента WIA или свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="73288-118">Use these to add any WIA item or device property to the profile.</span></span> <span data-ttu-id="73288-119">Вы также можете разработать собственные `<Property>` дочерние элементы приобретения Image.</span><span class="sxs-lookup"><span data-stu-id="73288-119">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="73288-120">Это делает схему профиля сканирования расширяемой.</span><span class="sxs-lookup"><span data-stu-id="73288-120">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="73288-121">(Дополнительные сведения о расширении схемы см. в разделе [Определение пользовательских свойств](-wia-defining-custom-properties.md), [**исканпрофиле::-Property**](-wia-iscanprofile-getproperty.md)и [**исканпрофиле:: SetProperty**](-wia-iscanprofile-setproperty.md).)</span><span class="sxs-lookup"><span data-stu-id="73288-121">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

<span data-ttu-id="73288-122">Ниже приведена полная схема профиля сканирования.</span><span class="sxs-lookup"><span data-stu-id="73288-122">Here is the complete Scan Profile Schema.</span></span> <span data-ttu-id="73288-123">Ниже приведен пример профиля.</span><span class="sxs-lookup"><span data-stu-id="73288-123">A sample profile follows.</span></span>


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



<span data-ttu-id="73288-124">Щелкните **Показать пример** , чтобы просмотреть пример профиля.</span><span class="sxs-lookup"><span data-stu-id="73288-124">Click **Show Example** to see a sample profile.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="73288-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="73288-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="73288-126">**Reference**</span><span class="sxs-lookup"><span data-stu-id="73288-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="73288-127">**Исканпрофиле:: Property**</span><span class="sxs-lookup"><span data-stu-id="73288-127">**IScanProfile::GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[<span data-ttu-id="73288-128">**Исканпрофиле:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="73288-128">**IScanProfile::SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)
</dt> <dt>

<span data-ttu-id="73288-129">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="73288-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="73288-130">Константы свойств WIA</span><span class="sxs-lookup"><span data-stu-id="73288-130">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="73288-131">Определение пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="73288-131">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



