---
description: Содержит идентификатор SSID для беспроводной локальной сети.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID (Ссидконфиг), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910648"
---
# <a name="ssid-ssidconfig-element"></a><span data-ttu-id="0e8f8-103">SSID (Ссидконфиг), элемент</span><span class="sxs-lookup"><span data-stu-id="0e8f8-103">SSID (SSIDConfig) Element</span></span>

<span data-ttu-id="0e8f8-104">Элемент SSID (Ссидконфиг) содержит идентификатор SSID для беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-104">The SSID (SSIDConfig) element contains an SSID for a wireless LAN.</span></span>

<span data-ttu-id="0e8f8-105">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** В профиле может присутствовать не более одного элемента **SSID** .</span><span class="sxs-lookup"><span data-stu-id="0e8f8-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one **SSID** element can appear in a profile.</span></span>

``` syntax
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
```

<span data-ttu-id="0e8f8-106">Элемент **SSID** определяется элементом [**ссидконфиг**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0e8f8-106">The **SSID** element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0e8f8-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0e8f8-107">Child elements</span></span>



| <span data-ttu-id="0e8f8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="0e8f8-108">Element</span></span>                                              | <span data-ttu-id="0e8f8-109">Тип</span><span class="sxs-lookup"><span data-stu-id="0e8f8-109">Type</span></span> | <span data-ttu-id="0e8f8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0e8f8-110">Description</span></span>                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [<span data-ttu-id="0e8f8-111">**hex**</span><span class="sxs-lookup"><span data-stu-id="0e8f8-111">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)   |      | <span data-ttu-id="0e8f8-112">Содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-112">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/> |
| [<span data-ttu-id="0e8f8-113">**безымян**</span><span class="sxs-lookup"><span data-stu-id="0e8f8-113">**name**</span></span>](wlan-profileschema-name-ssid-element.md) |      | <span data-ttu-id="0e8f8-114">Содержит идентификатор SSID для беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-114">Contains the SSID for a wireless LAN.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="0e8f8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e8f8-115">Remarks</span></span>

<span data-ttu-id="0e8f8-116">Несмотря на то, что [**шестнадцатеричные**](wlan-profileschema-hex-ssid-element.md) элементы и [**имена**](wlan-profileschema-name-ssid-element.md) являются необязательными, по крайней мере один **Шестнадцатеричный** элемент или [**имя**](wlan-profileschema-name-ssid-element.md) должны быть дочерними элементами элемента **SSID** .</span><span class="sxs-lookup"><span data-stu-id="0e8f8-116">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the **SSID** element.</span></span>

<span data-ttu-id="0e8f8-117">Когда сведения о профиле преобразуются в идентификатор SSID, [**Шестнадцатеричный**](wlan-profileschema-hex-ssid-element.md) элемент преобразуется в SSID (если есть), а элемент [**Name**](wlan-profileschema-name-ssid-element.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-117">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored.</span></span> <span data-ttu-id="0e8f8-118">Если **Шестнадцатеричный** элемент отсутствует, элемент [**Name**](wlan-profileschema-name-ssid-element.md) преобразуется в идентификатор SSID с помощью преобразования Юникод в ASCII.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-118">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="0e8f8-119">Если идентификатор SSID хранится в профиле, всегда создается [**Шестнадцатеричный**](wlan-profileschema-hex-ssid-element.md) элемент.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-119">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="0e8f8-120">Элемент [**Name**](wlan-profileschema-name-ssid-element.md) создается только в случае успешного преобразования ASCII в формат SSID и создания профиля XML.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-120">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="0e8f8-121">При преобразовании в [**имя**](wlan-profileschema-name-ssid-element.md)некоторые сведения из исходного идентификатора SSID могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="0e8f8-121">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e8f8-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="0e8f8-122">Examples</span></span>

<span data-ttu-id="0e8f8-123">Чтобы просмотреть образцы профилей, в которых используется элемент **SSID** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0e8f8-123">To view sample profiles that use the **SSID** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8f8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0e8f8-124">Requirements</span></span>



| <span data-ttu-id="0e8f8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0e8f8-125">Requirement</span></span> | <span data-ttu-id="0e8f8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0e8f8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0e8f8-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e8f8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8f8-128">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e8f8-128">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0e8f8-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e8f8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8f8-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e8f8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="0e8f8-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0e8f8-131">Redistributable</span></span><br/>          | <span data-ttu-id="0e8f8-132">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="0e8f8-132">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0e8f8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e8f8-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e8f8-134">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="0e8f8-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0e8f8-135">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="0e8f8-135">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="0e8f8-136">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="0e8f8-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0e8f8-137">**Ссидконфиг (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="0e8f8-137">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




