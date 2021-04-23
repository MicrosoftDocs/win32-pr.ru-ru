---
description: Указывает пару для проверки подлинности и шифрования, которая будет использоваться для этого профиля.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Аусенкриптион (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673443"
---
# <a name="authencryption-security-element"></a><span data-ttu-id="5698f-103">Аусенкриптион (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="5698f-103">authEncryption (security) Element</span></span>

<span data-ttu-id="5698f-104">Элемент Аусенкриптион (Security) указывает пару проверки подлинности и шифрования, которая будет использоваться для этого профиля.</span><span class="sxs-lookup"><span data-stu-id="5698f-104">The authEncryption (security) element specifies the authentication and encryption pair to be used for this profile.</span></span>

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="encryption">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="none"
                         />
                        <xs:enumeration
                            value="WEP"
                         />
                        <xs:enumeration
                            value="TKIP"
                         />
                        <xs:enumeration
                            value="AES"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="useOneX"
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

<span data-ttu-id="5698f-105">Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5698f-105">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5698f-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5698f-106">Child elements</span></span>



| <span data-ttu-id="5698f-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="5698f-107">Element</span></span>                                                                            | <span data-ttu-id="5698f-108">Тип</span><span class="sxs-lookup"><span data-stu-id="5698f-108">Type</span></span>                                                              | <span data-ttu-id="5698f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5698f-109">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5698f-110">**идентификаци**</span><span class="sxs-lookup"><span data-stu-id="5698f-110">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="5698f-111">Указывает метод проверки подлинности, который должен использоваться для подключения к беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="5698f-111">Specifies the authentication method that must be used to connect to the wireless LAN.</span></span><br/> |
| [<span data-ttu-id="5698f-112">**ключ**</span><span class="sxs-lookup"><span data-stu-id="5698f-112">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="5698f-113">Задает шифрование данных, используемое для подключения к беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="5698f-113">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                       |
| [<span data-ttu-id="5698f-114">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="5698f-114">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="5698f-115">boolean</span><span class="sxs-lookup"><span data-stu-id="5698f-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="5698f-116">Указывает, используется ли 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="5698f-116">Indicates whether 802.1X is used.</span></span><br/>                                                     |



## <a name="remarks"></a><span data-ttu-id="5698f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5698f-117">Remarks</span></span>

<span data-ttu-id="5698f-118">Элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) может быть вставлен как дочерний элемент элемента **аусенкриптион** .</span><span class="sxs-lookup"><span data-stu-id="5698f-118">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the **authEncryption** element.</span></span>

## <a name="examples"></a><span data-ttu-id="5698f-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="5698f-119">Examples</span></span>

<span data-ttu-id="5698f-120">Чтобы просмотреть образцы профилей, использующих элемент **аусенкриптион** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5698f-120">To view sample profiles that use the **authEncryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span> <span data-ttu-id="5698f-121">Пример профиля, в котором используется элемент [**фипсмоде**](wlan-profileschema-fipsmode-authencryption-element.md) , см. в разделе [пример профиля FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5698f-121">To view a sample profile that uses the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5698f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5698f-122">Requirements</span></span>



| <span data-ttu-id="5698f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5698f-123">Requirement</span></span> | <span data-ttu-id="5698f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5698f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="5698f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5698f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5698f-126">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5698f-126">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5698f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5698f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5698f-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5698f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5698f-129">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="5698f-129">Redistributable</span></span><br/>          | <span data-ttu-id="5698f-130">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="5698f-130">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5698f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5698f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5698f-132">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="5698f-132">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="5698f-133">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="5698f-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5698f-134">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="5698f-134">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="5698f-135">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="5698f-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5698f-136">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="5698f-136">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
