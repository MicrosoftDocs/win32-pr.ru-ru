---
description: Указывает метод проверки подлинности, используемый для подключения к беспроводной локальной сети.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Элемент authentication (Аусенкриптион)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263474"
---
# <a name="authentication-authencryption-element"></a><span data-ttu-id="a2738-103">Элемент authentication (Аусенкриптион)</span><span class="sxs-lookup"><span data-stu-id="a2738-103">authentication (authEncryption) Element</span></span>

<span data-ttu-id="a2738-104">Элемент authentication (Аусенкриптион) определяет метод проверки подлинности, используемый для подключения к беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="a2738-104">The authentication (authEncryption) element specifies the authentication method to be used to connect to the wireless LAN.</span></span>

``` syntax
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
```

<span data-ttu-id="a2738-105">Элемент определяется элементом [**аусенкриптион**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a2738-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2738-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2738-106">Remarks</span></span>

<span data-ttu-id="a2738-107">В следующей таблице описаны значения перечисления.</span><span class="sxs-lookup"><span data-stu-id="a2738-107">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="a2738-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a2738-108">Value</span></span>   | <span data-ttu-id="a2738-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a2738-109">Description</span></span>                            |
|---------|----------------------------------------|
| <span data-ttu-id="a2738-110">open</span><span class="sxs-lookup"><span data-stu-id="a2738-110">open</span></span>    | <span data-ttu-id="a2738-111">Откройте аутентификацию 802,11.</span><span class="sxs-lookup"><span data-stu-id="a2738-111">Open 802.11 authentication.</span></span>            |
| <span data-ttu-id="a2738-112">общие</span><span class="sxs-lookup"><span data-stu-id="a2738-112">shared</span></span>  | <span data-ttu-id="a2738-113">Общая проверка подлинности 802,11.</span><span class="sxs-lookup"><span data-stu-id="a2738-113">Shared 802.11 authentication.</span></span>          |
| <span data-ttu-id="a2738-114">Активация Windows</span><span class="sxs-lookup"><span data-stu-id="a2738-114">WPA</span></span>     | <span data-ttu-id="a2738-115">Проверка подлинности WPA-Enterprise 802,11.</span><span class="sxs-lookup"><span data-stu-id="a2738-115">WPA-Enterprise 802.11 authentication.</span></span>  |
| <span data-ttu-id="a2738-116">впапск</span><span class="sxs-lookup"><span data-stu-id="a2738-116">WPAPSK</span></span>  | <span data-ttu-id="a2738-117">Проверка подлинности WPA-Personal 802,11.</span><span class="sxs-lookup"><span data-stu-id="a2738-117">WPA-Personal 802.11 authentication.</span></span>    |
| <span data-ttu-id="a2738-118">WPA2</span><span class="sxs-lookup"><span data-stu-id="a2738-118">WPA2</span></span>    | <span data-ttu-id="a2738-119">Проверка подлинности WPA2-Enterprise 802,11.</span><span class="sxs-lookup"><span data-stu-id="a2738-119">WPA2-Enterprise 802.11 authentication.</span></span> |
| <span data-ttu-id="a2738-120">WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="a2738-120">WPA2PSK</span></span> | <span data-ttu-id="a2738-121">Проверка подлинности WPA2-Personal 802,11.</span><span class="sxs-lookup"><span data-stu-id="a2738-121">WPA2-Personal 802.11 authentication.</span></span>   |



 

<span data-ttu-id="a2738-122">Дополнительные сведения о методах проверки подлинности 802,11 см. в спецификациях [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)и [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="a2738-122">For more information about 802.11 authentication methods, see the [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1X](https://ieeexplore.ieee.org/document/1438730), and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="a2738-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="a2738-123">Examples</span></span>

<span data-ttu-id="a2738-124">Чтобы просмотреть образцы профилей, в которых используется элемент **authentication** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a2738-124">To view sample profiles that use the **authentication** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2738-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a2738-125">Requirements</span></span>



| <span data-ttu-id="a2738-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a2738-126">Requirement</span></span> | <span data-ttu-id="a2738-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a2738-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a2738-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2738-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a2738-129">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2738-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a2738-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2738-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a2738-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2738-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a2738-132">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a2738-132">Redistributable</span></span><br/>          | <span data-ttu-id="a2738-133">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="a2738-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a2738-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2738-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2738-135">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="a2738-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a2738-136">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="a2738-136">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="a2738-137">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="a2738-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a2738-138">**Аусенкриптион (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="a2738-138">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




