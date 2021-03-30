---
description: Содержит один или несколько идентификаторов SSID для беспроводных локальных сетей.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Ссидконфиг (Вланпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910356"
---
# <a name="ssidconfig-wlanprofile-element"></a><span data-ttu-id="a1c9c-103">Ссидконфиг (Вланпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="a1c9c-103">SSIDConfig (WLANProfile) Element</span></span>

<span data-ttu-id="a1c9c-104">Элемент Ссидконфиг (Вланпрофиле) содержит один или несколько идентификаторов SSID для беспроводных локальных сетей.</span><span class="sxs-lookup"><span data-stu-id="a1c9c-104">The SSIDConfig (WLANProfile) element contains one or more SSIDs for wireless LANs.</span></span>

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="SSID"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="hex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="name"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="nonBroadcast"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a1c9c-105">Элемент **ссидконфиг** определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c9c-105">The **SSIDConfig** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a1c9c-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a1c9c-106">Child elements</span></span>



| <span data-ttu-id="a1c9c-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a1c9c-107">Element</span></span>                                                                    | <span data-ttu-id="a1c9c-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a1c9c-108">Type</span></span>                                                              | <span data-ttu-id="a1c9c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a1c9c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1c9c-110">**hex**</span><span class="sxs-lookup"><span data-stu-id="a1c9c-110">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | <span data-ttu-id="a1c9c-111">Содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="a1c9c-111">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a1c9c-112">**безымян**</span><span class="sxs-lookup"><span data-stu-id="a1c9c-112">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                       |                                                                   | <span data-ttu-id="a1c9c-113">Содержит имя SSID беспроводной локальной сети (с учетом регистра).</span><span class="sxs-lookup"><span data-stu-id="a1c9c-113">Contains the (case-sensitive) name of the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="a1c9c-114">**Нешироковещательная рассылка**</span><span class="sxs-lookup"><span data-stu-id="a1c9c-114">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [<span data-ttu-id="a1c9c-115">boolean</span><span class="sxs-lookup"><span data-stu-id="a1c9c-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="a1c9c-116">Указывает, будет ли сеть рассылать свое SSID.</span><span class="sxs-lookup"><span data-stu-id="a1c9c-116">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="a1c9c-117">Если для параметра [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) задано значение ESS, это может быть либо **true** , либо **false**.</span><span class="sxs-lookup"><span data-stu-id="a1c9c-117">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either **TRUE** or **FALSE**.</span></span> <span data-ttu-id="a1c9c-118">Значение по умолчанию — **true** , если этот элемент отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a1c9c-118">The default value is **TRUE** if this element is absent.</span></span><br/> <span data-ttu-id="a1c9c-119">Если параметр [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) имеет значение ибсс, это значение должно быть равно **false**.</span><span class="sxs-lookup"><span data-stu-id="a1c9c-119">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be **FALSE**.</span></span><br/> <span data-ttu-id="a1c9c-120">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a1c9c-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="a1c9c-121">**SSID**</span><span class="sxs-lookup"><span data-stu-id="a1c9c-121">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | <span data-ttu-id="a1c9c-122">Содержит идентификатор SSID для беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a1c9c-122">Contains an SSID for a wireless LAN.</span></span><br/> <span data-ttu-id="a1c9c-123">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** В профиле может присутствовать не более одного элемента [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c9c-123">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a><span data-ttu-id="a1c9c-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="a1c9c-124">Examples</span></span>

<span data-ttu-id="a1c9c-125">Чтобы просмотреть образцы профилей, использующих элемент **ссидконфиг** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a1c9c-125">To view sample profiles that use the **SSIDConfig** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1c9c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a1c9c-126">Requirements</span></span>



| <span data-ttu-id="a1c9c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a1c9c-127">Requirement</span></span> | <span data-ttu-id="a1c9c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a1c9c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a1c9c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1c9c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a1c9c-130">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1c9c-130">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a1c9c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1c9c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a1c9c-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1c9c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a1c9c-133">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a1c9c-133">Redistributable</span></span><br/>          | <span data-ttu-id="a1c9c-134">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="a1c9c-134">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a1c9c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1c9c-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1c9c-136">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="a1c9c-136">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a1c9c-137">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a1c9c-137">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a1c9c-138">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="a1c9c-138">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a1c9c-139">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a1c9c-139">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
