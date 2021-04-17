---
description: — Корневой элемент, определяющий профиль мобильного широкополосного подключения.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Мбнпрофиле, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 7016d492a70192a7d6accdcb3aaa57a9c564960e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711162"
---
# <a name="mbnprofile-element"></a><span data-ttu-id="ff09c-103">Мбнпрофиле, элемент</span><span class="sxs-lookup"><span data-stu-id="ff09c-103">MBNProfile Element</span></span>

<span data-ttu-id="ff09c-104">Элемент **мбнпрофиле** является корневым элементом, идентифицирующим профиль мобильного широкополосного подключения.</span><span class="sxs-lookup"><span data-stu-id="ff09c-104">The **MBNProfile** element is the root element that identifies a Mobile Broadband profile.</span></span>

<span data-ttu-id="ff09c-105">На документ может быть только один элемент этого типа.</span><span class="sxs-lookup"><span data-stu-id="ff09c-105">There can only be one element of this type per document.</span></span>

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
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

## <a name="child-elements"></a><span data-ttu-id="ff09c-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ff09c-106">Child elements</span></span>



| <span data-ttu-id="ff09c-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="ff09c-107">Element</span></span>                                                                          | <span data-ttu-id="ff09c-108">Тип</span><span class="sxs-lookup"><span data-stu-id="ff09c-108">Type</span></span>                                                           | <span data-ttu-id="ff09c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ff09c-109">Description</span></span>                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="ff09c-110">**аутоконнектонинтернет**</span><span class="sxs-lookup"><span data-stu-id="ff09c-110">**AutoConnectOnInternet**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md) | <span data-ttu-id="ff09c-111">Логическое</span><span class="sxs-lookup"><span data-stu-id="ff09c-111">boolean</span></span>                                                        | <span data-ttu-id="ff09c-112">Будет ли устройство автоматически подключаться.</span><span class="sxs-lookup"><span data-stu-id="ff09c-112">Whether the device will automatically connect.</span></span><br/> |
| [<span data-ttu-id="ff09c-113">**ConnectionMode**</span><span class="sxs-lookup"><span data-stu-id="ff09c-113">**ConnectionMode**</span></span>](schema-connectionmode-mbnprofile-element.md)               |                                                                | <span data-ttu-id="ff09c-114">Параметры автоматического подключения устройства.</span><span class="sxs-lookup"><span data-stu-id="ff09c-114">The device auto connection settings.</span></span><br/>           |
| [<span data-ttu-id="ff09c-115">**Локального**</span><span class="sxs-lookup"><span data-stu-id="ff09c-115">**Context**</span></span>](schema-context-mbnprofile-element.md)                             | [<span data-ttu-id="ff09c-116">**contextType**</span><span class="sxs-lookup"><span data-stu-id="ff09c-116">**contextType**</span></span>](schema-contexttype-complextype.md)          | <span data-ttu-id="ff09c-117">Параметры настройки подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ff09c-117">Data connection setup parameters.</span></span><br/>              |
| [<span data-ttu-id="ff09c-118">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="ff09c-118">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | <span data-ttu-id="ff09c-119">Предпочтительные поставщики сети для роуминга.</span><span class="sxs-lookup"><span data-stu-id="ff09c-119">Preferred network providers for roaming.</span></span><br/>       |
| [<span data-ttu-id="ff09c-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ff09c-120">**Description**</span></span>](schema-description-mbnprofile-element.md)                     | [<span data-ttu-id="ff09c-121">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="ff09c-121">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="ff09c-122">Описание профиля.</span><span class="sxs-lookup"><span data-stu-id="ff09c-122">Description of the profile.</span></span><br/>                    |
| [<span data-ttu-id="ff09c-123">**HomeProviderName**</span><span class="sxs-lookup"><span data-stu-id="ff09c-123">**HomeProviderName**</span></span>](schema-homeprovidername-mbnprofile-element.md)           | [<span data-ttu-id="ff09c-124">**провидернаметипе**</span><span class="sxs-lookup"><span data-stu-id="ff09c-124">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="ff09c-125">Имя поставщика услуг домашнего доступа.</span><span class="sxs-lookup"><span data-stu-id="ff09c-125">Name of the home provider.</span></span><br/>                     |
| [<span data-ttu-id="ff09c-126">**иконфилепас**</span><span class="sxs-lookup"><span data-stu-id="ff09c-126">**ICONFilePath**</span></span>](schema-iconfilepath-mbnprofile-element.md)                   | [<span data-ttu-id="ff09c-127">**иконфилетипе**</span><span class="sxs-lookup"><span data-stu-id="ff09c-127">**iconFileType**</span></span>](schema-iconfiletype-simpletype.md)         | <span data-ttu-id="ff09c-128">Путь к файлу значка.</span><span class="sxs-lookup"><span data-stu-id="ff09c-128">Path to the icon file.</span></span><br/>                         |
| [<span data-ttu-id="ff09c-129">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="ff09c-129">**IsDefault**</span></span>](schema-isdefault-mbnprofile-element.md)                         | <span data-ttu-id="ff09c-130">Логическое</span><span class="sxs-lookup"><span data-stu-id="ff09c-130">boolean</span></span>                                                        | <span data-ttu-id="ff09c-131">Является ли профиль стандартным.</span><span class="sxs-lookup"><span data-stu-id="ff09c-131">Whether the profile is the default.</span></span><br/>            |
| [<span data-ttu-id="ff09c-132">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ff09c-132">**Name**</span></span>](schema-name-mbnprofile-element.md)                                   | [<span data-ttu-id="ff09c-133">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="ff09c-133">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="ff09c-134">Имя профиля.</span><span class="sxs-lookup"><span data-stu-id="ff09c-134">Name of the profile.</span></span><br/>                           |
| [<span data-ttu-id="ff09c-135">**профилекреатионтипе**</span><span class="sxs-lookup"><span data-stu-id="ff09c-135">**ProfileCreationType**</span></span>](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | <span data-ttu-id="ff09c-136">Сведения о создателе профиля.</span><span class="sxs-lookup"><span data-stu-id="ff09c-136">Information about the profile creator.</span></span><br/>         |
| [<span data-ttu-id="ff09c-137">**симикЦид**</span><span class="sxs-lookup"><span data-stu-id="ff09c-137">**SimIccID**</span></span>](schema-simiccid-mbnprofile-element.md)                           | [<span data-ttu-id="ff09c-138">**симикЦидтипе**</span><span class="sxs-lookup"><span data-stu-id="ff09c-138">**simIccIDType**</span></span>](schema-simiccidtype-simpletype.md)         | <span data-ttu-id="ff09c-139">Идентификационный номер SIM-карты для устройств GSM.</span><span class="sxs-lookup"><span data-stu-id="ff09c-139">SIM identification number for GSM devices.</span></span><br/>     |
| [<span data-ttu-id="ff09c-140">**субскриберид**</span><span class="sxs-lookup"><span data-stu-id="ff09c-140">**SubscriberID**</span></span>](schema-subscriberid-mbnprofile-element.md)                   | [<span data-ttu-id="ff09c-141">**субскриберидтипе**</span><span class="sxs-lookup"><span data-stu-id="ff09c-141">**subscriberIdType**</span></span>](schema-subscriberidtype-simpletype.md) | <span data-ttu-id="ff09c-142">Уникальный идентификатор профиля.</span><span class="sxs-lookup"><span data-stu-id="ff09c-142">Unique identifier of the profile.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="ff09c-143">Требования</span><span class="sxs-lookup"><span data-stu-id="ff09c-143">Requirements</span></span>



| <span data-ttu-id="ff09c-144">Требование</span><span class="sxs-lookup"><span data-stu-id="ff09c-144">Requirement</span></span> | <span data-ttu-id="ff09c-145">Значение</span><span class="sxs-lookup"><span data-stu-id="ff09c-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ff09c-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff09c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ff09c-147">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ff09c-147">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ff09c-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff09c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ff09c-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ff09c-149">None supported</span></span><br/>                         |



 

 




