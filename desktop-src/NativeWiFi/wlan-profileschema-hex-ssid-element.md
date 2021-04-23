---
description: Содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: шестнадцатеричный элемент (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682823"
---
# <a name="hex-ssid-element"></a><span data-ttu-id="bd365-103">шестнадцатеричный элемент (SSID)</span><span class="sxs-lookup"><span data-stu-id="bd365-103">hex (SSID) Element</span></span>

<span data-ttu-id="bd365-104">Шестнадцатеричный элемент (SSID) содержит идентификатор SSID беспроводной локальной сети в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="bd365-104">The hex (SSID) element contains the SSID of a wireless LAN in hexadecimal format.</span></span>

``` syntax
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
```

<span data-ttu-id="bd365-105">Элемент определяется элементом [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bd365-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd365-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd365-106">Remarks</span></span>

<span data-ttu-id="bd365-107">Несмотря на то, что **шестнадцатеричные** элементы и [**имена**](wlan-profileschema-name-ssid-element.md) являются необязательными, по крайней мере один **Шестнадцатеричный** элемент или [**имя**](wlan-profileschema-name-ssid-element.md) должны быть дочерними элементами элемента [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bd365-107">Although the **hex** and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="bd365-108">Когда сведения о профиле преобразуются в идентификатор SSID, **Шестнадцатеричный** элемент преобразуется в SSID (если есть), а элемент [**Name**](wlan-profileschema-name-ssid-element.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bd365-108">When profile information is converted to an SSID, the **hex** element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored .</span></span> <span data-ttu-id="bd365-109">Если **Шестнадцатеричный** элемент отсутствует, элемент [**Name**](wlan-profileschema-name-ssid-element.md) преобразуется в идентификатор SSID с помощью преобразования Юникод в ASCII.</span><span class="sxs-lookup"><span data-stu-id="bd365-109">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="bd365-110">Если идентификатор SSID хранится в профиле, всегда создается **Шестнадцатеричный** элемент.</span><span class="sxs-lookup"><span data-stu-id="bd365-110">When an SSID is stored in a profile, the **hex** element is always generated.</span></span> <span data-ttu-id="bd365-111">Элемент [**Name**](wlan-profileschema-name-ssid-element.md) создается только в случае успешного преобразования ASCII в формат SSID и создания профиля XML.</span><span class="sxs-lookup"><span data-stu-id="bd365-111">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="bd365-112">При преобразовании в [**имя**](wlan-profileschema-name-ssid-element.md)некоторые сведения из исходного идентификатора SSID могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="bd365-112">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bd365-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="bd365-113">Examples</span></span>

<span data-ttu-id="bd365-114">Пример профиля, в котором используется элемент **Hex** , см. в разделе [пример профиля FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bd365-114">To view a sample profile that uses the **hex** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd365-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bd365-115">Requirements</span></span>



| <span data-ttu-id="bd365-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bd365-116">Requirement</span></span> | <span data-ttu-id="bd365-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bd365-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="bd365-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd365-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd365-119">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd365-119">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bd365-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd365-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd365-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd365-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="bd365-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bd365-122">Redistributable</span></span><br/>          | <span data-ttu-id="bd365-123">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="bd365-123">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="bd365-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd365-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd365-125">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="bd365-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bd365-126">**SSID**</span><span class="sxs-lookup"><span data-stu-id="bd365-126">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="bd365-127">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="bd365-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bd365-128">**SSID (Ссидконфиг)**</span><span class="sxs-lookup"><span data-stu-id="bd365-128">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




