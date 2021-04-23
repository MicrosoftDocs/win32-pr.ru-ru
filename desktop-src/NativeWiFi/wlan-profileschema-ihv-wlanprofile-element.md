---
description: Содержит различные параметры для независимых поставщиков оборудования.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Элемент IHV (Вланпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683034"
---
# <a name="ihv-wlanprofile-element"></a><span data-ttu-id="94443-103">Элемент IHV (Вланпрофиле)</span><span class="sxs-lookup"><span data-stu-id="94443-103">IHV (WLANProfile) Element</span></span>

<span data-ttu-id="94443-104">Элемент IHV (Вланпрофиле) содержит различные параметры для независимых поставщиков оборудования.</span><span class="sxs-lookup"><span data-stu-id="94443-104">The IHV (WLANProfile) element contains various settings for independent hardware vendors.</span></span> <span data-ttu-id="94443-105">Если профиль включает параметры безопасности IHV, они переопределяют любую систему безопасности, определенную корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="94443-105">If a profile includes IHV security settings, they override any Microsoft-defined security.</span></span>

<span data-ttu-id="94443-106">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="94443-106">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
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

<span data-ttu-id="94443-107">Элемент определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="94443-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="94443-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="94443-108">Child elements</span></span>



| <span data-ttu-id="94443-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="94443-109">Element</span></span>                                                             | <span data-ttu-id="94443-110">Тип</span><span class="sxs-lookup"><span data-stu-id="94443-110">Type</span></span>                                                              | <span data-ttu-id="94443-111">Описание</span><span class="sxs-lookup"><span data-stu-id="94443-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94443-112">**установлен**</span><span class="sxs-lookup"><span data-stu-id="94443-112">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | <span data-ttu-id="94443-113">Содержит параметры подключения, связанные с IHV.</span><span class="sxs-lookup"><span data-stu-id="94443-113">Contains IHV-related connectivity settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="94443-114">**КОДОМ**</span><span class="sxs-lookup"><span data-stu-id="94443-114">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | <span data-ttu-id="94443-115">Содержит 3-байтовый hexBinary, определяющий IHV.</span><span class="sxs-lookup"><span data-stu-id="94443-115">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="94443-116">**ауихеадер**</span><span class="sxs-lookup"><span data-stu-id="94443-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | <span data-ttu-id="94443-117">Идентифицирует независимый поставщик оборудования.</span><span class="sxs-lookup"><span data-stu-id="94443-117">Identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="94443-118">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="94443-118">**security**</span></span>](wlan-profileschema-security-ihv-element.md)         |                                                                   | <span data-ttu-id="94443-119">Содержит параметры безопасности, зависящие от IHV.</span><span class="sxs-lookup"><span data-stu-id="94443-119">Contains IHV-specific security settings.</span></span> <span data-ttu-id="94443-120">Параметры безопасности Microsoft и параметры безопасности IHV являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="94443-120">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="94443-121">Если заданы оба параметра безопасности, то весь профиль считается недопустимым.</span><span class="sxs-lookup"><span data-stu-id="94443-121">The entire profile is invalid if both security settings are present.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="94443-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="94443-122">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | <span data-ttu-id="94443-123">Содержит 1-байтовый hexBinary, используемый для различения сетевых карт одним и тем же IHV.</span><span class="sxs-lookup"><span data-stu-id="94443-123">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="94443-124">**усемсонекс**</span><span class="sxs-lookup"><span data-stu-id="94443-124">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)       | [<span data-ttu-id="94443-125">boolean</span><span class="sxs-lookup"><span data-stu-id="94443-125">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="94443-126">Указывает источник параметров безопасности 802.1 X, используемых компонентом безопасности независимого поставщика оборудования.</span><span class="sxs-lookup"><span data-stu-id="94443-126">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="94443-127">Если [**усемсонекс**](wlan-profileschema-usemsonex-ihv-element.md) имеет значение true, компоненты безопасности IHV используют определенные корпорацией Майкрософт параметры 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="94443-127">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="94443-128">Если **усемсонекс** имеет значение false, компоненты безопасности IHV используют предоставленные поставщиком параметры 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="94443-128">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="94443-129">По умолчанию **усемсонекс** имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="94443-129">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="94443-130">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="94443-130">This element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="94443-131">Требования</span><span class="sxs-lookup"><span data-stu-id="94443-131">Requirements</span></span>



| <span data-ttu-id="94443-132">Требование</span><span class="sxs-lookup"><span data-stu-id="94443-132">Requirement</span></span> | <span data-ttu-id="94443-133">Значение</span><span class="sxs-lookup"><span data-stu-id="94443-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94443-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94443-134">Minimum supported client</span></span><br/> | <span data-ttu-id="94443-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94443-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94443-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94443-136">Minimum supported server</span></span><br/> | <span data-ttu-id="94443-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94443-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94443-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94443-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="94443-139">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="94443-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="94443-140">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="94443-140">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="94443-141">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="94443-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="94443-142">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="94443-142">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
