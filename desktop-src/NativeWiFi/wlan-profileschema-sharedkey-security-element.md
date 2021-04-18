---
description: Содержит общие сведения о ключе.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: sharedKey (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673897"
---
# <a name="sharedkey-security-element"></a><span data-ttu-id="cfd51-103">sharedKey (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="cfd51-103">sharedKey (security) Element</span></span>

<span data-ttu-id="cfd51-104">Элемент sharedKey (Security) содержит общие сведения о ключе.</span><span class="sxs-lookup"><span data-stu-id="cfd51-104">The sharedKey (security) element contains shared key information.</span></span> <span data-ttu-id="cfd51-105">Этот элемент необходим только в том случае, если для пары "Проверка подлинности и шифрование" требуются ключи WEP или PSK.</span><span class="sxs-lookup"><span data-stu-id="cfd51-105">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span>

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="keyType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="networkKey"
                         />
                        <xs:enumeration
                            value="passPhrase"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
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

<span data-ttu-id="cfd51-106">Элемент определяется элементом [**безопасности**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cfd51-106">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cfd51-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cfd51-107">Child elements</span></span>



| <span data-ttu-id="cfd51-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="cfd51-108">Element</span></span>                                                                 | <span data-ttu-id="cfd51-109">Тип</span><span class="sxs-lookup"><span data-stu-id="cfd51-109">Type</span></span>                                                              | <span data-ttu-id="cfd51-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cfd51-110">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfd51-111">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="cfd51-111">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md) | [<span data-ttu-id="cfd51-112">string</span><span class="sxs-lookup"><span data-stu-id="cfd51-112">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="cfd51-113">Содержит ключ сети или парольную фразу.</span><span class="sxs-lookup"><span data-stu-id="cfd51-113">Contains the network key or passphrase.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="cfd51-114">**keyType**</span><span class="sxs-lookup"><span data-stu-id="cfd51-114">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | <span data-ttu-id="cfd51-115">Тип ключа.</span><span class="sxs-lookup"><span data-stu-id="cfd51-115">Type of key.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="cfd51-116">**protected**</span><span class="sxs-lookup"><span data-stu-id="cfd51-116">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)     | [<span data-ttu-id="cfd51-117">boolean</span><span class="sxs-lookup"><span data-stu-id="cfd51-117">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="cfd51-118">Указывает, зашифрован ли ключ.</span><span class="sxs-lookup"><span data-stu-id="cfd51-118">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="cfd51-119">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент должен иметь значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="cfd51-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cfd51-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfd51-120">Remarks</span></span>

<span data-ttu-id="cfd51-121">Для Windows Vista и Windows Server 2008 данные, связанные с элементом **sharedKey** , шифруются перед сохранением в хранилище профилей.</span><span class="sxs-lookup"><span data-stu-id="cfd51-121">For Windows Vista and Windows Server 2008, the data associated with the **sharedKey** element is encrypted before it is saved in the profile store.</span></span>

<span data-ttu-id="cfd51-122">Для Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2) данные не шифруются.</span><span class="sxs-lookup"><span data-stu-id="cfd51-122">For Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, the data is not encrypted.</span></span>

## <a name="examples"></a><span data-ttu-id="cfd51-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="cfd51-123">Examples</span></span>

<span data-ttu-id="cfd51-124">Для просмотра образцов профилей, использующих элемент **sharedKey** , см. пример [профиля без широковещательной рассылки](non-broadcast-profile-sample.md), [пример профиля WPA-личное](wpa-personal-profile-sample.md)и [профиль WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="cfd51-124">To view sample profiles that use the **sharedKey** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd51-125">Требования</span><span class="sxs-lookup"><span data-stu-id="cfd51-125">Requirements</span></span>



| <span data-ttu-id="cfd51-126">Требование</span><span class="sxs-lookup"><span data-stu-id="cfd51-126">Requirement</span></span> | <span data-ttu-id="cfd51-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cfd51-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="cfd51-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfd51-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cfd51-129">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cfd51-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cfd51-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfd51-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cfd51-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cfd51-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="cfd51-132">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cfd51-132">Redistributable</span></span><br/>          | <span data-ttu-id="cfd51-133">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="cfd51-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="cfd51-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfd51-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfd51-135">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="cfd51-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cfd51-136">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="cfd51-136">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="cfd51-137">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="cfd51-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cfd51-138">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="cfd51-138">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
